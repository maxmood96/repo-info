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
$ docker pull couchdb@sha256:92967097aa0f0a50c97c70c9aa9357c9fc43b446344c2d29130469b1e303a681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:f530aa464748189fb4cb9437f146f4a77054c49b01eec23326fc1ff901ce69df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84536131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96918c3fb276e53901e03168afdd8764c82624f3e73fd11835f262ce2d5f05eb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:32 GMT
ADD file:2818e508d01da2188fb234b38fb19aa1ea9eeeae92d361ecdf49318d949f51a9 in / 
# Mon, 12 Jun 2023 23:21:32 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:02:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jun 2023 04:02:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Jun 2023 04:02:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:03:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 13 Jun 2023 04:03:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jun 2023 04:03:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:03:29 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 13 Jun 2023 04:03:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Jun 2023 04:03:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Jun 2023 04:03:48 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Jun 2023 04:03:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Jun 2023 04:03:49 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 13 Jun 2023 04:03:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:03:49 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:03:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jun 2023 04:03:49 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Jun 2023 04:03:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8b91b88d557765cd8c6802668755a3f6dc4337b6ce15a17e4857139e5fc964f3`  
		Last Modified: Mon, 12 Jun 2023 23:27:09 GMT  
		Size: 27.1 MB (27138450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dce64dc1d986fe2a02da40cd4c32ca008166442ea4db561eab33b63f7cd126`  
		Last Modified: Tue, 13 Jun 2023 04:04:37 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6fb99156553b37b2d58e9a39225c37af49c63cfcc5f03833fd34bb10d34268`  
		Last Modified: Tue, 13 Jun 2023 04:04:36 GMT  
		Size: 6.7 MB (6704288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a50c5202daac6c76c5bd1d96dffd366da65456eddc306a8a77ef3de4a2cbb59`  
		Last Modified: Tue, 13 Jun 2023 04:04:35 GMT  
		Size: 1.3 MB (1259685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd650c9b2081d19a80d278a6396c0cbbdd34b45d6447ce293c4f8a5717981d54`  
		Last Modified: Tue, 13 Jun 2023 04:04:35 GMT  
		Size: 294.4 KB (294395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf42c30bc28466dc973f38316c0950f5661394dd2b9939b61540ca72422691a1`  
		Last Modified: Tue, 13 Jun 2023 04:04:48 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04306ba85711b8ab93c1b6a2c2e1319a6b9f032234fddce3fd1b2c09e59d6d4`  
		Last Modified: Tue, 13 Jun 2023 04:04:52 GMT  
		Size: 49.1 MB (49132304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85de8b774141c1c61eaa4be3d8a6b61262b278d238b20dc74f8c3bddb14aaa3`  
		Last Modified: Tue, 13 Jun 2023 04:04:46 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0d32f382de9d38f161ab52ccc6bd07bb3e3cc5a8046165fd6b42194c1a374a`  
		Last Modified: Tue, 13 Jun 2023 04:04:46 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adfdaf2d05607fa689935da29d8df4caa92273cd94634bd3ae59a9461fdb79a`  
		Last Modified: Tue, 13 Jun 2023 04:04:46 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ff3919f1c9f0c5ffb9d0415ced2e37ee361789a966cb0fe250695bc547cbfc`  
		Last Modified: Tue, 13 Jun 2023 04:04:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:45dfda4dbdfd2d6e559fe46f5c0cb4d613f251a2e31ff567ad1e956267095495
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72993981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7273aba545660bb46738d7029e0aeeb2086ec3221f79cedab92e284ae49592`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:58:08 GMT
ADD file:1368964550b1f674dd0365f72bb1d55cfebf5e3c651d49b5e168f9be97a6df76 in / 
# Tue, 04 Jul 2023 01:58:09 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:01:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 03:01:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 03:01:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:01:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 04 Jul 2023 03:01:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 03:01:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:01:51 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 04 Jul 2023 03:01:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 03:02:03 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 03:02:03 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 03:02:04 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 03:02:04 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 04 Jul 2023 03:02:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 03:02:04 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:02:04 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 03:02:04 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 03:02:04 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:30bfbe1cefebb80f6f9d5d90c39fcdf9d6367bbc76fa68e33ea3b4391c0f9a77`  
		Last Modified: Tue, 04 Jul 2023 02:02:39 GMT  
		Size: 25.9 MB (25921455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6954e131bac08371ce76b1ced14ebbd5df8fe886f3af6bc62930e38b5d5036d2`  
		Last Modified: Tue, 04 Jul 2023 03:02:37 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9050582020a4dbe57aacf513c8db4bb31101f1103335b402526976f5d9dd09a0`  
		Last Modified: Tue, 04 Jul 2023 03:02:36 GMT  
		Size: 6.6 MB (6577344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239c748e27f0d7331054f9fa77af9aff288057edd29e1f2a8c9ac69c3bae0372`  
		Last Modified: Tue, 04 Jul 2023 03:02:36 GMT  
		Size: 1.2 MB (1164583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7075b8de71333c68373efb4701fd47241802ef973ad5b13ab85ba14c44b2d78`  
		Last Modified: Tue, 04 Jul 2023 03:02:35 GMT  
		Size: 294.2 KB (294180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164db02d6ff7f85308c817569a3dbce99577c2b5d57dc84d6db4af73fb229cc0`  
		Last Modified: Tue, 04 Jul 2023 03:02:46 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee060527004f0f26072ee3f5d662ad6797f697228e5b867422c9eb82c5d7d5b`  
		Last Modified: Tue, 04 Jul 2023 03:02:48 GMT  
		Size: 39.0 MB (39029388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16910618a00fef4242b687f2a41f7e67d5be3a68c1f1f5341e85f44fb605210`  
		Last Modified: Tue, 04 Jul 2023 03:02:45 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0a179c3d25f3471e2a9316bad36c629accd787d8e21e6d9e943970543abef5`  
		Last Modified: Tue, 04 Jul 2023 03:02:45 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d791aaf8110a45e526a260337e66d353a3fcdf84504ae1eb53fb0d2a93d27dab`  
		Last Modified: Tue, 04 Jul 2023 03:02:45 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cbed26389f70f12bd0a3327c878478ba1882a373a609c5980e518fc7f7d4d6`  
		Last Modified: Tue, 04 Jul 2023 03:02:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:92967097aa0f0a50c97c70c9aa9357c9fc43b446344c2d29130469b1e303a681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:f530aa464748189fb4cb9437f146f4a77054c49b01eec23326fc1ff901ce69df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84536131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96918c3fb276e53901e03168afdd8764c82624f3e73fd11835f262ce2d5f05eb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:32 GMT
ADD file:2818e508d01da2188fb234b38fb19aa1ea9eeeae92d361ecdf49318d949f51a9 in / 
# Mon, 12 Jun 2023 23:21:32 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:02:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jun 2023 04:02:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Jun 2023 04:02:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:03:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 13 Jun 2023 04:03:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jun 2023 04:03:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:03:29 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 13 Jun 2023 04:03:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Jun 2023 04:03:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Jun 2023 04:03:48 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Jun 2023 04:03:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Jun 2023 04:03:49 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 13 Jun 2023 04:03:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:03:49 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:03:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jun 2023 04:03:49 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Jun 2023 04:03:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8b91b88d557765cd8c6802668755a3f6dc4337b6ce15a17e4857139e5fc964f3`  
		Last Modified: Mon, 12 Jun 2023 23:27:09 GMT  
		Size: 27.1 MB (27138450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dce64dc1d986fe2a02da40cd4c32ca008166442ea4db561eab33b63f7cd126`  
		Last Modified: Tue, 13 Jun 2023 04:04:37 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6fb99156553b37b2d58e9a39225c37af49c63cfcc5f03833fd34bb10d34268`  
		Last Modified: Tue, 13 Jun 2023 04:04:36 GMT  
		Size: 6.7 MB (6704288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a50c5202daac6c76c5bd1d96dffd366da65456eddc306a8a77ef3de4a2cbb59`  
		Last Modified: Tue, 13 Jun 2023 04:04:35 GMT  
		Size: 1.3 MB (1259685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd650c9b2081d19a80d278a6396c0cbbdd34b45d6447ce293c4f8a5717981d54`  
		Last Modified: Tue, 13 Jun 2023 04:04:35 GMT  
		Size: 294.4 KB (294395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf42c30bc28466dc973f38316c0950f5661394dd2b9939b61540ca72422691a1`  
		Last Modified: Tue, 13 Jun 2023 04:04:48 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04306ba85711b8ab93c1b6a2c2e1319a6b9f032234fddce3fd1b2c09e59d6d4`  
		Last Modified: Tue, 13 Jun 2023 04:04:52 GMT  
		Size: 49.1 MB (49132304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85de8b774141c1c61eaa4be3d8a6b61262b278d238b20dc74f8c3bddb14aaa3`  
		Last Modified: Tue, 13 Jun 2023 04:04:46 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0d32f382de9d38f161ab52ccc6bd07bb3e3cc5a8046165fd6b42194c1a374a`  
		Last Modified: Tue, 13 Jun 2023 04:04:46 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adfdaf2d05607fa689935da29d8df4caa92273cd94634bd3ae59a9461fdb79a`  
		Last Modified: Tue, 13 Jun 2023 04:04:46 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ff3919f1c9f0c5ffb9d0415ced2e37ee361789a966cb0fe250695bc547cbfc`  
		Last Modified: Tue, 13 Jun 2023 04:04:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:45dfda4dbdfd2d6e559fe46f5c0cb4d613f251a2e31ff567ad1e956267095495
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72993981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7273aba545660bb46738d7029e0aeeb2086ec3221f79cedab92e284ae49592`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:58:08 GMT
ADD file:1368964550b1f674dd0365f72bb1d55cfebf5e3c651d49b5e168f9be97a6df76 in / 
# Tue, 04 Jul 2023 01:58:09 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:01:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 03:01:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 03:01:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:01:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 04 Jul 2023 03:01:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 03:01:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:01:51 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 04 Jul 2023 03:01:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 03:02:03 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 03:02:03 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 03:02:04 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 03:02:04 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 04 Jul 2023 03:02:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 03:02:04 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:02:04 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 03:02:04 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 03:02:04 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:30bfbe1cefebb80f6f9d5d90c39fcdf9d6367bbc76fa68e33ea3b4391c0f9a77`  
		Last Modified: Tue, 04 Jul 2023 02:02:39 GMT  
		Size: 25.9 MB (25921455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6954e131bac08371ce76b1ced14ebbd5df8fe886f3af6bc62930e38b5d5036d2`  
		Last Modified: Tue, 04 Jul 2023 03:02:37 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9050582020a4dbe57aacf513c8db4bb31101f1103335b402526976f5d9dd09a0`  
		Last Modified: Tue, 04 Jul 2023 03:02:36 GMT  
		Size: 6.6 MB (6577344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239c748e27f0d7331054f9fa77af9aff288057edd29e1f2a8c9ac69c3bae0372`  
		Last Modified: Tue, 04 Jul 2023 03:02:36 GMT  
		Size: 1.2 MB (1164583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7075b8de71333c68373efb4701fd47241802ef973ad5b13ab85ba14c44b2d78`  
		Last Modified: Tue, 04 Jul 2023 03:02:35 GMT  
		Size: 294.2 KB (294180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164db02d6ff7f85308c817569a3dbce99577c2b5d57dc84d6db4af73fb229cc0`  
		Last Modified: Tue, 04 Jul 2023 03:02:46 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee060527004f0f26072ee3f5d662ad6797f697228e5b867422c9eb82c5d7d5b`  
		Last Modified: Tue, 04 Jul 2023 03:02:48 GMT  
		Size: 39.0 MB (39029388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16910618a00fef4242b687f2a41f7e67d5be3a68c1f1f5341e85f44fb605210`  
		Last Modified: Tue, 04 Jul 2023 03:02:45 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0a179c3d25f3471e2a9316bad36c629accd787d8e21e6d9e943970543abef5`  
		Last Modified: Tue, 04 Jul 2023 03:02:45 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d791aaf8110a45e526a260337e66d353a3fcdf84504ae1eb53fb0d2a93d27dab`  
		Last Modified: Tue, 04 Jul 2023 03:02:45 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cbed26389f70f12bd0a3327c878478ba1882a373a609c5980e518fc7f7d4d6`  
		Last Modified: Tue, 04 Jul 2023 03:02:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:92967097aa0f0a50c97c70c9aa9357c9fc43b446344c2d29130469b1e303a681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:f530aa464748189fb4cb9437f146f4a77054c49b01eec23326fc1ff901ce69df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84536131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96918c3fb276e53901e03168afdd8764c82624f3e73fd11835f262ce2d5f05eb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:32 GMT
ADD file:2818e508d01da2188fb234b38fb19aa1ea9eeeae92d361ecdf49318d949f51a9 in / 
# Mon, 12 Jun 2023 23:21:32 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:02:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jun 2023 04:02:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Jun 2023 04:02:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:03:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 13 Jun 2023 04:03:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jun 2023 04:03:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:03:29 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 13 Jun 2023 04:03:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Jun 2023 04:03:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Jun 2023 04:03:48 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Jun 2023 04:03:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Jun 2023 04:03:49 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 13 Jun 2023 04:03:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:03:49 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:03:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jun 2023 04:03:49 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Jun 2023 04:03:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8b91b88d557765cd8c6802668755a3f6dc4337b6ce15a17e4857139e5fc964f3`  
		Last Modified: Mon, 12 Jun 2023 23:27:09 GMT  
		Size: 27.1 MB (27138450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dce64dc1d986fe2a02da40cd4c32ca008166442ea4db561eab33b63f7cd126`  
		Last Modified: Tue, 13 Jun 2023 04:04:37 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6fb99156553b37b2d58e9a39225c37af49c63cfcc5f03833fd34bb10d34268`  
		Last Modified: Tue, 13 Jun 2023 04:04:36 GMT  
		Size: 6.7 MB (6704288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a50c5202daac6c76c5bd1d96dffd366da65456eddc306a8a77ef3de4a2cbb59`  
		Last Modified: Tue, 13 Jun 2023 04:04:35 GMT  
		Size: 1.3 MB (1259685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd650c9b2081d19a80d278a6396c0cbbdd34b45d6447ce293c4f8a5717981d54`  
		Last Modified: Tue, 13 Jun 2023 04:04:35 GMT  
		Size: 294.4 KB (294395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf42c30bc28466dc973f38316c0950f5661394dd2b9939b61540ca72422691a1`  
		Last Modified: Tue, 13 Jun 2023 04:04:48 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04306ba85711b8ab93c1b6a2c2e1319a6b9f032234fddce3fd1b2c09e59d6d4`  
		Last Modified: Tue, 13 Jun 2023 04:04:52 GMT  
		Size: 49.1 MB (49132304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85de8b774141c1c61eaa4be3d8a6b61262b278d238b20dc74f8c3bddb14aaa3`  
		Last Modified: Tue, 13 Jun 2023 04:04:46 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0d32f382de9d38f161ab52ccc6bd07bb3e3cc5a8046165fd6b42194c1a374a`  
		Last Modified: Tue, 13 Jun 2023 04:04:46 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adfdaf2d05607fa689935da29d8df4caa92273cd94634bd3ae59a9461fdb79a`  
		Last Modified: Tue, 13 Jun 2023 04:04:46 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ff3919f1c9f0c5ffb9d0415ced2e37ee361789a966cb0fe250695bc547cbfc`  
		Last Modified: Tue, 13 Jun 2023 04:04:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:45dfda4dbdfd2d6e559fe46f5c0cb4d613f251a2e31ff567ad1e956267095495
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72993981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7273aba545660bb46738d7029e0aeeb2086ec3221f79cedab92e284ae49592`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:58:08 GMT
ADD file:1368964550b1f674dd0365f72bb1d55cfebf5e3c651d49b5e168f9be97a6df76 in / 
# Tue, 04 Jul 2023 01:58:09 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:01:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 03:01:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 03:01:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:01:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 04 Jul 2023 03:01:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 03:01:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:01:51 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 04 Jul 2023 03:01:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 03:02:03 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 03:02:03 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 03:02:04 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 03:02:04 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 04 Jul 2023 03:02:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 03:02:04 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:02:04 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 03:02:04 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 03:02:04 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:30bfbe1cefebb80f6f9d5d90c39fcdf9d6367bbc76fa68e33ea3b4391c0f9a77`  
		Last Modified: Tue, 04 Jul 2023 02:02:39 GMT  
		Size: 25.9 MB (25921455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6954e131bac08371ce76b1ced14ebbd5df8fe886f3af6bc62930e38b5d5036d2`  
		Last Modified: Tue, 04 Jul 2023 03:02:37 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9050582020a4dbe57aacf513c8db4bb31101f1103335b402526976f5d9dd09a0`  
		Last Modified: Tue, 04 Jul 2023 03:02:36 GMT  
		Size: 6.6 MB (6577344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239c748e27f0d7331054f9fa77af9aff288057edd29e1f2a8c9ac69c3bae0372`  
		Last Modified: Tue, 04 Jul 2023 03:02:36 GMT  
		Size: 1.2 MB (1164583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7075b8de71333c68373efb4701fd47241802ef973ad5b13ab85ba14c44b2d78`  
		Last Modified: Tue, 04 Jul 2023 03:02:35 GMT  
		Size: 294.2 KB (294180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164db02d6ff7f85308c817569a3dbce99577c2b5d57dc84d6db4af73fb229cc0`  
		Last Modified: Tue, 04 Jul 2023 03:02:46 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee060527004f0f26072ee3f5d662ad6797f697228e5b867422c9eb82c5d7d5b`  
		Last Modified: Tue, 04 Jul 2023 03:02:48 GMT  
		Size: 39.0 MB (39029388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16910618a00fef4242b687f2a41f7e67d5be3a68c1f1f5341e85f44fb605210`  
		Last Modified: Tue, 04 Jul 2023 03:02:45 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0a179c3d25f3471e2a9316bad36c629accd787d8e21e6d9e943970543abef5`  
		Last Modified: Tue, 04 Jul 2023 03:02:45 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d791aaf8110a45e526a260337e66d353a3fcdf84504ae1eb53fb0d2a93d27dab`  
		Last Modified: Tue, 04 Jul 2023 03:02:45 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cbed26389f70f12bd0a3327c878478ba1882a373a609c5980e518fc7f7d4d6`  
		Last Modified: Tue, 04 Jul 2023 03:02:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:7c43bfb5025b2b976efce61c4d4d9dbdcae94826d25958c8a760d6f820d893a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:40016f83b61df0ac945f1536e3a52e6ea2761a18326933513bbe358e5f787102
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90239977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b725f6b2513a8b4ec7c8b706aed6ac7a7166a5c833b1a23dd2f559310808110`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:01:57 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jun 2023 04:01:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Jun 2023 04:02:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:02:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 13 Jun 2023 04:02:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jun 2023 04:02:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:02:14 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 13 Jun 2023 04:02:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Jun 2023 04:02:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Jun 2023 04:02:27 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Jun 2023 04:02:27 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 13 Jun 2023 04:02:27 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 13 Jun 2023 04:02:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:02:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:02:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jun 2023 04:02:28 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Jun 2023 04:02:28 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fa5a08f48785d08765b7746d507926063e6ab14084ec52c45ad658c9900e2`  
		Last Modified: Tue, 13 Jun 2023 04:04:05 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effeea359db8a5b5241e47adb1070cec93345c3cc2011db12b74a56d6cec9151`  
		Last Modified: Tue, 13 Jun 2023 04:04:04 GMT  
		Size: 5.2 MB (5224468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b83a1bd5e8dd69f1172af3053ab31900973778718afe1abb82dd6d9cf4075a`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 610.3 KB (610265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d5ee803171a181293d9529fab444ccda628ce617e53d52acb7bbd34e1dbe3f`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 294.4 KB (294377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abff9bf83b2eee5ea095f234f197ed3bdc13ba5c1d9d27e366d814ca232560d3`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c0289451f671b5a57844126e484dc7f940b217bdd9badb059bda68d8764ab`  
		Last Modified: Tue, 13 Jun 2023 04:04:07 GMT  
		Size: 52.7 MB (52686042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7f7afef66f9db1812bc4358426b2221d5126baecd2715d01530d1fa9ea2e86`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d22413df733620c7d50f6db00f44e8dd5cd48ae5343fcbb767b482c4f0f9ad`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7983d64b4de2667bb5662734e159cb3529658b676c0c32a3e5906a4a26d27ce3`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf22f027705f7c7b494a7c2f2bd1d7b88f54297a0cd015536fdf35b915ace46`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:111bef69577b043b2f8af1fdd73ffa8e23898a6bc70b3f82fd3182ff1618236a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88684312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d016bedbaaaf56c355df33a499d3e134c6c17b26780b48454292818e0a91487f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:00:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 03:00:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 03:00:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:00:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 03:00:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 03:00:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:00:31 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 03:00:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 03:00:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 03:00:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 03:00:44 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 03:00:44 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 03:00:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 03:00:45 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:00:45 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 03:00:45 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 03:00:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc0d271896e1f31b2370d23711036a521e9acd3228114cc23f8fac55f387dbd`  
		Last Modified: Tue, 04 Jul 2023 03:02:19 GMT  
		Size: 3.4 KB (3432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8aac13251911c1284e2d4984341c6755bbe92e937e630352f4637e979958e68`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 5.2 MB (5209578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4219899a34e5a710d067929c59cf4cee7af11394da04941e8ec8dbdfa78c74c3`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 566.3 KB (566278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5043581719683361a4b86cda02be153567823f8d994de5929cf109fde6360729`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 294.3 KB (294323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6faedae003b0a46ef804c85e87d669f2ac496327ecfe31589fc2ef8cb795d9`  
		Last Modified: Tue, 04 Jul 2023 03:02:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bb64485bf61484d6294808283f6a71accee5b23965b220feea15e713cfe140`  
		Last Modified: Tue, 04 Jul 2023 03:02:20 GMT  
		Size: 52.5 MB (52543741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de90cc018497f0216ecab317a8a855961340c9bad495e67de724c2050657df6`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3f0725b25615db7255060c7d284ae18f16ad4b6eed961e19e8b6843453968`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9180ffcb545467f2e03ea97afe6c338090bda754a8660337cb26ba571028b18d`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0e1825ffd91b4338bf24761c3146c6d0a90ea00e5d87b2b89c62e7a2489e73`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:3eb5767e878cf69f2870e99b9c95b3be3dfcc0471c122389a9d0dfb659234883
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e065d599166a5dc0bcef7979716402c5fca0bbc616c07314ded86709614f51e1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:33 GMT
ADD file:37fa020aca7253d41d395ed529c38db73caaa4da098754836244552f65fa7d5d in / 
# Tue, 04 Jul 2023 01:18:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:47:38 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 04:47:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 04:48:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:48:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 04:48:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 04:48:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:48:46 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 04:48:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 04:49:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 04:49:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 04:49:23 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 04:49:24 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 04:49:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 04:49:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 04:49:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 04:49:28 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 04:49:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:147bb8b5828c99cd6b07d252d2987490463c142099eaa0815025685f8fa4f3d8`  
		Last Modified: Tue, 04 Jul 2023 01:25:40 GMT  
		Size: 35.3 MB (35291082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2701cbef8ba9fc49aabcd763212b84907356b9d67b68018587e12e7c54af3fee`  
		Last Modified: Tue, 04 Jul 2023 04:50:24 GMT  
		Size: 3.4 KB (3406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf807338a413416db46fc9e534bbe3265bc56baad887760486a0a54d25123b2`  
		Last Modified: Tue, 04 Jul 2023 04:50:24 GMT  
		Size: 6.0 MB (6044173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7409825b5d24fb99ad06438d83de58bf0ec20c4238d23657386eb390b56cf14a`  
		Last Modified: Tue, 04 Jul 2023 04:50:22 GMT  
		Size: 662.2 KB (662178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f62ee6bf18f44a92fdcdf0283d02bd2a4f1af5b1a8bd7e85621f45a95f8a04b`  
		Last Modified: Tue, 04 Jul 2023 04:50:21 GMT  
		Size: 294.4 KB (294369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716fa9059088e2aa7f1ea452b78d008438054cf553aec84db5f0b1c9d45af07d`  
		Last Modified: Tue, 04 Jul 2023 04:50:21 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646ca9755ca8690dde79876e5cc2575157aa6676d4f208ae1df21923cccd99cd`  
		Last Modified: Tue, 04 Jul 2023 04:50:28 GMT  
		Size: 53.7 MB (53662975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f92d3e00609286c22a6359ccd30574b19d50f9d6697f0a0ea5eab26ab12bc76`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339e7380fa4b617f06e977822abe3be70818da7d6d685880896b0eae0a1515be`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080782760cb6436e3664eb4f4e11c5008ca48beefe7641cd9296bcb2b0596458`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0412cece6d0a349aed06c4894e09a68bcee9300a4e7f88f629d13647544596e6`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:0bcccda85f5c60188048ec57dd9459e296f769c5ad766371be2f057c1cb31202
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86992279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b56bdcd62fdc551f2173e4ad2ca3ca6490f7f1acec77826451b8fabe35fa900`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:32:44 GMT
ADD file:799c0afa70fa3bf4bb7804964481cba79e80aa3fad5c7a25beadde206ed6a8ff in / 
# Tue, 04 Jul 2023 01:32:46 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 02:31:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 02:32:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 02:32:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:32:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 02:32:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 02:32:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:32:15 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 02:32:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 02:32:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 02:32:33 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 02:32:33 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 02:32:33 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 02:32:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 02:32:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 02:32:34 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 02:32:34 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 02:32:34 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bbee891481f2623da9c7d37a49947926519c858c2b06773370a6189440d4b4de`  
		Last Modified: Tue, 04 Jul 2023 01:37:37 GMT  
		Size: 29.7 MB (29652540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ca3d8ad5e25fe241e125f8bbbe38fc1732c37f3caa96c1ef02a7f489a5aae6`  
		Last Modified: Tue, 04 Jul 2023 02:32:52 GMT  
		Size: 3.4 KB (3432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60572b3f976bbdc302097dea095b6bea87f04aaa5902a11eb46130547c2f0154`  
		Last Modified: Tue, 04 Jul 2023 02:32:52 GMT  
		Size: 5.1 MB (5110438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056d956cd8463eed79cf7d437deb772330ad221345369e72ac6295e5713ca302`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 573.0 KB (573005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd772a2ca35e7648d7321fb6b0eb780c57418a1902a7805f6217c3e30e57893`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 294.4 KB (294392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a421ebc7a36d0af94ef7d446133f4686c9ef5a16e88004505d10bbf259c14db6`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9f6c295417043fc04a54083419e1707a71800e53f2d2643c9a2085f368fb87`  
		Last Modified: Tue, 04 Jul 2023 02:32:55 GMT  
		Size: 51.4 MB (51354464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83bfa157ad1e19b57a9df85aa0579c82163bee844e2c05b20095043b063b28`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235315086a5d8e7a181854f2e016c9da2abc0c2f9a30e583979f1b0d4326ee86`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dbfd2547b3b689e42acaaa81c5eb50c74f032cf42d0e18e33a29f8253ec632`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dac4cd592579b8351c686a4fe857238634639bd8f332711ec4d2545d6a95b71`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:1685a2ac2d495300a633d7012fbfabba04aa704666947a499148c05ab1181414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:2a2307415ded35db033de3738950a0cbb9b17dadee7f140896f31b1d8ad5ce9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80023796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134062f2fcc091d3d855826efe96aa5309b7c4dbd1d3da286cd66d09fa01d8bd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:32 GMT
ADD file:2818e508d01da2188fb234b38fb19aa1ea9eeeae92d361ecdf49318d949f51a9 in / 
# Mon, 12 Jun 2023 23:21:32 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:02:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jun 2023 04:02:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Jun 2023 04:02:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:03:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 13 Jun 2023 04:03:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jun 2023 04:03:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:03:11 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 13 Jun 2023 04:03:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Jun 2023 04:03:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Jun 2023 04:03:25 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Jun 2023 04:03:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Jun 2023 04:03:25 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 13 Jun 2023 04:03:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:03:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:03:26 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jun 2023 04:03:26 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Jun 2023 04:03:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8b91b88d557765cd8c6802668755a3f6dc4337b6ce15a17e4857139e5fc964f3`  
		Last Modified: Mon, 12 Jun 2023 23:27:09 GMT  
		Size: 27.1 MB (27138450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dce64dc1d986fe2a02da40cd4c32ca008166442ea4db561eab33b63f7cd126`  
		Last Modified: Tue, 13 Jun 2023 04:04:37 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6fb99156553b37b2d58e9a39225c37af49c63cfcc5f03833fd34bb10d34268`  
		Last Modified: Tue, 13 Jun 2023 04:04:36 GMT  
		Size: 6.7 MB (6704288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a50c5202daac6c76c5bd1d96dffd366da65456eddc306a8a77ef3de4a2cbb59`  
		Last Modified: Tue, 13 Jun 2023 04:04:35 GMT  
		Size: 1.3 MB (1259685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd650c9b2081d19a80d278a6396c0cbbdd34b45d6447ce293c4f8a5717981d54`  
		Last Modified: Tue, 13 Jun 2023 04:04:35 GMT  
		Size: 294.4 KB (294395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22c2981ce802ff3af09597af4c3d5fa3c00b9c1d470c90e0be6e3040d1cffcc`  
		Last Modified: Tue, 13 Jun 2023 04:04:35 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81596bdfad922a44b726226abb7db7f4c97c88ec16e805ac13cbdd5b5ec125a6`  
		Last Modified: Tue, 13 Jun 2023 04:04:38 GMT  
		Size: 44.6 MB (44619975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c0b99740b533501ceaad0807cd7be644e8aa431d479aecaff8cd03f9f9296d`  
		Last Modified: Tue, 13 Jun 2023 04:04:33 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c86518fe5107ac033c504c023a35d97166b8f64e9e1450a55cf79bf2c060c1`  
		Last Modified: Tue, 13 Jun 2023 04:04:33 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3dc7f68ec827cd8a7c6b88ccc917646e5872f284e9ec624daf6949faa2147aa`  
		Last Modified: Tue, 13 Jun 2023 04:04:33 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d80149eff3a59dbc742ea73df38ce43e01cc9beb72aca8d415e20ae25a11d9`  
		Last Modified: Tue, 13 Jun 2023 04:04:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f10a681d5ab99953bb6804013de878d1ceb420175d11a43f05710009ee6174c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75090775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079e2eddcebf6a56ab5f7da946b68800d2a5905b6a537a4bdcdc9f32e7734511`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:58:08 GMT
ADD file:1368964550b1f674dd0365f72bb1d55cfebf5e3c651d49b5e168f9be97a6df76 in / 
# Tue, 04 Jul 2023 01:58:09 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:01:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 03:01:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 03:01:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:01:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 04 Jul 2023 03:01:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 03:01:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:01:30 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 04 Jul 2023 03:01:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 03:01:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 03:01:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 03:01:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 03:01:44 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 04 Jul 2023 03:01:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 03:01:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:01:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 03:01:44 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 03:01:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:30bfbe1cefebb80f6f9d5d90c39fcdf9d6367bbc76fa68e33ea3b4391c0f9a77`  
		Last Modified: Tue, 04 Jul 2023 02:02:39 GMT  
		Size: 25.9 MB (25921455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6954e131bac08371ce76b1ced14ebbd5df8fe886f3af6bc62930e38b5d5036d2`  
		Last Modified: Tue, 04 Jul 2023 03:02:37 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9050582020a4dbe57aacf513c8db4bb31101f1103335b402526976f5d9dd09a0`  
		Last Modified: Tue, 04 Jul 2023 03:02:36 GMT  
		Size: 6.6 MB (6577344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239c748e27f0d7331054f9fa77af9aff288057edd29e1f2a8c9ac69c3bae0372`  
		Last Modified: Tue, 04 Jul 2023 03:02:36 GMT  
		Size: 1.2 MB (1164583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7075b8de71333c68373efb4701fd47241802ef973ad5b13ab85ba14c44b2d78`  
		Last Modified: Tue, 04 Jul 2023 03:02:35 GMT  
		Size: 294.2 KB (294180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1011936f7431fc16c7e21c10c209bff5718cb777dfb0c953397ea8226bdd320`  
		Last Modified: Tue, 04 Jul 2023 03:02:35 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465dead1bb40707a13854c1a212bb17549b2504972cbc680b27b5783ac7e8d7d`  
		Last Modified: Tue, 04 Jul 2023 03:02:37 GMT  
		Size: 41.1 MB (41126183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73d5c72d12baa9a8d2e6548e26c45a5a9cef7a9f20fd751aba1bffa5a2cfdd0`  
		Last Modified: Tue, 04 Jul 2023 03:02:33 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc9f89faa408b17a5ca49e1283ea58f0a88152645799b9ce7c6e382305bbb82`  
		Last Modified: Tue, 04 Jul 2023 03:02:33 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9a0548c1d91f04e194a7d10a65f67ede0230463c91b278dd3759bf1313783c`  
		Last Modified: Tue, 04 Jul 2023 03:02:33 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84387f2743573536866f5ea56fa49c5a4bd5973b2404303a2c872312283c1725`  
		Last Modified: Tue, 04 Jul 2023 03:02:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:1685a2ac2d495300a633d7012fbfabba04aa704666947a499148c05ab1181414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:2a2307415ded35db033de3738950a0cbb9b17dadee7f140896f31b1d8ad5ce9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80023796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134062f2fcc091d3d855826efe96aa5309b7c4dbd1d3da286cd66d09fa01d8bd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:32 GMT
ADD file:2818e508d01da2188fb234b38fb19aa1ea9eeeae92d361ecdf49318d949f51a9 in / 
# Mon, 12 Jun 2023 23:21:32 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:02:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jun 2023 04:02:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Jun 2023 04:02:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:03:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 13 Jun 2023 04:03:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jun 2023 04:03:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:03:11 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 13 Jun 2023 04:03:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Jun 2023 04:03:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Jun 2023 04:03:25 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Jun 2023 04:03:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Jun 2023 04:03:25 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 13 Jun 2023 04:03:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:03:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:03:26 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jun 2023 04:03:26 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Jun 2023 04:03:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8b91b88d557765cd8c6802668755a3f6dc4337b6ce15a17e4857139e5fc964f3`  
		Last Modified: Mon, 12 Jun 2023 23:27:09 GMT  
		Size: 27.1 MB (27138450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dce64dc1d986fe2a02da40cd4c32ca008166442ea4db561eab33b63f7cd126`  
		Last Modified: Tue, 13 Jun 2023 04:04:37 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6fb99156553b37b2d58e9a39225c37af49c63cfcc5f03833fd34bb10d34268`  
		Last Modified: Tue, 13 Jun 2023 04:04:36 GMT  
		Size: 6.7 MB (6704288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a50c5202daac6c76c5bd1d96dffd366da65456eddc306a8a77ef3de4a2cbb59`  
		Last Modified: Tue, 13 Jun 2023 04:04:35 GMT  
		Size: 1.3 MB (1259685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd650c9b2081d19a80d278a6396c0cbbdd34b45d6447ce293c4f8a5717981d54`  
		Last Modified: Tue, 13 Jun 2023 04:04:35 GMT  
		Size: 294.4 KB (294395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22c2981ce802ff3af09597af4c3d5fa3c00b9c1d470c90e0be6e3040d1cffcc`  
		Last Modified: Tue, 13 Jun 2023 04:04:35 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81596bdfad922a44b726226abb7db7f4c97c88ec16e805ac13cbdd5b5ec125a6`  
		Last Modified: Tue, 13 Jun 2023 04:04:38 GMT  
		Size: 44.6 MB (44619975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c0b99740b533501ceaad0807cd7be644e8aa431d479aecaff8cd03f9f9296d`  
		Last Modified: Tue, 13 Jun 2023 04:04:33 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c86518fe5107ac033c504c023a35d97166b8f64e9e1450a55cf79bf2c060c1`  
		Last Modified: Tue, 13 Jun 2023 04:04:33 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3dc7f68ec827cd8a7c6b88ccc917646e5872f284e9ec624daf6949faa2147aa`  
		Last Modified: Tue, 13 Jun 2023 04:04:33 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d80149eff3a59dbc742ea73df38ce43e01cc9beb72aca8d415e20ae25a11d9`  
		Last Modified: Tue, 13 Jun 2023 04:04:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f10a681d5ab99953bb6804013de878d1ceb420175d11a43f05710009ee6174c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75090775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079e2eddcebf6a56ab5f7da946b68800d2a5905b6a537a4bdcdc9f32e7734511`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:58:08 GMT
ADD file:1368964550b1f674dd0365f72bb1d55cfebf5e3c651d49b5e168f9be97a6df76 in / 
# Tue, 04 Jul 2023 01:58:09 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:01:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 03:01:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 03:01:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:01:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 04 Jul 2023 03:01:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 03:01:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:01:30 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 04 Jul 2023 03:01:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 03:01:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 03:01:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 03:01:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 03:01:44 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 04 Jul 2023 03:01:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 03:01:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:01:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 03:01:44 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 03:01:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:30bfbe1cefebb80f6f9d5d90c39fcdf9d6367bbc76fa68e33ea3b4391c0f9a77`  
		Last Modified: Tue, 04 Jul 2023 02:02:39 GMT  
		Size: 25.9 MB (25921455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6954e131bac08371ce76b1ced14ebbd5df8fe886f3af6bc62930e38b5d5036d2`  
		Last Modified: Tue, 04 Jul 2023 03:02:37 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9050582020a4dbe57aacf513c8db4bb31101f1103335b402526976f5d9dd09a0`  
		Last Modified: Tue, 04 Jul 2023 03:02:36 GMT  
		Size: 6.6 MB (6577344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239c748e27f0d7331054f9fa77af9aff288057edd29e1f2a8c9ac69c3bae0372`  
		Last Modified: Tue, 04 Jul 2023 03:02:36 GMT  
		Size: 1.2 MB (1164583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7075b8de71333c68373efb4701fd47241802ef973ad5b13ab85ba14c44b2d78`  
		Last Modified: Tue, 04 Jul 2023 03:02:35 GMT  
		Size: 294.2 KB (294180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1011936f7431fc16c7e21c10c209bff5718cb777dfb0c953397ea8226bdd320`  
		Last Modified: Tue, 04 Jul 2023 03:02:35 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465dead1bb40707a13854c1a212bb17549b2504972cbc680b27b5783ac7e8d7d`  
		Last Modified: Tue, 04 Jul 2023 03:02:37 GMT  
		Size: 41.1 MB (41126183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73d5c72d12baa9a8d2e6548e26c45a5a9cef7a9f20fd751aba1bffa5a2cfdd0`  
		Last Modified: Tue, 04 Jul 2023 03:02:33 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc9f89faa408b17a5ca49e1283ea58f0a88152645799b9ce7c6e382305bbb82`  
		Last Modified: Tue, 04 Jul 2023 03:02:33 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9a0548c1d91f04e194a7d10a65f67ede0230463c91b278dd3759bf1313783c`  
		Last Modified: Tue, 04 Jul 2023 03:02:33 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84387f2743573536866f5ea56fa49c5a4bd5973b2404303a2c872312283c1725`  
		Last Modified: Tue, 04 Jul 2023 03:02:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:d86c0902299a50886c853fb3c4e15fb9168c42fbe2edb9f14c2f683f3920028c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:22fdd25d4eef5d0385853f6079463a23ca52bfcbd8d0dc7092dbd9797adf897d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89740540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a70f12d6bc5aa3e6c706277ff2c517d3bfcd6bc7dcdff28e99c7318d0c5f318`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:01:57 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jun 2023 04:01:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Jun 2023 04:02:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:02:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 13 Jun 2023 04:02:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jun 2023 04:02:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:02:32 GMT
ENV COUCHDB_VERSION=3.2.3
# Tue, 13 Jun 2023 04:02:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Jun 2023 04:02:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Jun 2023 04:02:45 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Jun 2023 04:02:45 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 13 Jun 2023 04:02:45 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 13 Jun 2023 04:02:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:02:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:02:46 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jun 2023 04:02:46 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Jun 2023 04:02:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fa5a08f48785d08765b7746d507926063e6ab14084ec52c45ad658c9900e2`  
		Last Modified: Tue, 13 Jun 2023 04:04:05 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effeea359db8a5b5241e47adb1070cec93345c3cc2011db12b74a56d6cec9151`  
		Last Modified: Tue, 13 Jun 2023 04:04:04 GMT  
		Size: 5.2 MB (5224468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b83a1bd5e8dd69f1172af3053ab31900973778718afe1abb82dd6d9cf4075a`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 610.3 KB (610265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d5ee803171a181293d9529fab444ccda628ce617e53d52acb7bbd34e1dbe3f`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 294.4 KB (294377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7bcd34bc103365c025d56bb91321fb3f909de9d2d8a3f86e2e42840dd5c967`  
		Last Modified: Tue, 13 Jun 2023 04:04:21 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c75aaa8226bcf8bd5abde0889b8926be9f496fb20715116927c48c9805a805`  
		Last Modified: Tue, 13 Jun 2023 04:04:25 GMT  
		Size: 52.2 MB (52186611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80869518eed6425bb6d52d653b7eafa53284cb556b9cc2d90b6ed8cd003dc773`  
		Last Modified: Tue, 13 Jun 2023 04:04:20 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c58c4494b65a294c8086500f80de0b3f1f88777384b4a0bf59f39d1374bb32`  
		Last Modified: Tue, 13 Jun 2023 04:04:20 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0453ee6f28c2aca08755a0990b9e7e89af4760c203915d0701b6e041498a0b1`  
		Last Modified: Tue, 13 Jun 2023 04:04:20 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e1a0063344ada8ed441664af0f10f3f8e507014eeeeb1f145a78b67931ec74`  
		Last Modified: Tue, 13 Jun 2023 04:04:20 GMT  
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
$ docker pull couchdb@sha256:f230dbb6694e33b90b1c48782b20b1d71f7fb42c7b2099818d9c39782e60d380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchdb:3.2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:22fdd25d4eef5d0385853f6079463a23ca52bfcbd8d0dc7092dbd9797adf897d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89740540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a70f12d6bc5aa3e6c706277ff2c517d3bfcd6bc7dcdff28e99c7318d0c5f318`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:01:57 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jun 2023 04:01:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Jun 2023 04:02:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:02:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 13 Jun 2023 04:02:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jun 2023 04:02:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:02:32 GMT
ENV COUCHDB_VERSION=3.2.3
# Tue, 13 Jun 2023 04:02:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Jun 2023 04:02:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Jun 2023 04:02:45 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Jun 2023 04:02:45 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 13 Jun 2023 04:02:45 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 13 Jun 2023 04:02:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:02:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:02:46 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jun 2023 04:02:46 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Jun 2023 04:02:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fa5a08f48785d08765b7746d507926063e6ab14084ec52c45ad658c9900e2`  
		Last Modified: Tue, 13 Jun 2023 04:04:05 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effeea359db8a5b5241e47adb1070cec93345c3cc2011db12b74a56d6cec9151`  
		Last Modified: Tue, 13 Jun 2023 04:04:04 GMT  
		Size: 5.2 MB (5224468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b83a1bd5e8dd69f1172af3053ab31900973778718afe1abb82dd6d9cf4075a`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 610.3 KB (610265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d5ee803171a181293d9529fab444ccda628ce617e53d52acb7bbd34e1dbe3f`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 294.4 KB (294377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7bcd34bc103365c025d56bb91321fb3f909de9d2d8a3f86e2e42840dd5c967`  
		Last Modified: Tue, 13 Jun 2023 04:04:21 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c75aaa8226bcf8bd5abde0889b8926be9f496fb20715116927c48c9805a805`  
		Last Modified: Tue, 13 Jun 2023 04:04:25 GMT  
		Size: 52.2 MB (52186611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80869518eed6425bb6d52d653b7eafa53284cb556b9cc2d90b6ed8cd003dc773`  
		Last Modified: Tue, 13 Jun 2023 04:04:20 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c58c4494b65a294c8086500f80de0b3f1f88777384b4a0bf59f39d1374bb32`  
		Last Modified: Tue, 13 Jun 2023 04:04:20 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0453ee6f28c2aca08755a0990b9e7e89af4760c203915d0701b6e041498a0b1`  
		Last Modified: Tue, 13 Jun 2023 04:04:20 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e1a0063344ada8ed441664af0f10f3f8e507014eeeeb1f145a78b67931ec74`  
		Last Modified: Tue, 13 Jun 2023 04:04:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:7c43bfb5025b2b976efce61c4d4d9dbdcae94826d25958c8a760d6f820d893a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:40016f83b61df0ac945f1536e3a52e6ea2761a18326933513bbe358e5f787102
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90239977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b725f6b2513a8b4ec7c8b706aed6ac7a7166a5c833b1a23dd2f559310808110`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:01:57 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jun 2023 04:01:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Jun 2023 04:02:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:02:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 13 Jun 2023 04:02:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jun 2023 04:02:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:02:14 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 13 Jun 2023 04:02:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Jun 2023 04:02:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Jun 2023 04:02:27 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Jun 2023 04:02:27 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 13 Jun 2023 04:02:27 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 13 Jun 2023 04:02:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:02:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:02:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jun 2023 04:02:28 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Jun 2023 04:02:28 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fa5a08f48785d08765b7746d507926063e6ab14084ec52c45ad658c9900e2`  
		Last Modified: Tue, 13 Jun 2023 04:04:05 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effeea359db8a5b5241e47adb1070cec93345c3cc2011db12b74a56d6cec9151`  
		Last Modified: Tue, 13 Jun 2023 04:04:04 GMT  
		Size: 5.2 MB (5224468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b83a1bd5e8dd69f1172af3053ab31900973778718afe1abb82dd6d9cf4075a`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 610.3 KB (610265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d5ee803171a181293d9529fab444ccda628ce617e53d52acb7bbd34e1dbe3f`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 294.4 KB (294377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abff9bf83b2eee5ea095f234f197ed3bdc13ba5c1d9d27e366d814ca232560d3`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c0289451f671b5a57844126e484dc7f940b217bdd9badb059bda68d8764ab`  
		Last Modified: Tue, 13 Jun 2023 04:04:07 GMT  
		Size: 52.7 MB (52686042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7f7afef66f9db1812bc4358426b2221d5126baecd2715d01530d1fa9ea2e86`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d22413df733620c7d50f6db00f44e8dd5cd48ae5343fcbb767b482c4f0f9ad`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7983d64b4de2667bb5662734e159cb3529658b676c0c32a3e5906a4a26d27ce3`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf22f027705f7c7b494a7c2f2bd1d7b88f54297a0cd015536fdf35b915ace46`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:111bef69577b043b2f8af1fdd73ffa8e23898a6bc70b3f82fd3182ff1618236a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88684312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d016bedbaaaf56c355df33a499d3e134c6c17b26780b48454292818e0a91487f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:00:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 03:00:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 03:00:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:00:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 03:00:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 03:00:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:00:31 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 03:00:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 03:00:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 03:00:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 03:00:44 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 03:00:44 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 03:00:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 03:00:45 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:00:45 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 03:00:45 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 03:00:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc0d271896e1f31b2370d23711036a521e9acd3228114cc23f8fac55f387dbd`  
		Last Modified: Tue, 04 Jul 2023 03:02:19 GMT  
		Size: 3.4 KB (3432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8aac13251911c1284e2d4984341c6755bbe92e937e630352f4637e979958e68`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 5.2 MB (5209578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4219899a34e5a710d067929c59cf4cee7af11394da04941e8ec8dbdfa78c74c3`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 566.3 KB (566278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5043581719683361a4b86cda02be153567823f8d994de5929cf109fde6360729`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 294.3 KB (294323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6faedae003b0a46ef804c85e87d669f2ac496327ecfe31589fc2ef8cb795d9`  
		Last Modified: Tue, 04 Jul 2023 03:02:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bb64485bf61484d6294808283f6a71accee5b23965b220feea15e713cfe140`  
		Last Modified: Tue, 04 Jul 2023 03:02:20 GMT  
		Size: 52.5 MB (52543741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de90cc018497f0216ecab317a8a855961340c9bad495e67de724c2050657df6`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3f0725b25615db7255060c7d284ae18f16ad4b6eed961e19e8b6843453968`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9180ffcb545467f2e03ea97afe6c338090bda754a8660337cb26ba571028b18d`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0e1825ffd91b4338bf24761c3146c6d0a90ea00e5d87b2b89c62e7a2489e73`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:3eb5767e878cf69f2870e99b9c95b3be3dfcc0471c122389a9d0dfb659234883
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e065d599166a5dc0bcef7979716402c5fca0bbc616c07314ded86709614f51e1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:33 GMT
ADD file:37fa020aca7253d41d395ed529c38db73caaa4da098754836244552f65fa7d5d in / 
# Tue, 04 Jul 2023 01:18:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:47:38 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 04:47:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 04:48:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:48:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 04:48:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 04:48:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:48:46 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 04:48:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 04:49:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 04:49:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 04:49:23 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 04:49:24 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 04:49:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 04:49:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 04:49:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 04:49:28 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 04:49:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:147bb8b5828c99cd6b07d252d2987490463c142099eaa0815025685f8fa4f3d8`  
		Last Modified: Tue, 04 Jul 2023 01:25:40 GMT  
		Size: 35.3 MB (35291082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2701cbef8ba9fc49aabcd763212b84907356b9d67b68018587e12e7c54af3fee`  
		Last Modified: Tue, 04 Jul 2023 04:50:24 GMT  
		Size: 3.4 KB (3406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf807338a413416db46fc9e534bbe3265bc56baad887760486a0a54d25123b2`  
		Last Modified: Tue, 04 Jul 2023 04:50:24 GMT  
		Size: 6.0 MB (6044173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7409825b5d24fb99ad06438d83de58bf0ec20c4238d23657386eb390b56cf14a`  
		Last Modified: Tue, 04 Jul 2023 04:50:22 GMT  
		Size: 662.2 KB (662178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f62ee6bf18f44a92fdcdf0283d02bd2a4f1af5b1a8bd7e85621f45a95f8a04b`  
		Last Modified: Tue, 04 Jul 2023 04:50:21 GMT  
		Size: 294.4 KB (294369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716fa9059088e2aa7f1ea452b78d008438054cf553aec84db5f0b1c9d45af07d`  
		Last Modified: Tue, 04 Jul 2023 04:50:21 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646ca9755ca8690dde79876e5cc2575157aa6676d4f208ae1df21923cccd99cd`  
		Last Modified: Tue, 04 Jul 2023 04:50:28 GMT  
		Size: 53.7 MB (53662975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f92d3e00609286c22a6359ccd30574b19d50f9d6697f0a0ea5eab26ab12bc76`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339e7380fa4b617f06e977822abe3be70818da7d6d685880896b0eae0a1515be`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080782760cb6436e3664eb4f4e11c5008ca48beefe7641cd9296bcb2b0596458`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0412cece6d0a349aed06c4894e09a68bcee9300a4e7f88f629d13647544596e6`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:0bcccda85f5c60188048ec57dd9459e296f769c5ad766371be2f057c1cb31202
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86992279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b56bdcd62fdc551f2173e4ad2ca3ca6490f7f1acec77826451b8fabe35fa900`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:32:44 GMT
ADD file:799c0afa70fa3bf4bb7804964481cba79e80aa3fad5c7a25beadde206ed6a8ff in / 
# Tue, 04 Jul 2023 01:32:46 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 02:31:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 02:32:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 02:32:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:32:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 02:32:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 02:32:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:32:15 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 02:32:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 02:32:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 02:32:33 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 02:32:33 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 02:32:33 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 02:32:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 02:32:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 02:32:34 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 02:32:34 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 02:32:34 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bbee891481f2623da9c7d37a49947926519c858c2b06773370a6189440d4b4de`  
		Last Modified: Tue, 04 Jul 2023 01:37:37 GMT  
		Size: 29.7 MB (29652540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ca3d8ad5e25fe241e125f8bbbe38fc1732c37f3caa96c1ef02a7f489a5aae6`  
		Last Modified: Tue, 04 Jul 2023 02:32:52 GMT  
		Size: 3.4 KB (3432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60572b3f976bbdc302097dea095b6bea87f04aaa5902a11eb46130547c2f0154`  
		Last Modified: Tue, 04 Jul 2023 02:32:52 GMT  
		Size: 5.1 MB (5110438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056d956cd8463eed79cf7d437deb772330ad221345369e72ac6295e5713ca302`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 573.0 KB (573005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd772a2ca35e7648d7321fb6b0eb780c57418a1902a7805f6217c3e30e57893`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 294.4 KB (294392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a421ebc7a36d0af94ef7d446133f4686c9ef5a16e88004505d10bbf259c14db6`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9f6c295417043fc04a54083419e1707a71800e53f2d2643c9a2085f368fb87`  
		Last Modified: Tue, 04 Jul 2023 02:32:55 GMT  
		Size: 51.4 MB (51354464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83bfa157ad1e19b57a9df85aa0579c82163bee844e2c05b20095043b063b28`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235315086a5d8e7a181854f2e016c9da2abc0c2f9a30e583979f1b0d4326ee86`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dbfd2547b3b689e42acaaa81c5eb50c74f032cf42d0e18e33a29f8253ec632`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dac4cd592579b8351c686a4fe857238634639bd8f332711ec4d2545d6a95b71`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3.2`

```console
$ docker pull couchdb@sha256:7c43bfb5025b2b976efce61c4d4d9dbdcae94826d25958c8a760d6f820d893a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3.3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:40016f83b61df0ac945f1536e3a52e6ea2761a18326933513bbe358e5f787102
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90239977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b725f6b2513a8b4ec7c8b706aed6ac7a7166a5c833b1a23dd2f559310808110`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:01:57 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jun 2023 04:01:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Jun 2023 04:02:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:02:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 13 Jun 2023 04:02:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jun 2023 04:02:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:02:14 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 13 Jun 2023 04:02:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Jun 2023 04:02:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Jun 2023 04:02:27 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Jun 2023 04:02:27 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 13 Jun 2023 04:02:27 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 13 Jun 2023 04:02:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:02:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:02:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jun 2023 04:02:28 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Jun 2023 04:02:28 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fa5a08f48785d08765b7746d507926063e6ab14084ec52c45ad658c9900e2`  
		Last Modified: Tue, 13 Jun 2023 04:04:05 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effeea359db8a5b5241e47adb1070cec93345c3cc2011db12b74a56d6cec9151`  
		Last Modified: Tue, 13 Jun 2023 04:04:04 GMT  
		Size: 5.2 MB (5224468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b83a1bd5e8dd69f1172af3053ab31900973778718afe1abb82dd6d9cf4075a`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 610.3 KB (610265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d5ee803171a181293d9529fab444ccda628ce617e53d52acb7bbd34e1dbe3f`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 294.4 KB (294377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abff9bf83b2eee5ea095f234f197ed3bdc13ba5c1d9d27e366d814ca232560d3`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c0289451f671b5a57844126e484dc7f940b217bdd9badb059bda68d8764ab`  
		Last Modified: Tue, 13 Jun 2023 04:04:07 GMT  
		Size: 52.7 MB (52686042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7f7afef66f9db1812bc4358426b2221d5126baecd2715d01530d1fa9ea2e86`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d22413df733620c7d50f6db00f44e8dd5cd48ae5343fcbb767b482c4f0f9ad`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7983d64b4de2667bb5662734e159cb3529658b676c0c32a3e5906a4a26d27ce3`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf22f027705f7c7b494a7c2f2bd1d7b88f54297a0cd015536fdf35b915ace46`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:111bef69577b043b2f8af1fdd73ffa8e23898a6bc70b3f82fd3182ff1618236a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88684312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d016bedbaaaf56c355df33a499d3e134c6c17b26780b48454292818e0a91487f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:00:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 03:00:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 03:00:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:00:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 03:00:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 03:00:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:00:31 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 03:00:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 03:00:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 03:00:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 03:00:44 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 03:00:44 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 03:00:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 03:00:45 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:00:45 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 03:00:45 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 03:00:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc0d271896e1f31b2370d23711036a521e9acd3228114cc23f8fac55f387dbd`  
		Last Modified: Tue, 04 Jul 2023 03:02:19 GMT  
		Size: 3.4 KB (3432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8aac13251911c1284e2d4984341c6755bbe92e937e630352f4637e979958e68`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 5.2 MB (5209578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4219899a34e5a710d067929c59cf4cee7af11394da04941e8ec8dbdfa78c74c3`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 566.3 KB (566278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5043581719683361a4b86cda02be153567823f8d994de5929cf109fde6360729`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 294.3 KB (294323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6faedae003b0a46ef804c85e87d669f2ac496327ecfe31589fc2ef8cb795d9`  
		Last Modified: Tue, 04 Jul 2023 03:02:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bb64485bf61484d6294808283f6a71accee5b23965b220feea15e713cfe140`  
		Last Modified: Tue, 04 Jul 2023 03:02:20 GMT  
		Size: 52.5 MB (52543741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de90cc018497f0216ecab317a8a855961340c9bad495e67de724c2050657df6`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3f0725b25615db7255060c7d284ae18f16ad4b6eed961e19e8b6843453968`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9180ffcb545467f2e03ea97afe6c338090bda754a8660337cb26ba571028b18d`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0e1825ffd91b4338bf24761c3146c6d0a90ea00e5d87b2b89c62e7a2489e73`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:3eb5767e878cf69f2870e99b9c95b3be3dfcc0471c122389a9d0dfb659234883
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e065d599166a5dc0bcef7979716402c5fca0bbc616c07314ded86709614f51e1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:33 GMT
ADD file:37fa020aca7253d41d395ed529c38db73caaa4da098754836244552f65fa7d5d in / 
# Tue, 04 Jul 2023 01:18:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:47:38 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 04:47:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 04:48:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:48:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 04:48:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 04:48:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:48:46 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 04:48:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 04:49:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 04:49:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 04:49:23 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 04:49:24 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 04:49:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 04:49:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 04:49:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 04:49:28 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 04:49:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:147bb8b5828c99cd6b07d252d2987490463c142099eaa0815025685f8fa4f3d8`  
		Last Modified: Tue, 04 Jul 2023 01:25:40 GMT  
		Size: 35.3 MB (35291082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2701cbef8ba9fc49aabcd763212b84907356b9d67b68018587e12e7c54af3fee`  
		Last Modified: Tue, 04 Jul 2023 04:50:24 GMT  
		Size: 3.4 KB (3406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf807338a413416db46fc9e534bbe3265bc56baad887760486a0a54d25123b2`  
		Last Modified: Tue, 04 Jul 2023 04:50:24 GMT  
		Size: 6.0 MB (6044173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7409825b5d24fb99ad06438d83de58bf0ec20c4238d23657386eb390b56cf14a`  
		Last Modified: Tue, 04 Jul 2023 04:50:22 GMT  
		Size: 662.2 KB (662178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f62ee6bf18f44a92fdcdf0283d02bd2a4f1af5b1a8bd7e85621f45a95f8a04b`  
		Last Modified: Tue, 04 Jul 2023 04:50:21 GMT  
		Size: 294.4 KB (294369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716fa9059088e2aa7f1ea452b78d008438054cf553aec84db5f0b1c9d45af07d`  
		Last Modified: Tue, 04 Jul 2023 04:50:21 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646ca9755ca8690dde79876e5cc2575157aa6676d4f208ae1df21923cccd99cd`  
		Last Modified: Tue, 04 Jul 2023 04:50:28 GMT  
		Size: 53.7 MB (53662975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f92d3e00609286c22a6359ccd30574b19d50f9d6697f0a0ea5eab26ab12bc76`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339e7380fa4b617f06e977822abe3be70818da7d6d685880896b0eae0a1515be`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080782760cb6436e3664eb4f4e11c5008ca48beefe7641cd9296bcb2b0596458`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0412cece6d0a349aed06c4894e09a68bcee9300a4e7f88f629d13647544596e6`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; s390x

```console
$ docker pull couchdb@sha256:0bcccda85f5c60188048ec57dd9459e296f769c5ad766371be2f057c1cb31202
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86992279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b56bdcd62fdc551f2173e4ad2ca3ca6490f7f1acec77826451b8fabe35fa900`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:32:44 GMT
ADD file:799c0afa70fa3bf4bb7804964481cba79e80aa3fad5c7a25beadde206ed6a8ff in / 
# Tue, 04 Jul 2023 01:32:46 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 02:31:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 02:32:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 02:32:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:32:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 02:32:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 02:32:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:32:15 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 02:32:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 02:32:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 02:32:33 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 02:32:33 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 02:32:33 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 02:32:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 02:32:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 02:32:34 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 02:32:34 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 02:32:34 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bbee891481f2623da9c7d37a49947926519c858c2b06773370a6189440d4b4de`  
		Last Modified: Tue, 04 Jul 2023 01:37:37 GMT  
		Size: 29.7 MB (29652540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ca3d8ad5e25fe241e125f8bbbe38fc1732c37f3caa96c1ef02a7f489a5aae6`  
		Last Modified: Tue, 04 Jul 2023 02:32:52 GMT  
		Size: 3.4 KB (3432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60572b3f976bbdc302097dea095b6bea87f04aaa5902a11eb46130547c2f0154`  
		Last Modified: Tue, 04 Jul 2023 02:32:52 GMT  
		Size: 5.1 MB (5110438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056d956cd8463eed79cf7d437deb772330ad221345369e72ac6295e5713ca302`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 573.0 KB (573005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd772a2ca35e7648d7321fb6b0eb780c57418a1902a7805f6217c3e30e57893`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 294.4 KB (294392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a421ebc7a36d0af94ef7d446133f4686c9ef5a16e88004505d10bbf259c14db6`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9f6c295417043fc04a54083419e1707a71800e53f2d2643c9a2085f368fb87`  
		Last Modified: Tue, 04 Jul 2023 02:32:55 GMT  
		Size: 51.4 MB (51354464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83bfa157ad1e19b57a9df85aa0579c82163bee844e2c05b20095043b063b28`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235315086a5d8e7a181854f2e016c9da2abc0c2f9a30e583979f1b0d4326ee86`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dbfd2547b3b689e42acaaa81c5eb50c74f032cf42d0e18e33a29f8253ec632`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dac4cd592579b8351c686a4fe857238634639bd8f332711ec4d2545d6a95b71`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:7c43bfb5025b2b976efce61c4d4d9dbdcae94826d25958c8a760d6f820d893a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:40016f83b61df0ac945f1536e3a52e6ea2761a18326933513bbe358e5f787102
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90239977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b725f6b2513a8b4ec7c8b706aed6ac7a7166a5c833b1a23dd2f559310808110`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:01:57 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jun 2023 04:01:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Jun 2023 04:02:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:02:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 13 Jun 2023 04:02:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jun 2023 04:02:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:02:14 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 13 Jun 2023 04:02:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Jun 2023 04:02:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Jun 2023 04:02:27 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Jun 2023 04:02:27 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 13 Jun 2023 04:02:27 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 13 Jun 2023 04:02:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:02:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:02:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jun 2023 04:02:28 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Jun 2023 04:02:28 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fa5a08f48785d08765b7746d507926063e6ab14084ec52c45ad658c9900e2`  
		Last Modified: Tue, 13 Jun 2023 04:04:05 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effeea359db8a5b5241e47adb1070cec93345c3cc2011db12b74a56d6cec9151`  
		Last Modified: Tue, 13 Jun 2023 04:04:04 GMT  
		Size: 5.2 MB (5224468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b83a1bd5e8dd69f1172af3053ab31900973778718afe1abb82dd6d9cf4075a`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 610.3 KB (610265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d5ee803171a181293d9529fab444ccda628ce617e53d52acb7bbd34e1dbe3f`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 294.4 KB (294377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abff9bf83b2eee5ea095f234f197ed3bdc13ba5c1d9d27e366d814ca232560d3`  
		Last Modified: Tue, 13 Jun 2023 04:04:03 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c0289451f671b5a57844126e484dc7f940b217bdd9badb059bda68d8764ab`  
		Last Modified: Tue, 13 Jun 2023 04:04:07 GMT  
		Size: 52.7 MB (52686042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7f7afef66f9db1812bc4358426b2221d5126baecd2715d01530d1fa9ea2e86`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d22413df733620c7d50f6db00f44e8dd5cd48ae5343fcbb767b482c4f0f9ad`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7983d64b4de2667bb5662734e159cb3529658b676c0c32a3e5906a4a26d27ce3`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf22f027705f7c7b494a7c2f2bd1d7b88f54297a0cd015536fdf35b915ace46`  
		Last Modified: Tue, 13 Jun 2023 04:04:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:111bef69577b043b2f8af1fdd73ffa8e23898a6bc70b3f82fd3182ff1618236a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88684312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d016bedbaaaf56c355df33a499d3e134c6c17b26780b48454292818e0a91487f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:00:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 03:00:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 03:00:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:00:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 03:00:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 03:00:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:00:31 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 03:00:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 03:00:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 03:00:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 03:00:44 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 03:00:44 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 03:00:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 03:00:45 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:00:45 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 03:00:45 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 03:00:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc0d271896e1f31b2370d23711036a521e9acd3228114cc23f8fac55f387dbd`  
		Last Modified: Tue, 04 Jul 2023 03:02:19 GMT  
		Size: 3.4 KB (3432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8aac13251911c1284e2d4984341c6755bbe92e937e630352f4637e979958e68`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 5.2 MB (5209578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4219899a34e5a710d067929c59cf4cee7af11394da04941e8ec8dbdfa78c74c3`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 566.3 KB (566278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5043581719683361a4b86cda02be153567823f8d994de5929cf109fde6360729`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 294.3 KB (294323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6faedae003b0a46ef804c85e87d669f2ac496327ecfe31589fc2ef8cb795d9`  
		Last Modified: Tue, 04 Jul 2023 03:02:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bb64485bf61484d6294808283f6a71accee5b23965b220feea15e713cfe140`  
		Last Modified: Tue, 04 Jul 2023 03:02:20 GMT  
		Size: 52.5 MB (52543741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de90cc018497f0216ecab317a8a855961340c9bad495e67de724c2050657df6`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3f0725b25615db7255060c7d284ae18f16ad4b6eed961e19e8b6843453968`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9180ffcb545467f2e03ea97afe6c338090bda754a8660337cb26ba571028b18d`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0e1825ffd91b4338bf24761c3146c6d0a90ea00e5d87b2b89c62e7a2489e73`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:3eb5767e878cf69f2870e99b9c95b3be3dfcc0471c122389a9d0dfb659234883
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e065d599166a5dc0bcef7979716402c5fca0bbc616c07314ded86709614f51e1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:33 GMT
ADD file:37fa020aca7253d41d395ed529c38db73caaa4da098754836244552f65fa7d5d in / 
# Tue, 04 Jul 2023 01:18:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:47:38 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 04:47:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 04:48:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:48:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 04:48:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 04:48:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:48:46 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 04:48:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 04:49:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 04:49:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 04:49:23 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 04:49:24 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 04:49:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 04:49:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 04:49:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 04:49:28 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 04:49:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:147bb8b5828c99cd6b07d252d2987490463c142099eaa0815025685f8fa4f3d8`  
		Last Modified: Tue, 04 Jul 2023 01:25:40 GMT  
		Size: 35.3 MB (35291082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2701cbef8ba9fc49aabcd763212b84907356b9d67b68018587e12e7c54af3fee`  
		Last Modified: Tue, 04 Jul 2023 04:50:24 GMT  
		Size: 3.4 KB (3406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf807338a413416db46fc9e534bbe3265bc56baad887760486a0a54d25123b2`  
		Last Modified: Tue, 04 Jul 2023 04:50:24 GMT  
		Size: 6.0 MB (6044173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7409825b5d24fb99ad06438d83de58bf0ec20c4238d23657386eb390b56cf14a`  
		Last Modified: Tue, 04 Jul 2023 04:50:22 GMT  
		Size: 662.2 KB (662178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f62ee6bf18f44a92fdcdf0283d02bd2a4f1af5b1a8bd7e85621f45a95f8a04b`  
		Last Modified: Tue, 04 Jul 2023 04:50:21 GMT  
		Size: 294.4 KB (294369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716fa9059088e2aa7f1ea452b78d008438054cf553aec84db5f0b1c9d45af07d`  
		Last Modified: Tue, 04 Jul 2023 04:50:21 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646ca9755ca8690dde79876e5cc2575157aa6676d4f208ae1df21923cccd99cd`  
		Last Modified: Tue, 04 Jul 2023 04:50:28 GMT  
		Size: 53.7 MB (53662975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f92d3e00609286c22a6359ccd30574b19d50f9d6697f0a0ea5eab26ab12bc76`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339e7380fa4b617f06e977822abe3be70818da7d6d685880896b0eae0a1515be`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080782760cb6436e3664eb4f4e11c5008ca48beefe7641cd9296bcb2b0596458`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0412cece6d0a349aed06c4894e09a68bcee9300a4e7f88f629d13647544596e6`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:0bcccda85f5c60188048ec57dd9459e296f769c5ad766371be2f057c1cb31202
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86992279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b56bdcd62fdc551f2173e4ad2ca3ca6490f7f1acec77826451b8fabe35fa900`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:32:44 GMT
ADD file:799c0afa70fa3bf4bb7804964481cba79e80aa3fad5c7a25beadde206ed6a8ff in / 
# Tue, 04 Jul 2023 01:32:46 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 02:31:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 02:32:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 02:32:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:32:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 02:32:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 02:32:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:32:15 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 02:32:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 02:32:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 02:32:33 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 02:32:33 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 02:32:33 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 02:32:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 02:32:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 02:32:34 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 02:32:34 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 02:32:34 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bbee891481f2623da9c7d37a49947926519c858c2b06773370a6189440d4b4de`  
		Last Modified: Tue, 04 Jul 2023 01:37:37 GMT  
		Size: 29.7 MB (29652540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ca3d8ad5e25fe241e125f8bbbe38fc1732c37f3caa96c1ef02a7f489a5aae6`  
		Last Modified: Tue, 04 Jul 2023 02:32:52 GMT  
		Size: 3.4 KB (3432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60572b3f976bbdc302097dea095b6bea87f04aaa5902a11eb46130547c2f0154`  
		Last Modified: Tue, 04 Jul 2023 02:32:52 GMT  
		Size: 5.1 MB (5110438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056d956cd8463eed79cf7d437deb772330ad221345369e72ac6295e5713ca302`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 573.0 KB (573005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd772a2ca35e7648d7321fb6b0eb780c57418a1902a7805f6217c3e30e57893`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 294.4 KB (294392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a421ebc7a36d0af94ef7d446133f4686c9ef5a16e88004505d10bbf259c14db6`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9f6c295417043fc04a54083419e1707a71800e53f2d2643c9a2085f368fb87`  
		Last Modified: Tue, 04 Jul 2023 02:32:55 GMT  
		Size: 51.4 MB (51354464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83bfa157ad1e19b57a9df85aa0579c82163bee844e2c05b20095043b063b28`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235315086a5d8e7a181854f2e016c9da2abc0c2f9a30e583979f1b0d4326ee86`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dbfd2547b3b689e42acaaa81c5eb50c74f032cf42d0e18e33a29f8253ec632`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dac4cd592579b8351c686a4fe857238634639bd8f332711ec4d2545d6a95b71`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
