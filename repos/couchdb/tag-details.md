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
$ docker pull couchdb@sha256:b1e4e460f38981434294200e8dcba370627a3ac74811bf08e69be9c65ff6c5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:6deabbe84258c2151a91a3a82e6d127b2bcce1bb6b8659be675ca4005c795acc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84590179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b72c4b3a9488f8358040dab8d2a1945460a6a17f63aa229e34e6831fe43f53`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:29 GMT
ADD file:20e7ad6bec617357895302b08431eb3430cce3113bdf0a8ff9827115f858d313 in / 
# Thu, 27 Jul 2023 23:25:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:54:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 00:54:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 00:54:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Fri, 28 Jul 2023 00:54:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 00:55:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:55:24 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Fri, 28 Jul 2023 00:55:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 00:55:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 00:55:43 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 00:55:43 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 00:55:43 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Fri, 28 Jul 2023 00:55:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 00:55:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 00:55:44 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 00:55:44 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 00:55:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3240fe174df9a5a4923c4b52f1d887dd1ad1a9ee69245c1fb867f399167584dd`  
		Last Modified: Thu, 27 Jul 2023 23:30:49 GMT  
		Size: 27.2 MB (27187431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d89b65f2dc832c2f7c348d9f12cf4b9e110e543efc4813b9f870c494429957`  
		Last Modified: Fri, 28 Jul 2023 00:56:38 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef28276cebf24c8afba60bbb3445613b21460493b508d02d292c0fdd8b18f44`  
		Last Modified: Fri, 28 Jul 2023 00:56:37 GMT  
		Size: 6.7 MB (6704542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c905d0380fb2306d3e35170fbbc2bc64a4128012ea5e12393ed06dff6c5ce8b6`  
		Last Modified: Fri, 28 Jul 2023 00:56:36 GMT  
		Size: 1.3 MB (1259891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7672fd27b19b3a699dcc283d34f31cc9ef507fb4b8905d4d8ab9528e4ffbf8e3`  
		Last Modified: Fri, 28 Jul 2023 00:56:36 GMT  
		Size: 294.6 KB (294631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc9781684c058f6264128d586906d723e7969eb84e485a50c109c9df1973a30`  
		Last Modified: Fri, 28 Jul 2023 00:56:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9869b39f486c4ca6de8c713784e3c26bd689c63fb1c2417b420234c072a4e12e`  
		Last Modified: Fri, 28 Jul 2023 00:56:54 GMT  
		Size: 49.1 MB (49136664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840995d1ded1168d5abac83569f50653b98a44cb3bc3f81f02bdf77708ddef05`  
		Last Modified: Fri, 28 Jul 2023 00:56:48 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3f31d9c327854d02f8a037f4c6af150724e0f819fa2a2583856c6affbe5fc6`  
		Last Modified: Fri, 28 Jul 2023 00:56:48 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7955f1dacbb3649aba741a5cb06aa8ecf9f8e906d4cc0c41255e803b54803dc6`  
		Last Modified: Fri, 28 Jul 2023 00:56:48 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fdd11a7c5ae8e5a94524653edad7bf72a6b28465d450065fe16a236c989446`  
		Last Modified: Fri, 28 Jul 2023 00:56:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:513bf9edd59d4359077c696a6b8abd5e3e6a7024f32506ed77442050407e1cc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73041146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550820b306975bae3f2b4b30c8b2735bea2192cb1a2a641973ebc3ea30a22e38`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:29 GMT
ADD file:ff126e7e4d046d566ea77f196c35d57f2d755b935cda365c5e3bba5f4d18ebf2 in / 
# Thu, 27 Jul 2023 23:43:29 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:55:21 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 01:55:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 01:55:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:55:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Fri, 28 Jul 2023 01:55:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 01:55:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:55:55 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Fri, 28 Jul 2023 01:55:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 01:56:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 01:56:07 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 01:56:07 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 01:56:07 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Fri, 28 Jul 2023 01:56:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 01:56:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:56:08 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 01:56:08 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 01:56:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d71ee974c4e69baa159b185ea2bebfc5b3d814a08167ed09a79596f4707642c0`  
		Last Modified: Thu, 27 Jul 2023 23:47:51 GMT  
		Size: 26.0 MB (25967808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5ed2f5251688c7911c07a3afc2d8fe296d7b2cc6100dbfa9b8b41ef34f4cf3`  
		Last Modified: Fri, 28 Jul 2023 01:56:45 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1520a23e0d6c339c2f929d97df639e69bcb50d375b2021b489e877ae74969158`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 6.6 MB (6577647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab60e0e7bbd22b9de27de87e8887415f0c42dca5e711d4a1ce37301deb2537b`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 1.2 MB (1164841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2216a631ec9538e028e3e45ccb598a9b1b46a8fa0d90ce038781a5435b473aff`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 294.4 KB (294427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397c889b1e71f3f2791e720c8049dec9563836900aa928da280be62b052125cf`  
		Last Modified: Fri, 28 Jul 2023 01:56:55 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98266f80b21ef7f287aae120481946c13abeda9e287dc1713653a336d48902bc`  
		Last Modified: Fri, 28 Jul 2023 01:56:56 GMT  
		Size: 39.0 MB (39029384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0b13769ed8dcc801b8f2b8af2c9b3d36a531529fcafac726b94c9bfa9c0cc5`  
		Last Modified: Fri, 28 Jul 2023 01:56:53 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96146de7ecef122317c2c68449de955cca40e9f2a359919afbb59887609ecd34`  
		Last Modified: Fri, 28 Jul 2023 01:56:53 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a653713b2bc33337e7d82f02e0e82af127d1a09ac61dbb3182fabdc60329aa16`  
		Last Modified: Fri, 28 Jul 2023 01:56:53 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f80844b21c0dfb1fd717a0126298e80882723c7bca0c5529c7df48c419ed86`  
		Last Modified: Fri, 28 Jul 2023 01:56:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:b1e4e460f38981434294200e8dcba370627a3ac74811bf08e69be9c65ff6c5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:6deabbe84258c2151a91a3a82e6d127b2bcce1bb6b8659be675ca4005c795acc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84590179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b72c4b3a9488f8358040dab8d2a1945460a6a17f63aa229e34e6831fe43f53`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:29 GMT
ADD file:20e7ad6bec617357895302b08431eb3430cce3113bdf0a8ff9827115f858d313 in / 
# Thu, 27 Jul 2023 23:25:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:54:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 00:54:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 00:54:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Fri, 28 Jul 2023 00:54:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 00:55:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:55:24 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Fri, 28 Jul 2023 00:55:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 00:55:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 00:55:43 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 00:55:43 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 00:55:43 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Fri, 28 Jul 2023 00:55:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 00:55:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 00:55:44 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 00:55:44 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 00:55:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3240fe174df9a5a4923c4b52f1d887dd1ad1a9ee69245c1fb867f399167584dd`  
		Last Modified: Thu, 27 Jul 2023 23:30:49 GMT  
		Size: 27.2 MB (27187431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d89b65f2dc832c2f7c348d9f12cf4b9e110e543efc4813b9f870c494429957`  
		Last Modified: Fri, 28 Jul 2023 00:56:38 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef28276cebf24c8afba60bbb3445613b21460493b508d02d292c0fdd8b18f44`  
		Last Modified: Fri, 28 Jul 2023 00:56:37 GMT  
		Size: 6.7 MB (6704542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c905d0380fb2306d3e35170fbbc2bc64a4128012ea5e12393ed06dff6c5ce8b6`  
		Last Modified: Fri, 28 Jul 2023 00:56:36 GMT  
		Size: 1.3 MB (1259891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7672fd27b19b3a699dcc283d34f31cc9ef507fb4b8905d4d8ab9528e4ffbf8e3`  
		Last Modified: Fri, 28 Jul 2023 00:56:36 GMT  
		Size: 294.6 KB (294631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc9781684c058f6264128d586906d723e7969eb84e485a50c109c9df1973a30`  
		Last Modified: Fri, 28 Jul 2023 00:56:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9869b39f486c4ca6de8c713784e3c26bd689c63fb1c2417b420234c072a4e12e`  
		Last Modified: Fri, 28 Jul 2023 00:56:54 GMT  
		Size: 49.1 MB (49136664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840995d1ded1168d5abac83569f50653b98a44cb3bc3f81f02bdf77708ddef05`  
		Last Modified: Fri, 28 Jul 2023 00:56:48 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3f31d9c327854d02f8a037f4c6af150724e0f819fa2a2583856c6affbe5fc6`  
		Last Modified: Fri, 28 Jul 2023 00:56:48 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7955f1dacbb3649aba741a5cb06aa8ecf9f8e906d4cc0c41255e803b54803dc6`  
		Last Modified: Fri, 28 Jul 2023 00:56:48 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fdd11a7c5ae8e5a94524653edad7bf72a6b28465d450065fe16a236c989446`  
		Last Modified: Fri, 28 Jul 2023 00:56:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:513bf9edd59d4359077c696a6b8abd5e3e6a7024f32506ed77442050407e1cc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73041146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550820b306975bae3f2b4b30c8b2735bea2192cb1a2a641973ebc3ea30a22e38`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:29 GMT
ADD file:ff126e7e4d046d566ea77f196c35d57f2d755b935cda365c5e3bba5f4d18ebf2 in / 
# Thu, 27 Jul 2023 23:43:29 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:55:21 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 01:55:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 01:55:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:55:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Fri, 28 Jul 2023 01:55:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 01:55:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:55:55 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Fri, 28 Jul 2023 01:55:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 01:56:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 01:56:07 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 01:56:07 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 01:56:07 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Fri, 28 Jul 2023 01:56:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 01:56:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:56:08 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 01:56:08 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 01:56:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d71ee974c4e69baa159b185ea2bebfc5b3d814a08167ed09a79596f4707642c0`  
		Last Modified: Thu, 27 Jul 2023 23:47:51 GMT  
		Size: 26.0 MB (25967808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5ed2f5251688c7911c07a3afc2d8fe296d7b2cc6100dbfa9b8b41ef34f4cf3`  
		Last Modified: Fri, 28 Jul 2023 01:56:45 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1520a23e0d6c339c2f929d97df639e69bcb50d375b2021b489e877ae74969158`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 6.6 MB (6577647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab60e0e7bbd22b9de27de87e8887415f0c42dca5e711d4a1ce37301deb2537b`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 1.2 MB (1164841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2216a631ec9538e028e3e45ccb598a9b1b46a8fa0d90ce038781a5435b473aff`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 294.4 KB (294427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397c889b1e71f3f2791e720c8049dec9563836900aa928da280be62b052125cf`  
		Last Modified: Fri, 28 Jul 2023 01:56:55 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98266f80b21ef7f287aae120481946c13abeda9e287dc1713653a336d48902bc`  
		Last Modified: Fri, 28 Jul 2023 01:56:56 GMT  
		Size: 39.0 MB (39029384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0b13769ed8dcc801b8f2b8af2c9b3d36a531529fcafac726b94c9bfa9c0cc5`  
		Last Modified: Fri, 28 Jul 2023 01:56:53 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96146de7ecef122317c2c68449de955cca40e9f2a359919afbb59887609ecd34`  
		Last Modified: Fri, 28 Jul 2023 01:56:53 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a653713b2bc33337e7d82f02e0e82af127d1a09ac61dbb3182fabdc60329aa16`  
		Last Modified: Fri, 28 Jul 2023 01:56:53 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f80844b21c0dfb1fd717a0126298e80882723c7bca0c5529c7df48c419ed86`  
		Last Modified: Fri, 28 Jul 2023 01:56:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:b1e4e460f38981434294200e8dcba370627a3ac74811bf08e69be9c65ff6c5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:6deabbe84258c2151a91a3a82e6d127b2bcce1bb6b8659be675ca4005c795acc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84590179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b72c4b3a9488f8358040dab8d2a1945460a6a17f63aa229e34e6831fe43f53`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:29 GMT
ADD file:20e7ad6bec617357895302b08431eb3430cce3113bdf0a8ff9827115f858d313 in / 
# Thu, 27 Jul 2023 23:25:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:54:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 00:54:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 00:54:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Fri, 28 Jul 2023 00:54:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 00:55:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:55:24 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Fri, 28 Jul 2023 00:55:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 00:55:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 00:55:43 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 00:55:43 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 00:55:43 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Fri, 28 Jul 2023 00:55:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 00:55:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 00:55:44 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 00:55:44 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 00:55:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3240fe174df9a5a4923c4b52f1d887dd1ad1a9ee69245c1fb867f399167584dd`  
		Last Modified: Thu, 27 Jul 2023 23:30:49 GMT  
		Size: 27.2 MB (27187431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d89b65f2dc832c2f7c348d9f12cf4b9e110e543efc4813b9f870c494429957`  
		Last Modified: Fri, 28 Jul 2023 00:56:38 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef28276cebf24c8afba60bbb3445613b21460493b508d02d292c0fdd8b18f44`  
		Last Modified: Fri, 28 Jul 2023 00:56:37 GMT  
		Size: 6.7 MB (6704542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c905d0380fb2306d3e35170fbbc2bc64a4128012ea5e12393ed06dff6c5ce8b6`  
		Last Modified: Fri, 28 Jul 2023 00:56:36 GMT  
		Size: 1.3 MB (1259891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7672fd27b19b3a699dcc283d34f31cc9ef507fb4b8905d4d8ab9528e4ffbf8e3`  
		Last Modified: Fri, 28 Jul 2023 00:56:36 GMT  
		Size: 294.6 KB (294631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc9781684c058f6264128d586906d723e7969eb84e485a50c109c9df1973a30`  
		Last Modified: Fri, 28 Jul 2023 00:56:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9869b39f486c4ca6de8c713784e3c26bd689c63fb1c2417b420234c072a4e12e`  
		Last Modified: Fri, 28 Jul 2023 00:56:54 GMT  
		Size: 49.1 MB (49136664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840995d1ded1168d5abac83569f50653b98a44cb3bc3f81f02bdf77708ddef05`  
		Last Modified: Fri, 28 Jul 2023 00:56:48 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3f31d9c327854d02f8a037f4c6af150724e0f819fa2a2583856c6affbe5fc6`  
		Last Modified: Fri, 28 Jul 2023 00:56:48 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7955f1dacbb3649aba741a5cb06aa8ecf9f8e906d4cc0c41255e803b54803dc6`  
		Last Modified: Fri, 28 Jul 2023 00:56:48 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fdd11a7c5ae8e5a94524653edad7bf72a6b28465d450065fe16a236c989446`  
		Last Modified: Fri, 28 Jul 2023 00:56:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:513bf9edd59d4359077c696a6b8abd5e3e6a7024f32506ed77442050407e1cc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73041146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550820b306975bae3f2b4b30c8b2735bea2192cb1a2a641973ebc3ea30a22e38`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:29 GMT
ADD file:ff126e7e4d046d566ea77f196c35d57f2d755b935cda365c5e3bba5f4d18ebf2 in / 
# Thu, 27 Jul 2023 23:43:29 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:55:21 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 01:55:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 01:55:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:55:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Fri, 28 Jul 2023 01:55:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 01:55:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:55:55 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Fri, 28 Jul 2023 01:55:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 01:56:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 01:56:07 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 01:56:07 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 01:56:07 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Fri, 28 Jul 2023 01:56:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 01:56:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:56:08 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 01:56:08 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 01:56:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d71ee974c4e69baa159b185ea2bebfc5b3d814a08167ed09a79596f4707642c0`  
		Last Modified: Thu, 27 Jul 2023 23:47:51 GMT  
		Size: 26.0 MB (25967808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5ed2f5251688c7911c07a3afc2d8fe296d7b2cc6100dbfa9b8b41ef34f4cf3`  
		Last Modified: Fri, 28 Jul 2023 01:56:45 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1520a23e0d6c339c2f929d97df639e69bcb50d375b2021b489e877ae74969158`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 6.6 MB (6577647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab60e0e7bbd22b9de27de87e8887415f0c42dca5e711d4a1ce37301deb2537b`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 1.2 MB (1164841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2216a631ec9538e028e3e45ccb598a9b1b46a8fa0d90ce038781a5435b473aff`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 294.4 KB (294427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397c889b1e71f3f2791e720c8049dec9563836900aa928da280be62b052125cf`  
		Last Modified: Fri, 28 Jul 2023 01:56:55 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98266f80b21ef7f287aae120481946c13abeda9e287dc1713653a336d48902bc`  
		Last Modified: Fri, 28 Jul 2023 01:56:56 GMT  
		Size: 39.0 MB (39029384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0b13769ed8dcc801b8f2b8af2c9b3d36a531529fcafac726b94c9bfa9c0cc5`  
		Last Modified: Fri, 28 Jul 2023 01:56:53 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96146de7ecef122317c2c68449de955cca40e9f2a359919afbb59887609ecd34`  
		Last Modified: Fri, 28 Jul 2023 01:56:53 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a653713b2bc33337e7d82f02e0e82af127d1a09ac61dbb3182fabdc60329aa16`  
		Last Modified: Fri, 28 Jul 2023 01:56:53 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f80844b21c0dfb1fd717a0126298e80882723c7bca0c5529c7df48c419ed86`  
		Last Modified: Fri, 28 Jul 2023 01:56:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:fce5d02e200e3a96030084a057b4430f9f946cefb7df9abca3a1120153b5e265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:227198eb13b4d8e48ab02a69862ac03b68e44b2e879441399c96c3e130ed8cac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90240323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d827434098752cb94ff077a95fef98532ff66a71643aa133e760eeeda419ecb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:53:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 00:53:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 00:54:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 00:54:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 00:54:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:08 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 00:54:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 00:54:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 00:54:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 00:54:22 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 00:54:22 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 00:54:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 00:54:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 00:54:23 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 00:54:23 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 00:54:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c404450a25c52aaf36ad6cf2df7bf83eb65d98bca7cb78649b4a22fbe62aba`  
		Last Modified: Fri, 28 Jul 2023 00:56:02 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e16992934da47a606ee48c95eebfce4c426068c7b046352ca614ce1161a10`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 5.2 MB (5224480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4e80f87d5f0ac56fd4616490a14b6299e1b71054316e29e79922dabfe4cc77`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 610.3 KB (610275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcb668df53bd84b62cfbd8b5ca4fa69e26041fdd9a7e919993f81fa1de5dfaf`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 294.4 KB (294410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519c2591a1a074436d27db4d303d302c79f5317fa1873cbdbf6a711863c6ef2c`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc7cbd8bea6ee19dbafe441e0b78a2a7fe1c01a4e83f2d8518c09fcb2a4b57a`  
		Last Modified: Fri, 28 Jul 2023 00:56:03 GMT  
		Size: 52.7 MB (52686137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fe90e4dff94e302b5f98efe1337955d9a56d04f64eaa8cd4642552a30dbeca`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0572f1b6b33e5a9a305c54b7ac1ba36188faa7a53e3461c213bfa0f17eb9b4`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520ff0c4c1c630b2c9838ee8eb05a11d541dfe16c5ac442c1db62fd8cb592fd2`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c53a8228db1b37a14d63d5945d500959e69ab4832bfbe9d335a1bd314cb69`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2e70f5d37f5cc7cf4b3650aa83698c05e29e4328b28742c4d62d23f3fb1b6f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88684803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56332a507d98c5fa88cbd5c18427e6a0800e1a7abf254ed11626b02b9fa166d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:54:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 01:54:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 01:54:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 01:54:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 01:54:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:50 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 01:54:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 01:55:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 01:55:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 01:55:02 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 01:55:02 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 01:55:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 01:55:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:55:03 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 01:55:03 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 01:55:03 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7f9b366f53bc414354cc8f76b4a69b8a893a5ec10d1eb92df285ea58245e46`  
		Last Modified: Fri, 28 Jul 2023 01:56:25 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219ecbff31414f0f2ad54c2cd4518b665c19f0e00070963eae158f618fd8939d`  
		Last Modified: Fri, 28 Jul 2023 01:56:24 GMT  
		Size: 5.2 MB (5209548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4404fb20af6a73b94f81a1c25c6830a3e0e0c11d7e67eee7c83959875945ecd`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 566.3 KB (566291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40659943f33c45b039960055ee53cff41e91c4d354ea2dcf5b0b9577e4a40450`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 294.3 KB (294296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6da584c0e08eb2f1723a97553ba41ebafabd4cc802967fb1ffec13223613dd`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905bdb07374a015ef787de5082afc33403aa603166b94703f7230771d5291fa2`  
		Last Modified: Fri, 28 Jul 2023 01:56:26 GMT  
		Size: 52.5 MB (52544396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b47c179c832b7798be1c9b78f682f0796fc80c9c1fe3d1fd0bd4e133f3d0584`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae080c493858f5df5a92c38f7672c9a8e1043e8d36e871e541df543232646818`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98abec4e2dd5439587c3a84207dd9b94e400f9c2a210935144cfa25de112a60`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448423c6a5375ebc98e39645b49903543b6de8d6c1df8146f7129c837b2125a5`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:195e387b9e77db7faf72f3138d8e494d67869deb38acb0d1dc5deae048f10c22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b1b56534f75b9f1bbfbf2b5af66f6aed83154e252a6a25a6b6178032fa36f5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:23:41 GMT
ADD file:bc63550bad6e6b1e46c01c4911ac409a0a01e632b56a9a846fa2d7c86d8bb292 in / 
# Thu, 27 Jul 2023 23:23:43 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:44:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 03:44:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 03:44:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:44:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 03:44:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 03:45:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:45:08 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 03:45:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 03:45:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 03:45:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 03:45:45 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 03:45:45 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 03:45:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 03:45:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 03:45:47 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 03:45:48 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 03:45:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:90fff1cd317dd6511bdf25cbc4f6797ea09a5bc0657b6e1d88772d885bed1da0`  
		Last Modified: Thu, 27 Jul 2023 23:30:33 GMT  
		Size: 35.3 MB (35291031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89881e295647078d9c302e443081459979a2cd3b1161a78a449001074720911`  
		Last Modified: Fri, 28 Jul 2023 03:46:39 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44e1763c279db8dfa52f1640c68fa14adfa41f5a055addc6f0a7b9959585354`  
		Last Modified: Fri, 28 Jul 2023 03:46:38 GMT  
		Size: 6.0 MB (6044154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b95b80c92cb8cda5a88e018d853eff3eb94b9df3651a91fe4238fb4cf0dc0ef`  
		Last Modified: Fri, 28 Jul 2023 03:46:37 GMT  
		Size: 662.2 KB (662169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a478ddd7fcbd6eff286a6cc7dfe93f5ee5d3de16ccfc19e827e0b4fd82249e0b`  
		Last Modified: Fri, 28 Jul 2023 03:46:36 GMT  
		Size: 294.4 KB (294375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93724178719de15b26283a933ff2f41443ff52b2b11b6191b5b484501ad51c9b`  
		Last Modified: Fri, 28 Jul 2023 03:46:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eeb8574d1906c43163ebcd0459cf5a3d8298a7a9fec7d2a16f9e6cc052b121`  
		Last Modified: Fri, 28 Jul 2023 03:46:44 GMT  
		Size: 53.7 MB (53663059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b1aa1f11ad7febca6e0e6a1d29121fbba6dd3a4abbe795f1d7184015e0caae`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3094563d60c9c847de9ae3119c4afc8edd6877d73a4308b4dc314eed18e4e`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76163dedbf2715457e9f61f4d785a3ad85110c6911e164bea2196d513e05835`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b593398a60565eddef5653aa64a341cc80bcd14d839d4ae79cb54818f3c6ae6`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:b4436cfee6fb1f617f62f435cf8f8928ef5ff65a17f8d250d113fcad60db722b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86992654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0462abac2949145f42dbd36149a362a2799a53b4ce92e5bcd092207ead848744`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:42 GMT
ADD file:af0651fb20da5a08d22c074a04a2d96d68d66b5be86a11d348364e151de46196 in / 
# Thu, 27 Jul 2023 23:47:44 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:05:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 02:05:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 02:05:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:05:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 02:05:19 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 02:05:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:05:24 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 02:05:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 02:05:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 02:05:40 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 02:05:40 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 02:05:40 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 02:05:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 02:05:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:05:41 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 02:05:41 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 02:05:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:010ebc9d3534dabb784b6e93117170f0f20f698913991111a4ea549e5d951b7b`  
		Last Modified: Thu, 27 Jul 2023 23:52:47 GMT  
		Size: 29.7 MB (29652882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebe9433e686daf506ce0412a2e870f9375f2b4a9adebc1124bdac2c94e40b84`  
		Last Modified: Fri, 28 Jul 2023 02:06:00 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b1f4c5fb7051b121d29432853340993dacd3820b783719cec985e575a5b097`  
		Last Modified: Fri, 28 Jul 2023 02:06:00 GMT  
		Size: 5.1 MB (5110361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09ff47afedc1f64df9b0457edfb716da23b39d1d0635ed9b9c2827c8fcc80fb`  
		Last Modified: Fri, 28 Jul 2023 02:05:59 GMT  
		Size: 573.0 KB (573002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882364bf72cf29abbd9eea99f4deab7dc5d006774b680cd8cf7c873004c5c7f1`  
		Last Modified: Fri, 28 Jul 2023 02:05:59 GMT  
		Size: 294.3 KB (294349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0c556952b0caa59dbb74cd9caaee7c9b2a41bc40e89d6ac7711314b0b6c7ed`  
		Last Modified: Fri, 28 Jul 2023 02:05:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5478d623f0f5fdf2104ed41f8b821dbcb1faa8d511b9aca76081d7794ad5b2a`  
		Last Modified: Fri, 28 Jul 2023 02:06:03 GMT  
		Size: 51.4 MB (51354617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cefca2110efbbc66b98c4c51fad325440374d2c837d943c357e6e668bb4ddfb`  
		Last Modified: Fri, 28 Jul 2023 02:05:58 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad59591fc8983f5880fe5317ee964acbdf74c5b5aedf0c28e796eec6644265fd`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 997.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb0d9378e1540623419ca5aa93a86c26104ca658ae6b5ceb3c40977e448a174`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44cb5db485ad317f73a25062fc2d6509149caeb60585c2cd08daf9af133bf5f`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:60919a2c33064e5268b96fa9f2c5ff067b43ba43318a6299096d56fb2cf00697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:6d3320fa0a2ff4ea9e6b006a632579cfa20b3166aba1646aa768c2f22714e8a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80074627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead0a95f6afc924f3982ae788b88458f47a2739c915e0209ae7922d1fe723ca1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:29 GMT
ADD file:20e7ad6bec617357895302b08431eb3430cce3113bdf0a8ff9827115f858d313 in / 
# Thu, 27 Jul 2023 23:25:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:54:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 00:54:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 00:54:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Fri, 28 Jul 2023 00:54:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 00:55:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:55:04 GMT
ENV COUCHDB_VERSION=3.1.2
# Fri, 28 Jul 2023 00:55:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 00:55:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 00:55:18 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 00:55:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 00:55:19 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 28 Jul 2023 00:55:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 00:55:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 00:55:19 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 00:55:19 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 00:55:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3240fe174df9a5a4923c4b52f1d887dd1ad1a9ee69245c1fb867f399167584dd`  
		Last Modified: Thu, 27 Jul 2023 23:30:49 GMT  
		Size: 27.2 MB (27187431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d89b65f2dc832c2f7c348d9f12cf4b9e110e543efc4813b9f870c494429957`  
		Last Modified: Fri, 28 Jul 2023 00:56:38 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef28276cebf24c8afba60bbb3445613b21460493b508d02d292c0fdd8b18f44`  
		Last Modified: Fri, 28 Jul 2023 00:56:37 GMT  
		Size: 6.7 MB (6704542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c905d0380fb2306d3e35170fbbc2bc64a4128012ea5e12393ed06dff6c5ce8b6`  
		Last Modified: Fri, 28 Jul 2023 00:56:36 GMT  
		Size: 1.3 MB (1259891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7672fd27b19b3a699dcc283d34f31cc9ef507fb4b8905d4d8ab9528e4ffbf8e3`  
		Last Modified: Fri, 28 Jul 2023 00:56:36 GMT  
		Size: 294.6 KB (294631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a60738e02b1b10e1918577229022c10aee9b81972200f20fbf1767ec9f4f43`  
		Last Modified: Fri, 28 Jul 2023 00:56:36 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1eb9b5bcba498cae5a10dc7483e01f52ab00c327077d57da73bf9db4df6806`  
		Last Modified: Fri, 28 Jul 2023 00:56:38 GMT  
		Size: 44.6 MB (44621118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882f1dbfe924668195838b85a49ef8fbde9d86b22257234434d782637ecd2bcd`  
		Last Modified: Fri, 28 Jul 2023 00:56:34 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986e9c436a7f1cf8a979637771ff0e2cde3502dccdda06806fc8068b2035eb57`  
		Last Modified: Fri, 28 Jul 2023 00:56:34 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ee7e2e9225a67265f1588a3cea2e4f2196093bf0ed09adab2e6b890913cc24`  
		Last Modified: Fri, 28 Jul 2023 00:56:34 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ae0c5a95ec5fb85130d31b1ac170ece67e422788039912f1d9b1085e2138eb`  
		Last Modified: Fri, 28 Jul 2023 00:56:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ab4ce94cb48e66dd9c392b8b6e49fd199f679cfa19d8dd05c085d761fcb893c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75138204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff8b9c64f3b4b9b1086db3a56094baf5ffc36f01aba2b351813612b85781161`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:29 GMT
ADD file:ff126e7e4d046d566ea77f196c35d57f2d755b935cda365c5e3bba5f4d18ebf2 in / 
# Thu, 27 Jul 2023 23:43:29 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:55:21 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 01:55:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 01:55:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:55:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Fri, 28 Jul 2023 01:55:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 01:55:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:55:37 GMT
ENV COUCHDB_VERSION=3.1.2
# Fri, 28 Jul 2023 01:55:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 01:55:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 01:55:50 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 01:55:50 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 01:55:50 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 28 Jul 2023 01:55:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 01:55:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:55:51 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 01:55:51 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 01:55:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d71ee974c4e69baa159b185ea2bebfc5b3d814a08167ed09a79596f4707642c0`  
		Last Modified: Thu, 27 Jul 2023 23:47:51 GMT  
		Size: 26.0 MB (25967808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5ed2f5251688c7911c07a3afc2d8fe296d7b2cc6100dbfa9b8b41ef34f4cf3`  
		Last Modified: Fri, 28 Jul 2023 01:56:45 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1520a23e0d6c339c2f929d97df639e69bcb50d375b2021b489e877ae74969158`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 6.6 MB (6577647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab60e0e7bbd22b9de27de87e8887415f0c42dca5e711d4a1ce37301deb2537b`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 1.2 MB (1164841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2216a631ec9538e028e3e45ccb598a9b1b46a8fa0d90ce038781a5435b473aff`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 294.4 KB (294427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727a215782f0634377aa9a595ea0e3639f83558c207ff5ccc5b8ce2d624cb62e`  
		Last Modified: Fri, 28 Jul 2023 01:56:42 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abac1080418b5a85428d991929c8b6dbccbae57d0e7d2e3aa6a596d88d6c5a8c`  
		Last Modified: Fri, 28 Jul 2023 01:56:44 GMT  
		Size: 41.1 MB (41126441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d92e3d0e9cbc64d408455533f0da5c82dcc88f210cfa753b758e7c2363624c9`  
		Last Modified: Fri, 28 Jul 2023 01:56:41 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a34fc782bcb36697eea38f571edcee23ac0b8eeea5cc3b11d26676a138c4b4`  
		Last Modified: Fri, 28 Jul 2023 01:56:41 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ba707a2f39d41bdc82df8ee6fa8c38ec2d4bb6420ee5fe3aecc5de83538fad`  
		Last Modified: Fri, 28 Jul 2023 01:56:41 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f882f3a2921dc037c46797fd28ecc387dffc9deab898261899bd14940ad45390`  
		Last Modified: Fri, 28 Jul 2023 01:56:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:60919a2c33064e5268b96fa9f2c5ff067b43ba43318a6299096d56fb2cf00697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:6d3320fa0a2ff4ea9e6b006a632579cfa20b3166aba1646aa768c2f22714e8a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80074627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead0a95f6afc924f3982ae788b88458f47a2739c915e0209ae7922d1fe723ca1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:29 GMT
ADD file:20e7ad6bec617357895302b08431eb3430cce3113bdf0a8ff9827115f858d313 in / 
# Thu, 27 Jul 2023 23:25:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:54:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 00:54:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 00:54:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Fri, 28 Jul 2023 00:54:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 00:55:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:55:04 GMT
ENV COUCHDB_VERSION=3.1.2
# Fri, 28 Jul 2023 00:55:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 00:55:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 00:55:18 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 00:55:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 00:55:19 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 28 Jul 2023 00:55:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 00:55:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 00:55:19 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 00:55:19 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 00:55:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3240fe174df9a5a4923c4b52f1d887dd1ad1a9ee69245c1fb867f399167584dd`  
		Last Modified: Thu, 27 Jul 2023 23:30:49 GMT  
		Size: 27.2 MB (27187431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d89b65f2dc832c2f7c348d9f12cf4b9e110e543efc4813b9f870c494429957`  
		Last Modified: Fri, 28 Jul 2023 00:56:38 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef28276cebf24c8afba60bbb3445613b21460493b508d02d292c0fdd8b18f44`  
		Last Modified: Fri, 28 Jul 2023 00:56:37 GMT  
		Size: 6.7 MB (6704542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c905d0380fb2306d3e35170fbbc2bc64a4128012ea5e12393ed06dff6c5ce8b6`  
		Last Modified: Fri, 28 Jul 2023 00:56:36 GMT  
		Size: 1.3 MB (1259891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7672fd27b19b3a699dcc283d34f31cc9ef507fb4b8905d4d8ab9528e4ffbf8e3`  
		Last Modified: Fri, 28 Jul 2023 00:56:36 GMT  
		Size: 294.6 KB (294631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a60738e02b1b10e1918577229022c10aee9b81972200f20fbf1767ec9f4f43`  
		Last Modified: Fri, 28 Jul 2023 00:56:36 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1eb9b5bcba498cae5a10dc7483e01f52ab00c327077d57da73bf9db4df6806`  
		Last Modified: Fri, 28 Jul 2023 00:56:38 GMT  
		Size: 44.6 MB (44621118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882f1dbfe924668195838b85a49ef8fbde9d86b22257234434d782637ecd2bcd`  
		Last Modified: Fri, 28 Jul 2023 00:56:34 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986e9c436a7f1cf8a979637771ff0e2cde3502dccdda06806fc8068b2035eb57`  
		Last Modified: Fri, 28 Jul 2023 00:56:34 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ee7e2e9225a67265f1588a3cea2e4f2196093bf0ed09adab2e6b890913cc24`  
		Last Modified: Fri, 28 Jul 2023 00:56:34 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ae0c5a95ec5fb85130d31b1ac170ece67e422788039912f1d9b1085e2138eb`  
		Last Modified: Fri, 28 Jul 2023 00:56:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ab4ce94cb48e66dd9c392b8b6e49fd199f679cfa19d8dd05c085d761fcb893c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75138204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff8b9c64f3b4b9b1086db3a56094baf5ffc36f01aba2b351813612b85781161`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:29 GMT
ADD file:ff126e7e4d046d566ea77f196c35d57f2d755b935cda365c5e3bba5f4d18ebf2 in / 
# Thu, 27 Jul 2023 23:43:29 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:55:21 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 01:55:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 01:55:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:55:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Fri, 28 Jul 2023 01:55:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 01:55:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:55:37 GMT
ENV COUCHDB_VERSION=3.1.2
# Fri, 28 Jul 2023 01:55:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 01:55:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 01:55:50 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 01:55:50 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 01:55:50 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 28 Jul 2023 01:55:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 01:55:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:55:51 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 01:55:51 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 01:55:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d71ee974c4e69baa159b185ea2bebfc5b3d814a08167ed09a79596f4707642c0`  
		Last Modified: Thu, 27 Jul 2023 23:47:51 GMT  
		Size: 26.0 MB (25967808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5ed2f5251688c7911c07a3afc2d8fe296d7b2cc6100dbfa9b8b41ef34f4cf3`  
		Last Modified: Fri, 28 Jul 2023 01:56:45 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1520a23e0d6c339c2f929d97df639e69bcb50d375b2021b489e877ae74969158`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 6.6 MB (6577647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab60e0e7bbd22b9de27de87e8887415f0c42dca5e711d4a1ce37301deb2537b`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 1.2 MB (1164841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2216a631ec9538e028e3e45ccb598a9b1b46a8fa0d90ce038781a5435b473aff`  
		Last Modified: Fri, 28 Jul 2023 01:56:43 GMT  
		Size: 294.4 KB (294427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727a215782f0634377aa9a595ea0e3639f83558c207ff5ccc5b8ce2d624cb62e`  
		Last Modified: Fri, 28 Jul 2023 01:56:42 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abac1080418b5a85428d991929c8b6dbccbae57d0e7d2e3aa6a596d88d6c5a8c`  
		Last Modified: Fri, 28 Jul 2023 01:56:44 GMT  
		Size: 41.1 MB (41126441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d92e3d0e9cbc64d408455533f0da5c82dcc88f210cfa753b758e7c2363624c9`  
		Last Modified: Fri, 28 Jul 2023 01:56:41 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a34fc782bcb36697eea38f571edcee23ac0b8eeea5cc3b11d26676a138c4b4`  
		Last Modified: Fri, 28 Jul 2023 01:56:41 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ba707a2f39d41bdc82df8ee6fa8c38ec2d4bb6420ee5fe3aecc5de83538fad`  
		Last Modified: Fri, 28 Jul 2023 01:56:41 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f882f3a2921dc037c46797fd28ecc387dffc9deab898261899bd14940ad45390`  
		Last Modified: Fri, 28 Jul 2023 01:56:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:34e176ad511efe713c43c58c2aab962c2fc4811cbfc303d893eb7175c60c1c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:8d7483a7fd7da6a84fdc44099771efbe3d5d5430b545e1726a92f34c3d25e8fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89740721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ff1f0f1b2be8b4a2243fd4c8a2a3a034e4226f0fb521ea9a038f5ee8ac7299`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:53:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 00:53:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 00:54:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 00:54:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 00:54:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:26 GMT
ENV COUCHDB_VERSION=3.2.3
# Fri, 28 Jul 2023 00:54:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 00:54:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 00:54:39 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 00:54:39 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 00:54:39 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 00:54:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 00:54:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 00:54:40 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 00:54:40 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 00:54:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c404450a25c52aaf36ad6cf2df7bf83eb65d98bca7cb78649b4a22fbe62aba`  
		Last Modified: Fri, 28 Jul 2023 00:56:02 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e16992934da47a606ee48c95eebfce4c426068c7b046352ca614ce1161a10`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 5.2 MB (5224480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4e80f87d5f0ac56fd4616490a14b6299e1b71054316e29e79922dabfe4cc77`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 610.3 KB (610275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcb668df53bd84b62cfbd8b5ca4fa69e26041fdd9a7e919993f81fa1de5dfaf`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 294.4 KB (294410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692a2c8068b693b18caf9eeb950329bc0ae0c12b3d71915d6d57f5ba24ff568f`  
		Last Modified: Fri, 28 Jul 2023 00:56:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c51160478bd0b149db84b0a56afc74ac4487a6933e71abfedb930da0b97f33`  
		Last Modified: Fri, 28 Jul 2023 00:56:24 GMT  
		Size: 52.2 MB (52186536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5295ff357554364e67230615e4a45658795749ef72dd64da65872ffd8b2c81a`  
		Last Modified: Fri, 28 Jul 2023 00:56:19 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ea65d0e2775c623a813f0e00990615f643c375dd029103cb4c4e0661610459`  
		Last Modified: Fri, 28 Jul 2023 00:56:19 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c134731a8b6b3db7d4bd899d93d90e6d0a9f00f1391d50290c7b37e4ead15e9e`  
		Last Modified: Fri, 28 Jul 2023 00:56:19 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d24eeed9a8e1d9cfd216e63108877e2c5f2d2892a592e75c9e63e32aec4ff5`  
		Last Modified: Fri, 28 Jul 2023 00:56:19 GMT  
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
$ docker pull couchdb@sha256:0861effa71efdd75f0e46835e72a6b2726f30f6f9e733e0229c35cd6c1d2ba3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchdb:3.2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:8d7483a7fd7da6a84fdc44099771efbe3d5d5430b545e1726a92f34c3d25e8fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89740721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ff1f0f1b2be8b4a2243fd4c8a2a3a034e4226f0fb521ea9a038f5ee8ac7299`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:53:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 00:53:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 00:54:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 00:54:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 00:54:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:26 GMT
ENV COUCHDB_VERSION=3.2.3
# Fri, 28 Jul 2023 00:54:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 00:54:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 00:54:39 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 00:54:39 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 00:54:39 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 00:54:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 00:54:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 00:54:40 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 00:54:40 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 00:54:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c404450a25c52aaf36ad6cf2df7bf83eb65d98bca7cb78649b4a22fbe62aba`  
		Last Modified: Fri, 28 Jul 2023 00:56:02 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e16992934da47a606ee48c95eebfce4c426068c7b046352ca614ce1161a10`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 5.2 MB (5224480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4e80f87d5f0ac56fd4616490a14b6299e1b71054316e29e79922dabfe4cc77`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 610.3 KB (610275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcb668df53bd84b62cfbd8b5ca4fa69e26041fdd9a7e919993f81fa1de5dfaf`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 294.4 KB (294410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692a2c8068b693b18caf9eeb950329bc0ae0c12b3d71915d6d57f5ba24ff568f`  
		Last Modified: Fri, 28 Jul 2023 00:56:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c51160478bd0b149db84b0a56afc74ac4487a6933e71abfedb930da0b97f33`  
		Last Modified: Fri, 28 Jul 2023 00:56:24 GMT  
		Size: 52.2 MB (52186536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5295ff357554364e67230615e4a45658795749ef72dd64da65872ffd8b2c81a`  
		Last Modified: Fri, 28 Jul 2023 00:56:19 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ea65d0e2775c623a813f0e00990615f643c375dd029103cb4c4e0661610459`  
		Last Modified: Fri, 28 Jul 2023 00:56:19 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c134731a8b6b3db7d4bd899d93d90e6d0a9f00f1391d50290c7b37e4ead15e9e`  
		Last Modified: Fri, 28 Jul 2023 00:56:19 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d24eeed9a8e1d9cfd216e63108877e2c5f2d2892a592e75c9e63e32aec4ff5`  
		Last Modified: Fri, 28 Jul 2023 00:56:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:fce5d02e200e3a96030084a057b4430f9f946cefb7df9abca3a1120153b5e265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:227198eb13b4d8e48ab02a69862ac03b68e44b2e879441399c96c3e130ed8cac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90240323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d827434098752cb94ff077a95fef98532ff66a71643aa133e760eeeda419ecb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:53:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 00:53:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 00:54:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 00:54:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 00:54:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:08 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 00:54:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 00:54:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 00:54:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 00:54:22 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 00:54:22 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 00:54:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 00:54:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 00:54:23 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 00:54:23 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 00:54:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c404450a25c52aaf36ad6cf2df7bf83eb65d98bca7cb78649b4a22fbe62aba`  
		Last Modified: Fri, 28 Jul 2023 00:56:02 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e16992934da47a606ee48c95eebfce4c426068c7b046352ca614ce1161a10`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 5.2 MB (5224480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4e80f87d5f0ac56fd4616490a14b6299e1b71054316e29e79922dabfe4cc77`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 610.3 KB (610275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcb668df53bd84b62cfbd8b5ca4fa69e26041fdd9a7e919993f81fa1de5dfaf`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 294.4 KB (294410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519c2591a1a074436d27db4d303d302c79f5317fa1873cbdbf6a711863c6ef2c`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc7cbd8bea6ee19dbafe441e0b78a2a7fe1c01a4e83f2d8518c09fcb2a4b57a`  
		Last Modified: Fri, 28 Jul 2023 00:56:03 GMT  
		Size: 52.7 MB (52686137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fe90e4dff94e302b5f98efe1337955d9a56d04f64eaa8cd4642552a30dbeca`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0572f1b6b33e5a9a305c54b7ac1ba36188faa7a53e3461c213bfa0f17eb9b4`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520ff0c4c1c630b2c9838ee8eb05a11d541dfe16c5ac442c1db62fd8cb592fd2`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c53a8228db1b37a14d63d5945d500959e69ab4832bfbe9d335a1bd314cb69`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2e70f5d37f5cc7cf4b3650aa83698c05e29e4328b28742c4d62d23f3fb1b6f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88684803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56332a507d98c5fa88cbd5c18427e6a0800e1a7abf254ed11626b02b9fa166d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:54:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 01:54:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 01:54:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 01:54:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 01:54:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:50 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 01:54:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 01:55:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 01:55:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 01:55:02 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 01:55:02 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 01:55:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 01:55:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:55:03 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 01:55:03 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 01:55:03 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7f9b366f53bc414354cc8f76b4a69b8a893a5ec10d1eb92df285ea58245e46`  
		Last Modified: Fri, 28 Jul 2023 01:56:25 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219ecbff31414f0f2ad54c2cd4518b665c19f0e00070963eae158f618fd8939d`  
		Last Modified: Fri, 28 Jul 2023 01:56:24 GMT  
		Size: 5.2 MB (5209548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4404fb20af6a73b94f81a1c25c6830a3e0e0c11d7e67eee7c83959875945ecd`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 566.3 KB (566291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40659943f33c45b039960055ee53cff41e91c4d354ea2dcf5b0b9577e4a40450`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 294.3 KB (294296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6da584c0e08eb2f1723a97553ba41ebafabd4cc802967fb1ffec13223613dd`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905bdb07374a015ef787de5082afc33403aa603166b94703f7230771d5291fa2`  
		Last Modified: Fri, 28 Jul 2023 01:56:26 GMT  
		Size: 52.5 MB (52544396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b47c179c832b7798be1c9b78f682f0796fc80c9c1fe3d1fd0bd4e133f3d0584`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae080c493858f5df5a92c38f7672c9a8e1043e8d36e871e541df543232646818`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98abec4e2dd5439587c3a84207dd9b94e400f9c2a210935144cfa25de112a60`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448423c6a5375ebc98e39645b49903543b6de8d6c1df8146f7129c837b2125a5`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:195e387b9e77db7faf72f3138d8e494d67869deb38acb0d1dc5deae048f10c22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b1b56534f75b9f1bbfbf2b5af66f6aed83154e252a6a25a6b6178032fa36f5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:23:41 GMT
ADD file:bc63550bad6e6b1e46c01c4911ac409a0a01e632b56a9a846fa2d7c86d8bb292 in / 
# Thu, 27 Jul 2023 23:23:43 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:44:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 03:44:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 03:44:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:44:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 03:44:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 03:45:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:45:08 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 03:45:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 03:45:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 03:45:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 03:45:45 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 03:45:45 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 03:45:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 03:45:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 03:45:47 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 03:45:48 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 03:45:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:90fff1cd317dd6511bdf25cbc4f6797ea09a5bc0657b6e1d88772d885bed1da0`  
		Last Modified: Thu, 27 Jul 2023 23:30:33 GMT  
		Size: 35.3 MB (35291031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89881e295647078d9c302e443081459979a2cd3b1161a78a449001074720911`  
		Last Modified: Fri, 28 Jul 2023 03:46:39 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44e1763c279db8dfa52f1640c68fa14adfa41f5a055addc6f0a7b9959585354`  
		Last Modified: Fri, 28 Jul 2023 03:46:38 GMT  
		Size: 6.0 MB (6044154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b95b80c92cb8cda5a88e018d853eff3eb94b9df3651a91fe4238fb4cf0dc0ef`  
		Last Modified: Fri, 28 Jul 2023 03:46:37 GMT  
		Size: 662.2 KB (662169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a478ddd7fcbd6eff286a6cc7dfe93f5ee5d3de16ccfc19e827e0b4fd82249e0b`  
		Last Modified: Fri, 28 Jul 2023 03:46:36 GMT  
		Size: 294.4 KB (294375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93724178719de15b26283a933ff2f41443ff52b2b11b6191b5b484501ad51c9b`  
		Last Modified: Fri, 28 Jul 2023 03:46:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eeb8574d1906c43163ebcd0459cf5a3d8298a7a9fec7d2a16f9e6cc052b121`  
		Last Modified: Fri, 28 Jul 2023 03:46:44 GMT  
		Size: 53.7 MB (53663059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b1aa1f11ad7febca6e0e6a1d29121fbba6dd3a4abbe795f1d7184015e0caae`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3094563d60c9c847de9ae3119c4afc8edd6877d73a4308b4dc314eed18e4e`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76163dedbf2715457e9f61f4d785a3ad85110c6911e164bea2196d513e05835`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b593398a60565eddef5653aa64a341cc80bcd14d839d4ae79cb54818f3c6ae6`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:b4436cfee6fb1f617f62f435cf8f8928ef5ff65a17f8d250d113fcad60db722b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86992654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0462abac2949145f42dbd36149a362a2799a53b4ce92e5bcd092207ead848744`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:42 GMT
ADD file:af0651fb20da5a08d22c074a04a2d96d68d66b5be86a11d348364e151de46196 in / 
# Thu, 27 Jul 2023 23:47:44 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:05:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 02:05:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 02:05:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:05:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 02:05:19 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 02:05:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:05:24 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 02:05:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 02:05:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 02:05:40 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 02:05:40 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 02:05:40 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 02:05:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 02:05:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:05:41 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 02:05:41 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 02:05:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:010ebc9d3534dabb784b6e93117170f0f20f698913991111a4ea549e5d951b7b`  
		Last Modified: Thu, 27 Jul 2023 23:52:47 GMT  
		Size: 29.7 MB (29652882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebe9433e686daf506ce0412a2e870f9375f2b4a9adebc1124bdac2c94e40b84`  
		Last Modified: Fri, 28 Jul 2023 02:06:00 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b1f4c5fb7051b121d29432853340993dacd3820b783719cec985e575a5b097`  
		Last Modified: Fri, 28 Jul 2023 02:06:00 GMT  
		Size: 5.1 MB (5110361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09ff47afedc1f64df9b0457edfb716da23b39d1d0635ed9b9c2827c8fcc80fb`  
		Last Modified: Fri, 28 Jul 2023 02:05:59 GMT  
		Size: 573.0 KB (573002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882364bf72cf29abbd9eea99f4deab7dc5d006774b680cd8cf7c873004c5c7f1`  
		Last Modified: Fri, 28 Jul 2023 02:05:59 GMT  
		Size: 294.3 KB (294349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0c556952b0caa59dbb74cd9caaee7c9b2a41bc40e89d6ac7711314b0b6c7ed`  
		Last Modified: Fri, 28 Jul 2023 02:05:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5478d623f0f5fdf2104ed41f8b821dbcb1faa8d511b9aca76081d7794ad5b2a`  
		Last Modified: Fri, 28 Jul 2023 02:06:03 GMT  
		Size: 51.4 MB (51354617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cefca2110efbbc66b98c4c51fad325440374d2c837d943c357e6e668bb4ddfb`  
		Last Modified: Fri, 28 Jul 2023 02:05:58 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad59591fc8983f5880fe5317ee964acbdf74c5b5aedf0c28e796eec6644265fd`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 997.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb0d9378e1540623419ca5aa93a86c26104ca658ae6b5ceb3c40977e448a174`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44cb5db485ad317f73a25062fc2d6509149caeb60585c2cd08daf9af133bf5f`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3.2`

```console
$ docker pull couchdb@sha256:fce5d02e200e3a96030084a057b4430f9f946cefb7df9abca3a1120153b5e265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3.3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:227198eb13b4d8e48ab02a69862ac03b68e44b2e879441399c96c3e130ed8cac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90240323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d827434098752cb94ff077a95fef98532ff66a71643aa133e760eeeda419ecb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:53:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 00:53:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 00:54:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 00:54:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 00:54:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:08 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 00:54:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 00:54:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 00:54:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 00:54:22 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 00:54:22 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 00:54:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 00:54:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 00:54:23 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 00:54:23 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 00:54:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c404450a25c52aaf36ad6cf2df7bf83eb65d98bca7cb78649b4a22fbe62aba`  
		Last Modified: Fri, 28 Jul 2023 00:56:02 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e16992934da47a606ee48c95eebfce4c426068c7b046352ca614ce1161a10`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 5.2 MB (5224480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4e80f87d5f0ac56fd4616490a14b6299e1b71054316e29e79922dabfe4cc77`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 610.3 KB (610275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcb668df53bd84b62cfbd8b5ca4fa69e26041fdd9a7e919993f81fa1de5dfaf`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 294.4 KB (294410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519c2591a1a074436d27db4d303d302c79f5317fa1873cbdbf6a711863c6ef2c`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc7cbd8bea6ee19dbafe441e0b78a2a7fe1c01a4e83f2d8518c09fcb2a4b57a`  
		Last Modified: Fri, 28 Jul 2023 00:56:03 GMT  
		Size: 52.7 MB (52686137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fe90e4dff94e302b5f98efe1337955d9a56d04f64eaa8cd4642552a30dbeca`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0572f1b6b33e5a9a305c54b7ac1ba36188faa7a53e3461c213bfa0f17eb9b4`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520ff0c4c1c630b2c9838ee8eb05a11d541dfe16c5ac442c1db62fd8cb592fd2`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c53a8228db1b37a14d63d5945d500959e69ab4832bfbe9d335a1bd314cb69`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2e70f5d37f5cc7cf4b3650aa83698c05e29e4328b28742c4d62d23f3fb1b6f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88684803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56332a507d98c5fa88cbd5c18427e6a0800e1a7abf254ed11626b02b9fa166d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:54:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 01:54:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 01:54:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 01:54:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 01:54:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:50 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 01:54:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 01:55:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 01:55:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 01:55:02 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 01:55:02 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 01:55:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 01:55:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:55:03 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 01:55:03 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 01:55:03 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7f9b366f53bc414354cc8f76b4a69b8a893a5ec10d1eb92df285ea58245e46`  
		Last Modified: Fri, 28 Jul 2023 01:56:25 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219ecbff31414f0f2ad54c2cd4518b665c19f0e00070963eae158f618fd8939d`  
		Last Modified: Fri, 28 Jul 2023 01:56:24 GMT  
		Size: 5.2 MB (5209548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4404fb20af6a73b94f81a1c25c6830a3e0e0c11d7e67eee7c83959875945ecd`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 566.3 KB (566291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40659943f33c45b039960055ee53cff41e91c4d354ea2dcf5b0b9577e4a40450`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 294.3 KB (294296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6da584c0e08eb2f1723a97553ba41ebafabd4cc802967fb1ffec13223613dd`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905bdb07374a015ef787de5082afc33403aa603166b94703f7230771d5291fa2`  
		Last Modified: Fri, 28 Jul 2023 01:56:26 GMT  
		Size: 52.5 MB (52544396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b47c179c832b7798be1c9b78f682f0796fc80c9c1fe3d1fd0bd4e133f3d0584`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae080c493858f5df5a92c38f7672c9a8e1043e8d36e871e541df543232646818`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98abec4e2dd5439587c3a84207dd9b94e400f9c2a210935144cfa25de112a60`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448423c6a5375ebc98e39645b49903543b6de8d6c1df8146f7129c837b2125a5`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:195e387b9e77db7faf72f3138d8e494d67869deb38acb0d1dc5deae048f10c22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b1b56534f75b9f1bbfbf2b5af66f6aed83154e252a6a25a6b6178032fa36f5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:23:41 GMT
ADD file:bc63550bad6e6b1e46c01c4911ac409a0a01e632b56a9a846fa2d7c86d8bb292 in / 
# Thu, 27 Jul 2023 23:23:43 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:44:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 03:44:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 03:44:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:44:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 03:44:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 03:45:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:45:08 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 03:45:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 03:45:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 03:45:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 03:45:45 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 03:45:45 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 03:45:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 03:45:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 03:45:47 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 03:45:48 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 03:45:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:90fff1cd317dd6511bdf25cbc4f6797ea09a5bc0657b6e1d88772d885bed1da0`  
		Last Modified: Thu, 27 Jul 2023 23:30:33 GMT  
		Size: 35.3 MB (35291031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89881e295647078d9c302e443081459979a2cd3b1161a78a449001074720911`  
		Last Modified: Fri, 28 Jul 2023 03:46:39 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44e1763c279db8dfa52f1640c68fa14adfa41f5a055addc6f0a7b9959585354`  
		Last Modified: Fri, 28 Jul 2023 03:46:38 GMT  
		Size: 6.0 MB (6044154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b95b80c92cb8cda5a88e018d853eff3eb94b9df3651a91fe4238fb4cf0dc0ef`  
		Last Modified: Fri, 28 Jul 2023 03:46:37 GMT  
		Size: 662.2 KB (662169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a478ddd7fcbd6eff286a6cc7dfe93f5ee5d3de16ccfc19e827e0b4fd82249e0b`  
		Last Modified: Fri, 28 Jul 2023 03:46:36 GMT  
		Size: 294.4 KB (294375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93724178719de15b26283a933ff2f41443ff52b2b11b6191b5b484501ad51c9b`  
		Last Modified: Fri, 28 Jul 2023 03:46:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eeb8574d1906c43163ebcd0459cf5a3d8298a7a9fec7d2a16f9e6cc052b121`  
		Last Modified: Fri, 28 Jul 2023 03:46:44 GMT  
		Size: 53.7 MB (53663059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b1aa1f11ad7febca6e0e6a1d29121fbba6dd3a4abbe795f1d7184015e0caae`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3094563d60c9c847de9ae3119c4afc8edd6877d73a4308b4dc314eed18e4e`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76163dedbf2715457e9f61f4d785a3ad85110c6911e164bea2196d513e05835`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b593398a60565eddef5653aa64a341cc80bcd14d839d4ae79cb54818f3c6ae6`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; s390x

```console
$ docker pull couchdb@sha256:b4436cfee6fb1f617f62f435cf8f8928ef5ff65a17f8d250d113fcad60db722b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86992654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0462abac2949145f42dbd36149a362a2799a53b4ce92e5bcd092207ead848744`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:42 GMT
ADD file:af0651fb20da5a08d22c074a04a2d96d68d66b5be86a11d348364e151de46196 in / 
# Thu, 27 Jul 2023 23:47:44 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:05:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 02:05:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 02:05:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:05:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 02:05:19 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 02:05:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:05:24 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 02:05:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 02:05:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 02:05:40 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 02:05:40 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 02:05:40 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 02:05:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 02:05:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:05:41 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 02:05:41 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 02:05:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:010ebc9d3534dabb784b6e93117170f0f20f698913991111a4ea549e5d951b7b`  
		Last Modified: Thu, 27 Jul 2023 23:52:47 GMT  
		Size: 29.7 MB (29652882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebe9433e686daf506ce0412a2e870f9375f2b4a9adebc1124bdac2c94e40b84`  
		Last Modified: Fri, 28 Jul 2023 02:06:00 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b1f4c5fb7051b121d29432853340993dacd3820b783719cec985e575a5b097`  
		Last Modified: Fri, 28 Jul 2023 02:06:00 GMT  
		Size: 5.1 MB (5110361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09ff47afedc1f64df9b0457edfb716da23b39d1d0635ed9b9c2827c8fcc80fb`  
		Last Modified: Fri, 28 Jul 2023 02:05:59 GMT  
		Size: 573.0 KB (573002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882364bf72cf29abbd9eea99f4deab7dc5d006774b680cd8cf7c873004c5c7f1`  
		Last Modified: Fri, 28 Jul 2023 02:05:59 GMT  
		Size: 294.3 KB (294349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0c556952b0caa59dbb74cd9caaee7c9b2a41bc40e89d6ac7711314b0b6c7ed`  
		Last Modified: Fri, 28 Jul 2023 02:05:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5478d623f0f5fdf2104ed41f8b821dbcb1faa8d511b9aca76081d7794ad5b2a`  
		Last Modified: Fri, 28 Jul 2023 02:06:03 GMT  
		Size: 51.4 MB (51354617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cefca2110efbbc66b98c4c51fad325440374d2c837d943c357e6e668bb4ddfb`  
		Last Modified: Fri, 28 Jul 2023 02:05:58 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad59591fc8983f5880fe5317ee964acbdf74c5b5aedf0c28e796eec6644265fd`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 997.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb0d9378e1540623419ca5aa93a86c26104ca658ae6b5ceb3c40977e448a174`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44cb5db485ad317f73a25062fc2d6509149caeb60585c2cd08daf9af133bf5f`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:fce5d02e200e3a96030084a057b4430f9f946cefb7df9abca3a1120153b5e265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:227198eb13b4d8e48ab02a69862ac03b68e44b2e879441399c96c3e130ed8cac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90240323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d827434098752cb94ff077a95fef98532ff66a71643aa133e760eeeda419ecb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:53:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 00:53:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 00:54:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 00:54:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 00:54:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:08 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 00:54:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 00:54:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 00:54:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 00:54:22 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 00:54:22 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 00:54:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 00:54:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 00:54:23 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 00:54:23 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 00:54:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c404450a25c52aaf36ad6cf2df7bf83eb65d98bca7cb78649b4a22fbe62aba`  
		Last Modified: Fri, 28 Jul 2023 00:56:02 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e16992934da47a606ee48c95eebfce4c426068c7b046352ca614ce1161a10`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 5.2 MB (5224480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4e80f87d5f0ac56fd4616490a14b6299e1b71054316e29e79922dabfe4cc77`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 610.3 KB (610275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcb668df53bd84b62cfbd8b5ca4fa69e26041fdd9a7e919993f81fa1de5dfaf`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 294.4 KB (294410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519c2591a1a074436d27db4d303d302c79f5317fa1873cbdbf6a711863c6ef2c`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc7cbd8bea6ee19dbafe441e0b78a2a7fe1c01a4e83f2d8518c09fcb2a4b57a`  
		Last Modified: Fri, 28 Jul 2023 00:56:03 GMT  
		Size: 52.7 MB (52686137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fe90e4dff94e302b5f98efe1337955d9a56d04f64eaa8cd4642552a30dbeca`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0572f1b6b33e5a9a305c54b7ac1ba36188faa7a53e3461c213bfa0f17eb9b4`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520ff0c4c1c630b2c9838ee8eb05a11d541dfe16c5ac442c1db62fd8cb592fd2`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c53a8228db1b37a14d63d5945d500959e69ab4832bfbe9d335a1bd314cb69`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2e70f5d37f5cc7cf4b3650aa83698c05e29e4328b28742c4d62d23f3fb1b6f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88684803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56332a507d98c5fa88cbd5c18427e6a0800e1a7abf254ed11626b02b9fa166d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:54:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 01:54:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 01:54:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 01:54:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 01:54:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:50 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 01:54:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 01:55:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 01:55:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 01:55:02 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 01:55:02 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 01:55:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 01:55:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:55:03 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 01:55:03 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 01:55:03 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7f9b366f53bc414354cc8f76b4a69b8a893a5ec10d1eb92df285ea58245e46`  
		Last Modified: Fri, 28 Jul 2023 01:56:25 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219ecbff31414f0f2ad54c2cd4518b665c19f0e00070963eae158f618fd8939d`  
		Last Modified: Fri, 28 Jul 2023 01:56:24 GMT  
		Size: 5.2 MB (5209548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4404fb20af6a73b94f81a1c25c6830a3e0e0c11d7e67eee7c83959875945ecd`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 566.3 KB (566291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40659943f33c45b039960055ee53cff41e91c4d354ea2dcf5b0b9577e4a40450`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 294.3 KB (294296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6da584c0e08eb2f1723a97553ba41ebafabd4cc802967fb1ffec13223613dd`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905bdb07374a015ef787de5082afc33403aa603166b94703f7230771d5291fa2`  
		Last Modified: Fri, 28 Jul 2023 01:56:26 GMT  
		Size: 52.5 MB (52544396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b47c179c832b7798be1c9b78f682f0796fc80c9c1fe3d1fd0bd4e133f3d0584`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae080c493858f5df5a92c38f7672c9a8e1043e8d36e871e541df543232646818`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98abec4e2dd5439587c3a84207dd9b94e400f9c2a210935144cfa25de112a60`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448423c6a5375ebc98e39645b49903543b6de8d6c1df8146f7129c837b2125a5`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:195e387b9e77db7faf72f3138d8e494d67869deb38acb0d1dc5deae048f10c22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b1b56534f75b9f1bbfbf2b5af66f6aed83154e252a6a25a6b6178032fa36f5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:23:41 GMT
ADD file:bc63550bad6e6b1e46c01c4911ac409a0a01e632b56a9a846fa2d7c86d8bb292 in / 
# Thu, 27 Jul 2023 23:23:43 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:44:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 03:44:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 03:44:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:44:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 03:44:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 03:45:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:45:08 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 03:45:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 03:45:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 03:45:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 03:45:45 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 03:45:45 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 03:45:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 03:45:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 03:45:47 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 03:45:48 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 03:45:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:90fff1cd317dd6511bdf25cbc4f6797ea09a5bc0657b6e1d88772d885bed1da0`  
		Last Modified: Thu, 27 Jul 2023 23:30:33 GMT  
		Size: 35.3 MB (35291031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89881e295647078d9c302e443081459979a2cd3b1161a78a449001074720911`  
		Last Modified: Fri, 28 Jul 2023 03:46:39 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44e1763c279db8dfa52f1640c68fa14adfa41f5a055addc6f0a7b9959585354`  
		Last Modified: Fri, 28 Jul 2023 03:46:38 GMT  
		Size: 6.0 MB (6044154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b95b80c92cb8cda5a88e018d853eff3eb94b9df3651a91fe4238fb4cf0dc0ef`  
		Last Modified: Fri, 28 Jul 2023 03:46:37 GMT  
		Size: 662.2 KB (662169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a478ddd7fcbd6eff286a6cc7dfe93f5ee5d3de16ccfc19e827e0b4fd82249e0b`  
		Last Modified: Fri, 28 Jul 2023 03:46:36 GMT  
		Size: 294.4 KB (294375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93724178719de15b26283a933ff2f41443ff52b2b11b6191b5b484501ad51c9b`  
		Last Modified: Fri, 28 Jul 2023 03:46:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eeb8574d1906c43163ebcd0459cf5a3d8298a7a9fec7d2a16f9e6cc052b121`  
		Last Modified: Fri, 28 Jul 2023 03:46:44 GMT  
		Size: 53.7 MB (53663059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b1aa1f11ad7febca6e0e6a1d29121fbba6dd3a4abbe795f1d7184015e0caae`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3094563d60c9c847de9ae3119c4afc8edd6877d73a4308b4dc314eed18e4e`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76163dedbf2715457e9f61f4d785a3ad85110c6911e164bea2196d513e05835`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b593398a60565eddef5653aa64a341cc80bcd14d839d4ae79cb54818f3c6ae6`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:b4436cfee6fb1f617f62f435cf8f8928ef5ff65a17f8d250d113fcad60db722b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86992654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0462abac2949145f42dbd36149a362a2799a53b4ce92e5bcd092207ead848744`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:42 GMT
ADD file:af0651fb20da5a08d22c074a04a2d96d68d66b5be86a11d348364e151de46196 in / 
# Thu, 27 Jul 2023 23:47:44 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:05:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 02:05:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 02:05:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:05:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 02:05:19 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 02:05:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:05:24 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 02:05:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 02:05:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 02:05:40 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 02:05:40 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 02:05:40 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 02:05:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 02:05:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:05:41 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 02:05:41 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 02:05:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:010ebc9d3534dabb784b6e93117170f0f20f698913991111a4ea549e5d951b7b`  
		Last Modified: Thu, 27 Jul 2023 23:52:47 GMT  
		Size: 29.7 MB (29652882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebe9433e686daf506ce0412a2e870f9375f2b4a9adebc1124bdac2c94e40b84`  
		Last Modified: Fri, 28 Jul 2023 02:06:00 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b1f4c5fb7051b121d29432853340993dacd3820b783719cec985e575a5b097`  
		Last Modified: Fri, 28 Jul 2023 02:06:00 GMT  
		Size: 5.1 MB (5110361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09ff47afedc1f64df9b0457edfb716da23b39d1d0635ed9b9c2827c8fcc80fb`  
		Last Modified: Fri, 28 Jul 2023 02:05:59 GMT  
		Size: 573.0 KB (573002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882364bf72cf29abbd9eea99f4deab7dc5d006774b680cd8cf7c873004c5c7f1`  
		Last Modified: Fri, 28 Jul 2023 02:05:59 GMT  
		Size: 294.3 KB (294349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0c556952b0caa59dbb74cd9caaee7c9b2a41bc40e89d6ac7711314b0b6c7ed`  
		Last Modified: Fri, 28 Jul 2023 02:05:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5478d623f0f5fdf2104ed41f8b821dbcb1faa8d511b9aca76081d7794ad5b2a`  
		Last Modified: Fri, 28 Jul 2023 02:06:03 GMT  
		Size: 51.4 MB (51354617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cefca2110efbbc66b98c4c51fad325440374d2c837d943c357e6e668bb4ddfb`  
		Last Modified: Fri, 28 Jul 2023 02:05:58 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad59591fc8983f5880fe5317ee964acbdf74c5b5aedf0c28e796eec6644265fd`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 997.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb0d9378e1540623419ca5aa93a86c26104ca658ae6b5ceb3c40977e448a174`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44cb5db485ad317f73a25062fc2d6509149caeb60585c2cd08daf9af133bf5f`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
