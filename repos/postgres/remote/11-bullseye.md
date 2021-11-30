## `postgres:11-bullseye`

```console
$ docker pull postgres@sha256:c1b74313b4bf0cc9020cf094359701646dfb744fcd19be8f028ecf038da277a9
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

### `postgres:11-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:c28f3cd4110d7049743b0be01c6885b139fa8fbe978203d0b801d787d8a6dd21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134332865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7313489f82c11be840376188824ae56dddd9d4d122716605d1238ede49bb99c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 21:54:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 21:54:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 30 Nov 2021 04:58:24 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Nov 2021 04:58:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Nov 2021 04:58:41 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 30 Nov 2021 04:58:41 GMT
ENV LANG=en_US.utf8
# Tue, 30 Nov 2021 04:58:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Nov 2021 04:58:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 30 Nov 2021 04:58:51 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 30 Nov 2021 05:25:09 GMT
ENV PG_MAJOR=11
# Tue, 30 Nov 2021 05:25:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Tue, 30 Nov 2021 05:25:10 GMT
ENV PG_VERSION=11.14-1.pgdg110+1
# Tue, 30 Nov 2021 05:25:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 30 Nov 2021 05:25:45 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 30 Nov 2021 05:25:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 30 Nov 2021 05:25:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Nov 2021 05:25:49 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 30 Nov 2021 05:25:49 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Nov 2021 05:25:50 GMT
COPY file:6e4de9271291e4bdd4a40b73fffe4d6d1aeff033460f5b14d74e948686daa095 in /usr/local/bin/ 
# Tue, 30 Nov 2021 05:25:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 05:25:50 GMT
STOPSIGNAL SIGINT
# Tue, 30 Nov 2021 05:25:51 GMT
EXPOSE 5432
# Tue, 30 Nov 2021 05:25:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b4ab3ade5ac7d8afea5bd7c2ba3747bcbeedcffa046a29b403f0fb358691c`  
		Last Modified: Wed, 17 Nov 2021 22:01:37 GMT  
		Size: 4.4 MB (4414468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108afa831d95d33af5adc9360a1bf1e5635459bb3ec8e3d9bd2ceb1c82b2632c`  
		Last Modified: Wed, 17 Nov 2021 22:01:36 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f36a620c9a0d4789b1cc287e7cbc0fdb05a9de195131783608c7e5768b845e`  
		Last Modified: Tue, 30 Nov 2021 05:48:14 GMT  
		Size: 1.4 MB (1418386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c78220cdd7f632a539dc45b5f88e431dc0504bdd21f7c20b37985d747abc379`  
		Last Modified: Tue, 30 Nov 2021 05:48:14 GMT  
		Size: 8.0 MB (8045287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fc8d555476ac466ce5474480981d09392b67fee009c0faebf7548ab5b4bb02`  
		Last Modified: Tue, 30 Nov 2021 05:48:12 GMT  
		Size: 441.6 KB (441629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf6f19a1e0f722a85c250ed5f0c54bbe44cd12e9ff87dee3fb8580c21402116`  
		Last Modified: Tue, 30 Nov 2021 05:48:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5367c24392415d54d11bea3e29d555f55dd363f7fb49cf9bd08a7793f575b6c7`  
		Last Modified: Tue, 30 Nov 2021 05:48:11 GMT  
		Size: 3.1 KB (3057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c806a3d4700c06d90b0ca8d294cb666a4b0c82e6227b3a1da39d96f2651ea343`  
		Last Modified: Tue, 30 Nov 2021 05:51:51 GMT  
		Size: 88.6 MB (88624449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1af72c8010dae2b8280409b4f34eec378f3bc0bcfcdd5f7969d5e74969c573`  
		Last Modified: Tue, 30 Nov 2021 05:51:38 GMT  
		Size: 8.3 KB (8328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655b9845e6f5c125365b398b5eb8958bbea8f0380f672a3f66f8aa7f0f99562a`  
		Last Modified: Tue, 30 Nov 2021 05:51:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c17c5b3563109d5f698a9d0b31f6c747725b344d2a9bfc2caa28bad957fd74`  
		Last Modified: Tue, 30 Nov 2021 05:51:38 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eefa64674909abf64bcd68357c6f011b0b658684a9f71b29341d1867f86b874`  
		Last Modified: Tue, 30 Nov 2021 05:51:38 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:7fc337ce78a44ca9f48ae4792fc31bf0dbb9081e8aa64b58c9468fcba391b6a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127577657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5585a82e02dc8a3fda8eb38301f12cd9d4897b2f0f0911fffd6a2d5e62b4bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Nov 2021 02:50:37 GMT
ADD file:738a04a17bdb9077594ad9a847333abe28216a7f04d3058718a5e21c236c24bb in / 
# Wed, 17 Nov 2021 02:50:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 07:04:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 07:04:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 30 Nov 2021 03:28:14 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Nov 2021 03:28:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Nov 2021 03:29:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 30 Nov 2021 03:29:04 GMT
ENV LANG=en_US.utf8
# Tue, 30 Nov 2021 03:29:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Nov 2021 03:29:16 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 30 Nov 2021 03:29:19 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 30 Nov 2021 04:46:14 GMT
ENV PG_MAJOR=11
# Tue, 30 Nov 2021 04:46:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Tue, 30 Nov 2021 04:46:15 GMT
ENV PG_VERSION=11.14-1.pgdg110+1
# Tue, 30 Nov 2021 09:29:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 30 Nov 2021 09:29:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 30 Nov 2021 09:29:09 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 30 Nov 2021 09:29:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Nov 2021 09:29:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 30 Nov 2021 09:29:11 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Nov 2021 09:29:12 GMT
COPY file:6e4de9271291e4bdd4a40b73fffe4d6d1aeff033460f5b14d74e948686daa095 in /usr/local/bin/ 
# Tue, 30 Nov 2021 09:29:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 09:29:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Nov 2021 09:29:13 GMT
EXPOSE 5432
# Tue, 30 Nov 2021 09:29:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a960a56baa1baffbe2aa1e0c1fb02f9ee4816337d02fec259b312c409d77fafc`  
		Last Modified: Wed, 17 Nov 2021 03:06:09 GMT  
		Size: 28.9 MB (28911006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2ac9e3ed26a54de75a39a02c813343c2f2da6d330db5aedec6ce0c53224e9c`  
		Last Modified: Wed, 17 Nov 2021 11:38:04 GMT  
		Size: 4.1 MB (4096446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940c573b71bfb0dc5d6257ac0a038c717a7659ce616e33ce43ab01fe09be44ec`  
		Last Modified: Wed, 17 Nov 2021 11:38:01 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6152fb09c0f5e7d2cc8e098e7c775069fb152c392c8d46d6455198283b0eb8f`  
		Last Modified: Tue, 30 Nov 2021 06:57:37 GMT  
		Size: 1.4 MB (1382589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf6eedb8a4a883a6bee30fb3e5e7f1a297d467c6ff3a76e5bf0917fb9dbc922`  
		Last Modified: Tue, 30 Nov 2021 06:57:41 GMT  
		Size: 8.0 MB (8045209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e523a399f6b98d6c4d5d2ce105ddb3c4922e3a4af50d344707bf708b957f353`  
		Last Modified: Tue, 30 Nov 2021 06:57:35 GMT  
		Size: 439.9 KB (439869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7172045007d975f925a294a0c4180ec6ba5e20a528efe89df20c55334b9c4e`  
		Last Modified: Tue, 30 Nov 2021 06:57:36 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e88e93259d74b937ed812db0f0bfa2bbdeaf2294bc4f271b914ca27bccfd251`  
		Last Modified: Tue, 30 Nov 2021 06:57:35 GMT  
		Size: 3.1 KB (3059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c29ae28a8cfc0f4c0d8eb9fe751d20d27e057a233d0c7686bda348851afd0e5`  
		Last Modified: Tue, 30 Nov 2021 09:35:06 GMT  
		Size: 84.7 MB (84684156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bb62dd1ceef80622c90524429898367e6c4d40d78d03d331794fac2cb08cb2`  
		Last Modified: Tue, 30 Nov 2021 09:34:12 GMT  
		Size: 8.3 KB (8333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b09b2fdfa89212c8b59ba7ea8d4924bdc4b90e66ee7205c028b16054fb6d511`  
		Last Modified: Tue, 30 Nov 2021 09:34:12 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08fe1af671ddbb2f33367580766e01c0f63da7b2dd562227500381559f43e10`  
		Last Modified: Tue, 30 Nov 2021 09:34:12 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52606ae0c467d09605a1f32027d89ae441662f6e26c1ba0567022e1acca40a4c`  
		Last Modified: Tue, 30 Nov 2021 09:34:12 GMT  
		Size: 4.7 KB (4716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:17710bf80ded26fc15d41dbb8b1fba5c115310ffd079779a45f9de68d6b02ff1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122597786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f91f90fa84468846f7aba101cb1c08b704b5089f4138d85035455987e6b364d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Nov 2021 01:59:43 GMT
ADD file:cd2ac52107a2ea6657f23850a4b29366309eb39fa177321e0a9fd6d58562ae80 in / 
# Wed, 17 Nov 2021 01:59:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:03:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 18:03:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 17 Nov 2021 18:03:09 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Nov 2021 18:03:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Nov 2021 18:03:49 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 17 Nov 2021 18:03:49 GMT
ENV LANG=en_US.utf8
# Wed, 17 Nov 2021 18:03:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:03:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Nov 2021 18:04:10 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 17 Nov 2021 19:44:08 GMT
ENV PG_MAJOR=11
# Wed, 17 Nov 2021 19:44:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 17 Nov 2021 19:44:09 GMT
ENV PG_VERSION=11.14-1.pgdg110+1
# Wed, 17 Nov 2021 20:15:04 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 17 Nov 2021 20:15:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 17 Nov 2021 20:15:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 17 Nov 2021 20:15:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 17 Nov 2021 20:15:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 17 Nov 2021 20:15:11 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 17 Nov 2021 20:15:12 GMT
COPY file:6e4de9271291e4bdd4a40b73fffe4d6d1aeff033460f5b14d74e948686daa095 in /usr/local/bin/ 
# Wed, 17 Nov 2021 20:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:15:13 GMT
STOPSIGNAL SIGINT
# Wed, 17 Nov 2021 20:15:13 GMT
EXPOSE 5432
# Wed, 17 Nov 2021 20:15:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b6e5ca4da96841e58eb27c88695a059e5105fad5a066de803f4b94ae4002ba66`  
		Last Modified: Wed, 17 Nov 2021 02:15:13 GMT  
		Size: 26.6 MB (26573160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef876aa8c0afe0078ed4f8132182e2d6c94a884d4dce472cea77744820bc9fb`  
		Last Modified: Wed, 17 Nov 2021 22:13:45 GMT  
		Size: 3.7 MB (3717163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74a37ede70c9a36c8032109fff79b082ee9060ea110a45d59ead46d5f42159b`  
		Last Modified: Wed, 17 Nov 2021 22:13:43 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae26ca21bba22f81e35b24e1f77ac61da5f4445512b2d1c694fd3c1a7fa3ee3a`  
		Last Modified: Wed, 17 Nov 2021 22:13:43 GMT  
		Size: 1.4 MB (1402387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b022af5735d1b45d84f5a373033475fb41151fa3bd8ddb50efc2980d3a20e8c6`  
		Last Modified: Wed, 17 Nov 2021 22:13:47 GMT  
		Size: 8.0 MB (8045253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b8341697d7e9eb52c2eb301ad908053771a3c7d5676e1bc7bd3937eb99c84a`  
		Last Modified: Wed, 17 Nov 2021 22:13:41 GMT  
		Size: 434.5 KB (434532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8cc2c0eedfcf76116f35dffe8e4bb5cb537f6e3d22d701a45548b227fc75c6`  
		Last Modified: Wed, 17 Nov 2021 22:13:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d70f71d0a71225751d3ec0e2891899cb368b348761c958059410b7eaaeab35`  
		Last Modified: Wed, 17 Nov 2021 22:13:41 GMT  
		Size: 3.1 KB (3057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2eccc146df12c4e3d5a5536e340a525c26a6a1d654282aad0f240999f52da6`  
		Last Modified: Wed, 17 Nov 2021 22:20:09 GMT  
		Size: 82.4 MB (82406911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9669a0dd1c133eacdec95187f8e6a4de64d613c8ce8642f64f72625a2f1500ad`  
		Last Modified: Wed, 17 Nov 2021 22:19:21 GMT  
		Size: 8.3 KB (8329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d043fa7ae5cca07f399614bf3e3c7d0d778eef10f0cb529fe2e13f111b753d23`  
		Last Modified: Wed, 17 Nov 2021 22:19:20 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da661d02a3c3c0923c61b9462d2dcdc750ba7140c2a20734c88fe562958a134`  
		Last Modified: Wed, 17 Nov 2021 22:19:20 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3991094c576466d86822c9f6d598d65de2eee9958f61b64a3479351bded36`  
		Last Modified: Wed, 17 Nov 2021 22:19:20 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:8dacb528d5df13d1444640f698aa4975323b60b99265a5b48c024f193e1ca0c5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129028926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24e60ab9556845960a37e7ab6e1c8f6c7008c6a370683dbc612b17190efe01e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:15 GMT
ADD file:4203242b2b09a65239092c4780b59181da7b861b3c0be40810b3588aa200f72c in / 
# Wed, 17 Nov 2021 02:40:16 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 10:56:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 10:56:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 30 Nov 2021 04:26:06 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Nov 2021 04:26:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Nov 2021 04:26:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 30 Nov 2021 04:26:22 GMT
ENV LANG=en_US.utf8
# Tue, 30 Nov 2021 04:26:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Nov 2021 04:26:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 30 Nov 2021 04:26:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 30 Nov 2021 04:39:50 GMT
ENV PG_MAJOR=11
# Tue, 30 Nov 2021 04:39:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Tue, 30 Nov 2021 04:39:52 GMT
ENV PG_VERSION=11.14-1.pgdg110+1
# Tue, 30 Nov 2021 04:40:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 30 Nov 2021 04:40:15 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 30 Nov 2021 04:40:16 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 30 Nov 2021 04:40:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Nov 2021 04:40:18 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 30 Nov 2021 04:40:19 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Nov 2021 04:40:21 GMT
COPY file:6e4de9271291e4bdd4a40b73fffe4d6d1aeff033460f5b14d74e948686daa095 in /usr/local/bin/ 
# Tue, 30 Nov 2021 04:40:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 04:40:22 GMT
STOPSIGNAL SIGINT
# Tue, 30 Nov 2021 04:40:23 GMT
EXPOSE 5432
# Tue, 30 Nov 2021 04:40:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eb9a2845ed124d072b117aba4f0508e00c1ecd0d147dc324d14b00d24092046c`  
		Last Modified: Wed, 17 Nov 2021 02:47:17 GMT  
		Size: 30.1 MB (30056521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0a8f5dc8469747b817020b211885445957c2ebbb768fc67891799e36e47cb8`  
		Last Modified: Wed, 17 Nov 2021 11:35:10 GMT  
		Size: 4.2 MB (4208882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d8025a640ac47adb95ca00802aa24eee591c5cf682195cd62eed14df139a1e`  
		Last Modified: Wed, 17 Nov 2021 11:35:09 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3b77b17d26c881dacc0e00745309c888b8730bd3fab5c0046d333c6c8d4a25`  
		Last Modified: Tue, 30 Nov 2021 05:21:58 GMT  
		Size: 1.3 MB (1346085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b00058a7fa17063701aefce71afab312a23255fcaeeebae4d58846234dbdb7c`  
		Last Modified: Tue, 30 Nov 2021 05:21:58 GMT  
		Size: 8.0 MB (8043437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a95a8f3e4724d0de20446b507e102e9b8e6786b823e7f570aa080e566fc5d2`  
		Last Modified: Tue, 30 Nov 2021 05:21:56 GMT  
		Size: 218.6 KB (218616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd56901a45b2f25f68146b9c62f316e3de49aa3f93def385092637ec34ded258`  
		Last Modified: Tue, 30 Nov 2021 05:21:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5941ed27cc1356c51e55e300519ebf714aa2543ac3ee4c0fafab7412928063d`  
		Last Modified: Tue, 30 Nov 2021 05:21:56 GMT  
		Size: 3.0 KB (3027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec483611885f6a525d898b14e4e0b36056e3494625362aa25d7180daee401c7`  
		Last Modified: Tue, 30 Nov 2021 05:25:18 GMT  
		Size: 85.1 MB (85137247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff10e72a0db1dbe9e22e0f7d96f828a4aa971e8d9ad21bcf4de5cc814ba8cc9`  
		Last Modified: Tue, 30 Nov 2021 05:25:07 GMT  
		Size: 8.3 KB (8330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f77ed5cc8e6d2f2d3257ba8fbfc913946eb4da518337f7e2829b6cb16f9dfb`  
		Last Modified: Tue, 30 Nov 2021 05:25:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f308160d1dfed94b91ecbc653f410c2d0144eae55b995a2c1574aa87bb1b9871`  
		Last Modified: Tue, 30 Nov 2021 05:25:07 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1c7cb66be8f0b1927fd99ed80ea3bc94b6211a301c1700516f810e93cd9eaf`  
		Last Modified: Tue, 30 Nov 2021 05:25:07 GMT  
		Size: 4.7 KB (4716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:61c0549c2878a55e08439e97707d62410bb116733418d20798100ab7a3eff6f6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136334196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408b656a383da60c61efaabcb128d10c629f00bbadcfedb574d7f333786e1bc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Nov 2021 02:39:53 GMT
ADD file:ff018048717c0f5aa1730480d0bfea1c2bf94d6e2dae2d7cef46d05ffb0d93e1 in / 
# Wed, 17 Nov 2021 02:39:53 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:42:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 13:42:31 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 30 Nov 2021 02:22:34 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Nov 2021 02:23:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Nov 2021 02:23:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 30 Nov 2021 02:23:17 GMT
ENV LANG=en_US.utf8
# Tue, 30 Nov 2021 02:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Nov 2021 02:23:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 30 Nov 2021 02:23:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 30 Nov 2021 03:41:18 GMT
ENV PG_MAJOR=11
# Tue, 30 Nov 2021 03:41:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Tue, 30 Nov 2021 03:41:18 GMT
ENV PG_VERSION=11.14-1.pgdg110+1
# Tue, 30 Nov 2021 03:57:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 30 Nov 2021 03:57:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 30 Nov 2021 03:57:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 30 Nov 2021 03:57:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Nov 2021 03:57:04 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 30 Nov 2021 03:57:04 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Nov 2021 03:57:05 GMT
COPY file:6e4de9271291e4bdd4a40b73fffe4d6d1aeff033460f5b14d74e948686daa095 in /usr/local/bin/ 
# Tue, 30 Nov 2021 03:57:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 03:57:05 GMT
STOPSIGNAL SIGINT
# Tue, 30 Nov 2021 03:57:05 GMT
EXPOSE 5432
# Tue, 30 Nov 2021 03:57:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0bae0e1d4cb1d56ffeb9d05de7a097d3157267eef07b6d8131344d99bd97c431`  
		Last Modified: Wed, 17 Nov 2021 02:47:49 GMT  
		Size: 32.4 MB (32380683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47dc0c82cbdb8d80bc1e74add189651c4ffd82853181cb884190c0781a720bb`  
		Last Modified: Wed, 17 Nov 2021 15:21:35 GMT  
		Size: 4.8 MB (4812958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a5817009e5bad1ebe7c8bdaeb9bf7528a1dbf5f160bb79da932163b814a887`  
		Last Modified: Wed, 17 Nov 2021 15:21:33 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224d92437c5d642dc59456a1db1b95f8a3b56a04f34f3caaf91e85ad55ee1b7`  
		Last Modified: Tue, 30 Nov 2021 04:42:56 GMT  
		Size: 1.4 MB (1385584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b188aabed17ad4819a6802ce244fe2ae1ad0abc44cc8b45d61a0745a50fa86`  
		Last Modified: Tue, 30 Nov 2021 04:42:56 GMT  
		Size: 8.0 MB (8045186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ffbc79a6052c96f094712da112483d243d8fc9f67b1933bca51bd977c020fc`  
		Last Modified: Tue, 30 Nov 2021 04:42:53 GMT  
		Size: 448.1 KB (448065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e49a8f355f9a7ad2b204f215d77c352a4a2d00004dbd9bb5cb142564f545a9`  
		Last Modified: Tue, 30 Nov 2021 04:42:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1b3e8bea3acd7a497b47480f01ccde1bdafbcb01ff320a37a4e56a79d3c453`  
		Last Modified: Tue, 30 Nov 2021 04:42:53 GMT  
		Size: 3.1 KB (3054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3dbd0a71d5e3a86ae9bccb998682707c47875ab38fcd61fe11c53f197f0b89`  
		Last Modified: Tue, 30 Nov 2021 04:47:24 GMT  
		Size: 89.2 MB (89243350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f692eee7b32ac27e0cf0f53fcd905e713ae43053b929ff44639d52cdf10adb8e`  
		Last Modified: Tue, 30 Nov 2021 04:47:04 GMT  
		Size: 8.3 KB (8323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9356f966580c2373cbb1d54928f406d002f61c4d049f82096a7cb20fd804e96f`  
		Last Modified: Tue, 30 Nov 2021 04:47:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86758fd50c04413350c903000f93c942c12eccd2419184b8f8ec3a164b12af2e`  
		Last Modified: Tue, 30 Nov 2021 04:47:04 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1185ef2bdc7bc5fde02fc69a6b78544b76b8d3d7c6a4448fdf221ef4a84cb0b6`  
		Last Modified: Tue, 30 Nov 2021 04:47:04 GMT  
		Size: 4.7 KB (4724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:ab792ef5d252373bd4c99dd6904328af97dfb8741871e83d3d3d42494ebfe633
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129154285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:defe81c9d752c89cad1511d23375ecd85eb7b221dc0eba1568463cc7e4c7c6a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Nov 2021 02:10:13 GMT
ADD file:10bc783d286d0a800f59d5009e87ecb4651659c82cae1325132756c7c8b1dec0 in / 
# Wed, 17 Nov 2021 02:10:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:38:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 03:38:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 30 Nov 2021 03:51:38 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Nov 2021 03:51:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Nov 2021 03:52:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 30 Nov 2021 03:52:24 GMT
ENV LANG=en_US.utf8
# Tue, 30 Nov 2021 03:52:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Nov 2021 03:52:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 30 Nov 2021 03:52:41 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 30 Nov 2021 06:33:15 GMT
ENV PG_MAJOR=11
# Tue, 30 Nov 2021 06:33:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Tue, 30 Nov 2021 06:33:15 GMT
ENV PG_VERSION=11.14-1.pgdg110+1
# Tue, 30 Nov 2021 07:22:34 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 30 Nov 2021 07:22:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 30 Nov 2021 07:22:39 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 30 Nov 2021 07:22:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Nov 2021 07:22:41 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 30 Nov 2021 07:22:42 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Nov 2021 07:22:42 GMT
COPY file:6e4de9271291e4bdd4a40b73fffe4d6d1aeff033460f5b14d74e948686daa095 in /usr/local/bin/ 
# Tue, 30 Nov 2021 07:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 07:22:43 GMT
STOPSIGNAL SIGINT
# Tue, 30 Nov 2021 07:22:43 GMT
EXPOSE 5432
# Tue, 30 Nov 2021 07:22:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08bca22fbffb4e58224e9e4f6a56f1ca5099c002b1aeb6181df63af308a3da58`  
		Last Modified: Wed, 17 Nov 2021 02:19:09 GMT  
		Size: 29.6 MB (29630388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173240a7e67fd44ecc0ad5edd818557628d50f00c5d2a5f3d580e0a2ac091610`  
		Last Modified: Wed, 17 Nov 2021 08:20:21 GMT  
		Size: 4.4 MB (4402817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5442a27e75e2c0fbbf3bcf39b1c33f75d31863490f96ba2f0f1921ef6da25caf`  
		Last Modified: Wed, 17 Nov 2021 08:20:17 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2054e4460d2a19717dd4a336b47653df9571eda928f0f361edc1ab86244ddcc2`  
		Last Modified: Tue, 30 Nov 2021 08:33:27 GMT  
		Size: 1.3 MB (1298194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7d76eb66b099fba3c2444676a5f23198b89f04ca562d92fe3cbad93e17ed6f`  
		Last Modified: Tue, 30 Nov 2021 08:33:31 GMT  
		Size: 8.0 MB (8043954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde934ccf5b463f3cc67c5e044fdb538461feed010e478a8adb22f25017f220b`  
		Last Modified: Tue, 30 Nov 2021 08:33:24 GMT  
		Size: 439.2 KB (439195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0517cbc7ba02213b80d94a9809694781806502aef56896f981df723099874173`  
		Last Modified: Tue, 30 Nov 2021 08:33:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ff4ee65102820557350a5542a9ce98ad5efe0fcb3cf0a382b9ef99f9850a99`  
		Last Modified: Tue, 30 Nov 2021 08:33:23 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd6d30a8c56ed217fd23deb58751b197dcfdd121ee34c10fde89dd792e27d35`  
		Last Modified: Tue, 30 Nov 2021 08:38:37 GMT  
		Size: 85.3 MB (85321457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1a1a384467a4ec93314fc945d08f8c92912d8ef664cedfe88e709319a0ac4b`  
		Last Modified: Tue, 30 Nov 2021 08:37:38 GMT  
		Size: 8.3 KB (8331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564b2c511c2bf47c51e509da01430303b9d7659af6baa192680eb2ed79362b32`  
		Last Modified: Tue, 30 Nov 2021 08:37:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be47d5915a263791a09a35a1282dc358b2424e5fe938f7d111c6c0138f84ee77`  
		Last Modified: Tue, 30 Nov 2021 08:37:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c54d5be75ef078e0ad275340aae9f3f86d79da5c5d6413da9316a9ad1685f9`  
		Last Modified: Tue, 30 Nov 2021 08:37:38 GMT  
		Size: 4.7 KB (4716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:e62ea3ab98a248b56021784690b3e66bbca1eb2da6a9ef9a0e1a433a8eb76763
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143085600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19350f4be3ee8de4bc0e9f133616b07cb2a997b2c4c152b45c712979784060e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Nov 2021 03:28:22 GMT
ADD file:5ed330f0fe1328f694fcaefb961cf4da4d8a4ff03100b21af718b69316168706 in / 
# Wed, 17 Nov 2021 03:28:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 12:35:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 12:35:29 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 30 Nov 2021 04:22:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Nov 2021 04:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Nov 2021 04:23:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 30 Nov 2021 04:23:25 GMT
ENV LANG=en_US.utf8
# Tue, 30 Nov 2021 04:23:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Nov 2021 04:23:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 30 Nov 2021 04:24:02 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 30 Nov 2021 04:48:06 GMT
ENV PG_MAJOR=11
# Tue, 30 Nov 2021 04:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Tue, 30 Nov 2021 04:48:08 GMT
ENV PG_VERSION=11.14-1.pgdg110+1
# Tue, 30 Nov 2021 04:49:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 30 Nov 2021 04:49:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 30 Nov 2021 04:49:19 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 30 Nov 2021 04:49:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Nov 2021 04:49:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 30 Nov 2021 04:49:28 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Nov 2021 04:49:29 GMT
COPY file:6e4de9271291e4bdd4a40b73fffe4d6d1aeff033460f5b14d74e948686daa095 in /usr/local/bin/ 
# Tue, 30 Nov 2021 04:49:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 04:49:32 GMT
STOPSIGNAL SIGINT
# Tue, 30 Nov 2021 04:49:34 GMT
EXPOSE 5432
# Tue, 30 Nov 2021 04:49:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:258ff2a13858db8f51b65662e02137c0abcfd2528ca73e92b7a40061d938fb1e`  
		Last Modified: Wed, 17 Nov 2021 03:54:34 GMT  
		Size: 35.3 MB (35271382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b509e11eadbd1f0594371e0c0328a97ea632aee62bcb4d80035bf0eb4e27d9`  
		Last Modified: Wed, 17 Nov 2021 12:54:55 GMT  
		Size: 5.2 MB (5222878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098bb2fd895d09bedc6646b1f22374ade668fedde3c9f80a50c9c2608420a5b`  
		Last Modified: Wed, 17 Nov 2021 12:54:52 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35b2a8dfe6aeea228d81c43283e5a62e5953809f4a37c66206ba07e6b1f8627`  
		Last Modified: Tue, 30 Nov 2021 05:09:39 GMT  
		Size: 1.3 MB (1317537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c1943e77464726e531ba0fa41402bf8b74e45d88b2f66a3ac4d88c8e91445d`  
		Last Modified: Tue, 30 Nov 2021 05:09:41 GMT  
		Size: 8.0 MB (8045492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43663cab90f09a0a9f91d3d042e111627e277fe2a8787747840d43232f316b3`  
		Last Modified: Tue, 30 Nov 2021 05:09:35 GMT  
		Size: 451.6 KB (451618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804f299ce3f30a2131f474586ce820567662cf36273a04aff65c57497ee55fb`  
		Last Modified: Tue, 30 Nov 2021 05:09:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f36786db7d917c78021991cf37d395dd46c97e91ea5290fbb7f25d7bcbd318`  
		Last Modified: Tue, 30 Nov 2021 05:09:35 GMT  
		Size: 3.1 KB (3053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84632b8bd8e035ead90a6596c66a87896123f5633f81358ba3893937b7eba443`  
		Last Modified: Tue, 30 Nov 2021 05:14:27 GMT  
		Size: 92.8 MB (92758305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608606887d7f03a8d8c71d423ddbdff76b5deed302e83f08358f66cda581d632`  
		Last Modified: Tue, 30 Nov 2021 05:14:11 GMT  
		Size: 8.3 KB (8335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61e401ec35e40539dba18807a5256c026cf8ae0c09b15dfd87c151ee32e8f68`  
		Last Modified: Tue, 30 Nov 2021 05:14:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa7dc2c5a5aba5bc5a2009d1ef723dc53db22f41f94c07226d5d4b7601d5203`  
		Last Modified: Tue, 30 Nov 2021 05:14:10 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6735561df527016432f9269bad5d3b989bf6e4a020b6f7b4f823d9c60c13de`  
		Last Modified: Tue, 30 Nov 2021 05:14:10 GMT  
		Size: 4.7 KB (4715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:6a44b01575a250c2fd71aee2cbb64d6f034c3d99fa3ff88ab92e7e21b79a12e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138061614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f202153eec26ac268b24eb5442585391cb7551e849811f0b536c37f2775b4af4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:27 GMT
ADD file:42f73dac307a6a5232e3100f3d3b36e8125f73a4ca504b106e60e2b66d242b2f in / 
# Wed, 17 Nov 2021 02:42:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 04:19:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 04:19:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 30 Nov 2021 08:40:04 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Nov 2021 08:40:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Nov 2021 08:40:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 30 Nov 2021 08:40:17 GMT
ENV LANG=en_US.utf8
# Tue, 30 Nov 2021 08:40:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Nov 2021 08:40:21 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 30 Nov 2021 08:40:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 30 Nov 2021 09:15:13 GMT
ENV PG_MAJOR=11
# Tue, 30 Nov 2021 09:15:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Tue, 30 Nov 2021 09:15:13 GMT
ENV PG_VERSION=11.14-1.pgdg110+1
# Tue, 30 Nov 2021 09:23:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 30 Nov 2021 09:23:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 30 Nov 2021 09:23:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 30 Nov 2021 09:23:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Nov 2021 09:23:30 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 30 Nov 2021 09:23:30 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Nov 2021 09:23:30 GMT
COPY file:6e4de9271291e4bdd4a40b73fffe4d6d1aeff033460f5b14d74e948686daa095 in /usr/local/bin/ 
# Tue, 30 Nov 2021 09:23:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 09:23:31 GMT
STOPSIGNAL SIGINT
# Tue, 30 Nov 2021 09:23:31 GMT
EXPOSE 5432
# Tue, 30 Nov 2021 09:23:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8d71e885edf612b507bbdcc48a970548d436b8709eeedfc2c98f6843a214b5e2`  
		Last Modified: Wed, 17 Nov 2021 02:48:25 GMT  
		Size: 29.7 MB (29650960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f117b4d1df6500c1b1b8489bf7f0c4a49ebfed67aa499b78150ab0fdf26ef25`  
		Last Modified: Wed, 17 Nov 2021 05:07:31 GMT  
		Size: 4.3 MB (4302200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6121d676711df302dfeaa794390cdb627d2ce10fe23004c4dca743581730c9`  
		Last Modified: Wed, 17 Nov 2021 05:07:30 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2521af9885f1d52a07c8fab37668726694a323dff40da457b93bdcbb403393a2`  
		Last Modified: Tue, 30 Nov 2021 09:46:19 GMT  
		Size: 1.4 MB (1381393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433801c4665ae2cb3cc25bccc44049e9f5862f408a6f72bb81e717c4b2649d7e`  
		Last Modified: Tue, 30 Nov 2021 09:46:19 GMT  
		Size: 8.1 MB (8099111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2942930c51f5262403a850a2cee58c0ee918dcd6350fc825a9067dcca86cdeed`  
		Last Modified: Tue, 30 Nov 2021 09:46:17 GMT  
		Size: 438.3 KB (438335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405434a7a3640e8df44a267f2e98a2da8d1fea4c02c9bacb7ae53e311f71fb20`  
		Last Modified: Tue, 30 Nov 2021 09:46:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149e15d5acb4f2f6c65fe6ed786d09a003dad410b5593636c25d2b1bf6db13ed`  
		Last Modified: Tue, 30 Nov 2021 09:46:17 GMT  
		Size: 3.1 KB (3056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6777069688968d7d33fa1c79c274936fa2f835dddcbdd1862bb0b0234d89bf8e`  
		Last Modified: Tue, 30 Nov 2021 09:48:38 GMT  
		Size: 94.2 MB (94171226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663b1ff2fa9f53d7700a775835be859311fa7b036c521d4e7175233891fed65b`  
		Last Modified: Tue, 30 Nov 2021 09:48:27 GMT  
		Size: 8.3 KB (8331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9a3df569911f095f4bc40a9d07f5ab0123ff2b489b7fb868069031a1d76a23`  
		Last Modified: Tue, 30 Nov 2021 09:48:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632f4a3340830e116c1d2e8ce8bff561596c31db5ec8f96da68387645e265584`  
		Last Modified: Tue, 30 Nov 2021 09:48:27 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40325e1dd84bbc02f35c22ef2b6fe41c34d48199f6f36df83ac5416426cd296d`  
		Last Modified: Tue, 30 Nov 2021 09:48:27 GMT  
		Size: 4.7 KB (4717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
