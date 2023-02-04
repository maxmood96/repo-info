<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.2`](#couchdb312)
-	[`couchdb:3.2`](#couchdb32)
-	[`couchdb:3.2.2`](#couchdb322)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.1`](#couchdb331)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:38b645be402d16d36b8e6c79832e0d43115b320ca9eee4d5ded31e8ee08b8ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:2ae35f05964d869e9e0a91a4439e9bd2f221ab7a55c805f9506c508ee88300a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84537227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ccfdedceb663e349949001f3c5f441c074ad46d5a85ae709bfe812a49391da`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:07 GMT
ADD file:4fbe1e3712cf37c85529cc81e0d03c82085203de00d64b0d669b5996e975925a in / 
# Sat, 04 Feb 2023 06:52:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:17:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 07:17:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 07:17:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:17:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 07:17:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 07:18:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:18:20 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Sat, 04 Feb 2023 07:18:21 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 07:18:40 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 07:18:40 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 07:18:40 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 07:18:40 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Sat, 04 Feb 2023 07:18:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 07:18:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 07:18:41 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 07:18:41 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 07:18:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0cf508b37688dca559387b506062329202aaf08b48be5f55f9278b2a818ad2c9`  
		Last Modified: Sat, 04 Feb 2023 06:56:58 GMT  
		Size: 27.1 MB (27140353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2077aca956be48413850558c99aed2abe9648b6f9b9426c1135e15b89dc335ca`  
		Last Modified: Sat, 04 Feb 2023 07:19:33 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7242eb760000d68511583e5224849d57fcf7a36c0e53982efab6da6ed3e8760b`  
		Last Modified: Sat, 04 Feb 2023 07:19:32 GMT  
		Size: 6.7 MB (6703784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7226bb128a799d16fae1c3ca8f2cc831f56e1a799146562752f3665a224983e6`  
		Last Modified: Sat, 04 Feb 2023 07:19:31 GMT  
		Size: 1.3 MB (1259577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bbbd4823cbeb627c5529042b3857b765bfed971236216aea4249a891e32b90`  
		Last Modified: Sat, 04 Feb 2023 07:19:31 GMT  
		Size: 294.3 KB (294296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0068092afc5d3cde2f17a4f5152fc93ef48bb689d1bc10d8bbc66d18366d992d`  
		Last Modified: Sat, 04 Feb 2023 07:19:45 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ac500017a4fd00865fee794536ce43a2dd246477176f3a4ea1eba2f15c61d3`  
		Last Modified: Sat, 04 Feb 2023 07:19:49 GMT  
		Size: 49.1 MB (49132205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9992ec80c106f5db7bebac91263b1f1a873ca656352d1b3c3e874d168fac5cef`  
		Last Modified: Sat, 04 Feb 2023 07:19:43 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687a2cb80cde226d4d1bef9e0f91be6fd273a6e39da85339a87728a19384bde7`  
		Last Modified: Sat, 04 Feb 2023 07:19:43 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2434c1b2ac9467a54b63ce080c730ae0872966330badc4b3bd8963373b8aa5`  
		Last Modified: Sat, 04 Feb 2023 07:19:43 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3ce40c4c2e027fcfb04f5c173fe8fe34d0fae4e1306d670143b3acd88883c2`  
		Last Modified: Sat, 04 Feb 2023 07:19:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:1cb5a3e7aef4e216952743c76b29c4eb88b1a578b5f9d6d4162e0cd95ad4ac7a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72987090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2f7d541e92b28205022f9b17a0e8569566b08eebda8395c320798bf3e97b02`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:52 GMT
ADD file:08addf73dde8bf5ac64e0d9bdd1997ce5f406976c19da431616783c14fdb36ac in / 
# Wed, 11 Jan 2023 02:57:52 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:58:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:58:25 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:58:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:58:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:58:36 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:58:58 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 11 Jan 2023 03:58:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:59:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:59:10 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:59:10 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:59:10 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 11 Jan 2023 03:59:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:59:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:59:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:59:11 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:59:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7fac02f4cd2bcf681b9e156a67009cf4609f45447818b52327d93553bfeb2965`  
		Last Modified: Wed, 11 Jan 2023 03:01:58 GMT  
		Size: 25.9 MB (25914925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49c2ee40908e629f9af8a7cab6dd0cd3837146e1417c5687ea458a09e766135`  
		Last Modified: Wed, 11 Jan 2023 04:00:06 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c510231b78ec40191b73fcf37265b834eb84575e8e9e59214e699e0fb2443f23`  
		Last Modified: Wed, 11 Jan 2023 04:00:06 GMT  
		Size: 6.6 MB (6577083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7fa713a90ae4df09d27f1f23a63a2a6e7df1f68b7907280efb3d944b8bd006`  
		Last Modified: Wed, 11 Jan 2023 04:00:05 GMT  
		Size: 1.2 MB (1164501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83d395471dc77d8f630b48a40ec852957fdb479ef92505965c06a0297d3c0f`  
		Last Modified: Wed, 11 Jan 2023 04:00:04 GMT  
		Size: 294.1 KB (294133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1efd60f371e1e52363f272f85918ac4387fdaef6f0ac760cf27a1a129cdd7ca`  
		Last Modified: Wed, 11 Jan 2023 04:00:19 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df5cd36bc757fedbf7593edbc3ebb33dec27a4bfc364586b6194fe45a759650`  
		Last Modified: Wed, 11 Jan 2023 04:00:21 GMT  
		Size: 39.0 MB (39029409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812d9c58c0bb5f21046fa51f640b0fc96b54baf6d6fbbc87e2f9e46ccc35642d`  
		Last Modified: Wed, 11 Jan 2023 04:00:17 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6606db77f6e9fa1b66078936a6df4c5140f5803969ea6ab782d53cc730c71274`  
		Last Modified: Wed, 11 Jan 2023 04:00:17 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aee9ecdb2af156a7acbd8dbb24a7e6612149aa1d96568b0ad1ab1d637ec113b`  
		Last Modified: Wed, 11 Jan 2023 04:00:17 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e477447789dc28dd2ba5c7c08e7e4c96f84786e0cee41c144091143c345c7f`  
		Last Modified: Wed, 11 Jan 2023 04:00:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:38b645be402d16d36b8e6c79832e0d43115b320ca9eee4d5ded31e8ee08b8ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:2ae35f05964d869e9e0a91a4439e9bd2f221ab7a55c805f9506c508ee88300a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84537227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ccfdedceb663e349949001f3c5f441c074ad46d5a85ae709bfe812a49391da`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:07 GMT
ADD file:4fbe1e3712cf37c85529cc81e0d03c82085203de00d64b0d669b5996e975925a in / 
# Sat, 04 Feb 2023 06:52:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:17:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 07:17:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 07:17:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:17:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 07:17:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 07:18:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:18:20 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Sat, 04 Feb 2023 07:18:21 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 07:18:40 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 07:18:40 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 07:18:40 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 07:18:40 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Sat, 04 Feb 2023 07:18:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 07:18:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 07:18:41 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 07:18:41 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 07:18:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0cf508b37688dca559387b506062329202aaf08b48be5f55f9278b2a818ad2c9`  
		Last Modified: Sat, 04 Feb 2023 06:56:58 GMT  
		Size: 27.1 MB (27140353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2077aca956be48413850558c99aed2abe9648b6f9b9426c1135e15b89dc335ca`  
		Last Modified: Sat, 04 Feb 2023 07:19:33 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7242eb760000d68511583e5224849d57fcf7a36c0e53982efab6da6ed3e8760b`  
		Last Modified: Sat, 04 Feb 2023 07:19:32 GMT  
		Size: 6.7 MB (6703784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7226bb128a799d16fae1c3ca8f2cc831f56e1a799146562752f3665a224983e6`  
		Last Modified: Sat, 04 Feb 2023 07:19:31 GMT  
		Size: 1.3 MB (1259577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bbbd4823cbeb627c5529042b3857b765bfed971236216aea4249a891e32b90`  
		Last Modified: Sat, 04 Feb 2023 07:19:31 GMT  
		Size: 294.3 KB (294296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0068092afc5d3cde2f17a4f5152fc93ef48bb689d1bc10d8bbc66d18366d992d`  
		Last Modified: Sat, 04 Feb 2023 07:19:45 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ac500017a4fd00865fee794536ce43a2dd246477176f3a4ea1eba2f15c61d3`  
		Last Modified: Sat, 04 Feb 2023 07:19:49 GMT  
		Size: 49.1 MB (49132205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9992ec80c106f5db7bebac91263b1f1a873ca656352d1b3c3e874d168fac5cef`  
		Last Modified: Sat, 04 Feb 2023 07:19:43 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687a2cb80cde226d4d1bef9e0f91be6fd273a6e39da85339a87728a19384bde7`  
		Last Modified: Sat, 04 Feb 2023 07:19:43 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2434c1b2ac9467a54b63ce080c730ae0872966330badc4b3bd8963373b8aa5`  
		Last Modified: Sat, 04 Feb 2023 07:19:43 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3ce40c4c2e027fcfb04f5c173fe8fe34d0fae4e1306d670143b3acd88883c2`  
		Last Modified: Sat, 04 Feb 2023 07:19:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:1cb5a3e7aef4e216952743c76b29c4eb88b1a578b5f9d6d4162e0cd95ad4ac7a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72987090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2f7d541e92b28205022f9b17a0e8569566b08eebda8395c320798bf3e97b02`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:52 GMT
ADD file:08addf73dde8bf5ac64e0d9bdd1997ce5f406976c19da431616783c14fdb36ac in / 
# Wed, 11 Jan 2023 02:57:52 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:58:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:58:25 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:58:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:58:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:58:36 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:58:58 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 11 Jan 2023 03:58:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:59:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:59:10 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:59:10 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:59:10 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 11 Jan 2023 03:59:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:59:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:59:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:59:11 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:59:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7fac02f4cd2bcf681b9e156a67009cf4609f45447818b52327d93553bfeb2965`  
		Last Modified: Wed, 11 Jan 2023 03:01:58 GMT  
		Size: 25.9 MB (25914925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49c2ee40908e629f9af8a7cab6dd0cd3837146e1417c5687ea458a09e766135`  
		Last Modified: Wed, 11 Jan 2023 04:00:06 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c510231b78ec40191b73fcf37265b834eb84575e8e9e59214e699e0fb2443f23`  
		Last Modified: Wed, 11 Jan 2023 04:00:06 GMT  
		Size: 6.6 MB (6577083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7fa713a90ae4df09d27f1f23a63a2a6e7df1f68b7907280efb3d944b8bd006`  
		Last Modified: Wed, 11 Jan 2023 04:00:05 GMT  
		Size: 1.2 MB (1164501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83d395471dc77d8f630b48a40ec852957fdb479ef92505965c06a0297d3c0f`  
		Last Modified: Wed, 11 Jan 2023 04:00:04 GMT  
		Size: 294.1 KB (294133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1efd60f371e1e52363f272f85918ac4387fdaef6f0ac760cf27a1a129cdd7ca`  
		Last Modified: Wed, 11 Jan 2023 04:00:19 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df5cd36bc757fedbf7593edbc3ebb33dec27a4bfc364586b6194fe45a759650`  
		Last Modified: Wed, 11 Jan 2023 04:00:21 GMT  
		Size: 39.0 MB (39029409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812d9c58c0bb5f21046fa51f640b0fc96b54baf6d6fbbc87e2f9e46ccc35642d`  
		Last Modified: Wed, 11 Jan 2023 04:00:17 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6606db77f6e9fa1b66078936a6df4c5140f5803969ea6ab782d53cc730c71274`  
		Last Modified: Wed, 11 Jan 2023 04:00:17 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aee9ecdb2af156a7acbd8dbb24a7e6612149aa1d96568b0ad1ab1d637ec113b`  
		Last Modified: Wed, 11 Jan 2023 04:00:17 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e477447789dc28dd2ba5c7c08e7e4c96f84786e0cee41c144091143c345c7f`  
		Last Modified: Wed, 11 Jan 2023 04:00:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:38b645be402d16d36b8e6c79832e0d43115b320ca9eee4d5ded31e8ee08b8ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:2ae35f05964d869e9e0a91a4439e9bd2f221ab7a55c805f9506c508ee88300a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84537227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ccfdedceb663e349949001f3c5f441c074ad46d5a85ae709bfe812a49391da`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:07 GMT
ADD file:4fbe1e3712cf37c85529cc81e0d03c82085203de00d64b0d669b5996e975925a in / 
# Sat, 04 Feb 2023 06:52:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:17:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 07:17:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 07:17:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:17:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 07:17:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 07:18:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:18:20 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Sat, 04 Feb 2023 07:18:21 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 07:18:40 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 07:18:40 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 07:18:40 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 07:18:40 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Sat, 04 Feb 2023 07:18:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 07:18:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 07:18:41 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 07:18:41 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 07:18:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0cf508b37688dca559387b506062329202aaf08b48be5f55f9278b2a818ad2c9`  
		Last Modified: Sat, 04 Feb 2023 06:56:58 GMT  
		Size: 27.1 MB (27140353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2077aca956be48413850558c99aed2abe9648b6f9b9426c1135e15b89dc335ca`  
		Last Modified: Sat, 04 Feb 2023 07:19:33 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7242eb760000d68511583e5224849d57fcf7a36c0e53982efab6da6ed3e8760b`  
		Last Modified: Sat, 04 Feb 2023 07:19:32 GMT  
		Size: 6.7 MB (6703784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7226bb128a799d16fae1c3ca8f2cc831f56e1a799146562752f3665a224983e6`  
		Last Modified: Sat, 04 Feb 2023 07:19:31 GMT  
		Size: 1.3 MB (1259577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bbbd4823cbeb627c5529042b3857b765bfed971236216aea4249a891e32b90`  
		Last Modified: Sat, 04 Feb 2023 07:19:31 GMT  
		Size: 294.3 KB (294296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0068092afc5d3cde2f17a4f5152fc93ef48bb689d1bc10d8bbc66d18366d992d`  
		Last Modified: Sat, 04 Feb 2023 07:19:45 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ac500017a4fd00865fee794536ce43a2dd246477176f3a4ea1eba2f15c61d3`  
		Last Modified: Sat, 04 Feb 2023 07:19:49 GMT  
		Size: 49.1 MB (49132205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9992ec80c106f5db7bebac91263b1f1a873ca656352d1b3c3e874d168fac5cef`  
		Last Modified: Sat, 04 Feb 2023 07:19:43 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687a2cb80cde226d4d1bef9e0f91be6fd273a6e39da85339a87728a19384bde7`  
		Last Modified: Sat, 04 Feb 2023 07:19:43 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2434c1b2ac9467a54b63ce080c730ae0872966330badc4b3bd8963373b8aa5`  
		Last Modified: Sat, 04 Feb 2023 07:19:43 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3ce40c4c2e027fcfb04f5c173fe8fe34d0fae4e1306d670143b3acd88883c2`  
		Last Modified: Sat, 04 Feb 2023 07:19:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:1cb5a3e7aef4e216952743c76b29c4eb88b1a578b5f9d6d4162e0cd95ad4ac7a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72987090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2f7d541e92b28205022f9b17a0e8569566b08eebda8395c320798bf3e97b02`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:52 GMT
ADD file:08addf73dde8bf5ac64e0d9bdd1997ce5f406976c19da431616783c14fdb36ac in / 
# Wed, 11 Jan 2023 02:57:52 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:58:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:58:25 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:58:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:58:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:58:36 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:58:58 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 11 Jan 2023 03:58:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:59:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:59:10 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:59:10 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:59:10 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 11 Jan 2023 03:59:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:59:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:59:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:59:11 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:59:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7fac02f4cd2bcf681b9e156a67009cf4609f45447818b52327d93553bfeb2965`  
		Last Modified: Wed, 11 Jan 2023 03:01:58 GMT  
		Size: 25.9 MB (25914925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49c2ee40908e629f9af8a7cab6dd0cd3837146e1417c5687ea458a09e766135`  
		Last Modified: Wed, 11 Jan 2023 04:00:06 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c510231b78ec40191b73fcf37265b834eb84575e8e9e59214e699e0fb2443f23`  
		Last Modified: Wed, 11 Jan 2023 04:00:06 GMT  
		Size: 6.6 MB (6577083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7fa713a90ae4df09d27f1f23a63a2a6e7df1f68b7907280efb3d944b8bd006`  
		Last Modified: Wed, 11 Jan 2023 04:00:05 GMT  
		Size: 1.2 MB (1164501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83d395471dc77d8f630b48a40ec852957fdb479ef92505965c06a0297d3c0f`  
		Last Modified: Wed, 11 Jan 2023 04:00:04 GMT  
		Size: 294.1 KB (294133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1efd60f371e1e52363f272f85918ac4387fdaef6f0ac760cf27a1a129cdd7ca`  
		Last Modified: Wed, 11 Jan 2023 04:00:19 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df5cd36bc757fedbf7593edbc3ebb33dec27a4bfc364586b6194fe45a759650`  
		Last Modified: Wed, 11 Jan 2023 04:00:21 GMT  
		Size: 39.0 MB (39029409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812d9c58c0bb5f21046fa51f640b0fc96b54baf6d6fbbc87e2f9e46ccc35642d`  
		Last Modified: Wed, 11 Jan 2023 04:00:17 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6606db77f6e9fa1b66078936a6df4c5140f5803969ea6ab782d53cc730c71274`  
		Last Modified: Wed, 11 Jan 2023 04:00:17 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aee9ecdb2af156a7acbd8dbb24a7e6612149aa1d96568b0ad1ab1d637ec113b`  
		Last Modified: Wed, 11 Jan 2023 04:00:17 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e477447789dc28dd2ba5c7c08e7e4c96f84786e0cee41c144091143c345c7f`  
		Last Modified: Wed, 11 Jan 2023 04:00:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:58881fc8a4a12abb739fab6ded5677c04a5e04d8a3f61b5ae53286b64dfac9a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:6d588a96a550033c02f45a4ce38c296cbe08f9ec14cdd4f5ca4320d8af8eb00b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91153896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1274dd1bda729da68f2c64f847a63ec5d6634042dbe09ee8fb9ee1810b35493a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:16:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 07:16:46 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 07:16:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:16:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 07:16:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 07:17:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:17:02 GMT
ENV COUCHDB_VERSION=3.3.1
# Sat, 04 Feb 2023 07:17:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 07:17:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 07:17:16 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 07:17:16 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 07:17:16 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 04 Feb 2023 07:17:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 07:17:17 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 07:17:17 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 07:17:17 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 07:17:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77476cf11acd0f8081beb4a23efc99a2652c66cabe691898d51dd54b7a973967`  
		Last Modified: Sat, 04 Feb 2023 07:19:00 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e5ab1e54fdd1586bf4c41713f66e3c3dd536afdf177ab750bac5420e11af8b`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 5.2 MB (5224338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aea5b54023137f626790058724f9349eb5aece02da7ca2ec80ff98cbb34df42`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 1.6 MB (1553311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd561fdfab9d1eed8c99fefa269d1b26ceae1633127918de8c9bba901cd8642e`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 295.6 KB (295625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e24cec0cc44eeb1e0f1880275166759ac0aab64b4dcca3410a217f78fe5e2a`  
		Last Modified: Sat, 04 Feb 2023 07:18:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3132b1e018f6c5014588752194c7ac7ffabf8e0eec4b3528ff1fce2b24a6df5`  
		Last Modified: Sat, 04 Feb 2023 07:19:02 GMT  
		Size: 52.7 MB (52676329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768bc1a4f6854d19062811091a6930b6efd398b9dd84643f35bc1ced44ea5bba`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6b69d74d3c03eb77600518b7afdc0ed80493cd272bfc1c2c664656cf195381`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e138b051b652e40f53e6ace489845ca2a92f430f592f5112730c8b2bce6866aa`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3809ab88d6017f3f38fea418f135f4f8c181568eb8302a3bc9b42f69eea21122`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ed00ba73f951d5f496355f043a50b0c1d28169ff66e1383605c87cd5b26c6144
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89524742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855eaae40b75dc29eb937b8f1d1a345f679ef01cbf689fa45b0637fa2e139c9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:57:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:57:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:57:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:57:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:57:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:57:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 22:08:39 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 11 Jan 2023 22:08:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 22:08:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 22:08:52 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 22:08:52 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 22:08:53 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 22:08:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 22:08:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 22:08:53 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 22:08:53 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 22:08:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961831464917d8a5133f3840f3e3d15b6bb840593a5cbb857f67c46f39d73546`  
		Last Modified: Wed, 11 Jan 2023 03:59:34 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ba419ee6c06e64643e7104acf6aaa7133d872e801ba6d5559cf58a005e1d13`  
		Last Modified: Wed, 11 Jan 2023 03:59:33 GMT  
		Size: 5.2 MB (5209470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2fd7db3c36ccb6f388d0be04337eaf1c4c0b32352e9a7d95b4ae708024cdbd`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 1.4 MB (1435925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7fbb1ce521b1b1a114c87f3991a7a9de1562c8be484357ddc8d03f2f2c1404`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 295.5 KB (295517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5bcd70f03fefccc3314c5bd804107f5ca7ec891100c2e85d481e9b84f377c3`  
		Last Modified: Wed, 11 Jan 2023 22:09:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a54b1952a30cff448a907d4f82fbbac930beeb1bc452c05e9270fef7a3b056e`  
		Last Modified: Wed, 11 Jan 2023 22:09:18 GMT  
		Size: 52.5 MB (52531616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0782ea0b803ce74bf6e5d05e1a11776e25001beb73576a0c42faa330c238eda0`  
		Last Modified: Wed, 11 Jan 2023 22:09:13 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d347329aa65d9c4b005d93d848c27e025f14d6cb638099fafbecd04dbd43c4f7`  
		Last Modified: Wed, 11 Jan 2023 22:09:13 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0736c691206ce54706b7761f838f3cedd9a8c8f72b933d6ee58c55070659bfb5`  
		Last Modified: Wed, 11 Jan 2023 22:09:14 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0d0ee154aca0d4270a4eced51b0e6de35a1d7336bb1dc51549889432ea5afc`  
		Last Modified: Wed, 11 Jan 2023 22:09:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:169c08ffd541c72b2a9615587f87774d4b8047b8a2baeea19668987253ed48fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96660088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcda0be97c2bcc7cd1d4cca5ce768530b9e41fd99a7fb1a0c41e110153f32673`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 12:25:55 GMT
ADD file:2c82cc89d7ac2efeaf54e7589e28644e3e8436d66f6909bf295a2b030116ac58 in / 
# Sat, 04 Feb 2023 12:25:58 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 12:51:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 12:51:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 12:51:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 12:51:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 12:51:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 12:51:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 12:51:50 GMT
ENV COUCHDB_VERSION=3.3.1
# Sat, 04 Feb 2023 12:51:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 12:52:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 12:52:16 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 12:52:16 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 12:52:17 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 04 Feb 2023 12:52:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 12:52:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 12:52:19 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 12:52:19 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 12:52:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0604364135762a6c4b3503dd7f0396a51396443bf6052b34b8df7f67679b42c0`  
		Last Modified: Sat, 04 Feb 2023 12:32:12 GMT  
		Size: 35.3 MB (35268795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0db1dae9c381949243f87d00a076dd8935eadd9dfbb4a26770b524da132c28`  
		Last Modified: Sat, 04 Feb 2023 12:53:30 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb94746f03717925610786197b18595ba7711a5da5b2b691065b02f97414f8`  
		Last Modified: Sat, 04 Feb 2023 12:53:30 GMT  
		Size: 6.0 MB (6043885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffda288060566d345a0058dc1b6f9d096be2045f7d3513b4f20c3d02702e267a`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 1.5 MB (1509213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29955520a52a30117d393a5c4ec1010873a9bdc7b3d20b207b28b405b0ff648c`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 295.5 KB (295538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb000d7900471baa0e0264363864b8b3eeb4c04cdb58e634bd1269c20845e7c7`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a4e664ddc338ba1e6a85ef75b34219f136dbde3d7b1185395835ad562bc6d7`  
		Last Modified: Sat, 04 Feb 2023 12:53:35 GMT  
		Size: 53.5 MB (53535280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b178a6f96077dd23d510229a7e4030f5fc16474f7cc3164854ac56e093b5715d`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952cec49825f14d1b7dda9a2abc0eaae519d7c0a986e8802df091983c330c6ea`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574106f414796bdfe45f81d686c17d256278791e951bb805d23a1864624cd20a`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0dbba1f74a1ce38b5ed919e7bafc5ddf118b6a9111ea35faa296c5a2c2fdb2`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:53b39fbb73a3a209e52e39a9c8c3af93a03cc9de1b69fec9f2a9a55c00abb9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:46064776b5eea6b9723add4a461249ba4867495d368173e1212fe38db00dfce5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80024635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411ed82dfe5a9675836b6d38656c85b281f0ac052ed41230354dcfe828f66c9f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:07 GMT
ADD file:4fbe1e3712cf37c85529cc81e0d03c82085203de00d64b0d669b5996e975925a in / 
# Sat, 04 Feb 2023 06:52:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:17:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 07:17:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 07:17:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:17:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 07:17:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 07:18:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:18:00 GMT
ENV COUCHDB_VERSION=3.1.2
# Sat, 04 Feb 2023 07:18:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 07:18:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 07:18:15 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 07:18:15 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 07:18:15 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Sat, 04 Feb 2023 07:18:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 07:18:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 07:18:16 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 07:18:16 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 07:18:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0cf508b37688dca559387b506062329202aaf08b48be5f55f9278b2a818ad2c9`  
		Last Modified: Sat, 04 Feb 2023 06:56:58 GMT  
		Size: 27.1 MB (27140353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2077aca956be48413850558c99aed2abe9648b6f9b9426c1135e15b89dc335ca`  
		Last Modified: Sat, 04 Feb 2023 07:19:33 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7242eb760000d68511583e5224849d57fcf7a36c0e53982efab6da6ed3e8760b`  
		Last Modified: Sat, 04 Feb 2023 07:19:32 GMT  
		Size: 6.7 MB (6703784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7226bb128a799d16fae1c3ca8f2cc831f56e1a799146562752f3665a224983e6`  
		Last Modified: Sat, 04 Feb 2023 07:19:31 GMT  
		Size: 1.3 MB (1259577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bbbd4823cbeb627c5529042b3857b765bfed971236216aea4249a891e32b90`  
		Last Modified: Sat, 04 Feb 2023 07:19:31 GMT  
		Size: 294.3 KB (294296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8e0827227c253602e25bf3924aed5af3a9d145ac6600ee8c455029b9fb5b5c`  
		Last Modified: Sat, 04 Feb 2023 07:19:31 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e164a9e3abf791c0eeac9d02c8a6eec719f121a806f747749981c78ac8bb00`  
		Last Modified: Sat, 04 Feb 2023 07:19:34 GMT  
		Size: 44.6 MB (44619618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38d19f05fce411a5c7d03595278edfff9be5e29c76b73ea0239127d9eb51f38`  
		Last Modified: Sat, 04 Feb 2023 07:19:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b79dd7eab7bbe21605e7417f3abbe77a6a43bdf6308771b35e69baf0f65434`  
		Last Modified: Sat, 04 Feb 2023 07:19:29 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e3617cd28cde174c912e6e888307d690517dfdd8aa29382578018a337832ef`  
		Last Modified: Sat, 04 Feb 2023 07:19:29 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986e56bb9a0dd25a27c5132c564191e0d145018fef2c9ea4830232820aa46b93`  
		Last Modified: Sat, 04 Feb 2023 07:19:29 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:068cf4b3782452a97c9347f5f7cf97018cf85c390cf250738baf218100b7999e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f730d0ebb1efe32b4c88aeae93dc6b4773ff70b50b38e9c75d2a0231a773f47d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:52 GMT
ADD file:08addf73dde8bf5ac64e0d9bdd1997ce5f406976c19da431616783c14fdb36ac in / 
# Wed, 11 Jan 2023 02:57:52 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:58:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:58:25 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:58:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:58:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:58:36 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:58:42 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 11 Jan 2023 03:58:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:58:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:58:54 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:58:54 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:58:54 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 11 Jan 2023 03:58:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:58:55 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:58:55 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:58:55 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:58:55 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7fac02f4cd2bcf681b9e156a67009cf4609f45447818b52327d93553bfeb2965`  
		Last Modified: Wed, 11 Jan 2023 03:01:58 GMT  
		Size: 25.9 MB (25914925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49c2ee40908e629f9af8a7cab6dd0cd3837146e1417c5687ea458a09e766135`  
		Last Modified: Wed, 11 Jan 2023 04:00:06 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c510231b78ec40191b73fcf37265b834eb84575e8e9e59214e699e0fb2443f23`  
		Last Modified: Wed, 11 Jan 2023 04:00:06 GMT  
		Size: 6.6 MB (6577083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7fa713a90ae4df09d27f1f23a63a2a6e7df1f68b7907280efb3d944b8bd006`  
		Last Modified: Wed, 11 Jan 2023 04:00:05 GMT  
		Size: 1.2 MB (1164501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83d395471dc77d8f630b48a40ec852957fdb479ef92505965c06a0297d3c0f`  
		Last Modified: Wed, 11 Jan 2023 04:00:04 GMT  
		Size: 294.1 KB (294133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2ea83fca2dabeb73ea6c9b6afe718c85e6cf1fbe99a4a2ea231b2e08bbada8`  
		Last Modified: Wed, 11 Jan 2023 04:00:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639e30434c64b9391fcc739fc0e4f5a3fc0405b0fdb1e52addfbce2802c5fd14`  
		Last Modified: Wed, 11 Jan 2023 04:00:06 GMT  
		Size: 41.1 MB (41121896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6265546072ca4d14a307205cad17f850ca4ed021860e18a8fe246b9997bcdda6`  
		Last Modified: Wed, 11 Jan 2023 04:00:02 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a782805964de8364f24425f37c312a88327e815dcefbe8b00d7913483ca1cf45`  
		Last Modified: Wed, 11 Jan 2023 04:00:02 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c69755a439c0f644c08edfed09861b37c19b50a581ba984ae38399d7f8f8e1a`  
		Last Modified: Wed, 11 Jan 2023 04:00:02 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da7ca01a16a2f7d15cd4d9a6365a8fb58bc7414b6a675688eda576855fd9285`  
		Last Modified: Wed, 11 Jan 2023 04:00:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:53b39fbb73a3a209e52e39a9c8c3af93a03cc9de1b69fec9f2a9a55c00abb9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:46064776b5eea6b9723add4a461249ba4867495d368173e1212fe38db00dfce5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80024635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411ed82dfe5a9675836b6d38656c85b281f0ac052ed41230354dcfe828f66c9f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:07 GMT
ADD file:4fbe1e3712cf37c85529cc81e0d03c82085203de00d64b0d669b5996e975925a in / 
# Sat, 04 Feb 2023 06:52:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:17:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 07:17:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 07:17:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:17:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 07:17:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 07:18:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:18:00 GMT
ENV COUCHDB_VERSION=3.1.2
# Sat, 04 Feb 2023 07:18:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 07:18:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 07:18:15 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 07:18:15 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 07:18:15 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Sat, 04 Feb 2023 07:18:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 07:18:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 07:18:16 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 07:18:16 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 07:18:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0cf508b37688dca559387b506062329202aaf08b48be5f55f9278b2a818ad2c9`  
		Last Modified: Sat, 04 Feb 2023 06:56:58 GMT  
		Size: 27.1 MB (27140353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2077aca956be48413850558c99aed2abe9648b6f9b9426c1135e15b89dc335ca`  
		Last Modified: Sat, 04 Feb 2023 07:19:33 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7242eb760000d68511583e5224849d57fcf7a36c0e53982efab6da6ed3e8760b`  
		Last Modified: Sat, 04 Feb 2023 07:19:32 GMT  
		Size: 6.7 MB (6703784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7226bb128a799d16fae1c3ca8f2cc831f56e1a799146562752f3665a224983e6`  
		Last Modified: Sat, 04 Feb 2023 07:19:31 GMT  
		Size: 1.3 MB (1259577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bbbd4823cbeb627c5529042b3857b765bfed971236216aea4249a891e32b90`  
		Last Modified: Sat, 04 Feb 2023 07:19:31 GMT  
		Size: 294.3 KB (294296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8e0827227c253602e25bf3924aed5af3a9d145ac6600ee8c455029b9fb5b5c`  
		Last Modified: Sat, 04 Feb 2023 07:19:31 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e164a9e3abf791c0eeac9d02c8a6eec719f121a806f747749981c78ac8bb00`  
		Last Modified: Sat, 04 Feb 2023 07:19:34 GMT  
		Size: 44.6 MB (44619618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38d19f05fce411a5c7d03595278edfff9be5e29c76b73ea0239127d9eb51f38`  
		Last Modified: Sat, 04 Feb 2023 07:19:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b79dd7eab7bbe21605e7417f3abbe77a6a43bdf6308771b35e69baf0f65434`  
		Last Modified: Sat, 04 Feb 2023 07:19:29 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e3617cd28cde174c912e6e888307d690517dfdd8aa29382578018a337832ef`  
		Last Modified: Sat, 04 Feb 2023 07:19:29 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986e56bb9a0dd25a27c5132c564191e0d145018fef2c9ea4830232820aa46b93`  
		Last Modified: Sat, 04 Feb 2023 07:19:29 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:068cf4b3782452a97c9347f5f7cf97018cf85c390cf250738baf218100b7999e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f730d0ebb1efe32b4c88aeae93dc6b4773ff70b50b38e9c75d2a0231a773f47d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:52 GMT
ADD file:08addf73dde8bf5ac64e0d9bdd1997ce5f406976c19da431616783c14fdb36ac in / 
# Wed, 11 Jan 2023 02:57:52 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:58:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:58:25 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:58:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:58:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:58:36 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:58:42 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 11 Jan 2023 03:58:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:58:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:58:54 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:58:54 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:58:54 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 11 Jan 2023 03:58:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:58:55 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:58:55 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:58:55 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:58:55 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7fac02f4cd2bcf681b9e156a67009cf4609f45447818b52327d93553bfeb2965`  
		Last Modified: Wed, 11 Jan 2023 03:01:58 GMT  
		Size: 25.9 MB (25914925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49c2ee40908e629f9af8a7cab6dd0cd3837146e1417c5687ea458a09e766135`  
		Last Modified: Wed, 11 Jan 2023 04:00:06 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c510231b78ec40191b73fcf37265b834eb84575e8e9e59214e699e0fb2443f23`  
		Last Modified: Wed, 11 Jan 2023 04:00:06 GMT  
		Size: 6.6 MB (6577083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7fa713a90ae4df09d27f1f23a63a2a6e7df1f68b7907280efb3d944b8bd006`  
		Last Modified: Wed, 11 Jan 2023 04:00:05 GMT  
		Size: 1.2 MB (1164501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83d395471dc77d8f630b48a40ec852957fdb479ef92505965c06a0297d3c0f`  
		Last Modified: Wed, 11 Jan 2023 04:00:04 GMT  
		Size: 294.1 KB (294133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2ea83fca2dabeb73ea6c9b6afe718c85e6cf1fbe99a4a2ea231b2e08bbada8`  
		Last Modified: Wed, 11 Jan 2023 04:00:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639e30434c64b9391fcc739fc0e4f5a3fc0405b0fdb1e52addfbce2802c5fd14`  
		Last Modified: Wed, 11 Jan 2023 04:00:06 GMT  
		Size: 41.1 MB (41121896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6265546072ca4d14a307205cad17f850ca4ed021860e18a8fe246b9997bcdda6`  
		Last Modified: Wed, 11 Jan 2023 04:00:02 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a782805964de8364f24425f37c312a88327e815dcefbe8b00d7913483ca1cf45`  
		Last Modified: Wed, 11 Jan 2023 04:00:02 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c69755a439c0f644c08edfed09861b37c19b50a581ba984ae38399d7f8f8e1a`  
		Last Modified: Wed, 11 Jan 2023 04:00:02 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da7ca01a16a2f7d15cd4d9a6365a8fb58bc7414b6a675688eda576855fd9285`  
		Last Modified: Wed, 11 Jan 2023 04:00:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:5392f5f1e8c48f7a3a4771367305a6f1b4928c880129535f60a83a4a157e7f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:eef425ab2025c66119f83c8678dda3e8c9708a8c7e63ac983c3f8e7c61f0bcd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87524351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba914f3f7e2c0514b7d64342ffa01ff61acf217303426fa0cf49bca6c1e16c0d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:16:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 07:16:46 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 07:16:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:16:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 07:16:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 07:17:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:17:19 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Sat, 04 Feb 2023 07:17:20 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 07:17:33 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 07:17:33 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 07:17:33 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 07:17:34 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 04 Feb 2023 07:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 07:17:34 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 07:17:34 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 07:17:34 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 07:17:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77476cf11acd0f8081beb4a23efc99a2652c66cabe691898d51dd54b7a973967`  
		Last Modified: Sat, 04 Feb 2023 07:19:00 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e5ab1e54fdd1586bf4c41713f66e3c3dd536afdf177ab750bac5420e11af8b`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 5.2 MB (5224338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aea5b54023137f626790058724f9349eb5aece02da7ca2ec80ff98cbb34df42`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 1.6 MB (1553311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd561fdfab9d1eed8c99fefa269d1b26ceae1633127918de8c9bba901cd8642e`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 295.6 KB (295625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b17ebcb880f4550003dc3fbf095b2c8ce01f10dc3361a34e678cd2c558165e`  
		Last Modified: Sat, 04 Feb 2023 07:19:17 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de52ef5c29d0fd49050c902d5b9148547baf472c5bdadb0055df8b3ed007b13f`  
		Last Modified: Sat, 04 Feb 2023 07:19:21 GMT  
		Size: 49.0 MB (49047011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5c1db9cc13ba70b8e1acb5074418aad0a2ee7b06788162c2f224e4e6762e89`  
		Last Modified: Sat, 04 Feb 2023 07:19:16 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f266404a325e853abdf4d88321bec76e5820faacfaf74c0f11eedf25681b4e82`  
		Last Modified: Sat, 04 Feb 2023 07:19:16 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4701880f67dd8c277b4992810ee8dd33b9905d7ced59409d0691a302ff0b7ac5`  
		Last Modified: Sat, 04 Feb 2023 07:19:15 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e680e922d77deb270acb9558b2d619a99fd2c1682bd663e7aaa6af801ad65bbe`  
		Last Modified: Sat, 04 Feb 2023 07:19:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:95d32b3ab15184cc130539fe8ba4899ebe65ff946b14787fd836c8944bf47936
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86058193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f789ec44b9bb25bf5e2cef5452bc852089f29219c41c03c3334a31ece6d2e329`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:57:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:57:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:57:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:57:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:57:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:57:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:58:09 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 11 Jan 2023 03:58:09 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:58:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:58:20 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:58:21 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:58:21 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 03:58:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:58:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:58:21 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:58:21 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:58:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961831464917d8a5133f3840f3e3d15b6bb840593a5cbb857f67c46f39d73546`  
		Last Modified: Wed, 11 Jan 2023 03:59:34 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ba419ee6c06e64643e7104acf6aaa7133d872e801ba6d5559cf58a005e1d13`  
		Last Modified: Wed, 11 Jan 2023 03:59:33 GMT  
		Size: 5.2 MB (5209470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2fd7db3c36ccb6f388d0be04337eaf1c4c0b32352e9a7d95b4ae708024cdbd`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 1.4 MB (1435925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7fbb1ce521b1b1a114c87f3991a7a9de1562c8be484357ddc8d03f2f2c1404`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 295.5 KB (295517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dad358ded8610705f625cdcdfcd647d3f5283af0c801fc763ff03a180a30c8`  
		Last Modified: Wed, 11 Jan 2023 03:59:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636d0283b23cdce42cee7bab78df338a1faad0c50cf95b85f98d05bd9390f25f`  
		Last Modified: Wed, 11 Jan 2023 03:59:53 GMT  
		Size: 49.1 MB (49065304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061db316aa0197baafc1ae6f4dee4bc7911a786207b26ea775ceb430f284b12a`  
		Last Modified: Wed, 11 Jan 2023 03:59:48 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7725be66e477a0f061abf8cafd5a073b4a5c9186d6bfad8a8d205156a3a3f3a`  
		Last Modified: Wed, 11 Jan 2023 03:59:48 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa56978aa2219eda9723688003514b9007bbc67dc17d4b2caa3ee2c3b5716fb`  
		Last Modified: Wed, 11 Jan 2023 03:59:48 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f7134d9aaf45c7033d01d8ecacef1f33b44dbe22ee7b250a37e621c8559ea`  
		Last Modified: Wed, 11 Jan 2023 03:59:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:0a1831ce1ba3833784186968dc0198e9de4884616a3e3d01785759cbda93f662
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93211071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8659a551041dd94e4816058f52f1f62a909362325a09a8abef166d2e09b27520`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 12:25:55 GMT
ADD file:2c82cc89d7ac2efeaf54e7589e28644e3e8436d66f6909bf295a2b030116ac58 in / 
# Sat, 04 Feb 2023 12:25:58 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 12:51:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 12:51:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 12:51:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 12:51:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 12:51:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 12:51:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 12:52:36 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Sat, 04 Feb 2023 12:52:37 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 12:53:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 12:53:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 12:53:03 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 12:53:03 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 04 Feb 2023 12:53:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 12:53:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 12:53:05 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 12:53:06 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 12:53:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0604364135762a6c4b3503dd7f0396a51396443bf6052b34b8df7f67679b42c0`  
		Last Modified: Sat, 04 Feb 2023 12:32:12 GMT  
		Size: 35.3 MB (35268795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0db1dae9c381949243f87d00a076dd8935eadd9dfbb4a26770b524da132c28`  
		Last Modified: Sat, 04 Feb 2023 12:53:30 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb94746f03717925610786197b18595ba7711a5da5b2b691065b02f97414f8`  
		Last Modified: Sat, 04 Feb 2023 12:53:30 GMT  
		Size: 6.0 MB (6043885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffda288060566d345a0058dc1b6f9d096be2045f7d3513b4f20c3d02702e267a`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 1.5 MB (1509213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29955520a52a30117d393a5c4ec1010873a9bdc7b3d20b207b28b405b0ff648c`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 295.5 KB (295538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c094478af3456f9e296f86f9168abaad9ed22970ff3afda436e454b258fbd`  
		Last Modified: Sat, 04 Feb 2023 12:53:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3619811146b2fb6872b5e21bfce7b51476595f68962ce09e71beb5af7ba4e564`  
		Last Modified: Sat, 04 Feb 2023 12:54:03 GMT  
		Size: 50.1 MB (50086503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db09c0e44ebe0e99368e2259d49fd60a09a378c0f3db1db86cb73c5443a797e5`  
		Last Modified: Sat, 04 Feb 2023 12:53:54 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fce7736048f051ca62f270940d5b0dca17ba4eb7ab4da055bbf6a220aeca139`  
		Last Modified: Sat, 04 Feb 2023 12:53:54 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5ce9a6f8375a170a8cb95fb41c417e27068b3319ffd3c6667ffc77fa842a82`  
		Last Modified: Sat, 04 Feb 2023 12:53:54 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4b24d52b42b49d361cc6f394acce6691888cbe5e4c9d0090661ce6179e6d0a`  
		Last Modified: Sat, 04 Feb 2023 12:53:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.2`

```console
$ docker pull couchdb@sha256:5392f5f1e8c48f7a3a4771367305a6f1b4928c880129535f60a83a4a157e7f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.2` - linux; amd64

```console
$ docker pull couchdb@sha256:eef425ab2025c66119f83c8678dda3e8c9708a8c7e63ac983c3f8e7c61f0bcd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87524351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba914f3f7e2c0514b7d64342ffa01ff61acf217303426fa0cf49bca6c1e16c0d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:16:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 07:16:46 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 07:16:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:16:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 07:16:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 07:17:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:17:19 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Sat, 04 Feb 2023 07:17:20 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 07:17:33 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 07:17:33 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 07:17:33 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 07:17:34 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 04 Feb 2023 07:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 07:17:34 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 07:17:34 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 07:17:34 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 07:17:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77476cf11acd0f8081beb4a23efc99a2652c66cabe691898d51dd54b7a973967`  
		Last Modified: Sat, 04 Feb 2023 07:19:00 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e5ab1e54fdd1586bf4c41713f66e3c3dd536afdf177ab750bac5420e11af8b`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 5.2 MB (5224338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aea5b54023137f626790058724f9349eb5aece02da7ca2ec80ff98cbb34df42`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 1.6 MB (1553311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd561fdfab9d1eed8c99fefa269d1b26ceae1633127918de8c9bba901cd8642e`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 295.6 KB (295625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b17ebcb880f4550003dc3fbf095b2c8ce01f10dc3361a34e678cd2c558165e`  
		Last Modified: Sat, 04 Feb 2023 07:19:17 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de52ef5c29d0fd49050c902d5b9148547baf472c5bdadb0055df8b3ed007b13f`  
		Last Modified: Sat, 04 Feb 2023 07:19:21 GMT  
		Size: 49.0 MB (49047011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5c1db9cc13ba70b8e1acb5074418aad0a2ee7b06788162c2f224e4e6762e89`  
		Last Modified: Sat, 04 Feb 2023 07:19:16 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f266404a325e853abdf4d88321bec76e5820faacfaf74c0f11eedf25681b4e82`  
		Last Modified: Sat, 04 Feb 2023 07:19:16 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4701880f67dd8c277b4992810ee8dd33b9905d7ced59409d0691a302ff0b7ac5`  
		Last Modified: Sat, 04 Feb 2023 07:19:15 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e680e922d77deb270acb9558b2d619a99fd2c1682bd663e7aaa6af801ad65bbe`  
		Last Modified: Sat, 04 Feb 2023 07:19:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:95d32b3ab15184cc130539fe8ba4899ebe65ff946b14787fd836c8944bf47936
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86058193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f789ec44b9bb25bf5e2cef5452bc852089f29219c41c03c3334a31ece6d2e329`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:57:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:57:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:57:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:57:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:57:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:57:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:58:09 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 11 Jan 2023 03:58:09 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:58:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:58:20 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:58:21 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:58:21 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 03:58:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:58:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:58:21 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:58:21 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:58:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961831464917d8a5133f3840f3e3d15b6bb840593a5cbb857f67c46f39d73546`  
		Last Modified: Wed, 11 Jan 2023 03:59:34 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ba419ee6c06e64643e7104acf6aaa7133d872e801ba6d5559cf58a005e1d13`  
		Last Modified: Wed, 11 Jan 2023 03:59:33 GMT  
		Size: 5.2 MB (5209470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2fd7db3c36ccb6f388d0be04337eaf1c4c0b32352e9a7d95b4ae708024cdbd`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 1.4 MB (1435925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7fbb1ce521b1b1a114c87f3991a7a9de1562c8be484357ddc8d03f2f2c1404`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 295.5 KB (295517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dad358ded8610705f625cdcdfcd647d3f5283af0c801fc763ff03a180a30c8`  
		Last Modified: Wed, 11 Jan 2023 03:59:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636d0283b23cdce42cee7bab78df338a1faad0c50cf95b85f98d05bd9390f25f`  
		Last Modified: Wed, 11 Jan 2023 03:59:53 GMT  
		Size: 49.1 MB (49065304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061db316aa0197baafc1ae6f4dee4bc7911a786207b26ea775ceb430f284b12a`  
		Last Modified: Wed, 11 Jan 2023 03:59:48 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7725be66e477a0f061abf8cafd5a073b4a5c9186d6bfad8a8d205156a3a3f3a`  
		Last Modified: Wed, 11 Jan 2023 03:59:48 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa56978aa2219eda9723688003514b9007bbc67dc17d4b2caa3ee2c3b5716fb`  
		Last Modified: Wed, 11 Jan 2023 03:59:48 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f7134d9aaf45c7033d01d8ecacef1f33b44dbe22ee7b250a37e621c8559ea`  
		Last Modified: Wed, 11 Jan 2023 03:59:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:0a1831ce1ba3833784186968dc0198e9de4884616a3e3d01785759cbda93f662
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93211071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8659a551041dd94e4816058f52f1f62a909362325a09a8abef166d2e09b27520`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 12:25:55 GMT
ADD file:2c82cc89d7ac2efeaf54e7589e28644e3e8436d66f6909bf295a2b030116ac58 in / 
# Sat, 04 Feb 2023 12:25:58 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 12:51:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 12:51:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 12:51:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 12:51:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 12:51:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 12:51:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 12:52:36 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Sat, 04 Feb 2023 12:52:37 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 12:53:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 12:53:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 12:53:03 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 12:53:03 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 04 Feb 2023 12:53:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 12:53:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 12:53:05 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 12:53:06 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 12:53:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0604364135762a6c4b3503dd7f0396a51396443bf6052b34b8df7f67679b42c0`  
		Last Modified: Sat, 04 Feb 2023 12:32:12 GMT  
		Size: 35.3 MB (35268795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0db1dae9c381949243f87d00a076dd8935eadd9dfbb4a26770b524da132c28`  
		Last Modified: Sat, 04 Feb 2023 12:53:30 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb94746f03717925610786197b18595ba7711a5da5b2b691065b02f97414f8`  
		Last Modified: Sat, 04 Feb 2023 12:53:30 GMT  
		Size: 6.0 MB (6043885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffda288060566d345a0058dc1b6f9d096be2045f7d3513b4f20c3d02702e267a`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 1.5 MB (1509213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29955520a52a30117d393a5c4ec1010873a9bdc7b3d20b207b28b405b0ff648c`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 295.5 KB (295538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c094478af3456f9e296f86f9168abaad9ed22970ff3afda436e454b258fbd`  
		Last Modified: Sat, 04 Feb 2023 12:53:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3619811146b2fb6872b5e21bfce7b51476595f68962ce09e71beb5af7ba4e564`  
		Last Modified: Sat, 04 Feb 2023 12:54:03 GMT  
		Size: 50.1 MB (50086503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db09c0e44ebe0e99368e2259d49fd60a09a378c0f3db1db86cb73c5443a797e5`  
		Last Modified: Sat, 04 Feb 2023 12:53:54 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fce7736048f051ca62f270940d5b0dca17ba4eb7ab4da055bbf6a220aeca139`  
		Last Modified: Sat, 04 Feb 2023 12:53:54 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5ce9a6f8375a170a8cb95fb41c417e27068b3319ffd3c6667ffc77fa842a82`  
		Last Modified: Sat, 04 Feb 2023 12:53:54 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4b24d52b42b49d361cc6f394acce6691888cbe5e4c9d0090661ce6179e6d0a`  
		Last Modified: Sat, 04 Feb 2023 12:53:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:58881fc8a4a12abb739fab6ded5677c04a5e04d8a3f61b5ae53286b64dfac9a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:6d588a96a550033c02f45a4ce38c296cbe08f9ec14cdd4f5ca4320d8af8eb00b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91153896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1274dd1bda729da68f2c64f847a63ec5d6634042dbe09ee8fb9ee1810b35493a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:16:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 07:16:46 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 07:16:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:16:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 07:16:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 07:17:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:17:02 GMT
ENV COUCHDB_VERSION=3.3.1
# Sat, 04 Feb 2023 07:17:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 07:17:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 07:17:16 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 07:17:16 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 07:17:16 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 04 Feb 2023 07:17:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 07:17:17 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 07:17:17 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 07:17:17 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 07:17:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77476cf11acd0f8081beb4a23efc99a2652c66cabe691898d51dd54b7a973967`  
		Last Modified: Sat, 04 Feb 2023 07:19:00 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e5ab1e54fdd1586bf4c41713f66e3c3dd536afdf177ab750bac5420e11af8b`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 5.2 MB (5224338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aea5b54023137f626790058724f9349eb5aece02da7ca2ec80ff98cbb34df42`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 1.6 MB (1553311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd561fdfab9d1eed8c99fefa269d1b26ceae1633127918de8c9bba901cd8642e`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 295.6 KB (295625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e24cec0cc44eeb1e0f1880275166759ac0aab64b4dcca3410a217f78fe5e2a`  
		Last Modified: Sat, 04 Feb 2023 07:18:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3132b1e018f6c5014588752194c7ac7ffabf8e0eec4b3528ff1fce2b24a6df5`  
		Last Modified: Sat, 04 Feb 2023 07:19:02 GMT  
		Size: 52.7 MB (52676329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768bc1a4f6854d19062811091a6930b6efd398b9dd84643f35bc1ced44ea5bba`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6b69d74d3c03eb77600518b7afdc0ed80493cd272bfc1c2c664656cf195381`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e138b051b652e40f53e6ace489845ca2a92f430f592f5112730c8b2bce6866aa`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3809ab88d6017f3f38fea418f135f4f8c181568eb8302a3bc9b42f69eea21122`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ed00ba73f951d5f496355f043a50b0c1d28169ff66e1383605c87cd5b26c6144
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89524742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855eaae40b75dc29eb937b8f1d1a345f679ef01cbf689fa45b0637fa2e139c9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:57:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:57:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:57:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:57:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:57:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:57:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 22:08:39 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 11 Jan 2023 22:08:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 22:08:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 22:08:52 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 22:08:52 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 22:08:53 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 22:08:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 22:08:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 22:08:53 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 22:08:53 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 22:08:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961831464917d8a5133f3840f3e3d15b6bb840593a5cbb857f67c46f39d73546`  
		Last Modified: Wed, 11 Jan 2023 03:59:34 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ba419ee6c06e64643e7104acf6aaa7133d872e801ba6d5559cf58a005e1d13`  
		Last Modified: Wed, 11 Jan 2023 03:59:33 GMT  
		Size: 5.2 MB (5209470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2fd7db3c36ccb6f388d0be04337eaf1c4c0b32352e9a7d95b4ae708024cdbd`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 1.4 MB (1435925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7fbb1ce521b1b1a114c87f3991a7a9de1562c8be484357ddc8d03f2f2c1404`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 295.5 KB (295517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5bcd70f03fefccc3314c5bd804107f5ca7ec891100c2e85d481e9b84f377c3`  
		Last Modified: Wed, 11 Jan 2023 22:09:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a54b1952a30cff448a907d4f82fbbac930beeb1bc452c05e9270fef7a3b056e`  
		Last Modified: Wed, 11 Jan 2023 22:09:18 GMT  
		Size: 52.5 MB (52531616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0782ea0b803ce74bf6e5d05e1a11776e25001beb73576a0c42faa330c238eda0`  
		Last Modified: Wed, 11 Jan 2023 22:09:13 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d347329aa65d9c4b005d93d848c27e025f14d6cb638099fafbecd04dbd43c4f7`  
		Last Modified: Wed, 11 Jan 2023 22:09:13 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0736c691206ce54706b7761f838f3cedd9a8c8f72b933d6ee58c55070659bfb5`  
		Last Modified: Wed, 11 Jan 2023 22:09:14 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0d0ee154aca0d4270a4eced51b0e6de35a1d7336bb1dc51549889432ea5afc`  
		Last Modified: Wed, 11 Jan 2023 22:09:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:169c08ffd541c72b2a9615587f87774d4b8047b8a2baeea19668987253ed48fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96660088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcda0be97c2bcc7cd1d4cca5ce768530b9e41fd99a7fb1a0c41e110153f32673`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 12:25:55 GMT
ADD file:2c82cc89d7ac2efeaf54e7589e28644e3e8436d66f6909bf295a2b030116ac58 in / 
# Sat, 04 Feb 2023 12:25:58 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 12:51:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 12:51:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 12:51:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 12:51:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 12:51:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 12:51:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 12:51:50 GMT
ENV COUCHDB_VERSION=3.3.1
# Sat, 04 Feb 2023 12:51:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 12:52:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 12:52:16 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 12:52:16 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 12:52:17 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 04 Feb 2023 12:52:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 12:52:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 12:52:19 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 12:52:19 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 12:52:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0604364135762a6c4b3503dd7f0396a51396443bf6052b34b8df7f67679b42c0`  
		Last Modified: Sat, 04 Feb 2023 12:32:12 GMT  
		Size: 35.3 MB (35268795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0db1dae9c381949243f87d00a076dd8935eadd9dfbb4a26770b524da132c28`  
		Last Modified: Sat, 04 Feb 2023 12:53:30 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb94746f03717925610786197b18595ba7711a5da5b2b691065b02f97414f8`  
		Last Modified: Sat, 04 Feb 2023 12:53:30 GMT  
		Size: 6.0 MB (6043885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffda288060566d345a0058dc1b6f9d096be2045f7d3513b4f20c3d02702e267a`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 1.5 MB (1509213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29955520a52a30117d393a5c4ec1010873a9bdc7b3d20b207b28b405b0ff648c`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 295.5 KB (295538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb000d7900471baa0e0264363864b8b3eeb4c04cdb58e634bd1269c20845e7c7`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a4e664ddc338ba1e6a85ef75b34219f136dbde3d7b1185395835ad562bc6d7`  
		Last Modified: Sat, 04 Feb 2023 12:53:35 GMT  
		Size: 53.5 MB (53535280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b178a6f96077dd23d510229a7e4030f5fc16474f7cc3164854ac56e093b5715d`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952cec49825f14d1b7dda9a2abc0eaae519d7c0a986e8802df091983c330c6ea`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574106f414796bdfe45f81d686c17d256278791e951bb805d23a1864624cd20a`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0dbba1f74a1ce38b5ed919e7bafc5ddf118b6a9111ea35faa296c5a2c2fdb2`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3.1`

```console
$ docker pull couchdb@sha256:58881fc8a4a12abb739fab6ded5677c04a5e04d8a3f61b5ae53286b64dfac9a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:6d588a96a550033c02f45a4ce38c296cbe08f9ec14cdd4f5ca4320d8af8eb00b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91153896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1274dd1bda729da68f2c64f847a63ec5d6634042dbe09ee8fb9ee1810b35493a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:16:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 07:16:46 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 07:16:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:16:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 07:16:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 07:17:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:17:02 GMT
ENV COUCHDB_VERSION=3.3.1
# Sat, 04 Feb 2023 07:17:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 07:17:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 07:17:16 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 07:17:16 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 07:17:16 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 04 Feb 2023 07:17:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 07:17:17 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 07:17:17 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 07:17:17 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 07:17:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77476cf11acd0f8081beb4a23efc99a2652c66cabe691898d51dd54b7a973967`  
		Last Modified: Sat, 04 Feb 2023 07:19:00 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e5ab1e54fdd1586bf4c41713f66e3c3dd536afdf177ab750bac5420e11af8b`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 5.2 MB (5224338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aea5b54023137f626790058724f9349eb5aece02da7ca2ec80ff98cbb34df42`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 1.6 MB (1553311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd561fdfab9d1eed8c99fefa269d1b26ceae1633127918de8c9bba901cd8642e`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 295.6 KB (295625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e24cec0cc44eeb1e0f1880275166759ac0aab64b4dcca3410a217f78fe5e2a`  
		Last Modified: Sat, 04 Feb 2023 07:18:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3132b1e018f6c5014588752194c7ac7ffabf8e0eec4b3528ff1fce2b24a6df5`  
		Last Modified: Sat, 04 Feb 2023 07:19:02 GMT  
		Size: 52.7 MB (52676329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768bc1a4f6854d19062811091a6930b6efd398b9dd84643f35bc1ced44ea5bba`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6b69d74d3c03eb77600518b7afdc0ed80493cd272bfc1c2c664656cf195381`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e138b051b652e40f53e6ace489845ca2a92f430f592f5112730c8b2bce6866aa`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3809ab88d6017f3f38fea418f135f4f8c181568eb8302a3bc9b42f69eea21122`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ed00ba73f951d5f496355f043a50b0c1d28169ff66e1383605c87cd5b26c6144
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89524742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855eaae40b75dc29eb937b8f1d1a345f679ef01cbf689fa45b0637fa2e139c9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:57:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:57:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:57:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:57:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:57:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:57:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 22:08:39 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 11 Jan 2023 22:08:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 22:08:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 22:08:52 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 22:08:52 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 22:08:53 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 22:08:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 22:08:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 22:08:53 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 22:08:53 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 22:08:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961831464917d8a5133f3840f3e3d15b6bb840593a5cbb857f67c46f39d73546`  
		Last Modified: Wed, 11 Jan 2023 03:59:34 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ba419ee6c06e64643e7104acf6aaa7133d872e801ba6d5559cf58a005e1d13`  
		Last Modified: Wed, 11 Jan 2023 03:59:33 GMT  
		Size: 5.2 MB (5209470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2fd7db3c36ccb6f388d0be04337eaf1c4c0b32352e9a7d95b4ae708024cdbd`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 1.4 MB (1435925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7fbb1ce521b1b1a114c87f3991a7a9de1562c8be484357ddc8d03f2f2c1404`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 295.5 KB (295517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5bcd70f03fefccc3314c5bd804107f5ca7ec891100c2e85d481e9b84f377c3`  
		Last Modified: Wed, 11 Jan 2023 22:09:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a54b1952a30cff448a907d4f82fbbac930beeb1bc452c05e9270fef7a3b056e`  
		Last Modified: Wed, 11 Jan 2023 22:09:18 GMT  
		Size: 52.5 MB (52531616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0782ea0b803ce74bf6e5d05e1a11776e25001beb73576a0c42faa330c238eda0`  
		Last Modified: Wed, 11 Jan 2023 22:09:13 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d347329aa65d9c4b005d93d848c27e025f14d6cb638099fafbecd04dbd43c4f7`  
		Last Modified: Wed, 11 Jan 2023 22:09:13 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0736c691206ce54706b7761f838f3cedd9a8c8f72b933d6ee58c55070659bfb5`  
		Last Modified: Wed, 11 Jan 2023 22:09:14 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0d0ee154aca0d4270a4eced51b0e6de35a1d7336bb1dc51549889432ea5afc`  
		Last Modified: Wed, 11 Jan 2023 22:09:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:169c08ffd541c72b2a9615587f87774d4b8047b8a2baeea19668987253ed48fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96660088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcda0be97c2bcc7cd1d4cca5ce768530b9e41fd99a7fb1a0c41e110153f32673`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 12:25:55 GMT
ADD file:2c82cc89d7ac2efeaf54e7589e28644e3e8436d66f6909bf295a2b030116ac58 in / 
# Sat, 04 Feb 2023 12:25:58 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 12:51:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 12:51:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 12:51:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 12:51:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 12:51:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 12:51:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 12:51:50 GMT
ENV COUCHDB_VERSION=3.3.1
# Sat, 04 Feb 2023 12:51:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 12:52:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 12:52:16 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 12:52:16 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 12:52:17 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 04 Feb 2023 12:52:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 12:52:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 12:52:19 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 12:52:19 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 12:52:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0604364135762a6c4b3503dd7f0396a51396443bf6052b34b8df7f67679b42c0`  
		Last Modified: Sat, 04 Feb 2023 12:32:12 GMT  
		Size: 35.3 MB (35268795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0db1dae9c381949243f87d00a076dd8935eadd9dfbb4a26770b524da132c28`  
		Last Modified: Sat, 04 Feb 2023 12:53:30 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb94746f03717925610786197b18595ba7711a5da5b2b691065b02f97414f8`  
		Last Modified: Sat, 04 Feb 2023 12:53:30 GMT  
		Size: 6.0 MB (6043885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffda288060566d345a0058dc1b6f9d096be2045f7d3513b4f20c3d02702e267a`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 1.5 MB (1509213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29955520a52a30117d393a5c4ec1010873a9bdc7b3d20b207b28b405b0ff648c`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 295.5 KB (295538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb000d7900471baa0e0264363864b8b3eeb4c04cdb58e634bd1269c20845e7c7`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a4e664ddc338ba1e6a85ef75b34219f136dbde3d7b1185395835ad562bc6d7`  
		Last Modified: Sat, 04 Feb 2023 12:53:35 GMT  
		Size: 53.5 MB (53535280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b178a6f96077dd23d510229a7e4030f5fc16474f7cc3164854ac56e093b5715d`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952cec49825f14d1b7dda9a2abc0eaae519d7c0a986e8802df091983c330c6ea`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574106f414796bdfe45f81d686c17d256278791e951bb805d23a1864624cd20a`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0dbba1f74a1ce38b5ed919e7bafc5ddf118b6a9111ea35faa296c5a2c2fdb2`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:58881fc8a4a12abb739fab6ded5677c04a5e04d8a3f61b5ae53286b64dfac9a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:6d588a96a550033c02f45a4ce38c296cbe08f9ec14cdd4f5ca4320d8af8eb00b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91153896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1274dd1bda729da68f2c64f847a63ec5d6634042dbe09ee8fb9ee1810b35493a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:16:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 07:16:46 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 07:16:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:16:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 07:16:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 07:17:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:17:02 GMT
ENV COUCHDB_VERSION=3.3.1
# Sat, 04 Feb 2023 07:17:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 07:17:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 07:17:16 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 07:17:16 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 07:17:16 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 04 Feb 2023 07:17:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 07:17:17 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 07:17:17 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 07:17:17 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 07:17:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77476cf11acd0f8081beb4a23efc99a2652c66cabe691898d51dd54b7a973967`  
		Last Modified: Sat, 04 Feb 2023 07:19:00 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e5ab1e54fdd1586bf4c41713f66e3c3dd536afdf177ab750bac5420e11af8b`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 5.2 MB (5224338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aea5b54023137f626790058724f9349eb5aece02da7ca2ec80ff98cbb34df42`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 1.6 MB (1553311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd561fdfab9d1eed8c99fefa269d1b26ceae1633127918de8c9bba901cd8642e`  
		Last Modified: Sat, 04 Feb 2023 07:18:59 GMT  
		Size: 295.6 KB (295625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e24cec0cc44eeb1e0f1880275166759ac0aab64b4dcca3410a217f78fe5e2a`  
		Last Modified: Sat, 04 Feb 2023 07:18:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3132b1e018f6c5014588752194c7ac7ffabf8e0eec4b3528ff1fce2b24a6df5`  
		Last Modified: Sat, 04 Feb 2023 07:19:02 GMT  
		Size: 52.7 MB (52676329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768bc1a4f6854d19062811091a6930b6efd398b9dd84643f35bc1ced44ea5bba`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6b69d74d3c03eb77600518b7afdc0ed80493cd272bfc1c2c664656cf195381`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e138b051b652e40f53e6ace489845ca2a92f430f592f5112730c8b2bce6866aa`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3809ab88d6017f3f38fea418f135f4f8c181568eb8302a3bc9b42f69eea21122`  
		Last Modified: Sat, 04 Feb 2023 07:18:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ed00ba73f951d5f496355f043a50b0c1d28169ff66e1383605c87cd5b26c6144
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89524742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855eaae40b75dc29eb937b8f1d1a345f679ef01cbf689fa45b0637fa2e139c9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:57:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:57:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:57:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:57:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:57:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:57:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 22:08:39 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 11 Jan 2023 22:08:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 22:08:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 22:08:52 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 22:08:52 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 22:08:53 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 22:08:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 22:08:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 22:08:53 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 22:08:53 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 22:08:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961831464917d8a5133f3840f3e3d15b6bb840593a5cbb857f67c46f39d73546`  
		Last Modified: Wed, 11 Jan 2023 03:59:34 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ba419ee6c06e64643e7104acf6aaa7133d872e801ba6d5559cf58a005e1d13`  
		Last Modified: Wed, 11 Jan 2023 03:59:33 GMT  
		Size: 5.2 MB (5209470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2fd7db3c36ccb6f388d0be04337eaf1c4c0b32352e9a7d95b4ae708024cdbd`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 1.4 MB (1435925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7fbb1ce521b1b1a114c87f3991a7a9de1562c8be484357ddc8d03f2f2c1404`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 295.5 KB (295517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5bcd70f03fefccc3314c5bd804107f5ca7ec891100c2e85d481e9b84f377c3`  
		Last Modified: Wed, 11 Jan 2023 22:09:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a54b1952a30cff448a907d4f82fbbac930beeb1bc452c05e9270fef7a3b056e`  
		Last Modified: Wed, 11 Jan 2023 22:09:18 GMT  
		Size: 52.5 MB (52531616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0782ea0b803ce74bf6e5d05e1a11776e25001beb73576a0c42faa330c238eda0`  
		Last Modified: Wed, 11 Jan 2023 22:09:13 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d347329aa65d9c4b005d93d848c27e025f14d6cb638099fafbecd04dbd43c4f7`  
		Last Modified: Wed, 11 Jan 2023 22:09:13 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0736c691206ce54706b7761f838f3cedd9a8c8f72b933d6ee58c55070659bfb5`  
		Last Modified: Wed, 11 Jan 2023 22:09:14 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0d0ee154aca0d4270a4eced51b0e6de35a1d7336bb1dc51549889432ea5afc`  
		Last Modified: Wed, 11 Jan 2023 22:09:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:169c08ffd541c72b2a9615587f87774d4b8047b8a2baeea19668987253ed48fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96660088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcda0be97c2bcc7cd1d4cca5ce768530b9e41fd99a7fb1a0c41e110153f32673`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 04 Feb 2023 12:25:55 GMT
ADD file:2c82cc89d7ac2efeaf54e7589e28644e3e8436d66f6909bf295a2b030116ac58 in / 
# Sat, 04 Feb 2023 12:25:58 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 12:51:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 04 Feb 2023 12:51:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 04 Feb 2023 12:51:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 12:51:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 04 Feb 2023 12:51:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 04 Feb 2023 12:51:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 12:51:50 GMT
ENV COUCHDB_VERSION=3.3.1
# Sat, 04 Feb 2023 12:51:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 04 Feb 2023 12:52:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Feb 2023 12:52:16 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 04 Feb 2023 12:52:16 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Sat, 04 Feb 2023 12:52:17 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 04 Feb 2023 12:52:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 12:52:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 12:52:19 GMT
VOLUME [/opt/couchdb/data]
# Sat, 04 Feb 2023 12:52:19 GMT
EXPOSE 4369 5984 9100
# Sat, 04 Feb 2023 12:52:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0604364135762a6c4b3503dd7f0396a51396443bf6052b34b8df7f67679b42c0`  
		Last Modified: Sat, 04 Feb 2023 12:32:12 GMT  
		Size: 35.3 MB (35268795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0db1dae9c381949243f87d00a076dd8935eadd9dfbb4a26770b524da132c28`  
		Last Modified: Sat, 04 Feb 2023 12:53:30 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb94746f03717925610786197b18595ba7711a5da5b2b691065b02f97414f8`  
		Last Modified: Sat, 04 Feb 2023 12:53:30 GMT  
		Size: 6.0 MB (6043885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffda288060566d345a0058dc1b6f9d096be2045f7d3513b4f20c3d02702e267a`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 1.5 MB (1509213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29955520a52a30117d393a5c4ec1010873a9bdc7b3d20b207b28b405b0ff648c`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 295.5 KB (295538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb000d7900471baa0e0264363864b8b3eeb4c04cdb58e634bd1269c20845e7c7`  
		Last Modified: Sat, 04 Feb 2023 12:53:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a4e664ddc338ba1e6a85ef75b34219f136dbde3d7b1185395835ad562bc6d7`  
		Last Modified: Sat, 04 Feb 2023 12:53:35 GMT  
		Size: 53.5 MB (53535280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b178a6f96077dd23d510229a7e4030f5fc16474f7cc3164854ac56e093b5715d`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952cec49825f14d1b7dda9a2abc0eaae519d7c0a986e8802df091983c330c6ea`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574106f414796bdfe45f81d686c17d256278791e951bb805d23a1864624cd20a`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0dbba1f74a1ce38b5ed919e7bafc5ddf118b6a9111ea35faa296c5a2c2fdb2`  
		Last Modified: Sat, 04 Feb 2023 12:53:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
