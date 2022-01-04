## `postgres:10-bullseye`

```console
$ docker pull postgres@sha256:cab10066dd499f08de809764e35abaf68a1043d2bb01849697d38409e7e93fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `postgres:10-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:060c2f6606328f8faac2202574da84a87e0b15d72a6d8879e859536c01cd1f2f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84481470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9537c29bf1ffd049ff6edbb10fddb4327657f5f2373ae563d7f00a3d27e870d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 23:31:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 23:31:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 21 Dec 2021 23:31:34 GMT
ENV GOSU_VERSION=1.14
# Tue, 21 Dec 2021 23:31:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 21 Dec 2021 23:32:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 21 Dec 2021 23:32:11 GMT
ENV LANG=en_US.utf8
# Tue, 21 Dec 2021 23:32:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 23:32:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 21 Dec 2021 23:32:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 21 Dec 2021 23:36:01 GMT
ENV PG_MAJOR=10
# Tue, 21 Dec 2021 23:36:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Tue, 21 Dec 2021 23:36:01 GMT
ENV PG_VERSION=10.19-1.pgdg110+1
# Tue, 21 Dec 2021 23:36:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 21 Dec 2021 23:36:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 21 Dec 2021 23:36:19 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 21 Dec 2021 23:36:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Dec 2021 23:36:20 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 21 Dec 2021 23:36:20 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:20:30 GMT
COPY file:b2fac085615145a2bee98d4185ef0748655fa7c086ca21daef1ca6cac272bf59 in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:20:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:20:31 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:20:31 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:20:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1769f49f9101e08b259481961baceea032c026337b960a2737ba58d84c08d5f`  
		Last Modified: Tue, 21 Dec 2021 23:39:01 GMT  
		Size: 4.4 MB (4414603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a59cfee47cee21e9a3725fc141ad856917e95a1817f3719d5e7bae0c4e9515`  
		Last Modified: Tue, 21 Dec 2021 23:38:59 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461b2090c345e5af01940b13f92bcdbd47ef70bd372fd0a565af08f53c0f1601`  
		Last Modified: Tue, 21 Dec 2021 23:39:00 GMT  
		Size: 1.4 MB (1418382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed8ab6290ac04d65ebec4245056773a6679334d17b77a9a6bf1b7f1e26ad08a`  
		Last Modified: Tue, 21 Dec 2021 23:38:59 GMT  
		Size: 8.0 MB (8045343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495e42c822a03224fc27a04cf05716b82a5f1c4c9252cc7457673be355ab12f2`  
		Last Modified: Tue, 21 Dec 2021 23:38:57 GMT  
		Size: 441.7 KB (441681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e858c71c58fe45a750a830bfab4fe11bbd4618ace209d0ad397e4647d648d2`  
		Last Modified: Tue, 21 Dec 2021 23:38:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594792c80d5fa95924c9f7abe6acec205e5db07fc6bd04c299e3cd48174d1fab`  
		Last Modified: Tue, 21 Dec 2021 23:38:57 GMT  
		Size: 3.1 KB (3057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0753acb00c1e712dfe4c35c39d0986aee4394516dcf9636300af4c1c7a5906`  
		Last Modified: Tue, 21 Dec 2021 23:41:46 GMT  
		Size: 38.8 MB (38785581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cff4258bbe776e80bf0b035856466ca6d88639edc142745a0670810278846d`  
		Last Modified: Tue, 21 Dec 2021 23:41:37 GMT  
		Size: 8.1 KB (8078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d78efc7842878da1bf15e238db124d111ae2e0ff547ce92a924e2c88e1101cd`  
		Last Modified: Tue, 21 Dec 2021 23:41:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a341c027655d5cda9c009255e06ee613d2b8ad535d4261ca008270f5eb96a2f1`  
		Last Modified: Tue, 21 Dec 2021 23:41:37 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddaef3a2a1d9fc4b725de7c2935d251bed4d08f06b248b07432718092368916`  
		Last Modified: Tue, 04 Jan 2022 01:24:27 GMT  
		Size: 4.7 KB (4716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf27aa822344ff4617104f84610ba2045aa79b1bab6d89e4c79f7cf66694c8c`  
		Last Modified: Tue, 04 Jan 2022 01:24:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:8da33dcd5fceacd992889859db04b4e277df25344ac6c11116cd9da27a778505
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80359631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819a42cb2872cf12431753402b3387cf7b52a848933e5dbcd61adff6dd64f7a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Dec 2021 01:50:31 GMT
ADD file:a3023f71bd93966e7db1419adda3ccde4fcc5e2e8cf58e7b13c51036ed5ff796 in / 
# Tue, 21 Dec 2021 01:50:32 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 07:30:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 07:30:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 21 Dec 2021 07:30:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 21 Dec 2021 07:31:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 21 Dec 2021 07:31:30 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 21 Dec 2021 07:31:31 GMT
ENV LANG=en_US.utf8
# Tue, 21 Dec 2021 07:31:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 07:31:43 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 21 Dec 2021 07:31:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 21 Dec 2021 10:25:25 GMT
ENV PG_MAJOR=10
# Tue, 21 Dec 2021 10:25:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Tue, 21 Dec 2021 10:25:26 GMT
ENV PG_VERSION=10.19-1.pgdg110+1
# Tue, 21 Dec 2021 10:48:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 21 Dec 2021 10:48:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 21 Dec 2021 10:48:32 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 21 Dec 2021 10:48:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Dec 2021 10:48:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 21 Dec 2021 10:48:34 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:50:08 GMT
COPY file:b2fac085615145a2bee98d4185ef0748655fa7c086ca21daef1ca6cac272bf59 in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:50:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:50:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:50:10 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:50:11 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:50:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:054429d0cf4038fef39a3b5eb6ce52f600f9a2cbb71a4fb3e95ecf9b2da62581`  
		Last Modified: Tue, 21 Dec 2021 02:05:52 GMT  
		Size: 28.9 MB (28900253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11c3b8663b33872a4cd51280b3b6213125ffb664af3544f78a8c00861d96529`  
		Last Modified: Tue, 21 Dec 2021 12:06:36 GMT  
		Size: 4.1 MB (4096469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7885af84e3728315efcdad4126b9cf21704918c9bd5b532975c20b15618b6d83`  
		Last Modified: Tue, 21 Dec 2021 12:06:31 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6966bd647e990282b34e4b0ccdcee10086f054b44ed0b3f0133f098b9967b23b`  
		Last Modified: Tue, 21 Dec 2021 12:06:31 GMT  
		Size: 1.4 MB (1382552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a4a1fd7b75dec70f07b372ad523c88e90a1d337f5a2488b84a134db9bbfe15`  
		Last Modified: Tue, 21 Dec 2021 12:06:35 GMT  
		Size: 8.0 MB (8045155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d0038c65b0aafcf1ea56729903d012a7a37126d4900f4861ca4a16d7573fa8`  
		Last Modified: Tue, 21 Dec 2021 12:06:30 GMT  
		Size: 439.8 KB (439838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359b44a703071420b378dcf42f848c5aa8fdf777498ebfb37c8cbe52f38c64b9`  
		Last Modified: Tue, 21 Dec 2021 12:06:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af723b478cfbdf181802077d97fe3ff370c9c0d1505f26ad33f479f19545e442`  
		Last Modified: Tue, 21 Dec 2021 12:06:29 GMT  
		Size: 3.1 KB (3056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae9aac517825b02c2bfd8ae089280c5bb5a2b8e9e21a22c2078bd4ccda56f0c`  
		Last Modified: Tue, 21 Dec 2021 12:12:42 GMT  
		Size: 37.5 MB (37477118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4ac3b9f9aed8f663f28b389b38906fd136fbf471a3811b959f3c31e855cf8b`  
		Last Modified: Tue, 21 Dec 2021 12:12:21 GMT  
		Size: 8.1 KB (8079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a160e0194f2d0daf2edcbdcf69793b8296ca6c448a4bda97fca3cced54ecd2`  
		Last Modified: Tue, 21 Dec 2021 12:12:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f15d7a01aec4eba55c6007c3305b944fd26e2365390cd2556c25a0f20e311ee`  
		Last Modified: Tue, 21 Dec 2021 12:12:21 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf2cb6fa8d4a5f1f82bcee3fa84f7f57913ffa2c4c5f9ea9224893e44a13117`  
		Last Modified: Tue, 04 Jan 2022 01:55:28 GMT  
		Size: 4.7 KB (4714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d654e581cdf986c17147fdff02574eac99462102d9293dda1353dca587ea0fa8`  
		Last Modified: Tue, 04 Jan 2022 01:55:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:3de2d96dbc4e067a792025d17bf2a62a28e03247a503f659e15adce32a64fee5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76652668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0f216d053e670d32afd4cf69739f0b02a442f233a60964dd0d548d41fbb1cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Dec 2021 01:59:48 GMT
ADD file:6a5555c3e40db91fae5bb112464a4c405a976de17ff64c98f25d3033a6a608d8 in / 
# Tue, 21 Dec 2021 01:59:48 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 13:34:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 13:34:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 21 Dec 2021 13:34:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 21 Dec 2021 13:35:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 21 Dec 2021 13:35:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 21 Dec 2021 13:35:36 GMT
ENV LANG=en_US.utf8
# Tue, 21 Dec 2021 13:35:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 13:35:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 21 Dec 2021 13:35:51 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 21 Dec 2021 16:13:45 GMT
ENV PG_MAJOR=10
# Tue, 21 Dec 2021 16:13:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Tue, 21 Dec 2021 16:13:46 GMT
ENV PG_VERSION=10.19-1.pgdg110+1
# Tue, 21 Dec 2021 16:35:04 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 21 Dec 2021 16:35:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 21 Dec 2021 16:35:07 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 21 Dec 2021 16:35:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Dec 2021 16:35:09 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 21 Dec 2021 16:35:10 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:00:27 GMT
COPY file:b2fac085615145a2bee98d4185ef0748655fa7c086ca21daef1ca6cac272bf59 in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:00:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:00:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:00:30 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:00:30 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:00:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d0061d6703dc4975804c3419e00c85efbe3f1b79c86d87e048fa14a683e88e31`  
		Last Modified: Tue, 21 Dec 2021 02:15:26 GMT  
		Size: 26.6 MB (26560815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63faa60732a43e018f66952afb7f45d04d6d4758ee3d81183a163f9b6f804d2a`  
		Last Modified: Tue, 21 Dec 2021 17:48:01 GMT  
		Size: 3.7 MB (3717142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0323b5281fb94b32757850d02213a35a5f22c233d2c30a49504f89067f72f573`  
		Last Modified: Tue, 21 Dec 2021 17:47:59 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22b25778e1eb533d3a049204db0bd7f35e725b44748eb5b53d7dbcfb5b3adf6`  
		Last Modified: Tue, 21 Dec 2021 17:48:00 GMT  
		Size: 1.4 MB (1375223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89817e68a18fa0bdfc9458a9b332f5b365056be1f503efa9c21faad188af3e92`  
		Last Modified: Tue, 21 Dec 2021 17:48:03 GMT  
		Size: 8.0 MB (8045328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1d4b88549ac5042ce416127fca3eb9ad03134d3f87810ea59ea4234237cfb5`  
		Last Modified: Tue, 21 Dec 2021 17:47:57 GMT  
		Size: 434.5 KB (434535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7fd84c8b77f1bed6ce41ca44ab4fb3dcd41ff89c2536a428f8652b8ddd33a5`  
		Last Modified: Tue, 21 Dec 2021 17:47:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0160dd882bce5ce444f89bf8732ff499fc30f3469341d635ea8d721d047c0505`  
		Last Modified: Tue, 21 Dec 2021 17:47:57 GMT  
		Size: 3.1 KB (3058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a577dd7ed9dc4c7a998ef8a62032b6754c5ac54d77c20aa3cbed175010ec5d22`  
		Last Modified: Tue, 21 Dec 2021 17:54:19 GMT  
		Size: 36.5 MB (36501381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2037dc2003ba80f2606fd3732989ea985e99548301306c8a74595843208740e8`  
		Last Modified: Tue, 21 Dec 2021 17:53:53 GMT  
		Size: 8.1 KB (8080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d63a248a63369a5f0f02269cae25a9c8f0e4c683ffa2cecad4f302e80707df2`  
		Last Modified: Tue, 21 Dec 2021 17:53:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6476007466f18c42fe57aa1b1689ad6b35f0eecfa8471091f6af8dd0cf3f3c16`  
		Last Modified: Tue, 21 Dec 2021 17:53:53 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e010f5eaae3a157a5a39158bb2cf541e1cb030a935a09cd717ceb625f692510b`  
		Last Modified: Tue, 04 Jan 2022 01:10:08 GMT  
		Size: 4.7 KB (4715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff01259bc8143b23fd71892f4e9c8e89709c6476905330de2655dd3cb4a8ac8`  
		Last Modified: Tue, 04 Jan 2022 01:10:08 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:bd13520a161eab0c728b2817aaa577befecd8b9e3d52a7bdd04e1bd7ef6e817a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82397274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a603431e9c0085ed914fada4379b2d4443e93a93098c435818e6bf5bb4b1b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:23 GMT
ADD file:986f91febed4aa8e2072081ff8419d52ba2060510822e717086d3b3d9469e4d7 in / 
# Tue, 21 Dec 2021 01:42:24 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 08:51:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 08:51:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 21 Dec 2021 08:51:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 21 Dec 2021 08:51:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 21 Dec 2021 08:51:58 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 21 Dec 2021 08:51:58 GMT
ENV LANG=en_US.utf8
# Tue, 21 Dec 2021 08:52:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 08:52:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 21 Dec 2021 08:52:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 21 Dec 2021 09:05:38 GMT
ENV PG_MAJOR=10
# Tue, 21 Dec 2021 09:05:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Tue, 21 Dec 2021 09:05:40 GMT
ENV PG_VERSION=10.19-1.pgdg110+1
# Tue, 21 Dec 2021 09:05:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 21 Dec 2021 09:05:56 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 21 Dec 2021 09:05:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 21 Dec 2021 09:05:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Dec 2021 09:05:58 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 21 Dec 2021 09:05:59 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:41:49 GMT
COPY file:b2fac085615145a2bee98d4185ef0748655fa7c086ca21daef1ca6cac272bf59 in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:41:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:41:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:41:51 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:41:52 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:41:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:927a35006d93ea08499b57046904046d7926cd76fb17be193e3e74f56d634a08`  
		Last Modified: Tue, 21 Dec 2021 01:48:54 GMT  
		Size: 30.0 MB (30043793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deff285050ab195320ae1fb86873be82d3e7c7c007a03f475d904a40cb8486bb`  
		Last Modified: Tue, 21 Dec 2021 09:27:12 GMT  
		Size: 4.2 MB (4208850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e224327e9ea2fd347288b5da1b4736a8739edc357975a048b1f160850cf98984`  
		Last Modified: Tue, 21 Dec 2021 09:27:11 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a193ca6ee34e98a79c93f1334abad65f7ad5e3f67f569b64ae36cd4b388d793e`  
		Last Modified: Tue, 21 Dec 2021 09:27:11 GMT  
		Size: 1.3 MB (1346013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40dd6251c43b5f5ad0934cc8e210d5562cbba1a7c6b6a9ae1646ccfc5862fa6e`  
		Last Modified: Tue, 21 Dec 2021 09:27:11 GMT  
		Size: 8.0 MB (8043461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e965c0036888b45a564a2e2d4ce2bce1a721b46181db34a5c0fe64d0cc8ff9`  
		Last Modified: Tue, 21 Dec 2021 09:27:09 GMT  
		Size: 218.6 KB (218636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa7eb1c3a64971a515150c61479f55ef60eb6bd6fde66ebe91adb8eef27e1ee`  
		Last Modified: Tue, 21 Dec 2021 09:27:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b306316bf0e9fa15744adcdc1bda51804a0b90a3c2cf2e0e52af6c805762b3c3`  
		Last Modified: Tue, 21 Dec 2021 09:27:08 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea20c94b431fbcb9c981709f7297bff84eefe48ffff8bad6050caff07e7d32cf`  
		Last Modified: Tue, 21 Dec 2021 09:29:54 GMT  
		Size: 38.5 MB (38518511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e848f1b93fe4aad2ee9261ad2ec2b2d39fee39b10a4c842c3027e92b3b197f`  
		Last Modified: Tue, 21 Dec 2021 09:29:45 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ad6ecfe4fccbca3892ec826f7254396f01d9fe09073a4bfe974c42b446ca69`  
		Last Modified: Tue, 21 Dec 2021 09:29:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c9ed6e89f309f99ba6e91001d432ab36d4288c0f9137209bf3ae1ffcfb6143`  
		Last Modified: Tue, 21 Dec 2021 09:29:45 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858228a4c3f67af8ad2f898358746d6e8a91e716b16f9ee014e0c4c953c608d6`  
		Last Modified: Tue, 04 Jan 2022 01:47:33 GMT  
		Size: 4.7 KB (4709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46a194a8e24adecc64fd579743594a4b10a664cad6b28792b9db969adbfa94d`  
		Last Modified: Tue, 04 Jan 2022 01:47:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:afcbeff28131f14e8d88c8a8f0a2d58eafe9675ccf6b578822d9f34d0e025475
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86207477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b5ba05d6e9a3375d69760eb2f911dc0b7b35a5d412557c0ece9809ca39e0a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Dec 2021 01:40:06 GMT
ADD file:6b67a0d4d176747cc8cefbd105facde82f1795467bf02eb45e8385c91cdc9c41 in / 
# Tue, 21 Dec 2021 01:40:09 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 17:32:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 17:32:31 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 21 Dec 2021 17:32:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 21 Dec 2021 17:32:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 21 Dec 2021 17:32:50 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 21 Dec 2021 17:32:51 GMT
ENV LANG=en_US.utf8
# Tue, 21 Dec 2021 17:32:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 17:32:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 21 Dec 2021 17:33:04 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 21 Dec 2021 18:45:31 GMT
ENV PG_MAJOR=10
# Tue, 21 Dec 2021 18:45:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Tue, 21 Dec 2021 18:45:32 GMT
ENV PG_VERSION=10.19-1.pgdg110+1
# Tue, 21 Dec 2021 18:55:21 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 21 Dec 2021 18:55:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 21 Dec 2021 18:55:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 21 Dec 2021 18:55:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Dec 2021 18:55:25 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 21 Dec 2021 18:55:25 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:39:57 GMT
COPY file:b2fac085615145a2bee98d4185ef0748655fa7c086ca21daef1ca6cac272bf59 in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:39:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:39:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:39:59 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:39:59 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:39:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9b9a100d632569e96aeb2d7b0bc45bc436609bb61335815f207994f3b557f0f7`  
		Last Modified: Tue, 21 Dec 2021 01:48:45 GMT  
		Size: 32.4 MB (32370850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e1cde80251c811d2a11419dd7d755ffd8bb6ee6c48d6c26f4963af66231091`  
		Last Modified: Tue, 21 Dec 2021 19:09:13 GMT  
		Size: 4.8 MB (4812928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e5319205e69940a9e1c4aa2eb8b128ceb099b3b1ff04f95e9b807a57bee635`  
		Last Modified: Tue, 21 Dec 2021 19:09:11 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986b5046b42a04043dea030af38801a4786894d4282a6c18ca760a3a7dc08a91`  
		Last Modified: Tue, 21 Dec 2021 19:09:11 GMT  
		Size: 1.4 MB (1385420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69e50d5aff566bb6bc43ae83d6f252488788b3297a5932cd665a9c9df4816a8`  
		Last Modified: Tue, 21 Dec 2021 19:09:12 GMT  
		Size: 8.0 MB (8045063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d4116276636907e25c3224b8a72e1c62e1b6040aae2a429a921513da0d0e4a`  
		Last Modified: Tue, 21 Dec 2021 19:09:09 GMT  
		Size: 448.0 KB (447958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e3213019f61cd51f01af4a70a4182fc67bdd71b82ea07c074f6796d4ff00f6`  
		Last Modified: Tue, 21 Dec 2021 19:09:09 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05967f41fcb3ecba7545ee6ced7b3f5419d14bc5e1fec038363f5e01c268e986`  
		Last Modified: Tue, 21 Dec 2021 19:09:08 GMT  
		Size: 3.1 KB (3053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f783c233b270e7b7e726a40510c1e4220894d0f425afb8f930f78b61df3fe2`  
		Last Modified: Tue, 21 Dec 2021 19:12:40 GMT  
		Size: 39.1 MB (39127017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57b6d1f392a9a68c883c9cd75baab7cf003ff4224e965a0550f387338415085`  
		Last Modified: Tue, 21 Dec 2021 19:12:29 GMT  
		Size: 8.1 KB (8083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f8c316ed8b0973061525fccd259bd33da5da5b3a8b4466f4a8d268d3fa8d0`  
		Last Modified: Tue, 21 Dec 2021 19:12:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ede4bbf6b18a13aa2880d796351f1ebbed89dcaeeea1540e6c4c2f998a0658`  
		Last Modified: Tue, 21 Dec 2021 19:12:29 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293a30a2178b07f335f06e2104fd63898cb1472bf546b6e6a3fea2da23fb2a04`  
		Last Modified: Tue, 04 Jan 2022 01:45:50 GMT  
		Size: 4.7 KB (4714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddf90eba6bab41af9537a38132f557697c0b1bce216c4823a073f1e899550f7`  
		Last Modified: Tue, 04 Jan 2022 01:45:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:3c9cf1bdb4e58ba79f4cf8e707e8296f6e11230ff45163a2f47845736aba7bf2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81622764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c447e93cff3c007c6c41759650dbbb8cc3734c6b7bd93c4f0924addd135c8d5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Dec 2021 02:09:07 GMT
ADD file:9e5931d5ed32a23b2e93bd8846258c647613637c581b6813bbc7d7e6b86bbdf5 in / 
# Tue, 21 Dec 2021 02:09:08 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:46:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 19:46:42 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 21 Dec 2021 19:46:42 GMT
ENV GOSU_VERSION=1.14
# Tue, 21 Dec 2021 19:47:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 21 Dec 2021 19:47:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 21 Dec 2021 19:47:27 GMT
ENV LANG=en_US.utf8
# Tue, 21 Dec 2021 19:47:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:47:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 21 Dec 2021 19:47:45 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 21 Dec 2021 23:18:17 GMT
ENV PG_MAJOR=10
# Tue, 21 Dec 2021 23:18:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Tue, 21 Dec 2021 23:18:18 GMT
ENV PG_VERSION=10.19-1.pgdg110+1
# Tue, 21 Dec 2021 23:53:41 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 21 Dec 2021 23:53:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 21 Dec 2021 23:53:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 21 Dec 2021 23:53:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Dec 2021 23:53:48 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 21 Dec 2021 23:53:48 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:07:55 GMT
COPY file:b2fac085615145a2bee98d4185ef0748655fa7c086ca21daef1ca6cac272bf59 in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:07:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:07:57 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:07:57 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:07:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a6edb95e2485a5b9b3c44b27b7ebad16384c0e08a3d61b7e48c65d7278763cf`  
		Last Modified: Tue, 21 Dec 2021 02:18:14 GMT  
		Size: 29.6 MB (29619177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653335db2e28f4bfd481492903832070d7b54f24e6dbe67b45fbffb8f93f5f20`  
		Last Modified: Wed, 22 Dec 2021 00:29:22 GMT  
		Size: 4.4 MB (4402849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383e4074bda5fb21527af7a93e33f31c633e43a90f4e44b18a33310b19b408fb`  
		Last Modified: Wed, 22 Dec 2021 00:29:17 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f76b983b76977ca3c9f7673149aeb74d2c70667cdaa2fd417ad3230f650169`  
		Last Modified: Wed, 22 Dec 2021 00:29:19 GMT  
		Size: 1.3 MB (1298144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7171701033e64ea4d7fa9ccf50c04e53f4dc6c699892fd7e860ea1a5a8909e`  
		Last Modified: Wed, 22 Dec 2021 00:29:23 GMT  
		Size: 8.0 MB (8043972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116ca8f780ee3685a34795364c930ee965bfb719b63da395abf7ffd84fd9b0cd`  
		Last Modified: Wed, 22 Dec 2021 00:29:15 GMT  
		Size: 439.2 KB (439173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87675c81c5f9c9c33f33cb6639eb0d676b031d16b7d33da01e300cb5ac98845c`  
		Last Modified: Wed, 22 Dec 2021 00:29:15 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc52613f4cea3e4b18408762b08e16750865b57c281ec9e1e567fe182a169ea`  
		Last Modified: Wed, 22 Dec 2021 00:29:15 GMT  
		Size: 3.1 KB (3058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19b157d601e053bd262de4dc3a71e08d00a91521590d8626ed4a2f5b1cad7b9`  
		Last Modified: Wed, 22 Dec 2021 00:35:07 GMT  
		Size: 37.8 MB (37801288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a61478afdff09cf99f671d8bba752e70880b02bedbac685b4567fad96591aa8`  
		Last Modified: Wed, 22 Dec 2021 00:34:36 GMT  
		Size: 8.1 KB (8083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b1560d76cfccc63f6a8f5551444683d400d0d1bdb6fccc789a24f654a8f75`  
		Last Modified: Wed, 22 Dec 2021 00:34:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a4d8b3a9e05fc1bbbe8aed78b01ea0990ea0bbbc5155f3240593964967517d`  
		Last Modified: Wed, 22 Dec 2021 00:34:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee0f59679d60e39cd39d3a968bb7fa0e95a372a5a6117c72dc76d4cb8445c7b`  
		Last Modified: Tue, 04 Jan 2022 01:09:49 GMT  
		Size: 4.7 KB (4714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c705f62fe6b59e7a43f9b164741ec48cb5697fada494d3f48336ddc6eb010b`  
		Last Modified: Tue, 04 Jan 2022 01:09:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:49b7113b7fa45bafa1c36686c04da64c304fcda31bf9a108072329443841ad3b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90709805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c801a3d52893e561a7c632d63e52143590f45c91fddb9f91fd9fd961496e0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Dec 2021 02:20:24 GMT
ADD file:078a17bf7e519cb7a60fbbf743ba7e5897554201cb44957154ab518d6991a033 in / 
# Tue, 21 Dec 2021 02:20:28 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:32:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 19:32:29 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 21 Dec 2021 19:32:32 GMT
ENV GOSU_VERSION=1.14
# Tue, 21 Dec 2021 19:33:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 21 Dec 2021 19:33:41 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 21 Dec 2021 19:33:45 GMT
ENV LANG=en_US.utf8
# Tue, 21 Dec 2021 19:34:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:34:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 21 Dec 2021 19:34:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 21 Dec 2021 19:47:59 GMT
ENV PG_MAJOR=10
# Tue, 21 Dec 2021 19:48:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Tue, 21 Dec 2021 19:48:05 GMT
ENV PG_VERSION=10.19-1.pgdg110+1
# Tue, 21 Dec 2021 19:49:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 21 Dec 2021 19:49:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 21 Dec 2021 19:49:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 21 Dec 2021 19:49:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Dec 2021 19:49:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 21 Dec 2021 19:49:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:19:27 GMT
COPY file:b2fac085615145a2bee98d4185ef0748655fa7c086ca21daef1ca6cac272bf59 in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:19:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:19:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:19:36 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:19:38 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:19:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3345479fea0cdce1382b927b0908af4f239b288b30efa203c50edf7ac0cb055e`  
		Last Modified: Tue, 21 Dec 2021 02:29:20 GMT  
		Size: 35.3 MB (35258992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08fad619d5e9b9134c50ee46d26ef57809bfd04852d94a70061b465fedc2585`  
		Last Modified: Tue, 21 Dec 2021 19:55:57 GMT  
		Size: 5.2 MB (5222905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7102b847099d38448e8497d5c9b44e7f49361334982bf01fda2a73889b9878`  
		Last Modified: Tue, 21 Dec 2021 19:55:53 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0c6341861b7e8f732f3cedf24bf499bd159fbeef06cc0fd930903f828d113b`  
		Last Modified: Tue, 21 Dec 2021 19:55:53 GMT  
		Size: 1.3 MB (1317578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371ec02786458e7b7790fdf8d336a55bed62bc6eedbd144764af964a5181ae0e`  
		Last Modified: Tue, 21 Dec 2021 19:55:54 GMT  
		Size: 8.0 MB (8045507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4be2382fa6b141791fb24b126e80a5bee7e0217eee2a2a84108bcf8e3552a59`  
		Last Modified: Tue, 21 Dec 2021 19:55:52 GMT  
		Size: 451.7 KB (451666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eecb4fbb66e4fea8d2b8dea47313c87717e686ccd4171ca1596bf1105b5558`  
		Last Modified: Tue, 21 Dec 2021 19:55:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5242e0f07598b8e0622a3525e3dfeca963999a00291b9d74c727d0c15314f8fe`  
		Last Modified: Tue, 21 Dec 2021 19:55:49 GMT  
		Size: 3.1 KB (3058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431286a2d75f64c5c95a2f901fb6c618447eb582df0fa700bc110bc1fe2390a`  
		Last Modified: Tue, 21 Dec 2021 19:58:39 GMT  
		Size: 40.4 MB (40394897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041595c7aba1e869546e8e60663193d9063998873ccf46d2ea70dc5ad7113140`  
		Last Modified: Tue, 21 Dec 2021 19:58:27 GMT  
		Size: 8.1 KB (8083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d044fb35260e3aacd917fb906c9f49d13fcd34c7157ea25d61300bef3b521469`  
		Last Modified: Tue, 21 Dec 2021 19:58:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffb764c615f767ee2dfcd4127ea9588da975ff06fd6efef9c3eeec7e238cddd`  
		Last Modified: Tue, 21 Dec 2021 19:58:27 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efb3397132aa500b21d0b52767bc787ba7fc4b8e933245202f0e5754d453b28`  
		Last Modified: Tue, 04 Jan 2022 01:25:25 GMT  
		Size: 4.7 KB (4712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e4465ebd397f399544e7db23fde8c62222ed4ed582bd962196d3415fc5f22f`  
		Last Modified: Tue, 04 Jan 2022 01:25:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:ec3901fca654b776876f3e2db3005fb227c1482858db9731c7ab792c673c6ae9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82922804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb6f2111630e062061046b14ef658a2c3c3d5b70c9868184c7e802bfd1f1f08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:27 GMT
ADD file:c8a482d41bf09dfb6484bf2a6e38535bf0594d26dd6eedd5abde4e3cc811fa6c in / 
# Tue, 21 Dec 2021 01:42:29 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 07:19:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 07:19:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 21 Dec 2021 07:19:34 GMT
ENV GOSU_VERSION=1.14
# Tue, 21 Dec 2021 07:19:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 21 Dec 2021 07:19:47 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 21 Dec 2021 07:19:48 GMT
ENV LANG=en_US.utf8
# Tue, 21 Dec 2021 07:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 07:19:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 21 Dec 2021 07:19:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 21 Dec 2021 07:55:14 GMT
ENV PG_MAJOR=10
# Tue, 21 Dec 2021 07:55:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Tue, 21 Dec 2021 07:55:14 GMT
ENV PG_VERSION=10.19-1.pgdg110+1
# Tue, 21 Dec 2021 08:01:31 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 21 Dec 2021 08:01:33 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 21 Dec 2021 08:01:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 21 Dec 2021 08:01:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Dec 2021 08:01:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 21 Dec 2021 08:01:35 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:42:45 GMT
COPY file:b2fac085615145a2bee98d4185ef0748655fa7c086ca21daef1ca6cac272bf59 in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:42:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:42:46 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:42:46 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:42:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:12562551722a758d23ceea9abcdc2bee737e38c8f62a0f3d3afb2cc2626c28b1`  
		Last Modified: Tue, 21 Dec 2021 01:48:15 GMT  
		Size: 29.6 MB (29641636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f342e6f0f3ddf6c3dafd520793311df8f4c603d2830585b7118909d91c05fb9c`  
		Last Modified: Tue, 21 Dec 2021 08:09:46 GMT  
		Size: 4.3 MB (4302230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd86460cfec7bb37c67c150741c85a49b917a3173b197fe40c2feeec89c4be9`  
		Last Modified: Tue, 21 Dec 2021 08:09:46 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b186fd2afab6b0a036714b95b838a8a3f3e579eadda7b367091509e8266c8f44`  
		Last Modified: Tue, 21 Dec 2021 08:09:46 GMT  
		Size: 1.4 MB (1381394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47cac5ae9ecf4b30344088ef2144a698445bfbc7e46f1b9110db44d05db890d`  
		Last Modified: Tue, 21 Dec 2021 08:09:46 GMT  
		Size: 8.1 MB (8099091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc00d5d9893faa3f8f563ecb0933c5a7809067c87245abcadc1a7bde564f8c93`  
		Last Modified: Tue, 21 Dec 2021 08:09:45 GMT  
		Size: 438.4 KB (438355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a4a20d7ea918ba7711a33ce7e6e76cc8cc72527c2147ec9fd70779d7e2adc4`  
		Last Modified: Tue, 21 Dec 2021 08:09:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da51307c57fca2dab3aa9b518c39aff4457ef33cfee64ffd256bb2be08dcfd7`  
		Last Modified: Tue, 21 Dec 2021 08:09:45 GMT  
		Size: 3.1 KB (3053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b50bc1c05e3782f8116aa2b27e89d3eac523f670e73f50d478724c12c26150`  
		Last Modified: Tue, 21 Dec 2021 08:11:35 GMT  
		Size: 39.0 MB (39041856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902bca178d92e116b1b9f90a9884fb7bca439ee4444b2d4b886738ca972c0380`  
		Last Modified: Tue, 21 Dec 2021 08:11:28 GMT  
		Size: 8.1 KB (8076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827866db91cdc9803cf5a07f1ca8cec37445f3a59558d302d8170d78218e447e`  
		Last Modified: Tue, 21 Dec 2021 08:11:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b3892bc815891ac9651b837556a3b659634a3e19d33c5cf60f752bf76e5297`  
		Last Modified: Tue, 21 Dec 2021 08:11:28 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af924847a5e046f57144f432562541ebf583500e6dadfe460fa128b45301da9`  
		Last Modified: Tue, 04 Jan 2022 01:46:42 GMT  
		Size: 4.7 KB (4709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688d2fef71e8efb408376f366a1307485681e8531bd906644fb66935401416c4`  
		Last Modified: Tue, 04 Jan 2022 01:46:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
