<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.2`](#couchdb312)
-	[`couchdb:3.2`](#couchdb32)
-	[`couchdb:3.2.3`](#couchdb323)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.2`](#couchdb332)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:f182cd08341af0c39b74343230b4f20c484401d84718f694a9d6ec37ff86ca62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:02b714ce49774225429e12917deb39f0fe81f43cf70751b8b0579eddde5bff9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84537855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77f1caae3ab3b43a7564cb921edf5fff88c11da3d067bd3c0472eb526b82c3a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:21:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 20:21:32 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 20:21:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:21:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 03 May 2023 20:21:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 20:21:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:22:11 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 03 May 2023 20:22:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 20:22:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 20:22:31 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 20:22:31 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 03 May 2023 20:22:31 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 03 May 2023 20:22:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 20:22:32 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:22:32 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 20:22:32 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 20:22:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af0fc1f7b67826700fd23eb653db08f6043772d85a38112e11bfecaffe7fc40`  
		Last Modified: Wed, 03 May 2023 20:23:20 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eca68a1c3ee4d4190107408aaa4de8c20a78e32827f004182f498d0a784e96e`  
		Last Modified: Wed, 03 May 2023 20:23:19 GMT  
		Size: 6.7 MB (6705927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06355754990a877d2d7142aba3242f280e0abe278c2ad963e7f764f381cc7eeb`  
		Last Modified: Wed, 03 May 2023 20:23:18 GMT  
		Size: 1.3 MB (1259585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031d8d542bb5a676d6eb6e5fbb0a0fd0dd1bddc9fa99e24105d88481e2229bce`  
		Last Modified: Wed, 03 May 2023 20:23:18 GMT  
		Size: 294.3 KB (294318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353d1bae8af459fb58ce7c6bd403d1c606e0507a99f49672a2896aa1cd73d823`  
		Last Modified: Wed, 03 May 2023 20:23:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5574b7366c7040d9560ea43d33f72e11c4e93f09713b107841a4e2d9dfb18e59`  
		Last Modified: Wed, 03 May 2023 20:23:34 GMT  
		Size: 49.1 MB (49132049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005e660db199163b26a4c83c4c0e9ca2e162bc8386af07cab5251600f0354a9e`  
		Last Modified: Wed, 03 May 2023 20:23:29 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f192698aaac86ed8388b79e703bd4c9fb962f6cbcd91753e985ac7b5892f3290`  
		Last Modified: Wed, 03 May 2023 20:23:29 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d526e49bdbff015c848e4a527fda4efd783977b14d0f7288d9eb64cc34f8bad2`  
		Last Modified: Wed, 03 May 2023 20:23:29 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a748cf484b76251894e5ceb5314a405cf9a4988a138fd9ee023f491a0a72b63f`  
		Last Modified: Wed, 03 May 2023 20:23:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e18ace8e3aecc5b2b197d61a9200b114cbb6cea6c92dc0017068f12d3a5efce4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72996534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b1507b9d649319642be966fa7e59d02405b482c2bbea433957a11fc58d5a4d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 03 May 2023 00:23:05 GMT
ADD file:1d8cf95f550bb4b86ad82b22e7195179335fa3b327fd1f1ba1e6c8357ee15c94 in / 
# Wed, 03 May 2023 00:23:05 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:59:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 17:59:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 17:59:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:00:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 03 May 2023 18:00:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 18:00:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:00:24 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 03 May 2023 18:00:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 18:00:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 18:00:37 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 18:00:37 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 03 May 2023 18:00:37 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 03 May 2023 18:00:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 18:00:37 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:00:37 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 18:00:37 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 18:00:37 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5627aec4010af613408c2ee78d5d32b9ecac22cb396d702906fb1160721f0011`  
		Last Modified: Wed, 03 May 2023 00:26:29 GMT  
		Size: 25.9 MB (25922039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05c54bc0d6c23b27f753798fc9848e2c187a403a12e3071e89d0ac92dc757b6`  
		Last Modified: Wed, 03 May 2023 18:01:09 GMT  
		Size: 3.4 KB (3444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35bba3551dc7acff4275c1d3a365cad6af564401eb3e59d914dc1463893ceab`  
		Last Modified: Wed, 03 May 2023 18:01:08 GMT  
		Size: 6.6 MB (6579432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd37c05a5b789fcd7af10553688a922082794b1e9d323584f062c923c4e58215`  
		Last Modified: Wed, 03 May 2023 18:01:07 GMT  
		Size: 1.2 MB (1164534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3088e3ee2f0e998d746ccf343d8cbf7ff5420240f9b9c89152780e7e130afa3`  
		Last Modified: Wed, 03 May 2023 18:01:07 GMT  
		Size: 294.2 KB (294163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8563e70bd3ef56e360c13f7c5d605b353f60502d90e3abda1d960452e7657c`  
		Last Modified: Wed, 03 May 2023 18:01:18 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94bc623f42df7036e44656a6e7a54caafa8f23eedd982341379f85061dcee33`  
		Last Modified: Wed, 03 May 2023 18:01:20 GMT  
		Size: 39.0 MB (39029328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e631dc376555351d7df5512925cb5783bf69277f1c34b9a0552befa8f90cda`  
		Last Modified: Wed, 03 May 2023 18:01:17 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c978bad9c0e7665295dd236f7c18a4355a5aeb86e107d1110d5e369b52950b9e`  
		Last Modified: Wed, 03 May 2023 18:01:17 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef5d90b9a3967e2fbfb6943009be80121edab7d6ad78dfca5df77f4f93165d5`  
		Last Modified: Wed, 03 May 2023 18:01:17 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c713abd6769ec70404c8f6aab5b93c7116290ba4a0254e9a994b131d5bdf18`  
		Last Modified: Wed, 03 May 2023 18:01:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:f182cd08341af0c39b74343230b4f20c484401d84718f694a9d6ec37ff86ca62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:02b714ce49774225429e12917deb39f0fe81f43cf70751b8b0579eddde5bff9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84537855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77f1caae3ab3b43a7564cb921edf5fff88c11da3d067bd3c0472eb526b82c3a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:21:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 20:21:32 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 20:21:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:21:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 03 May 2023 20:21:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 20:21:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:22:11 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 03 May 2023 20:22:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 20:22:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 20:22:31 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 20:22:31 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 03 May 2023 20:22:31 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 03 May 2023 20:22:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 20:22:32 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:22:32 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 20:22:32 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 20:22:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af0fc1f7b67826700fd23eb653db08f6043772d85a38112e11bfecaffe7fc40`  
		Last Modified: Wed, 03 May 2023 20:23:20 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eca68a1c3ee4d4190107408aaa4de8c20a78e32827f004182f498d0a784e96e`  
		Last Modified: Wed, 03 May 2023 20:23:19 GMT  
		Size: 6.7 MB (6705927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06355754990a877d2d7142aba3242f280e0abe278c2ad963e7f764f381cc7eeb`  
		Last Modified: Wed, 03 May 2023 20:23:18 GMT  
		Size: 1.3 MB (1259585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031d8d542bb5a676d6eb6e5fbb0a0fd0dd1bddc9fa99e24105d88481e2229bce`  
		Last Modified: Wed, 03 May 2023 20:23:18 GMT  
		Size: 294.3 KB (294318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353d1bae8af459fb58ce7c6bd403d1c606e0507a99f49672a2896aa1cd73d823`  
		Last Modified: Wed, 03 May 2023 20:23:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5574b7366c7040d9560ea43d33f72e11c4e93f09713b107841a4e2d9dfb18e59`  
		Last Modified: Wed, 03 May 2023 20:23:34 GMT  
		Size: 49.1 MB (49132049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005e660db199163b26a4c83c4c0e9ca2e162bc8386af07cab5251600f0354a9e`  
		Last Modified: Wed, 03 May 2023 20:23:29 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f192698aaac86ed8388b79e703bd4c9fb962f6cbcd91753e985ac7b5892f3290`  
		Last Modified: Wed, 03 May 2023 20:23:29 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d526e49bdbff015c848e4a527fda4efd783977b14d0f7288d9eb64cc34f8bad2`  
		Last Modified: Wed, 03 May 2023 20:23:29 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a748cf484b76251894e5ceb5314a405cf9a4988a138fd9ee023f491a0a72b63f`  
		Last Modified: Wed, 03 May 2023 20:23:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e18ace8e3aecc5b2b197d61a9200b114cbb6cea6c92dc0017068f12d3a5efce4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72996534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b1507b9d649319642be966fa7e59d02405b482c2bbea433957a11fc58d5a4d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 03 May 2023 00:23:05 GMT
ADD file:1d8cf95f550bb4b86ad82b22e7195179335fa3b327fd1f1ba1e6c8357ee15c94 in / 
# Wed, 03 May 2023 00:23:05 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:59:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 17:59:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 17:59:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:00:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 03 May 2023 18:00:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 18:00:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:00:24 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 03 May 2023 18:00:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 18:00:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 18:00:37 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 18:00:37 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 03 May 2023 18:00:37 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 03 May 2023 18:00:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 18:00:37 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:00:37 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 18:00:37 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 18:00:37 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5627aec4010af613408c2ee78d5d32b9ecac22cb396d702906fb1160721f0011`  
		Last Modified: Wed, 03 May 2023 00:26:29 GMT  
		Size: 25.9 MB (25922039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05c54bc0d6c23b27f753798fc9848e2c187a403a12e3071e89d0ac92dc757b6`  
		Last Modified: Wed, 03 May 2023 18:01:09 GMT  
		Size: 3.4 KB (3444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35bba3551dc7acff4275c1d3a365cad6af564401eb3e59d914dc1463893ceab`  
		Last Modified: Wed, 03 May 2023 18:01:08 GMT  
		Size: 6.6 MB (6579432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd37c05a5b789fcd7af10553688a922082794b1e9d323584f062c923c4e58215`  
		Last Modified: Wed, 03 May 2023 18:01:07 GMT  
		Size: 1.2 MB (1164534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3088e3ee2f0e998d746ccf343d8cbf7ff5420240f9b9c89152780e7e130afa3`  
		Last Modified: Wed, 03 May 2023 18:01:07 GMT  
		Size: 294.2 KB (294163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8563e70bd3ef56e360c13f7c5d605b353f60502d90e3abda1d960452e7657c`  
		Last Modified: Wed, 03 May 2023 18:01:18 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94bc623f42df7036e44656a6e7a54caafa8f23eedd982341379f85061dcee33`  
		Last Modified: Wed, 03 May 2023 18:01:20 GMT  
		Size: 39.0 MB (39029328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e631dc376555351d7df5512925cb5783bf69277f1c34b9a0552befa8f90cda`  
		Last Modified: Wed, 03 May 2023 18:01:17 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c978bad9c0e7665295dd236f7c18a4355a5aeb86e107d1110d5e369b52950b9e`  
		Last Modified: Wed, 03 May 2023 18:01:17 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef5d90b9a3967e2fbfb6943009be80121edab7d6ad78dfca5df77f4f93165d5`  
		Last Modified: Wed, 03 May 2023 18:01:17 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c713abd6769ec70404c8f6aab5b93c7116290ba4a0254e9a994b131d5bdf18`  
		Last Modified: Wed, 03 May 2023 18:01:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:f182cd08341af0c39b74343230b4f20c484401d84718f694a9d6ec37ff86ca62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:02b714ce49774225429e12917deb39f0fe81f43cf70751b8b0579eddde5bff9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84537855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77f1caae3ab3b43a7564cb921edf5fff88c11da3d067bd3c0472eb526b82c3a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:21:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 20:21:32 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 20:21:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:21:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 03 May 2023 20:21:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 20:21:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:22:11 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 03 May 2023 20:22:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 20:22:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 20:22:31 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 20:22:31 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 03 May 2023 20:22:31 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 03 May 2023 20:22:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 20:22:32 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:22:32 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 20:22:32 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 20:22:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af0fc1f7b67826700fd23eb653db08f6043772d85a38112e11bfecaffe7fc40`  
		Last Modified: Wed, 03 May 2023 20:23:20 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eca68a1c3ee4d4190107408aaa4de8c20a78e32827f004182f498d0a784e96e`  
		Last Modified: Wed, 03 May 2023 20:23:19 GMT  
		Size: 6.7 MB (6705927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06355754990a877d2d7142aba3242f280e0abe278c2ad963e7f764f381cc7eeb`  
		Last Modified: Wed, 03 May 2023 20:23:18 GMT  
		Size: 1.3 MB (1259585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031d8d542bb5a676d6eb6e5fbb0a0fd0dd1bddc9fa99e24105d88481e2229bce`  
		Last Modified: Wed, 03 May 2023 20:23:18 GMT  
		Size: 294.3 KB (294318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353d1bae8af459fb58ce7c6bd403d1c606e0507a99f49672a2896aa1cd73d823`  
		Last Modified: Wed, 03 May 2023 20:23:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5574b7366c7040d9560ea43d33f72e11c4e93f09713b107841a4e2d9dfb18e59`  
		Last Modified: Wed, 03 May 2023 20:23:34 GMT  
		Size: 49.1 MB (49132049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005e660db199163b26a4c83c4c0e9ca2e162bc8386af07cab5251600f0354a9e`  
		Last Modified: Wed, 03 May 2023 20:23:29 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f192698aaac86ed8388b79e703bd4c9fb962f6cbcd91753e985ac7b5892f3290`  
		Last Modified: Wed, 03 May 2023 20:23:29 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d526e49bdbff015c848e4a527fda4efd783977b14d0f7288d9eb64cc34f8bad2`  
		Last Modified: Wed, 03 May 2023 20:23:29 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a748cf484b76251894e5ceb5314a405cf9a4988a138fd9ee023f491a0a72b63f`  
		Last Modified: Wed, 03 May 2023 20:23:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e18ace8e3aecc5b2b197d61a9200b114cbb6cea6c92dc0017068f12d3a5efce4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72996534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b1507b9d649319642be966fa7e59d02405b482c2bbea433957a11fc58d5a4d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 03 May 2023 00:23:05 GMT
ADD file:1d8cf95f550bb4b86ad82b22e7195179335fa3b327fd1f1ba1e6c8357ee15c94 in / 
# Wed, 03 May 2023 00:23:05 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:59:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 17:59:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 17:59:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:00:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 03 May 2023 18:00:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 18:00:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:00:24 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 03 May 2023 18:00:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 18:00:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 18:00:37 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 18:00:37 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 03 May 2023 18:00:37 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 03 May 2023 18:00:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 18:00:37 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:00:37 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 18:00:37 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 18:00:37 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5627aec4010af613408c2ee78d5d32b9ecac22cb396d702906fb1160721f0011`  
		Last Modified: Wed, 03 May 2023 00:26:29 GMT  
		Size: 25.9 MB (25922039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05c54bc0d6c23b27f753798fc9848e2c187a403a12e3071e89d0ac92dc757b6`  
		Last Modified: Wed, 03 May 2023 18:01:09 GMT  
		Size: 3.4 KB (3444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35bba3551dc7acff4275c1d3a365cad6af564401eb3e59d914dc1463893ceab`  
		Last Modified: Wed, 03 May 2023 18:01:08 GMT  
		Size: 6.6 MB (6579432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd37c05a5b789fcd7af10553688a922082794b1e9d323584f062c923c4e58215`  
		Last Modified: Wed, 03 May 2023 18:01:07 GMT  
		Size: 1.2 MB (1164534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3088e3ee2f0e998d746ccf343d8cbf7ff5420240f9b9c89152780e7e130afa3`  
		Last Modified: Wed, 03 May 2023 18:01:07 GMT  
		Size: 294.2 KB (294163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8563e70bd3ef56e360c13f7c5d605b353f60502d90e3abda1d960452e7657c`  
		Last Modified: Wed, 03 May 2023 18:01:18 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94bc623f42df7036e44656a6e7a54caafa8f23eedd982341379f85061dcee33`  
		Last Modified: Wed, 03 May 2023 18:01:20 GMT  
		Size: 39.0 MB (39029328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e631dc376555351d7df5512925cb5783bf69277f1c34b9a0552befa8f90cda`  
		Last Modified: Wed, 03 May 2023 18:01:17 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c978bad9c0e7665295dd236f7c18a4355a5aeb86e107d1110d5e369b52950b9e`  
		Last Modified: Wed, 03 May 2023 18:01:17 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef5d90b9a3967e2fbfb6943009be80121edab7d6ad78dfca5df77f4f93165d5`  
		Last Modified: Wed, 03 May 2023 18:01:17 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c713abd6769ec70404c8f6aab5b93c7116290ba4a0254e9a994b131d5bdf18`  
		Last Modified: Wed, 03 May 2023 18:01:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:9760ef202c43ddfbdc3d8e220353ddef84ba50d1d757508a81e6ca7a6e62eb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:a78ecf1912d5046be84252e42c87b4ab88898be235ad23388b590870933d9c59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90226076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4894334bb0e847a86583bb98c2678f2ef00343fe485b0e7a77da57bf72386d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:20:41 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 20:20:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 20:20:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:20:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 03 May 2023 20:20:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 20:20:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:20:57 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 03 May 2023 20:20:57 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 20:21:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 20:21:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 20:21:10 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 03 May 2023 20:21:10 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 03 May 2023 20:21:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 20:21:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:21:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 20:21:11 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 20:21:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aae57dfaa0a56d12e531052d943db83aef0440c156d6fd9d192f6a1085a270`  
		Last Modified: Wed, 03 May 2023 20:22:47 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93caf13d63dac0c40ecd2e72ababf04b8014086e33b50ed00159c1332a5ae9`  
		Last Modified: Wed, 03 May 2023 20:22:46 GMT  
		Size: 5.2 MB (5224504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1357c913bae06fc471b1ba29963a41023b367169a33df605c24f688ca19fba6`  
		Last Modified: Wed, 03 May 2023 20:22:46 GMT  
		Size: 610.3 KB (610274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdeea262d51fa2fd0a20a1c0067906a28611ed6d893bbfc07b305a2ad12872bf`  
		Last Modified: Wed, 03 May 2023 20:22:45 GMT  
		Size: 294.4 KB (294388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d29c2f2da0eb28da20c5b6155cda5fe564867522531a0d737f4d5d38d70482`  
		Last Modified: Wed, 03 May 2023 20:22:45 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432ec4176080d53ddfca242d4a6ece47afb37dd56154f2f8d110a611220d81ce`  
		Last Modified: Wed, 03 May 2023 20:22:48 GMT  
		Size: 52.7 MB (52685980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab316a2c3ce230eb78543d590746289488ab2411ce32ab4a4fff829964f8d6`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9611ebaa996ba274a749a684e1eab5da6f2da79e516eddf4e7aefb4ad17340`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5433ac64532fa5d3c3168cc608f497b8e5988cfe6db3506e072c6954d4fb4e6`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96a1658cb7854650683f232eb1898ae52498d5838b2cdb433e66184970ca793`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9744d377ea8891887eb5854020c3a4545c7ef19e8986ee58d32b3cf4040b73b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88673594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdf7920dfd53b2df52213aee261dd4e41c0549d72f9e343c14cd2b9fcbd5f4f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:59:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 17:59:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 17:59:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:59:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 03 May 2023 17:59:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 17:59:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:59:21 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 03 May 2023 17:59:22 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 17:59:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 17:59:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 17:59:35 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 03 May 2023 17:59:35 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 03 May 2023 17:59:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 17:59:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 17:59:35 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 17:59:35 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 17:59:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc49e0f227abecd65ff6b6795c3f880303494db817c7e1e18ecda59fc7152e8e`  
		Last Modified: Wed, 03 May 2023 18:00:52 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0194f60c08f3777da4f834e63630710e50ad01aba6984abe85826ebc49af6a79`  
		Last Modified: Wed, 03 May 2023 18:00:51 GMT  
		Size: 5.2 MB (5209527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63900b96976ba15b59992aaf3958e1823702187a944ded17b4e7e574e5303602`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 566.3 KB (566271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaa51d00fbb637175fe6cd98964622811feb4a21e8ab226b746d44415e72e5f`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 294.3 KB (294281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa220909c065252e8254c4d40d57f803dad4012af471289e13ffd7fa688c7eb`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb46de8d7de131610fcf1b61d5a577b86afa7c4840ff37ccec2b17e8498225d2`  
		Last Modified: Wed, 03 May 2023 18:00:52 GMT  
		Size: 52.5 MB (52543335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f937d96179866f5702ff575f8c8f95bbb804136340edde11989b41f079e045d0`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90137057d1382e2128147af431662186fb94c170fd949f3648719510367dcff`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e79d5751c60bf65d33ec9b49e331aaa0b00505dd7e2dce70dab7d08b91a847b`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4add3ef4c8cc00343e2616e6ac05f104c708b83a23ff11f519c1ccc110d16a17`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:13c66352ec28fb818402ea6a162b1d26ab57afc84b0959c08626072202a864fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4a23d81c45d81d19aed05a650b92a338f047fdbeff466ec274cce2ce6e48d4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:23:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 12 Apr 2023 01:23:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 12 Apr 2023 01:23:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:24:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 12 Apr 2023 01:24:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 12 Apr 2023 01:24:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Apr 2023 22:16:20 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 25 Apr 2023 22:16:21 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Apr 2023 22:16:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Apr 2023 22:16:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Apr 2023 22:16:49 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 25 Apr 2023 22:16:49 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 25 Apr 2023 22:16:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Apr 2023 22:16:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Apr 2023 22:16:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Apr 2023 22:16:52 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Apr 2023 22:16:52 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7569dcea363c11bb071b416ea27193dbe62d8a210fa1f829efabb35b46600dae`  
		Last Modified: Wed, 12 Apr 2023 01:26:25 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a685c575c0e899abc0410edf84715dd5cf4184fcbd447fdbbcac069795eadd05`  
		Last Modified: Wed, 12 Apr 2023 01:26:26 GMT  
		Size: 6.0 MB (6044117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283a2882808914c7a35f392d4ad2d2921ccf8b8855ab399e2998c22d061f16e`  
		Last Modified: Wed, 12 Apr 2023 01:26:24 GMT  
		Size: 662.1 KB (662116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17deb4c48f5c43beee592bed99d27502afe8c8f60cde1cb4bebb7dce00e877c`  
		Last Modified: Wed, 12 Apr 2023 01:26:24 GMT  
		Size: 294.3 KB (294319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a005d1ac9dd4beafe87fd0d6df08fa72f0631b6ab8e23223294f78a242f748`  
		Last Modified: Tue, 25 Apr 2023 22:17:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab032b77afd1546e2bf51f362edad19e7661fb6470925250236ef4b8192eed99`  
		Last Modified: Tue, 25 Apr 2023 22:17:42 GMT  
		Size: 53.7 MB (53662597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14465f77288ec304103ebf17b65c6630abe30166373f91e89939385535147e4`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5effe25ef84c827ba988a853ea59f8afff941940d15ca66ad41ccba621b99829`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6745b0a9c210274967bf202717f0026edd9102ecab6c433b4164ec8642f72e95`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d7963f0595ab31b467b4da324625d275d24dd8d46f18e3ac2504b8d64ed7c6`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:a67bc825e03d00b88f5e1e7b7f5af8c18f578346dba102297e5e09ab366cd5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:f9d3886cd408ba1d310bbb13cf84c18d938f6c9493d3a2deca9478dceda5e7dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80025472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da63214920f1d67338b9412300618f48c1e7ccde90d285350e326e5f72bf7b44`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:21:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 20:21:32 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 20:21:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:21:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 03 May 2023 20:21:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 20:21:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:21:49 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 03 May 2023 20:21:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 20:22:03 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 20:22:04 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 20:22:04 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 03 May 2023 20:22:04 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 03 May 2023 20:22:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 20:22:04 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:22:05 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 20:22:05 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 20:22:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af0fc1f7b67826700fd23eb653db08f6043772d85a38112e11bfecaffe7fc40`  
		Last Modified: Wed, 03 May 2023 20:23:20 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eca68a1c3ee4d4190107408aaa4de8c20a78e32827f004182f498d0a784e96e`  
		Last Modified: Wed, 03 May 2023 20:23:19 GMT  
		Size: 6.7 MB (6705927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06355754990a877d2d7142aba3242f280e0abe278c2ad963e7f764f381cc7eeb`  
		Last Modified: Wed, 03 May 2023 20:23:18 GMT  
		Size: 1.3 MB (1259585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031d8d542bb5a676d6eb6e5fbb0a0fd0dd1bddc9fa99e24105d88481e2229bce`  
		Last Modified: Wed, 03 May 2023 20:23:18 GMT  
		Size: 294.3 KB (294318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bb419fe61bb0ad891e25beb6c361a6f99937a450dfef2ebc480eeb508c0a87`  
		Last Modified: Wed, 03 May 2023 20:23:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba55c9f6842ebcfbf499e2e01174e20d6b4f4ef30ed332ee753bb84e1eaec49d`  
		Last Modified: Wed, 03 May 2023 20:23:20 GMT  
		Size: 44.6 MB (44619669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9e6ca4bdcd9c8a8f6bdecb46cb666b15ad7d26db8fc725aad78fe2afb1f8a8`  
		Last Modified: Wed, 03 May 2023 20:23:16 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d46fcfc4002ea58eec01d39263a5f6eb4d322b038f820770377d8cfba6bd71`  
		Last Modified: Wed, 03 May 2023 20:23:16 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba9da3c55dff85aeeb4ea2127b4e44bb6bd200839d05cce6433e2790bf9bef3`  
		Last Modified: Wed, 03 May 2023 20:23:16 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519818145983dfab671cabd9b9c7b063b24f6c58f416a86d8d644d5e16d31680`  
		Last Modified: Wed, 03 May 2023 20:23:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:be0f2ec33acdc151efd6a8691fee7970b7182dafa686ab0fb59cc9f758f2337d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75093312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eff937c5050868128f2bdaec53e718e91fe4993ce7d0d3f5226d4ea312c9a9d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 03 May 2023 00:23:05 GMT
ADD file:1d8cf95f550bb4b86ad82b22e7195179335fa3b327fd1f1ba1e6c8357ee15c94 in / 
# Wed, 03 May 2023 00:23:05 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:59:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 17:59:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 17:59:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:00:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 03 May 2023 18:00:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 18:00:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:00:08 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 03 May 2023 18:00:09 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 18:00:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 18:00:20 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 18:00:21 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 03 May 2023 18:00:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 03 May 2023 18:00:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 18:00:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:00:21 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 18:00:21 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 18:00:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5627aec4010af613408c2ee78d5d32b9ecac22cb396d702906fb1160721f0011`  
		Last Modified: Wed, 03 May 2023 00:26:29 GMT  
		Size: 25.9 MB (25922039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05c54bc0d6c23b27f753798fc9848e2c187a403a12e3071e89d0ac92dc757b6`  
		Last Modified: Wed, 03 May 2023 18:01:09 GMT  
		Size: 3.4 KB (3444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35bba3551dc7acff4275c1d3a365cad6af564401eb3e59d914dc1463893ceab`  
		Last Modified: Wed, 03 May 2023 18:01:08 GMT  
		Size: 6.6 MB (6579432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd37c05a5b789fcd7af10553688a922082794b1e9d323584f062c923c4e58215`  
		Last Modified: Wed, 03 May 2023 18:01:07 GMT  
		Size: 1.2 MB (1164534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3088e3ee2f0e998d746ccf343d8cbf7ff5420240f9b9c89152780e7e130afa3`  
		Last Modified: Wed, 03 May 2023 18:01:07 GMT  
		Size: 294.2 KB (294163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6608f02c0062f546fd8b8f6b40f77f24f73677bedf20546bc6c7373f39265a`  
		Last Modified: Wed, 03 May 2023 18:01:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8112d9182313bc8e795e5e8cdbfaebd4e26288856715c07d271323174b213122`  
		Last Modified: Wed, 03 May 2023 18:01:09 GMT  
		Size: 41.1 MB (41126103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa817ee55cb1e4703309cd1ee743e9344de25a4e1564a9424986bd47bfa3811`  
		Last Modified: Wed, 03 May 2023 18:01:05 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551130a20b4ec2f30d4da5964fec499f452e34c7b1737e26cc8797d42af8f3cd`  
		Last Modified: Wed, 03 May 2023 18:01:05 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6b0e0a9773e5035f2de41c0af21719d7bb441e13617cba684fd748f2cb6d3f`  
		Last Modified: Wed, 03 May 2023 18:01:05 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede056d63d2f7a3f83f31f1626df073ba40c1523aefc0f04291e623b87a75234`  
		Last Modified: Wed, 03 May 2023 18:01:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:a67bc825e03d00b88f5e1e7b7f5af8c18f578346dba102297e5e09ab366cd5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:f9d3886cd408ba1d310bbb13cf84c18d938f6c9493d3a2deca9478dceda5e7dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80025472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da63214920f1d67338b9412300618f48c1e7ccde90d285350e326e5f72bf7b44`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:21:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 20:21:32 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 20:21:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:21:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 03 May 2023 20:21:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 20:21:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:21:49 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 03 May 2023 20:21:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 20:22:03 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 20:22:04 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 20:22:04 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 03 May 2023 20:22:04 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 03 May 2023 20:22:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 20:22:04 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:22:05 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 20:22:05 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 20:22:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af0fc1f7b67826700fd23eb653db08f6043772d85a38112e11bfecaffe7fc40`  
		Last Modified: Wed, 03 May 2023 20:23:20 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eca68a1c3ee4d4190107408aaa4de8c20a78e32827f004182f498d0a784e96e`  
		Last Modified: Wed, 03 May 2023 20:23:19 GMT  
		Size: 6.7 MB (6705927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06355754990a877d2d7142aba3242f280e0abe278c2ad963e7f764f381cc7eeb`  
		Last Modified: Wed, 03 May 2023 20:23:18 GMT  
		Size: 1.3 MB (1259585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031d8d542bb5a676d6eb6e5fbb0a0fd0dd1bddc9fa99e24105d88481e2229bce`  
		Last Modified: Wed, 03 May 2023 20:23:18 GMT  
		Size: 294.3 KB (294318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bb419fe61bb0ad891e25beb6c361a6f99937a450dfef2ebc480eeb508c0a87`  
		Last Modified: Wed, 03 May 2023 20:23:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba55c9f6842ebcfbf499e2e01174e20d6b4f4ef30ed332ee753bb84e1eaec49d`  
		Last Modified: Wed, 03 May 2023 20:23:20 GMT  
		Size: 44.6 MB (44619669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9e6ca4bdcd9c8a8f6bdecb46cb666b15ad7d26db8fc725aad78fe2afb1f8a8`  
		Last Modified: Wed, 03 May 2023 20:23:16 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d46fcfc4002ea58eec01d39263a5f6eb4d322b038f820770377d8cfba6bd71`  
		Last Modified: Wed, 03 May 2023 20:23:16 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba9da3c55dff85aeeb4ea2127b4e44bb6bd200839d05cce6433e2790bf9bef3`  
		Last Modified: Wed, 03 May 2023 20:23:16 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519818145983dfab671cabd9b9c7b063b24f6c58f416a86d8d644d5e16d31680`  
		Last Modified: Wed, 03 May 2023 20:23:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:be0f2ec33acdc151efd6a8691fee7970b7182dafa686ab0fb59cc9f758f2337d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75093312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eff937c5050868128f2bdaec53e718e91fe4993ce7d0d3f5226d4ea312c9a9d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 03 May 2023 00:23:05 GMT
ADD file:1d8cf95f550bb4b86ad82b22e7195179335fa3b327fd1f1ba1e6c8357ee15c94 in / 
# Wed, 03 May 2023 00:23:05 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:59:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 17:59:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 17:59:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:00:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 03 May 2023 18:00:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 18:00:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:00:08 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 03 May 2023 18:00:09 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 18:00:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 18:00:20 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 18:00:21 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 03 May 2023 18:00:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 03 May 2023 18:00:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 18:00:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:00:21 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 18:00:21 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 18:00:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5627aec4010af613408c2ee78d5d32b9ecac22cb396d702906fb1160721f0011`  
		Last Modified: Wed, 03 May 2023 00:26:29 GMT  
		Size: 25.9 MB (25922039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05c54bc0d6c23b27f753798fc9848e2c187a403a12e3071e89d0ac92dc757b6`  
		Last Modified: Wed, 03 May 2023 18:01:09 GMT  
		Size: 3.4 KB (3444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35bba3551dc7acff4275c1d3a365cad6af564401eb3e59d914dc1463893ceab`  
		Last Modified: Wed, 03 May 2023 18:01:08 GMT  
		Size: 6.6 MB (6579432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd37c05a5b789fcd7af10553688a922082794b1e9d323584f062c923c4e58215`  
		Last Modified: Wed, 03 May 2023 18:01:07 GMT  
		Size: 1.2 MB (1164534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3088e3ee2f0e998d746ccf343d8cbf7ff5420240f9b9c89152780e7e130afa3`  
		Last Modified: Wed, 03 May 2023 18:01:07 GMT  
		Size: 294.2 KB (294163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6608f02c0062f546fd8b8f6b40f77f24f73677bedf20546bc6c7373f39265a`  
		Last Modified: Wed, 03 May 2023 18:01:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8112d9182313bc8e795e5e8cdbfaebd4e26288856715c07d271323174b213122`  
		Last Modified: Wed, 03 May 2023 18:01:09 GMT  
		Size: 41.1 MB (41126103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa817ee55cb1e4703309cd1ee743e9344de25a4e1564a9424986bd47bfa3811`  
		Last Modified: Wed, 03 May 2023 18:01:05 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551130a20b4ec2f30d4da5964fec499f452e34c7b1737e26cc8797d42af8f3cd`  
		Last Modified: Wed, 03 May 2023 18:01:05 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6b0e0a9773e5035f2de41c0af21719d7bb441e13617cba684fd748f2cb6d3f`  
		Last Modified: Wed, 03 May 2023 18:01:05 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede056d63d2f7a3f83f31f1626df073ba40c1523aefc0f04291e623b87a75234`  
		Last Modified: Wed, 03 May 2023 18:01:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:44916974829e49af4fc859a956931b13c7690494a7a5ae78717ce8461a474d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:2de1c1dc0d06eab996b1e76668b6eab60978eecf19a46dca85792671faa654a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89725970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743f89c5e782349834e2dec90beb302f48cb1a0eeaaf608af4e1830e80a9a604`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:20:41 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 20:20:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 20:20:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:20:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 03 May 2023 20:20:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 20:20:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:21:14 GMT
ENV COUCHDB_VERSION=3.2.3
# Wed, 03 May 2023 20:21:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 20:21:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 20:21:28 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 20:21:28 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 03 May 2023 20:21:28 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 03 May 2023 20:21:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 20:21:29 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:21:29 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 20:21:29 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 20:21:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aae57dfaa0a56d12e531052d943db83aef0440c156d6fd9d192f6a1085a270`  
		Last Modified: Wed, 03 May 2023 20:22:47 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93caf13d63dac0c40ecd2e72ababf04b8014086e33b50ed00159c1332a5ae9`  
		Last Modified: Wed, 03 May 2023 20:22:46 GMT  
		Size: 5.2 MB (5224504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1357c913bae06fc471b1ba29963a41023b367169a33df605c24f688ca19fba6`  
		Last Modified: Wed, 03 May 2023 20:22:46 GMT  
		Size: 610.3 KB (610274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdeea262d51fa2fd0a20a1c0067906a28611ed6d893bbfc07b305a2ad12872bf`  
		Last Modified: Wed, 03 May 2023 20:22:45 GMT  
		Size: 294.4 KB (294388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e07ac044e3531957909d8805935e41f04caae7c5e40c67ffb38797715d72ccd`  
		Last Modified: Wed, 03 May 2023 20:23:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bc031704a4261b707862ac478ac730f7a1f2f64a0858da7e7f3ff82ab8f5e5`  
		Last Modified: Wed, 03 May 2023 20:23:08 GMT  
		Size: 52.2 MB (52185871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bca9090a0c2482044d341e17eddbb84f020f07e25918dabe8cb88bbc29510f`  
		Last Modified: Wed, 03 May 2023 20:23:02 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabfad0fe7bb0f69b7bbaa7434116074867eea330eccb80373d85d3f8f1b78f5`  
		Last Modified: Wed, 03 May 2023 20:23:02 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80a8ad75770c864245536a6ea88de0134ae19c79972f84156b5631b5299ee68`  
		Last Modified: Wed, 03 May 2023 20:23:02 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e25c23db7bc12571c9ef548a53f021d5d028bdb2893d95f3a5f70017df78cc`  
		Last Modified: Wed, 03 May 2023 20:23:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:960305e9b35826163f173e8b89eab4112410bee3725c3f0773140932dd9f7877
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85205205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352add31bc606968e9b4695dc003a06de6c7ca3682ea0d3145b972feb8dabfee`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:33:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 12 Apr 2023 01:33:39 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 12 Apr 2023 01:33:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:33:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 12 Apr 2023 01:33:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 12 Apr 2023 01:33:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:34:12 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 12 Apr 2023 01:34:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 12 Apr 2023 01:34:24 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 12 Apr 2023 01:34:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 12 Apr 2023 01:34:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 12 Apr 2023 01:34:24 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 12 Apr 2023 01:34:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 12 Apr 2023 01:34:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 01:34:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 12 Apr 2023 01:34:25 GMT
EXPOSE 4369 5984 9100
# Wed, 12 Apr 2023 01:34:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f522824805b9b3818de882a514dd5454399e3c21b512a09e64274bf12d18ab4`  
		Last Modified: Wed, 12 Apr 2023 01:35:29 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdfaf598c101b0427a73a7b5a1edb3b6229985b64794e6d215eb049125bbd25`  
		Last Modified: Wed, 12 Apr 2023 01:35:27 GMT  
		Size: 5.2 MB (5209561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc33796685833f0fdacecb6c4f2078915729822d8fb7a21aada1b767c48b377`  
		Last Modified: Wed, 12 Apr 2023 01:35:27 GMT  
		Size: 566.3 KB (566295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356323e70f7127294f4bee19c211582a4af79acc6d1f696d70fc94229c84aa52`  
		Last Modified: Wed, 12 Apr 2023 01:35:27 GMT  
		Size: 294.3 KB (294328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9652526d42f149093060de62ac3b39905fb0bfb8457d6148e4314ef71058a153`  
		Last Modified: Wed, 12 Apr 2023 01:35:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d95be693dac094ea4fe70ff2bd1f44b66a9ede007474a31cafcb829c361429`  
		Last Modified: Wed, 12 Apr 2023 01:35:47 GMT  
		Size: 49.1 MB (49063995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61eb7f6826c8440901fb275f2b3c5f6be3e97d95482db6770215d5bd31899ed1`  
		Last Modified: Wed, 12 Apr 2023 01:35:42 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d81fa00cdd93053287b1afda2f3cfda4475c6ac6307dc22125a76f843f21415`  
		Last Modified: Wed, 12 Apr 2023 01:35:43 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e726b19dd008ea8df7bf3ce90fa1947f685d2f6fdd3caa36e1f3b6e40526d0`  
		Last Modified: Wed, 12 Apr 2023 01:35:43 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c78146fce98da16e884fde6d22f444849c69c3da90555e336827ceb2b6a039`  
		Last Modified: Wed, 12 Apr 2023 01:35:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:90a95123b16f3f08c9e3b862a7e628ead429c8602d5dc110db1b038b5b47db9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92383985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c0714b286e5789d8b829c846536d1f8a5308d8cf419fa60995af8b91ab3b55`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:23:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 12 Apr 2023 01:23:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 12 Apr 2023 01:23:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:24:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 12 Apr 2023 01:24:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 12 Apr 2023 01:24:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:25:25 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 12 Apr 2023 01:25:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 12 Apr 2023 01:25:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 12 Apr 2023 01:26:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 12 Apr 2023 01:26:02 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 12 Apr 2023 01:26:03 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 12 Apr 2023 01:26:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 12 Apr 2023 01:26:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 01:26:06 GMT
VOLUME [/opt/couchdb/data]
# Wed, 12 Apr 2023 01:26:06 GMT
EXPOSE 4369 5984 9100
# Wed, 12 Apr 2023 01:26:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7569dcea363c11bb071b416ea27193dbe62d8a210fa1f829efabb35b46600dae`  
		Last Modified: Wed, 12 Apr 2023 01:26:25 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a685c575c0e899abc0410edf84715dd5cf4184fcbd447fdbbcac069795eadd05`  
		Last Modified: Wed, 12 Apr 2023 01:26:26 GMT  
		Size: 6.0 MB (6044117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283a2882808914c7a35f392d4ad2d2921ccf8b8855ab399e2998c22d061f16e`  
		Last Modified: Wed, 12 Apr 2023 01:26:24 GMT  
		Size: 662.1 KB (662116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17deb4c48f5c43beee592bed99d27502afe8c8f60cde1cb4bebb7dce00e877c`  
		Last Modified: Wed, 12 Apr 2023 01:26:24 GMT  
		Size: 294.3 KB (294319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7661a9384c6767a073bc8e86df2ec2c60bef8bad55fac7ab22d7ecffcdb1f1`  
		Last Modified: Wed, 12 Apr 2023 01:26:48 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74733b44093de42db86284861068e909838a6bca4f3ecf0bfd04eb99d5bf8c79`  
		Last Modified: Wed, 12 Apr 2023 01:26:56 GMT  
		Size: 50.1 MB (50084252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c567dbfb6ac3167b1cd2d6532940fd6fb66d9b5b6a1dedf22d61b92a7b4095eb`  
		Last Modified: Wed, 12 Apr 2023 01:26:46 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf08299e06354b4674e5fabd7e99da65832d26bc98826c051d261e7a03195099`  
		Last Modified: Wed, 12 Apr 2023 01:26:46 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5861e0f3152c23eda58111aaac02f82ed4973711f9a55c51cb55ebb9af6220`  
		Last Modified: Wed, 12 Apr 2023 01:26:46 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54774512e47b4b9a6dee9f79bf7ec483b3c7c234e949bc4f6c96fb22a3e8237`  
		Last Modified: Wed, 12 Apr 2023 01:26:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.3`

```console
$ docker pull couchdb@sha256:1bbd9468ba4cbaf44143981777070090f9afba1de1926e9f50b97f2303f987b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchdb:3.2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:2de1c1dc0d06eab996b1e76668b6eab60978eecf19a46dca85792671faa654a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89725970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743f89c5e782349834e2dec90beb302f48cb1a0eeaaf608af4e1830e80a9a604`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:20:41 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 20:20:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 20:20:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:20:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 03 May 2023 20:20:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 20:20:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:21:14 GMT
ENV COUCHDB_VERSION=3.2.3
# Wed, 03 May 2023 20:21:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 20:21:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 20:21:28 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 20:21:28 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 03 May 2023 20:21:28 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 03 May 2023 20:21:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 20:21:29 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:21:29 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 20:21:29 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 20:21:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aae57dfaa0a56d12e531052d943db83aef0440c156d6fd9d192f6a1085a270`  
		Last Modified: Wed, 03 May 2023 20:22:47 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93caf13d63dac0c40ecd2e72ababf04b8014086e33b50ed00159c1332a5ae9`  
		Last Modified: Wed, 03 May 2023 20:22:46 GMT  
		Size: 5.2 MB (5224504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1357c913bae06fc471b1ba29963a41023b367169a33df605c24f688ca19fba6`  
		Last Modified: Wed, 03 May 2023 20:22:46 GMT  
		Size: 610.3 KB (610274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdeea262d51fa2fd0a20a1c0067906a28611ed6d893bbfc07b305a2ad12872bf`  
		Last Modified: Wed, 03 May 2023 20:22:45 GMT  
		Size: 294.4 KB (294388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e07ac044e3531957909d8805935e41f04caae7c5e40c67ffb38797715d72ccd`  
		Last Modified: Wed, 03 May 2023 20:23:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bc031704a4261b707862ac478ac730f7a1f2f64a0858da7e7f3ff82ab8f5e5`  
		Last Modified: Wed, 03 May 2023 20:23:08 GMT  
		Size: 52.2 MB (52185871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bca9090a0c2482044d341e17eddbb84f020f07e25918dabe8cb88bbc29510f`  
		Last Modified: Wed, 03 May 2023 20:23:02 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabfad0fe7bb0f69b7bbaa7434116074867eea330eccb80373d85d3f8f1b78f5`  
		Last Modified: Wed, 03 May 2023 20:23:02 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80a8ad75770c864245536a6ea88de0134ae19c79972f84156b5631b5299ee68`  
		Last Modified: Wed, 03 May 2023 20:23:02 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e25c23db7bc12571c9ef548a53f021d5d028bdb2893d95f3a5f70017df78cc`  
		Last Modified: Wed, 03 May 2023 20:23:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:9760ef202c43ddfbdc3d8e220353ddef84ba50d1d757508a81e6ca7a6e62eb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:a78ecf1912d5046be84252e42c87b4ab88898be235ad23388b590870933d9c59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90226076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4894334bb0e847a86583bb98c2678f2ef00343fe485b0e7a77da57bf72386d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:20:41 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 20:20:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 20:20:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:20:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 03 May 2023 20:20:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 20:20:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:20:57 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 03 May 2023 20:20:57 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 20:21:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 20:21:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 20:21:10 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 03 May 2023 20:21:10 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 03 May 2023 20:21:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 20:21:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:21:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 20:21:11 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 20:21:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aae57dfaa0a56d12e531052d943db83aef0440c156d6fd9d192f6a1085a270`  
		Last Modified: Wed, 03 May 2023 20:22:47 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93caf13d63dac0c40ecd2e72ababf04b8014086e33b50ed00159c1332a5ae9`  
		Last Modified: Wed, 03 May 2023 20:22:46 GMT  
		Size: 5.2 MB (5224504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1357c913bae06fc471b1ba29963a41023b367169a33df605c24f688ca19fba6`  
		Last Modified: Wed, 03 May 2023 20:22:46 GMT  
		Size: 610.3 KB (610274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdeea262d51fa2fd0a20a1c0067906a28611ed6d893bbfc07b305a2ad12872bf`  
		Last Modified: Wed, 03 May 2023 20:22:45 GMT  
		Size: 294.4 KB (294388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d29c2f2da0eb28da20c5b6155cda5fe564867522531a0d737f4d5d38d70482`  
		Last Modified: Wed, 03 May 2023 20:22:45 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432ec4176080d53ddfca242d4a6ece47afb37dd56154f2f8d110a611220d81ce`  
		Last Modified: Wed, 03 May 2023 20:22:48 GMT  
		Size: 52.7 MB (52685980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab316a2c3ce230eb78543d590746289488ab2411ce32ab4a4fff829964f8d6`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9611ebaa996ba274a749a684e1eab5da6f2da79e516eddf4e7aefb4ad17340`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5433ac64532fa5d3c3168cc608f497b8e5988cfe6db3506e072c6954d4fb4e6`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96a1658cb7854650683f232eb1898ae52498d5838b2cdb433e66184970ca793`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9744d377ea8891887eb5854020c3a4545c7ef19e8986ee58d32b3cf4040b73b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88673594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdf7920dfd53b2df52213aee261dd4e41c0549d72f9e343c14cd2b9fcbd5f4f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:59:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 17:59:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 17:59:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:59:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 03 May 2023 17:59:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 17:59:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:59:21 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 03 May 2023 17:59:22 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 17:59:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 17:59:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 17:59:35 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 03 May 2023 17:59:35 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 03 May 2023 17:59:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 17:59:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 17:59:35 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 17:59:35 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 17:59:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc49e0f227abecd65ff6b6795c3f880303494db817c7e1e18ecda59fc7152e8e`  
		Last Modified: Wed, 03 May 2023 18:00:52 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0194f60c08f3777da4f834e63630710e50ad01aba6984abe85826ebc49af6a79`  
		Last Modified: Wed, 03 May 2023 18:00:51 GMT  
		Size: 5.2 MB (5209527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63900b96976ba15b59992aaf3958e1823702187a944ded17b4e7e574e5303602`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 566.3 KB (566271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaa51d00fbb637175fe6cd98964622811feb4a21e8ab226b746d44415e72e5f`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 294.3 KB (294281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa220909c065252e8254c4d40d57f803dad4012af471289e13ffd7fa688c7eb`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb46de8d7de131610fcf1b61d5a577b86afa7c4840ff37ccec2b17e8498225d2`  
		Last Modified: Wed, 03 May 2023 18:00:52 GMT  
		Size: 52.5 MB (52543335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f937d96179866f5702ff575f8c8f95bbb804136340edde11989b41f079e045d0`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90137057d1382e2128147af431662186fb94c170fd949f3648719510367dcff`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e79d5751c60bf65d33ec9b49e331aaa0b00505dd7e2dce70dab7d08b91a847b`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4add3ef4c8cc00343e2616e6ac05f104c708b83a23ff11f519c1ccc110d16a17`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:13c66352ec28fb818402ea6a162b1d26ab57afc84b0959c08626072202a864fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4a23d81c45d81d19aed05a650b92a338f047fdbeff466ec274cce2ce6e48d4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:23:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 12 Apr 2023 01:23:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 12 Apr 2023 01:23:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:24:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 12 Apr 2023 01:24:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 12 Apr 2023 01:24:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Apr 2023 22:16:20 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 25 Apr 2023 22:16:21 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Apr 2023 22:16:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Apr 2023 22:16:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Apr 2023 22:16:49 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 25 Apr 2023 22:16:49 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 25 Apr 2023 22:16:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Apr 2023 22:16:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Apr 2023 22:16:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Apr 2023 22:16:52 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Apr 2023 22:16:52 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7569dcea363c11bb071b416ea27193dbe62d8a210fa1f829efabb35b46600dae`  
		Last Modified: Wed, 12 Apr 2023 01:26:25 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a685c575c0e899abc0410edf84715dd5cf4184fcbd447fdbbcac069795eadd05`  
		Last Modified: Wed, 12 Apr 2023 01:26:26 GMT  
		Size: 6.0 MB (6044117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283a2882808914c7a35f392d4ad2d2921ccf8b8855ab399e2998c22d061f16e`  
		Last Modified: Wed, 12 Apr 2023 01:26:24 GMT  
		Size: 662.1 KB (662116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17deb4c48f5c43beee592bed99d27502afe8c8f60cde1cb4bebb7dce00e877c`  
		Last Modified: Wed, 12 Apr 2023 01:26:24 GMT  
		Size: 294.3 KB (294319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a005d1ac9dd4beafe87fd0d6df08fa72f0631b6ab8e23223294f78a242f748`  
		Last Modified: Tue, 25 Apr 2023 22:17:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab032b77afd1546e2bf51f362edad19e7661fb6470925250236ef4b8192eed99`  
		Last Modified: Tue, 25 Apr 2023 22:17:42 GMT  
		Size: 53.7 MB (53662597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14465f77288ec304103ebf17b65c6630abe30166373f91e89939385535147e4`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5effe25ef84c827ba988a853ea59f8afff941940d15ca66ad41ccba621b99829`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6745b0a9c210274967bf202717f0026edd9102ecab6c433b4164ec8642f72e95`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d7963f0595ab31b467b4da324625d275d24dd8d46f18e3ac2504b8d64ed7c6`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3.2`

```console
$ docker pull couchdb@sha256:9760ef202c43ddfbdc3d8e220353ddef84ba50d1d757508a81e6ca7a6e62eb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:a78ecf1912d5046be84252e42c87b4ab88898be235ad23388b590870933d9c59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90226076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4894334bb0e847a86583bb98c2678f2ef00343fe485b0e7a77da57bf72386d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:20:41 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 20:20:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 20:20:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:20:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 03 May 2023 20:20:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 20:20:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:20:57 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 03 May 2023 20:20:57 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 20:21:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 20:21:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 20:21:10 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 03 May 2023 20:21:10 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 03 May 2023 20:21:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 20:21:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:21:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 20:21:11 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 20:21:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aae57dfaa0a56d12e531052d943db83aef0440c156d6fd9d192f6a1085a270`  
		Last Modified: Wed, 03 May 2023 20:22:47 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93caf13d63dac0c40ecd2e72ababf04b8014086e33b50ed00159c1332a5ae9`  
		Last Modified: Wed, 03 May 2023 20:22:46 GMT  
		Size: 5.2 MB (5224504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1357c913bae06fc471b1ba29963a41023b367169a33df605c24f688ca19fba6`  
		Last Modified: Wed, 03 May 2023 20:22:46 GMT  
		Size: 610.3 KB (610274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdeea262d51fa2fd0a20a1c0067906a28611ed6d893bbfc07b305a2ad12872bf`  
		Last Modified: Wed, 03 May 2023 20:22:45 GMT  
		Size: 294.4 KB (294388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d29c2f2da0eb28da20c5b6155cda5fe564867522531a0d737f4d5d38d70482`  
		Last Modified: Wed, 03 May 2023 20:22:45 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432ec4176080d53ddfca242d4a6ece47afb37dd56154f2f8d110a611220d81ce`  
		Last Modified: Wed, 03 May 2023 20:22:48 GMT  
		Size: 52.7 MB (52685980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab316a2c3ce230eb78543d590746289488ab2411ce32ab4a4fff829964f8d6`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9611ebaa996ba274a749a684e1eab5da6f2da79e516eddf4e7aefb4ad17340`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5433ac64532fa5d3c3168cc608f497b8e5988cfe6db3506e072c6954d4fb4e6`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96a1658cb7854650683f232eb1898ae52498d5838b2cdb433e66184970ca793`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9744d377ea8891887eb5854020c3a4545c7ef19e8986ee58d32b3cf4040b73b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88673594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdf7920dfd53b2df52213aee261dd4e41c0549d72f9e343c14cd2b9fcbd5f4f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:59:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 17:59:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 17:59:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:59:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 03 May 2023 17:59:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 17:59:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:59:21 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 03 May 2023 17:59:22 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 17:59:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 17:59:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 17:59:35 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 03 May 2023 17:59:35 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 03 May 2023 17:59:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 17:59:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 17:59:35 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 17:59:35 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 17:59:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc49e0f227abecd65ff6b6795c3f880303494db817c7e1e18ecda59fc7152e8e`  
		Last Modified: Wed, 03 May 2023 18:00:52 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0194f60c08f3777da4f834e63630710e50ad01aba6984abe85826ebc49af6a79`  
		Last Modified: Wed, 03 May 2023 18:00:51 GMT  
		Size: 5.2 MB (5209527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63900b96976ba15b59992aaf3958e1823702187a944ded17b4e7e574e5303602`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 566.3 KB (566271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaa51d00fbb637175fe6cd98964622811feb4a21e8ab226b746d44415e72e5f`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 294.3 KB (294281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa220909c065252e8254c4d40d57f803dad4012af471289e13ffd7fa688c7eb`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb46de8d7de131610fcf1b61d5a577b86afa7c4840ff37ccec2b17e8498225d2`  
		Last Modified: Wed, 03 May 2023 18:00:52 GMT  
		Size: 52.5 MB (52543335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f937d96179866f5702ff575f8c8f95bbb804136340edde11989b41f079e045d0`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90137057d1382e2128147af431662186fb94c170fd949f3648719510367dcff`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e79d5751c60bf65d33ec9b49e331aaa0b00505dd7e2dce70dab7d08b91a847b`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4add3ef4c8cc00343e2616e6ac05f104c708b83a23ff11f519c1ccc110d16a17`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:13c66352ec28fb818402ea6a162b1d26ab57afc84b0959c08626072202a864fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4a23d81c45d81d19aed05a650b92a338f047fdbeff466ec274cce2ce6e48d4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:23:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 12 Apr 2023 01:23:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 12 Apr 2023 01:23:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:24:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 12 Apr 2023 01:24:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 12 Apr 2023 01:24:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Apr 2023 22:16:20 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 25 Apr 2023 22:16:21 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Apr 2023 22:16:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Apr 2023 22:16:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Apr 2023 22:16:49 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 25 Apr 2023 22:16:49 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 25 Apr 2023 22:16:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Apr 2023 22:16:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Apr 2023 22:16:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Apr 2023 22:16:52 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Apr 2023 22:16:52 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7569dcea363c11bb071b416ea27193dbe62d8a210fa1f829efabb35b46600dae`  
		Last Modified: Wed, 12 Apr 2023 01:26:25 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a685c575c0e899abc0410edf84715dd5cf4184fcbd447fdbbcac069795eadd05`  
		Last Modified: Wed, 12 Apr 2023 01:26:26 GMT  
		Size: 6.0 MB (6044117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283a2882808914c7a35f392d4ad2d2921ccf8b8855ab399e2998c22d061f16e`  
		Last Modified: Wed, 12 Apr 2023 01:26:24 GMT  
		Size: 662.1 KB (662116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17deb4c48f5c43beee592bed99d27502afe8c8f60cde1cb4bebb7dce00e877c`  
		Last Modified: Wed, 12 Apr 2023 01:26:24 GMT  
		Size: 294.3 KB (294319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a005d1ac9dd4beafe87fd0d6df08fa72f0631b6ab8e23223294f78a242f748`  
		Last Modified: Tue, 25 Apr 2023 22:17:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab032b77afd1546e2bf51f362edad19e7661fb6470925250236ef4b8192eed99`  
		Last Modified: Tue, 25 Apr 2023 22:17:42 GMT  
		Size: 53.7 MB (53662597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14465f77288ec304103ebf17b65c6630abe30166373f91e89939385535147e4`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5effe25ef84c827ba988a853ea59f8afff941940d15ca66ad41ccba621b99829`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6745b0a9c210274967bf202717f0026edd9102ecab6c433b4164ec8642f72e95`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d7963f0595ab31b467b4da324625d275d24dd8d46f18e3ac2504b8d64ed7c6`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:9760ef202c43ddfbdc3d8e220353ddef84ba50d1d757508a81e6ca7a6e62eb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:a78ecf1912d5046be84252e42c87b4ab88898be235ad23388b590870933d9c59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90226076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4894334bb0e847a86583bb98c2678f2ef00343fe485b0e7a77da57bf72386d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:20:41 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 20:20:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 20:20:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:20:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 03 May 2023 20:20:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 20:20:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:20:57 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 03 May 2023 20:20:57 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 20:21:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 20:21:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 20:21:10 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 03 May 2023 20:21:10 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 03 May 2023 20:21:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 20:21:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:21:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 20:21:11 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 20:21:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aae57dfaa0a56d12e531052d943db83aef0440c156d6fd9d192f6a1085a270`  
		Last Modified: Wed, 03 May 2023 20:22:47 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93caf13d63dac0c40ecd2e72ababf04b8014086e33b50ed00159c1332a5ae9`  
		Last Modified: Wed, 03 May 2023 20:22:46 GMT  
		Size: 5.2 MB (5224504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1357c913bae06fc471b1ba29963a41023b367169a33df605c24f688ca19fba6`  
		Last Modified: Wed, 03 May 2023 20:22:46 GMT  
		Size: 610.3 KB (610274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdeea262d51fa2fd0a20a1c0067906a28611ed6d893bbfc07b305a2ad12872bf`  
		Last Modified: Wed, 03 May 2023 20:22:45 GMT  
		Size: 294.4 KB (294388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d29c2f2da0eb28da20c5b6155cda5fe564867522531a0d737f4d5d38d70482`  
		Last Modified: Wed, 03 May 2023 20:22:45 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432ec4176080d53ddfca242d4a6ece47afb37dd56154f2f8d110a611220d81ce`  
		Last Modified: Wed, 03 May 2023 20:22:48 GMT  
		Size: 52.7 MB (52685980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab316a2c3ce230eb78543d590746289488ab2411ce32ab4a4fff829964f8d6`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9611ebaa996ba274a749a684e1eab5da6f2da79e516eddf4e7aefb4ad17340`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5433ac64532fa5d3c3168cc608f497b8e5988cfe6db3506e072c6954d4fb4e6`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96a1658cb7854650683f232eb1898ae52498d5838b2cdb433e66184970ca793`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9744d377ea8891887eb5854020c3a4545c7ef19e8986ee58d32b3cf4040b73b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88673594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdf7920dfd53b2df52213aee261dd4e41c0549d72f9e343c14cd2b9fcbd5f4f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:59:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 17:59:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 17:59:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:59:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 03 May 2023 17:59:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 17:59:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:59:21 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 03 May 2023 17:59:22 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 17:59:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 17:59:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 17:59:35 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 03 May 2023 17:59:35 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 03 May 2023 17:59:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 17:59:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 17:59:35 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 17:59:35 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 17:59:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc49e0f227abecd65ff6b6795c3f880303494db817c7e1e18ecda59fc7152e8e`  
		Last Modified: Wed, 03 May 2023 18:00:52 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0194f60c08f3777da4f834e63630710e50ad01aba6984abe85826ebc49af6a79`  
		Last Modified: Wed, 03 May 2023 18:00:51 GMT  
		Size: 5.2 MB (5209527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63900b96976ba15b59992aaf3958e1823702187a944ded17b4e7e574e5303602`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 566.3 KB (566271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaa51d00fbb637175fe6cd98964622811feb4a21e8ab226b746d44415e72e5f`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 294.3 KB (294281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa220909c065252e8254c4d40d57f803dad4012af471289e13ffd7fa688c7eb`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb46de8d7de131610fcf1b61d5a577b86afa7c4840ff37ccec2b17e8498225d2`  
		Last Modified: Wed, 03 May 2023 18:00:52 GMT  
		Size: 52.5 MB (52543335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f937d96179866f5702ff575f8c8f95bbb804136340edde11989b41f079e045d0`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90137057d1382e2128147af431662186fb94c170fd949f3648719510367dcff`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e79d5751c60bf65d33ec9b49e331aaa0b00505dd7e2dce70dab7d08b91a847b`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4add3ef4c8cc00343e2616e6ac05f104c708b83a23ff11f519c1ccc110d16a17`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:13c66352ec28fb818402ea6a162b1d26ab57afc84b0959c08626072202a864fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4a23d81c45d81d19aed05a650b92a338f047fdbeff466ec274cce2ce6e48d4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:23:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 12 Apr 2023 01:23:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 12 Apr 2023 01:23:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:24:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 12 Apr 2023 01:24:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 12 Apr 2023 01:24:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Apr 2023 22:16:20 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 25 Apr 2023 22:16:21 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Apr 2023 22:16:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Apr 2023 22:16:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Apr 2023 22:16:49 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 25 Apr 2023 22:16:49 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 25 Apr 2023 22:16:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Apr 2023 22:16:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Apr 2023 22:16:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Apr 2023 22:16:52 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Apr 2023 22:16:52 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7569dcea363c11bb071b416ea27193dbe62d8a210fa1f829efabb35b46600dae`  
		Last Modified: Wed, 12 Apr 2023 01:26:25 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a685c575c0e899abc0410edf84715dd5cf4184fcbd447fdbbcac069795eadd05`  
		Last Modified: Wed, 12 Apr 2023 01:26:26 GMT  
		Size: 6.0 MB (6044117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283a2882808914c7a35f392d4ad2d2921ccf8b8855ab399e2998c22d061f16e`  
		Last Modified: Wed, 12 Apr 2023 01:26:24 GMT  
		Size: 662.1 KB (662116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17deb4c48f5c43beee592bed99d27502afe8c8f60cde1cb4bebb7dce00e877c`  
		Last Modified: Wed, 12 Apr 2023 01:26:24 GMT  
		Size: 294.3 KB (294319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a005d1ac9dd4beafe87fd0d6df08fa72f0631b6ab8e23223294f78a242f748`  
		Last Modified: Tue, 25 Apr 2023 22:17:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab032b77afd1546e2bf51f362edad19e7661fb6470925250236ef4b8192eed99`  
		Last Modified: Tue, 25 Apr 2023 22:17:42 GMT  
		Size: 53.7 MB (53662597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14465f77288ec304103ebf17b65c6630abe30166373f91e89939385535147e4`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5effe25ef84c827ba988a853ea59f8afff941940d15ca66ad41ccba621b99829`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6745b0a9c210274967bf202717f0026edd9102ecab6c433b4164ec8642f72e95`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d7963f0595ab31b467b4da324625d275d24dd8d46f18e3ac2504b8d64ed7c6`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
