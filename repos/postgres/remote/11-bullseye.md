## `postgres:11-bullseye`

```console
$ docker pull postgres@sha256:e5b1d8fabcf3cc8559903d7790b7fb8b3e4d18abae8b94acf3f3ccd950419a95
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

### `postgres:11-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:b3de7d483937f2df1106398290b35c1bc0ecc7508e2d4a2d72ae7a42c41a4b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (135007421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fc44ccc1922d209d21ff054ba01718bd7bbcbf6cbe7e8777b7376b61c96908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 19:02:26 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_MAJOR=11
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_VERSION=11.22-1.pgdg110+1
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:02:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:02:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3841f1153f5e4aa10f3bc408d790bdefe1023f07e9ef8b0e97a2ec574a26e6`  
		Last Modified: Tue, 21 Nov 2023 06:17:52 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b70dd3ecaff4d9e35be665b85ad3c3c6ccde456bdd57860c6701021ca3a104`  
		Last Modified: Tue, 21 Nov 2023 06:17:52 GMT  
		Size: 4.2 MB (4207473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a7d9115821562339fd217cb9ea2d8457450dec2e2976e7e11d8d6a8b4939ec`  
		Last Modified: Tue, 21 Nov 2023 06:17:52 GMT  
		Size: 1.5 MB (1472480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3e0c3126d1b1b5ec0e36985be981f1384404ee39c607ee3f3bd621ad85a122`  
		Last Modified: Tue, 21 Nov 2023 06:17:53 GMT  
		Size: 8.0 MB (8045199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7147ae262b81c8ac5dc84e797bfe06b1a9ea4bae085c0718ba5ff3deefd42e90`  
		Last Modified: Tue, 21 Nov 2023 06:17:53 GMT  
		Size: 1.0 MB (1037437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47881ccf6831eacba2e27cf712044be4bc902e3472b48a05906cf851c9856fc2`  
		Last Modified: Tue, 21 Nov 2023 06:17:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e4b5dbf8b8bc6b4e967dc6f5cbc528977a3192f4002a5340e05f1dc8f72567`  
		Last Modified: Tue, 21 Nov 2023 06:17:54 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e525a4f185daa681a7b26b244d8805ea257467b524cc63e41723dd68398cefef`  
		Last Modified: Tue, 21 Nov 2023 06:17:57 GMT  
		Size: 88.8 MB (88808665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3eb0227830d93590ea1702da31c4378f554425d7d9f88012878c87788eccc2`  
		Last Modified: Tue, 21 Nov 2023 06:17:54 GMT  
		Size: 8.3 KB (8321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43e7fa23999204d8938906e4f6a2cb0a00a7d1406e185777645b07083b9f3e9`  
		Last Modified: Tue, 21 Nov 2023 06:17:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c800d1b37d020c3743df30620506a1d72d5284796ae456f757c5d39dc225c70e`  
		Last Modified: Tue, 21 Nov 2023 06:17:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b91e45a82d4b9f64cc9089453ad6b8cecfb73d85999bd15d44a98aa9febe62`  
		Last Modified: Tue, 21 Nov 2023 06:17:56 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:4749d2859b66f9876b38639df7f92d3c6183246cef1f039f6de51fc28b9148b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4991245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901718cf7d7482e8604f7c60eb69e916ee1d05dadc1277f6b2d6caea7909ccb0`

```dockerfile
```

-	Layers:
	-	`sha256:ed49c240c7c5af27c610a2116f230f209527e1dcbd33cdbe65f28f035d16aa22`  
		Last Modified: Tue, 21 Nov 2023 06:17:52 GMT  
		Size: 4.9 MB (4941215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b8e4d0b06d7af4d7e9d99a51f58395993812f7af17c63ccf249d52a62d51d1`  
		Last Modified: Tue, 21 Nov 2023 06:17:52 GMT  
		Size: 50.0 KB (50030 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:8391d8659640f49b79c2f8d9ffa26bdba4e9c56de8d0dd9db21182db8d032820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128156720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f5ce23b8c43ee2b5f6d8840da8fcf6957831e79e36b27bf376b27281f99288`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 19:02:26 GMT
ADD file:f7d1d017cc4e588f213f4536967b8d58c50b8602fb8a10b786856c35a843f31e in / 
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_MAJOR=11
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_VERSION=11.22-1.pgdg110+1
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:02:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:02:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d051266714ac5508b442ebbe5911d353bfacddc64f657eeba14a993cced96358`  
		Last Modified: Tue, 21 Nov 2023 05:04:38 GMT  
		Size: 28.9 MB (28921267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ece1beb92cce2ac06ca58cdf90840eefcd484ca3a322e1ede41adbd2aa5af81`  
		Last Modified: Tue, 21 Nov 2023 20:02:31 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b626f1f20e2d8180138b585029d4c234ef8f68fce1ea4de209c15160a571570`  
		Last Modified: Tue, 21 Nov 2023 20:02:31 GMT  
		Size: 3.9 MB (3889265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848c2a7661551b2883b51208a362b26b127489d0d144f9726925dfcb6c8f296c`  
		Last Modified: Tue, 21 Nov 2023 20:02:31 GMT  
		Size: 1.4 MB (1449946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa10149f3fedf3623013ea4617c0347bf1d5e1018a20c3acb3089fe3f16c201`  
		Last Modified: Tue, 21 Nov 2023 20:02:33 GMT  
		Size: 8.0 MB (8045273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f01ea795e7f5f05e14920788c8357f1db83187f8933ca15bf4b6818312e40b`  
		Last Modified: Tue, 21 Nov 2023 20:02:33 GMT  
		Size: 1.0 MB (1033914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a65ccf4e087845b4aaf62c24b518eb775f6e8ab3080d62030cde1e5890bf51e`  
		Last Modified: Tue, 21 Nov 2023 20:02:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0f312b2560772e07297fec490d54bb2c01a653ed43b44a32d9845e7993b5c7`  
		Last Modified: Tue, 21 Nov 2023 20:02:33 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598c52107178000adc35ccfc34bbef8916388ca977849aca0394d32a94e9a876`  
		Last Modified: Tue, 21 Nov 2023 22:25:06 GMT  
		Size: 84.8 MB (84798706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08096d06f9b52685dd903d5f9aa285759cc4ea6a8f6f2d2481550e695ba9a91f`  
		Last Modified: Tue, 21 Nov 2023 22:25:03 GMT  
		Size: 8.3 KB (8328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891bf150cd42bdfe0b7a9060a27c9f1a06c0d0bed8284babe9da3008c755fab2`  
		Last Modified: Tue, 21 Nov 2023 22:25:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fc4434b1263d9be0a7f117aa8c24e60b20e14d6d30bba13ba6b9fafd27f1b1`  
		Last Modified: Tue, 21 Nov 2023 22:25:03 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a2b02a913d7f4f24e5673cd4b0d35dd450562de2da0dc8d09d8898c14ec966`  
		Last Modified: Tue, 21 Nov 2023 22:25:04 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:431f54eee3aed48deb7d9043e87aff51ceb77f6e699b14d7b3cd50a3a6b100b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 KB (49832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c216a146692afc2738250cfd5098aaba5dced4ef7ab370a58883dbd3c8edd5b`

```dockerfile
```

-	Layers:
	-	`sha256:85756116b2d0ce3ba49eae0452019ae586132f910ccc41e422db8e9cb85dd45c`  
		Last Modified: Tue, 21 Nov 2023 22:25:03 GMT  
		Size: 49.8 KB (49832 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:032b74968aaacb0c3b35d0a2a5c5cc6897a4348cc26b5a66439fae9c25eb4270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123023159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979a16b5658f6ca84bb314f46de7770ad53be68edc876506bea06f71366aaef6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 19:02:26 GMT
ADD file:c4afced274aaa80ab3018b368ed739c1c55e49b41e9637ac44d63e61344fe865 in / 
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_MAJOR=11
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_VERSION=11.22-1.pgdg110+1
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:02:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:02:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6dc4ed5513793308b8e30b08e03f97fa54025c3d3f3172c6edccb1dbbc7ff139`  
		Last Modified: Tue, 21 Nov 2023 04:02:35 GMT  
		Size: 26.6 MB (26579014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cc7941b400f3bf57e88ca53cd8f503b865c5758c4a78c8b4c7a8e328530196`  
		Last Modified: Wed, 22 Nov 2023 01:48:04 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4a88703271fa81c161e06205d8313b2f8f0af319f9e0b3ad8c61257ecf43a8`  
		Last Modified: Wed, 22 Nov 2023 01:48:05 GMT  
		Size: 3.5 MB (3509868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a39292d0ae527985471598a74ca795bbde210667b000f267cd16afcf4db4df`  
		Last Modified: Wed, 22 Nov 2023 01:48:05 GMT  
		Size: 1.4 MB (1440036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9409bab78ee01b73d472aa8b928ed37ba03e08bb0b9a13dea577c13c60654b`  
		Last Modified: Wed, 22 Nov 2023 01:48:07 GMT  
		Size: 8.0 MB (8045202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22395ce5acb8645b4427e09aae3b58c5cc849b5d6a5a2a825396e15ac23a11d2`  
		Last Modified: Wed, 22 Nov 2023 01:48:06 GMT  
		Size: 907.8 KB (907774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681b290bd10a5aa1e8c51ba74de59868cb4d847b7e121c7b9363e822124e4772`  
		Last Modified: Wed, 22 Nov 2023 01:48:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dca2bf4cee3e9a783c855ca659a8048dcfcd8982a97eaa0f090e14a1ba182c`  
		Last Modified: Wed, 22 Nov 2023 01:48:06 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1390a12f617cce7db3b3427b17397bcfb7b5820cc077e44b337bb5130555a47`  
		Last Modified: Wed, 22 Nov 2023 04:27:29 GMT  
		Size: 82.5 MB (82522923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a092ebd1bb1cfe7ee6c194dac07cebaf4db205aa63da318a0e1dfbca5b4b232`  
		Last Modified: Wed, 22 Nov 2023 04:27:26 GMT  
		Size: 8.3 KB (8326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eee1baec1d0cfac1cc45db3a6c8c5227ca1096230b11bade2ae406ab357511`  
		Last Modified: Wed, 22 Nov 2023 04:27:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c2637f85de34392096d15ece38c73ac0481a443720deb37c1d2b15be0a8f61`  
		Last Modified: Wed, 22 Nov 2023 04:27:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0517076a1302d6883504184a8f2f734b4288c07e286d4d8e4a9068c513025711`  
		Last Modified: Wed, 22 Nov 2023 04:27:26 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:34f6dc8693e0609d84b153b598c853f453e548ade445e564dfb3e049174e7076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5002636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de83af5966144939ec4e3ba2a4861fe16ce0f512b1000e6ead5dfc672d970459`

```dockerfile
```

-	Layers:
	-	`sha256:a773a6320e25fc160842f10abebfeab51f86761b34a32a486c1a7cbc96d624c6`  
		Last Modified: Wed, 22 Nov 2023 04:27:26 GMT  
		Size: 5.0 MB (4952597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d539478054a464f91032571dc9428b342c951219cb3d20acd646f8d40c17d36`  
		Last Modified: Wed, 22 Nov 2023 04:27:25 GMT  
		Size: 50.0 KB (50039 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:8af74cbfd1c45a9e362696bd5ad0ae9305ec8be826751625b866af5f788c75e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130106911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546c10d0c4321d2a708ccd12da725fb7f09ca3c0fe1f410db22f9a2a28b4c40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_MAJOR=11
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_VERSION=11.22-1.pgdg110+1
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:02:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:02:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8cba8f347d25aea0b880c400cfad7e92ca8d19edd50109d050b203e7f03e08`  
		Last Modified: Wed, 01 Nov 2023 16:58:51 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b63f3a8e293aa06b35328b02736911ca54352d7daf4e428e09a993b7d52a57e`  
		Last Modified: Wed, 01 Nov 2023 16:58:51 GMT  
		Size: 4.2 MB (4209416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01abc326b7d92a05c285645a28a708e5e91a09458972d4e47dd74d2cc7a2856`  
		Last Modified: Wed, 01 Nov 2023 16:58:51 GMT  
		Size: 1.4 MB (1404399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5c0d930da84e77d9de84ef352658c7633e26fa5b2ea9b683904da3c5bb663a`  
		Last Modified: Wed, 01 Nov 2023 16:58:53 GMT  
		Size: 8.0 MB (8045154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a648afdd94c4f50847eb569dbf9ed80f07e2e3315648a0dcea4948bf9dd3093`  
		Last Modified: Wed, 01 Nov 2023 16:58:53 GMT  
		Size: 1.0 MB (1025899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f87ca9975d451933be1b2ac3fd31a8373a7a635b010d89d155023fc63dedb5`  
		Last Modified: Wed, 01 Nov 2023 16:58:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfde1066dd4bc68501086122feecf05986d46c9453b3583cfb58a81c8fd71c6`  
		Last Modified: Wed, 01 Nov 2023 16:58:54 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb068292645364faca5004a68d67560bb699487736a83db6dadc2ebf1a8f07bc`  
		Last Modified: Tue, 14 Nov 2023 02:28:14 GMT  
		Size: 85.3 MB (85339789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40156b66aaa97061d881ee7d33d74e7750e3e8250f83479df3ea80413d7152d`  
		Last Modified: Tue, 14 Nov 2023 02:28:10 GMT  
		Size: 8.3 KB (8323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf99e7ca69e0dca7915e3c7bcb6c65ca07be656f52e9d0a6237f0f48d95217e`  
		Last Modified: Tue, 14 Nov 2023 02:28:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab14e8f03172cdff86aff3ecfe3a8c1baae1b34de479701abed61a63f9e9834`  
		Last Modified: Tue, 14 Nov 2023 02:28:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb7162773a7f5b6750254f8e8df1584a9f6ff5963185bf586df5c34cf4aa037`  
		Last Modified: Tue, 14 Nov 2023 02:28:11 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:03bf419eba84e1c7d29659e3217156c65707694fb4365917ed22735828f1ac59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4996103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff1c41f236f696366ce9d10b27422216e0ceb250a66ec60f3eaf0a6f82699bd`

```dockerfile
```

-	Layers:
	-	`sha256:9fbe3d4475a3537395296fd8d8de6a29f5302476f2a3522f7788f9e3a8577d8d`  
		Last Modified: Tue, 14 Nov 2023 02:28:10 GMT  
		Size: 4.9 MB (4946234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009854d0ae440f859ec88bcd4244d3299de2c8e66c4c5d1fd6ec0937738c3945`  
		Last Modified: Tue, 14 Nov 2023 02:28:10 GMT  
		Size: 49.9 KB (49869 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:52242a28e513810d0e4a3d1bffdd4c9482b3e278777becd4cbcb04206ce41ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136889137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a348b3f7d6273b246408f75a4ffe1999e3c472d172715234510932a7851581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 10 Aug 2023 18:02:22 GMT
ADD file:67f223c9c48e525a23fb110e4c105d7128dcac0c10f32c38f98ea84a21d2bd00 in / 
# Thu, 10 Aug 2023 18:02:22 GMT
CMD ["bash"]
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
ENV GOSU_VERSION=1.16
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
ENV PG_MAJOR=11
# Thu, 10 Aug 2023 18:02:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 10 Aug 2023 18:02:22 GMT
ENV PG_VERSION=11.21-1.pgdg110+1
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:02:22 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:02:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:02:22 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:02:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:02:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bc6810e8fe9346a3caaff984163b789d12b6964a15a2029e384143ca19fef5ad`  
		Last Modified: Wed, 01 Nov 2023 00:44:14 GMT  
		Size: 32.4 MB (32402692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de62efeb2d2c08236797932bbdac574a323b4fb7b9c5f873c16162a2ddb33f82`  
		Last Modified: Wed, 01 Nov 2023 01:19:30 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302615dd6a87911f035908c5715c9f7c60f34b5e65aeabc01d9b1137b3d4293c`  
		Last Modified: Wed, 01 Nov 2023 01:19:30 GMT  
		Size: 4.6 MB (4607440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ac126b9ac03dbd29ca86d0e6a4151fb7f1aa921334c6963a13dc5e262d2588`  
		Last Modified: Wed, 01 Nov 2023 01:19:30 GMT  
		Size: 1.4 MB (1448292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ec8bbe9c52ed17c8cc6a00e6ad0d03f3c17ce86f08938b526db6cc6cb5aec6`  
		Last Modified: Wed, 01 Nov 2023 01:19:31 GMT  
		Size: 8.0 MB (8045178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3222de05b2bf2610d6394d9c15ba10d48c06f801f570bbcb4e4d099cef2138`  
		Last Modified: Wed, 01 Nov 2023 01:19:31 GMT  
		Size: 1.0 MB (1027977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a5e528f780129af6b6cce51901362105d6dd546e6d5c300270570cf141cf86`  
		Last Modified: Wed, 01 Nov 2023 01:03:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4de275d17c25c78a3b9524792e3cab0cfbcd291a3313341a40ee81ffd8fa7f`  
		Last Modified: Wed, 01 Nov 2023 01:03:30 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d274ce0d2ded81e4c0d360c0f105c2b535d15e44bc5241eb01a02f79e6b8239f`  
		Last Modified: Wed, 01 Nov 2023 01:19:35 GMT  
		Size: 89.3 MB (89339211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fe33feb8a61ac2fa9a89d276824cfd81fbdfded08c37da6cda4071ab21dc8b`  
		Last Modified: Wed, 01 Nov 2023 01:19:32 GMT  
		Size: 8.3 KB (8325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763238a31591cba2e6d192f23d35dbcd6e3d2d7f6a9599aa5414a50b2b6fdd61`  
		Last Modified: Wed, 01 Nov 2023 01:19:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec661614d00bba3b1d59ffda56ab9f8ee601410c229fcf61177f4f16bd8d0b2`  
		Last Modified: Wed, 01 Nov 2023 01:19:32 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be68a41dc00a010a239fab41bcee83f878355c86f9342fb57475242a5bcf34b1`  
		Last Modified: Wed, 01 Nov 2023 01:19:33 GMT  
		Size: 4.8 KB (4791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:00628b59067022e8115af0ff3576d4cf890fa04afb525bf78dbefdbe248dffad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 KB (49774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e061ee21bd29278ca4037d3ec142c1032561e888a0a743bb31530a6f7d81fdb`

```dockerfile
```

-	Layers:
	-	`sha256:3d8c832051aba75b546356933b70f62b6c995ef9693def6b0bbc5e59f1c44c92`  
		Last Modified: Wed, 01 Nov 2023 01:19:30 GMT  
		Size: 49.8 KB (49774 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:b2a2501c95299b3355d17047b47d46cd62ce24240b164ea1f3a6b674b79c93fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129774902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c2fe8b953515b9e42d3a24f2dd24ff67f08502acca390adff86ed8d1aef165`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 01 Nov 2023 01:10:15 GMT
ADD file:c58b99b54270e537286dd7f2ffb13d5a6a1a8ab45c0620c538634014259387e4 in / 
# Wed, 01 Nov 2023 01:10:19 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_MAJOR=11
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_VERSION=11.22-1.pgdg110+1
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:02:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:02:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c1d7e544711cc24ab1d89506dc11ffa6ff48b21690c7e1d7afff5f1871b8f5fe`  
		Last Modified: Wed, 01 Nov 2023 01:21:13 GMT  
		Size: 29.6 MB (29635977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8906d6e87c85fd15a289eae4ba06ed818eefe38a8901a512c4c641e6ba4660`  
		Last Modified: Thu, 02 Nov 2023 19:50:25 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1671e1bac79de449be1559922f5511825659c8ce95ab8bda818dab0926b40c`  
		Last Modified: Thu, 02 Nov 2023 19:50:26 GMT  
		Size: 4.2 MB (4196350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48dd275b2c7ef29590ac56234b6c0f0a5515f64b948785b91400ec0eb24cc0d5`  
		Last Modified: Thu, 02 Nov 2023 19:50:25 GMT  
		Size: 1.4 MB (1359996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c23a62a631474ce86bd18c01ab5f13e518a64fcef4936ab9ebd2b46895c6327`  
		Last Modified: Thu, 02 Nov 2023 19:50:28 GMT  
		Size: 8.0 MB (8045539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cabdb57d80964d4313be4918a70c3b1f599448ea8c2b4a1ad523260bc11a6f`  
		Last Modified: Thu, 02 Nov 2023 19:50:27 GMT  
		Size: 1.1 MB (1089546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8c4278af9b6a1bfb844bf6694bdf233ea6967b76f9959ad3d796ea8b512c89`  
		Last Modified: Thu, 02 Nov 2023 19:50:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e776be935a115d650dc469639aac684a892c3425fc4b465b6534f43e93a4fec8`  
		Last Modified: Thu, 02 Nov 2023 19:50:28 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da8e19016c0a28b8ada82014268a0f46cfa43e7bab8f160044826773062f2f`  
		Last Modified: Tue, 14 Nov 2023 14:14:11 GMT  
		Size: 85.4 MB (85429136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ad8d709661fd56e0c1b86e0a75e2678b9d155e334c2756906e21a1b0ae924f`  
		Last Modified: Tue, 14 Nov 2023 14:14:02 GMT  
		Size: 8.3 KB (8326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096c4896dd164985070c51aadb82ccbdaf1702ae042914a12f4eabcea960c954`  
		Last Modified: Tue, 14 Nov 2023 14:14:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ab7acf89d133fa668d1983b4db428f871b5406de6a2b418adbf152aa902fbc`  
		Last Modified: Tue, 14 Nov 2023 14:14:02 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759a69b8fc1baf4c2e40b103c3a8e17bb2c88f520954de10fd4eaeaf1d50b1ad`  
		Last Modified: Tue, 14 Nov 2023 14:14:03 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:c710963e17e0a3de8c9a203efcfefce562c26c506fec8b6942e50537b7942f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 KB (49716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d0713cd386dc0c6a7a9b64b4deac5b6c8aa37ff3806a892180ae79182d710a`

```dockerfile
```

-	Layers:
	-	`sha256:46a843b0a32cfb5e61557a0724cc4b7d05e199d80ddc87270f05457d72971464`  
		Last Modified: Tue, 14 Nov 2023 14:14:02 GMT  
		Size: 49.7 KB (49716 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:7256cf3a6c562e548fd23e4fb20699287666af86d92b5fe282454ea610d06505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143915621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea972bf3c780db9975342d0636501cb32af59a80e48a54319342cf9521533a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 19:02:26 GMT
ADD file:b0d18f2d04821eb50d1faecc1a64916f5c63dd386ae71a3b2cb1d6c4aac6e1c4 in / 
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_MAJOR=11
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_VERSION=11.22-1.pgdg110+1
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:02:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:02:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:60239a74847cd7e9a928353188f3cf096ca8cf648e2b27c765058e169d568fd9`  
		Last Modified: Tue, 21 Nov 2023 04:29:47 GMT  
		Size: 35.3 MB (35293727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16de6da61666e950a5b7b529f3038a00b9f2c676c778ce6877c9554fdd36857c`  
		Last Modified: Tue, 21 Nov 2023 23:56:59 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c98567766a405ce84a0be0e02e7cf9914d6d4691dffc5496c760a347867228`  
		Last Modified: Tue, 21 Nov 2023 23:56:59 GMT  
		Size: 5.0 MB (5015948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c61a8652eea248c5219212393f2a552f9493c1642d9219671579c1ee733f77d`  
		Last Modified: Tue, 21 Nov 2023 23:56:59 GMT  
		Size: 1.4 MB (1394026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdb4e3c161d5532d076597f8745f34a6f37d4c07e3b0e6b813a8739f23e1417`  
		Last Modified: Tue, 21 Nov 2023 23:57:00 GMT  
		Size: 8.0 MB (8045122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02ed0182f1b78eec622706c1ce7e2e3a5db1a8ff2f9e72219ed5427a3cfa888`  
		Last Modified: Tue, 21 Nov 2023 23:57:00 GMT  
		Size: 1.2 MB (1196901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4862e5122b808ebe059b3ed3a9d62dbbcfcfd0a4ee79f3185115cb2be9eb5889`  
		Last Modified: Tue, 21 Nov 2023 23:57:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f110a1ad0cf91d66fa9f7495dcf0d900b6a19805cca2e349d646c9211a38e3d`  
		Last Modified: Tue, 21 Nov 2023 23:57:00 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f818bdec53a30b3e18c316b86d6a152256dc8df6178be37a3064857ea60b091`  
		Last Modified: Wed, 22 Nov 2023 00:10:50 GMT  
		Size: 93.0 MB (92951541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06287cad1206bc98dac208856049fa243e5602b43eca10f2174c2a44e6c8675`  
		Last Modified: Wed, 22 Nov 2023 00:10:46 GMT  
		Size: 8.3 KB (8325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bfea963fda958f0b76da171861cbbb4ba78a9d822758be990b985a52d65c5`  
		Last Modified: Wed, 22 Nov 2023 00:10:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dead73bf975beb525e09ae3f9d97cd785f593515d2a38812b796332dc986bb`  
		Last Modified: Wed, 22 Nov 2023 00:10:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee413011f781e7cd0ab054c91ec3d984b65e1523ef5c31ffff6368374c12f4fe`  
		Last Modified: Wed, 22 Nov 2023 00:10:47 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:03368578e52b568faa9f6b45539a8c2ec18491be82c2ac4fa5cceeaada630e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4998258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb2e66d525bdd6940298a633b2c6b0200dd3e30541f7b180261236f77129e61`

```dockerfile
```

-	Layers:
	-	`sha256:51516ac42160de00908ad2abb09e75575fac7a2a600b2eb626a36bbef67240fa`  
		Last Modified: Wed, 22 Nov 2023 00:10:46 GMT  
		Size: 4.9 MB (4948349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:835349f9bfd9b98c62f73ce1208f26759f3ad47bf53b159116156bdcb042272a`  
		Last Modified: Wed, 22 Nov 2023 00:10:46 GMT  
		Size: 49.9 KB (49909 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:659f44d26abb6fecb6c708f4482651a74aa2265d40db49ac290f933ce3bdd6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138553296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2374b057d2d08eecfc3df79b432bb7e20cc42bd26a4cbe477cdc583fa4a39289`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 19:02:26 GMT
ADD file:a545f27075704ce13e33e539170d3f47007424d2cc2bea5aecfd2608a5194151 in / 
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_MAJOR=11
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_VERSION=11.22-1.pgdg110+1
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:02:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:02:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b114072f1cab66b7376d690985b12816aebab2e4e41fc170e32f111df27951dc`  
		Last Modified: Tue, 21 Nov 2023 05:10:48 GMT  
		Size: 29.7 MB (29656938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c14abe39e5d7af1af3f169efac214a4f5188f9cf0b1eeff4aa56e29edadb83e`  
		Last Modified: Tue, 21 Nov 2023 18:48:13 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda7c74bb621b77965678f0178a83d5ab3be51a08a147477342ecbce0570474b`  
		Last Modified: Tue, 21 Nov 2023 18:48:13 GMT  
		Size: 4.1 MB (4096138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24e48d76c2c7273893bb9fdadd72210e42e08d97d83c1951ece2885024a7ddf`  
		Last Modified: Tue, 21 Nov 2023 18:48:13 GMT  
		Size: 1.4 MB (1438342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907bad315ef26db29b2f1d30476df3623e928037f4f1245879d0acefc7d51fee`  
		Last Modified: Tue, 21 Nov 2023 18:48:14 GMT  
		Size: 8.1 MB (8099088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932751c91c6f7fde288cdfb18a762883255568a6d26c4bab31952f47a2412095`  
		Last Modified: Tue, 21 Nov 2023 18:48:14 GMT  
		Size: 1.0 MB (1014332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51466198f57f994776e57e10129e6e8b2e9e80ceda50f34cfddfd8c226e6a9e1`  
		Last Modified: Tue, 21 Nov 2023 18:48:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f4ed0154dba5579cb0fe28fe0064fd32f637f29598866ce370d1f8641be866`  
		Last Modified: Tue, 21 Nov 2023 18:48:15 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a225bd511fcd073f84c3feca3e80771e7c47435a801dd1c5d8332c305835cc72`  
		Last Modified: Tue, 21 Nov 2023 19:00:19 GMT  
		Size: 94.2 MB (94230110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0837f9b4114c4c20f1d023df2ac6724474136a33516675d0ae694731b1a9a7fb`  
		Last Modified: Tue, 21 Nov 2023 19:00:17 GMT  
		Size: 8.3 KB (8324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06e83bcf666bb04ba08bd0b3d23b15474a4f5a361c25495b50c1dd8e7c44946`  
		Last Modified: Tue, 21 Nov 2023 19:00:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad0429c7df47b1061106b7cff5d0682d55478f303c9444e66ef5bee18526c14`  
		Last Modified: Tue, 21 Nov 2023 19:00:17 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97def1aad53b83abad7eadd554ce6d6066dc1b9b288cc2555e8a1571f229165e`  
		Last Modified: Tue, 21 Nov 2023 19:00:18 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:b35b036e36bd26ecef19094bf5756873bfd4c2410e2414ad77d060d057f116ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4990056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9ecd3467bfad449dcea58e8786bccdecc5a513101fce2f6d62fb2d12c49993`

```dockerfile
```

-	Layers:
	-	`sha256:1fb6dd9a5962bfe09541b5683998ee586d70bc2bef3112cc5544663e69aa48ea`  
		Last Modified: Tue, 21 Nov 2023 19:00:17 GMT  
		Size: 4.9 MB (4940194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab6645026f1e433d7fe84d5af91be282f7afa0bd5e6a6a676a2fb5a4e51ccc9`  
		Last Modified: Tue, 21 Nov 2023 19:00:17 GMT  
		Size: 49.9 KB (49862 bytes)  
		MIME: application/vnd.in-toto+json
