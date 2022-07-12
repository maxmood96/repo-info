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
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:47f69daf37966835a440b15b83dd8d41e0673498487b41d38759c5b4f42bfef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:89ec990c38a98c072461b37efc3fdd3e6af059d26bab0bc14ca0c03a75eb9a29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7730f520a9e0d91cc76a3b1213178dc8c039c5f847aba061618f531f13e9b598`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:33 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 23 Jun 2022 01:07:33 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:52 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:53 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:53 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02b79ba8f20a74d6043fa2f3eceab9cb4311187e228e822cedc254f3c158b7`  
		Last Modified: Thu, 23 Jun 2022 01:08:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b44dcfa4a8386763976c2fa29204037a9051563713501777f0b060e85e38bb1`  
		Last Modified: Thu, 23 Jun 2022 01:08:53 GMT  
		Size: 49.1 MB (49127735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb73a35366ebb8c0aa3c79869555b534dabcb30bc834f9457de16c3681034e4f`  
		Last Modified: Thu, 23 Jun 2022 01:08:48 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c0c6f989ed30ae055bd89195fdc6a7330b0ec131d12fd1b3b277e8319d4f10`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f7fc0dd5f8432ce4345dadaeb1a417adf17681a5d1c27cbd407149d546d862`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ac49a371125c8caea5047c3e01280a947350ace78997afcd09bf91c05ab518`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:355ed9523a7a8317b718ab796784fa80c2fa05ca5dba93de53407f86a3f189e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72533064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e19c99a1fd34dcade109917f0241eaa5d6d359bd02ef2342b8f5faf1a3431a0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:02 GMT
ADD file:d6b43ca12a2cc7f73a66ace962f04878f02eab9345172028d77c21d3dc94fe0c in / 
# Tue, 12 Jul 2022 00:41:03 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:47:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jul 2022 02:47:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jul 2022 02:47:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:47:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Jul 2022 02:47:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Jul 2022 02:47:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:19 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 12 Jul 2022 02:48:20 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Jul 2022 02:48:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jul 2022 02:48:35 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jul 2022 02:48:36 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jul 2022 02:48:37 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 12 Jul 2022 02:48:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jul 2022 02:48:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 02:48:39 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jul 2022 02:48:40 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jul 2022 02:48:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8bd5501da4f4b37ad7488bd0eafa32d8927de3bf1e32747545810f2ca65429ed`  
		Last Modified: Tue, 12 Jul 2022 00:47:14 GMT  
		Size: 25.9 MB (25914236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c58fdb695fab9d1860c0b7b39046c6784937d1027efd6f068838d4caa7bde5`  
		Last Modified: Tue, 12 Jul 2022 02:49:35 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825159866a69517714b95f237a7ec44e15ca449d875008a1a218e1e24a5e2c63`  
		Last Modified: Tue, 12 Jul 2022 02:49:34 GMT  
		Size: 6.6 MB (6557100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b91311a9e4b93f1de681be6625b25b5d15a7ee3e8b9942bd5f18dcc02e8e98`  
		Last Modified: Tue, 12 Jul 2022 02:49:34 GMT  
		Size: 951.2 KB (951169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8c11983a2370cf06d7efa7fa81397e4de4f3d2e526d516ff5cc4045251870`  
		Last Modified: Tue, 12 Jul 2022 02:49:33 GMT  
		Size: 79.9 KB (79948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752116e0ca384297da80ac14c9d153ae52ff9da66d35bc97953a3f2d2ff02bc1`  
		Last Modified: Tue, 12 Jul 2022 02:49:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbc972fb3972fcac64fd9b6e7da3191bff401c34244c7dff8e1d7d6c8015658`  
		Last Modified: Tue, 12 Jul 2022 02:49:52 GMT  
		Size: 39.0 MB (39023687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950c6291aefa5ea57c3ac35c3a7834874c61847946600e2d4a475959cba30eab`  
		Last Modified: Tue, 12 Jul 2022 02:49:48 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b6869547059369e49719c56ebadd9e5b92efcc44fce9415ceb6063558706de`  
		Last Modified: Tue, 12 Jul 2022 02:49:48 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a16d7d2769eca455b423dc7ad9d19a25c68db54eb5fc14fef0a2f6e97ef5b6d`  
		Last Modified: Tue, 12 Jul 2022 02:49:48 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573faf24fbf357fd07235ba4ec3227bda196f486796e680765e323431ef61703`  
		Last Modified: Tue, 12 Jul 2022 02:49:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:47f69daf37966835a440b15b83dd8d41e0673498487b41d38759c5b4f42bfef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:89ec990c38a98c072461b37efc3fdd3e6af059d26bab0bc14ca0c03a75eb9a29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7730f520a9e0d91cc76a3b1213178dc8c039c5f847aba061618f531f13e9b598`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:33 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 23 Jun 2022 01:07:33 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:52 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:53 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:53 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02b79ba8f20a74d6043fa2f3eceab9cb4311187e228e822cedc254f3c158b7`  
		Last Modified: Thu, 23 Jun 2022 01:08:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b44dcfa4a8386763976c2fa29204037a9051563713501777f0b060e85e38bb1`  
		Last Modified: Thu, 23 Jun 2022 01:08:53 GMT  
		Size: 49.1 MB (49127735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb73a35366ebb8c0aa3c79869555b534dabcb30bc834f9457de16c3681034e4f`  
		Last Modified: Thu, 23 Jun 2022 01:08:48 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c0c6f989ed30ae055bd89195fdc6a7330b0ec131d12fd1b3b277e8319d4f10`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f7fc0dd5f8432ce4345dadaeb1a417adf17681a5d1c27cbd407149d546d862`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ac49a371125c8caea5047c3e01280a947350ace78997afcd09bf91c05ab518`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:355ed9523a7a8317b718ab796784fa80c2fa05ca5dba93de53407f86a3f189e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72533064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e19c99a1fd34dcade109917f0241eaa5d6d359bd02ef2342b8f5faf1a3431a0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:02 GMT
ADD file:d6b43ca12a2cc7f73a66ace962f04878f02eab9345172028d77c21d3dc94fe0c in / 
# Tue, 12 Jul 2022 00:41:03 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:47:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jul 2022 02:47:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jul 2022 02:47:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:47:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Jul 2022 02:47:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Jul 2022 02:47:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:19 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 12 Jul 2022 02:48:20 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Jul 2022 02:48:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jul 2022 02:48:35 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jul 2022 02:48:36 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jul 2022 02:48:37 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 12 Jul 2022 02:48:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jul 2022 02:48:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 02:48:39 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jul 2022 02:48:40 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jul 2022 02:48:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8bd5501da4f4b37ad7488bd0eafa32d8927de3bf1e32747545810f2ca65429ed`  
		Last Modified: Tue, 12 Jul 2022 00:47:14 GMT  
		Size: 25.9 MB (25914236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c58fdb695fab9d1860c0b7b39046c6784937d1027efd6f068838d4caa7bde5`  
		Last Modified: Tue, 12 Jul 2022 02:49:35 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825159866a69517714b95f237a7ec44e15ca449d875008a1a218e1e24a5e2c63`  
		Last Modified: Tue, 12 Jul 2022 02:49:34 GMT  
		Size: 6.6 MB (6557100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b91311a9e4b93f1de681be6625b25b5d15a7ee3e8b9942bd5f18dcc02e8e98`  
		Last Modified: Tue, 12 Jul 2022 02:49:34 GMT  
		Size: 951.2 KB (951169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8c11983a2370cf06d7efa7fa81397e4de4f3d2e526d516ff5cc4045251870`  
		Last Modified: Tue, 12 Jul 2022 02:49:33 GMT  
		Size: 79.9 KB (79948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752116e0ca384297da80ac14c9d153ae52ff9da66d35bc97953a3f2d2ff02bc1`  
		Last Modified: Tue, 12 Jul 2022 02:49:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbc972fb3972fcac64fd9b6e7da3191bff401c34244c7dff8e1d7d6c8015658`  
		Last Modified: Tue, 12 Jul 2022 02:49:52 GMT  
		Size: 39.0 MB (39023687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950c6291aefa5ea57c3ac35c3a7834874c61847946600e2d4a475959cba30eab`  
		Last Modified: Tue, 12 Jul 2022 02:49:48 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b6869547059369e49719c56ebadd9e5b92efcc44fce9415ceb6063558706de`  
		Last Modified: Tue, 12 Jul 2022 02:49:48 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a16d7d2769eca455b423dc7ad9d19a25c68db54eb5fc14fef0a2f6e97ef5b6d`  
		Last Modified: Tue, 12 Jul 2022 02:49:48 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573faf24fbf357fd07235ba4ec3227bda196f486796e680765e323431ef61703`  
		Last Modified: Tue, 12 Jul 2022 02:49:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:47f69daf37966835a440b15b83dd8d41e0673498487b41d38759c5b4f42bfef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:89ec990c38a98c072461b37efc3fdd3e6af059d26bab0bc14ca0c03a75eb9a29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7730f520a9e0d91cc76a3b1213178dc8c039c5f847aba061618f531f13e9b598`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:33 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 23 Jun 2022 01:07:33 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:52 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:53 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:53 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02b79ba8f20a74d6043fa2f3eceab9cb4311187e228e822cedc254f3c158b7`  
		Last Modified: Thu, 23 Jun 2022 01:08:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b44dcfa4a8386763976c2fa29204037a9051563713501777f0b060e85e38bb1`  
		Last Modified: Thu, 23 Jun 2022 01:08:53 GMT  
		Size: 49.1 MB (49127735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb73a35366ebb8c0aa3c79869555b534dabcb30bc834f9457de16c3681034e4f`  
		Last Modified: Thu, 23 Jun 2022 01:08:48 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c0c6f989ed30ae055bd89195fdc6a7330b0ec131d12fd1b3b277e8319d4f10`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f7fc0dd5f8432ce4345dadaeb1a417adf17681a5d1c27cbd407149d546d862`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ac49a371125c8caea5047c3e01280a947350ace78997afcd09bf91c05ab518`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:355ed9523a7a8317b718ab796784fa80c2fa05ca5dba93de53407f86a3f189e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72533064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e19c99a1fd34dcade109917f0241eaa5d6d359bd02ef2342b8f5faf1a3431a0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:02 GMT
ADD file:d6b43ca12a2cc7f73a66ace962f04878f02eab9345172028d77c21d3dc94fe0c in / 
# Tue, 12 Jul 2022 00:41:03 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:47:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jul 2022 02:47:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jul 2022 02:47:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:47:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Jul 2022 02:47:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Jul 2022 02:47:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:19 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 12 Jul 2022 02:48:20 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Jul 2022 02:48:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jul 2022 02:48:35 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jul 2022 02:48:36 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jul 2022 02:48:37 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 12 Jul 2022 02:48:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jul 2022 02:48:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 02:48:39 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jul 2022 02:48:40 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jul 2022 02:48:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8bd5501da4f4b37ad7488bd0eafa32d8927de3bf1e32747545810f2ca65429ed`  
		Last Modified: Tue, 12 Jul 2022 00:47:14 GMT  
		Size: 25.9 MB (25914236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c58fdb695fab9d1860c0b7b39046c6784937d1027efd6f068838d4caa7bde5`  
		Last Modified: Tue, 12 Jul 2022 02:49:35 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825159866a69517714b95f237a7ec44e15ca449d875008a1a218e1e24a5e2c63`  
		Last Modified: Tue, 12 Jul 2022 02:49:34 GMT  
		Size: 6.6 MB (6557100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b91311a9e4b93f1de681be6625b25b5d15a7ee3e8b9942bd5f18dcc02e8e98`  
		Last Modified: Tue, 12 Jul 2022 02:49:34 GMT  
		Size: 951.2 KB (951169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8c11983a2370cf06d7efa7fa81397e4de4f3d2e526d516ff5cc4045251870`  
		Last Modified: Tue, 12 Jul 2022 02:49:33 GMT  
		Size: 79.9 KB (79948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752116e0ca384297da80ac14c9d153ae52ff9da66d35bc97953a3f2d2ff02bc1`  
		Last Modified: Tue, 12 Jul 2022 02:49:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbc972fb3972fcac64fd9b6e7da3191bff401c34244c7dff8e1d7d6c8015658`  
		Last Modified: Tue, 12 Jul 2022 02:49:52 GMT  
		Size: 39.0 MB (39023687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950c6291aefa5ea57c3ac35c3a7834874c61847946600e2d4a475959cba30eab`  
		Last Modified: Tue, 12 Jul 2022 02:49:48 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b6869547059369e49719c56ebadd9e5b92efcc44fce9415ceb6063558706de`  
		Last Modified: Tue, 12 Jul 2022 02:49:48 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a16d7d2769eca455b423dc7ad9d19a25c68db54eb5fc14fef0a2f6e97ef5b6d`  
		Last Modified: Tue, 12 Jul 2022 02:49:48 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573faf24fbf357fd07235ba4ec3227bda196f486796e680765e323431ef61703`  
		Last Modified: Tue, 12 Jul 2022 02:49:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:5206fe4fe9f6b264b3db516efcbbf5f8f9dec6e6670cc6f58fd1d31f6bc4526a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:3ea7f178b119a1bbd2adbec78486241a087ba35d1d3ec9128a3ada704d55ec97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87498751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9d2dcf03aa6b53788baca7b138c9069926ce70119f77c999d0e2d0858e21d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:06:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:06:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:35 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:06:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:06:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:06:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:06:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:06:50 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:06:50 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:06:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b67ef10ab3031244bf995ed483d30c4423feb9f42f12d55c8511d7497c931`  
		Last Modified: Thu, 23 Jun 2022 01:08:14 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd945ed68b3fecb83857780d70642d81019952136407b87a9f4b6b94711e7dda`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 5.2 MB (5224047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1d67ad9668554764252390c4e5b06fb0f33517e33a831601a00c10a05cfbe7`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 1.6 MB (1553288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b56aaaffae17f3010ab5ba52d88e22126a8b18f5f8fd49ea4a01655c55e20b`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 295.6 KB (295555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e601de752a6ea7ddb9a0b7201437219d647dd0a6555b1d9f48ae8d94004f40`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd769730295be73a2aae5a0882ad80bb9284ad34c68bff96c93ccd15f3cc73`  
		Last Modified: Thu, 23 Jun 2022 01:08:15 GMT  
		Size: 49.0 MB (49039317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0fe21a89a509108c6d599b399458e374353649854cc07814e901deb7030198`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9700366d2b2b831d620b0ee23a1b1ed39c86a91aa69aaad560465e5dd33889`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd356f58092365eb5086db70cc449f1fce114ea73ac0ee9bc18298ac6c579120`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f797d1e3134f5eda53222acba18a0644f920f20c2431b5b3604ab90b7d882c09`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5985d1edef0613a93f2d7349a7cac2296ec956674df1f96d70d4eb23e83e6f80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85620381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b9e4e79dd10c80e29a2fecb5f9f3cd3e32d7c80f8b4b27fa3fc05d20cabf57`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:46:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jul 2022 02:46:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jul 2022 02:46:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:46:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Jul 2022 02:46:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Jul 2022 02:46:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:46:55 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 12 Jul 2022 02:46:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Jul 2022 02:47:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jul 2022 02:47:15 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jul 2022 02:47:16 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jul 2022 02:47:17 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 12 Jul 2022 02:47:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jul 2022 02:47:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 02:47:19 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jul 2022 02:47:20 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jul 2022 02:47:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7465db9b62d8b48810be110d459aefd7c0ad081513d833783a7562aef41e78d6`  
		Last Modified: Tue, 12 Jul 2022 02:49:11 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a3cff592ded12e484f1d97dcf8f9085ef644409ec4e2f18ad6c98d164e5d92`  
		Last Modified: Tue, 12 Jul 2022 02:49:09 GMT  
		Size: 5.2 MB (5207875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814d3780ef73deb609aa55ea065baba3d62461fab745d182156f44df4f37e219`  
		Last Modified: Tue, 12 Jul 2022 02:49:09 GMT  
		Size: 1.2 MB (1221085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd2b2b81e061ce298724584ab5f3607d132f085d872fdbcc1dd60e522373aa`  
		Last Modified: Tue, 12 Jul 2022 02:49:08 GMT  
		Size: 79.2 KB (79211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff676fcdcdd823ef08a4e8a1d6c970a5251eca7b127e65d1b09d000795e276f`  
		Last Modified: Tue, 12 Jul 2022 02:49:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c9e9d309e749b3822eb0c85e7ac1fe7b0ab46593eada60518f1037359952bd`  
		Last Modified: Tue, 12 Jul 2022 02:49:12 GMT  
		Size: 49.1 MB (49050941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56f7299ebdeade54cc83b0c17918710c993136a0e7d6d507f1db40f4271d455`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51cc2dbe5f24b3287814a216d05c221d724e80a8b62e119ecdd8fe30324a08d`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3df456dccfc3e68a1699f2788eacd3e05451ea656f405247b2ad4609874e31f`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 2.2 KB (2182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7b2d14d653177d0efbeb4d6b5feae31470ea31c924de3eca9c94e52c947358`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f667d0d4bf4acaeade0cf8510a4a1384ccd66c08e4ab0b678afb7f8651b9df41
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93209105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97be31cf5f19a6aab7d3705cac0a30da778d2cbabcc7b65e8e3e83d9ee69130d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jul 2022 01:25:28 GMT
ADD file:9e1afe48f40d94f879aefb12a7e68da2f0772d701e95b8219bd1f79a83e1933a in / 
# Tue, 12 Jul 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 05:07:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jul 2022 05:07:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jul 2022 05:08:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:08:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Jul 2022 05:08:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Jul 2022 05:09:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:09:16 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 12 Jul 2022 05:09:23 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Jul 2022 05:10:03 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jul 2022 05:10:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jul 2022 05:10:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jul 2022 05:10:11 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 12 Jul 2022 05:10:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jul 2022 05:10:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 05:10:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jul 2022 05:10:23 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jul 2022 05:10:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bd3d68d1ce583727f6378a16916795b955cc0ad39e0ebe754a26007ef54744fa`  
		Last Modified: Tue, 12 Jul 2022 01:36:03 GMT  
		Size: 35.3 MB (35272500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a816b1ecbe21c2d3295accb57f0a22f554c6ae767a70a4484a89694de329ad9`  
		Last Modified: Tue, 12 Jul 2022 05:10:57 GMT  
		Size: 3.4 KB (3418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0271d8dbcf501c744e33bf898b77265aca81898b869df5041a1c06d2d83ebe24`  
		Last Modified: Tue, 12 Jul 2022 05:10:55 GMT  
		Size: 6.0 MB (6043843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d3674eea9ced378725126b264323f3f0ff2d6990cec832c16bc105b0b16f5a`  
		Last Modified: Tue, 12 Jul 2022 05:10:55 GMT  
		Size: 1.5 MB (1509243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfd2a8749ad2d263caf1ce37413c496a7e3ade1b931c6b26f4b82f81050103d`  
		Last Modified: Tue, 12 Jul 2022 05:10:54 GMT  
		Size: 295.6 KB (295598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833f3e58c97f3db47bdb1766af1a03ba46192031bb9abbc9ff462c336824e462`  
		Last Modified: Tue, 12 Jul 2022 05:10:54 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfc470b8465c993edaa1fb6e3020c7f3a92508d3d0d83be1129f76b54ca5109`  
		Last Modified: Tue, 12 Jul 2022 05:10:59 GMT  
		Size: 50.1 MB (50080767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897291542ee6f3dbd4072e3c7b03d581285986087d05aa1228d6b8ba0032933`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67268035999ecdd7d95f95dcc3e1b15d74a7f086a262ca5bd93c908a9ade4843`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c09171a9b0a8bdba4afb1e5b703ae97ee3436fb56351df60835ba63cf1416`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ff2a8c18f301fb8ac4ff92fcd9631f382e7282d6483e951f29a82ab8bc08e`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:f24cc2f6267718f98fb2e2b5f61eab8f463e0f3ac86a47d5ea17eb1fd22b9009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:f5e1d26a55dca17d784c1f2b9f669b81abac7ef6338e7eea1521a44df2fa2f21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80009555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d833bfc7acc1bf6fb4701f88ab1edd3d6175e9fae0d5e5c87a0f63be9ea39785`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:10 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 23 Jun 2022 01:07:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:24 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:25 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:25 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:26 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab9ba22220b6188d53d6fc816b63e62996f696e875a21ba2861e839ec5a6861`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdda34c0972965fdcda16044c6018c724818515b86c4c58acf9c1b051b20858`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 44.6 MB (44612451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a85c10523399f67c5c6eefeda3cdd2db8d6ba9dae6f6ef9733ed4d1754e9553`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea223f715c88770fbcef6e32b8cb5f10171bdbe81362aec840af62e8fe3b03d`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35c25494b5c7fa8293dd4ada6b829e1802920894aaad64c7feb17e29b0057e0`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed9f94e6c2271887064031d91d640c36b409089a60fa5db5f7ef0734c643e48`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c4a4be0e8d4275d43397c8daf76b1f3bf3d1388aab26d6fbad00a80bbbdbc0d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74621834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42596514619ac7baa0da65c4ed1a0ec5ae6ce7e2ee3dfe4e7a0ada684205fb78`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:02 GMT
ADD file:d6b43ca12a2cc7f73a66ace962f04878f02eab9345172028d77c21d3dc94fe0c in / 
# Tue, 12 Jul 2022 00:41:03 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:47:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jul 2022 02:47:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jul 2022 02:47:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:47:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Jul 2022 02:47:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Jul 2022 02:47:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:47:48 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 12 Jul 2022 02:47:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Jul 2022 02:48:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jul 2022 02:48:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jul 2022 02:48:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jul 2022 02:48:10 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jul 2022 02:48:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jul 2022 02:48:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 02:48:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jul 2022 02:48:13 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jul 2022 02:48:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8bd5501da4f4b37ad7488bd0eafa32d8927de3bf1e32747545810f2ca65429ed`  
		Last Modified: Tue, 12 Jul 2022 00:47:14 GMT  
		Size: 25.9 MB (25914236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c58fdb695fab9d1860c0b7b39046c6784937d1027efd6f068838d4caa7bde5`  
		Last Modified: Tue, 12 Jul 2022 02:49:35 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825159866a69517714b95f237a7ec44e15ca449d875008a1a218e1e24a5e2c63`  
		Last Modified: Tue, 12 Jul 2022 02:49:34 GMT  
		Size: 6.6 MB (6557100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b91311a9e4b93f1de681be6625b25b5d15a7ee3e8b9942bd5f18dcc02e8e98`  
		Last Modified: Tue, 12 Jul 2022 02:49:34 GMT  
		Size: 951.2 KB (951169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8c11983a2370cf06d7efa7fa81397e4de4f3d2e526d516ff5cc4045251870`  
		Last Modified: Tue, 12 Jul 2022 02:49:33 GMT  
		Size: 79.9 KB (79948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80e72f27b28a9ef6a6c3905de932ddcdac3b4f40916f7e2753b951c5b04a9ed`  
		Last Modified: Tue, 12 Jul 2022 02:49:33 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eb63fac7affd697e2a76ec96ee32c35d9a552769fa0850038f510e8cfc40ac`  
		Last Modified: Tue, 12 Jul 2022 02:49:36 GMT  
		Size: 41.1 MB (41112462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439704bcc3d9ab7d985b762876cc6f84589128baac2f38501dbb296bd6229f7c`  
		Last Modified: Tue, 12 Jul 2022 02:49:31 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c5d080f2dc47881a88e7c76d46bab258172e473bf322dbbd87ceedb4f5881e`  
		Last Modified: Tue, 12 Jul 2022 02:49:31 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512290bbc751b401db5a6b8b1d635937718f259eca09d7d8f8d5ec2af4d93dd1`  
		Last Modified: Tue, 12 Jul 2022 02:49:31 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6626bcaf3d9b6b39fd4d45e99ee96f21c9633b389782c0ce6568a4b427ff49d2`  
		Last Modified: Tue, 12 Jul 2022 02:49:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:f24cc2f6267718f98fb2e2b5f61eab8f463e0f3ac86a47d5ea17eb1fd22b9009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:f5e1d26a55dca17d784c1f2b9f669b81abac7ef6338e7eea1521a44df2fa2f21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80009555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d833bfc7acc1bf6fb4701f88ab1edd3d6175e9fae0d5e5c87a0f63be9ea39785`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:10 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 23 Jun 2022 01:07:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:24 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:25 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:25 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:26 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab9ba22220b6188d53d6fc816b63e62996f696e875a21ba2861e839ec5a6861`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdda34c0972965fdcda16044c6018c724818515b86c4c58acf9c1b051b20858`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 44.6 MB (44612451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a85c10523399f67c5c6eefeda3cdd2db8d6ba9dae6f6ef9733ed4d1754e9553`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea223f715c88770fbcef6e32b8cb5f10171bdbe81362aec840af62e8fe3b03d`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35c25494b5c7fa8293dd4ada6b829e1802920894aaad64c7feb17e29b0057e0`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed9f94e6c2271887064031d91d640c36b409089a60fa5db5f7ef0734c643e48`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c4a4be0e8d4275d43397c8daf76b1f3bf3d1388aab26d6fbad00a80bbbdbc0d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74621834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42596514619ac7baa0da65c4ed1a0ec5ae6ce7e2ee3dfe4e7a0ada684205fb78`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:02 GMT
ADD file:d6b43ca12a2cc7f73a66ace962f04878f02eab9345172028d77c21d3dc94fe0c in / 
# Tue, 12 Jul 2022 00:41:03 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:47:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jul 2022 02:47:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jul 2022 02:47:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:47:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Jul 2022 02:47:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Jul 2022 02:47:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:47:48 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 12 Jul 2022 02:47:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Jul 2022 02:48:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jul 2022 02:48:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jul 2022 02:48:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jul 2022 02:48:10 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jul 2022 02:48:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jul 2022 02:48:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 02:48:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jul 2022 02:48:13 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jul 2022 02:48:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8bd5501da4f4b37ad7488bd0eafa32d8927de3bf1e32747545810f2ca65429ed`  
		Last Modified: Tue, 12 Jul 2022 00:47:14 GMT  
		Size: 25.9 MB (25914236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c58fdb695fab9d1860c0b7b39046c6784937d1027efd6f068838d4caa7bde5`  
		Last Modified: Tue, 12 Jul 2022 02:49:35 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825159866a69517714b95f237a7ec44e15ca449d875008a1a218e1e24a5e2c63`  
		Last Modified: Tue, 12 Jul 2022 02:49:34 GMT  
		Size: 6.6 MB (6557100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b91311a9e4b93f1de681be6625b25b5d15a7ee3e8b9942bd5f18dcc02e8e98`  
		Last Modified: Tue, 12 Jul 2022 02:49:34 GMT  
		Size: 951.2 KB (951169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8c11983a2370cf06d7efa7fa81397e4de4f3d2e526d516ff5cc4045251870`  
		Last Modified: Tue, 12 Jul 2022 02:49:33 GMT  
		Size: 79.9 KB (79948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80e72f27b28a9ef6a6c3905de932ddcdac3b4f40916f7e2753b951c5b04a9ed`  
		Last Modified: Tue, 12 Jul 2022 02:49:33 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eb63fac7affd697e2a76ec96ee32c35d9a552769fa0850038f510e8cfc40ac`  
		Last Modified: Tue, 12 Jul 2022 02:49:36 GMT  
		Size: 41.1 MB (41112462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439704bcc3d9ab7d985b762876cc6f84589128baac2f38501dbb296bd6229f7c`  
		Last Modified: Tue, 12 Jul 2022 02:49:31 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c5d080f2dc47881a88e7c76d46bab258172e473bf322dbbd87ceedb4f5881e`  
		Last Modified: Tue, 12 Jul 2022 02:49:31 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512290bbc751b401db5a6b8b1d635937718f259eca09d7d8f8d5ec2af4d93dd1`  
		Last Modified: Tue, 12 Jul 2022 02:49:31 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6626bcaf3d9b6b39fd4d45e99ee96f21c9633b389782c0ce6568a4b427ff49d2`  
		Last Modified: Tue, 12 Jul 2022 02:49:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:5206fe4fe9f6b264b3db516efcbbf5f8f9dec6e6670cc6f58fd1d31f6bc4526a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:3ea7f178b119a1bbd2adbec78486241a087ba35d1d3ec9128a3ada704d55ec97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87498751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9d2dcf03aa6b53788baca7b138c9069926ce70119f77c999d0e2d0858e21d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:06:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:06:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:35 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:06:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:06:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:06:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:06:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:06:50 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:06:50 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:06:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b67ef10ab3031244bf995ed483d30c4423feb9f42f12d55c8511d7497c931`  
		Last Modified: Thu, 23 Jun 2022 01:08:14 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd945ed68b3fecb83857780d70642d81019952136407b87a9f4b6b94711e7dda`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 5.2 MB (5224047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1d67ad9668554764252390c4e5b06fb0f33517e33a831601a00c10a05cfbe7`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 1.6 MB (1553288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b56aaaffae17f3010ab5ba52d88e22126a8b18f5f8fd49ea4a01655c55e20b`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 295.6 KB (295555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e601de752a6ea7ddb9a0b7201437219d647dd0a6555b1d9f48ae8d94004f40`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd769730295be73a2aae5a0882ad80bb9284ad34c68bff96c93ccd15f3cc73`  
		Last Modified: Thu, 23 Jun 2022 01:08:15 GMT  
		Size: 49.0 MB (49039317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0fe21a89a509108c6d599b399458e374353649854cc07814e901deb7030198`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9700366d2b2b831d620b0ee23a1b1ed39c86a91aa69aaad560465e5dd33889`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd356f58092365eb5086db70cc449f1fce114ea73ac0ee9bc18298ac6c579120`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f797d1e3134f5eda53222acba18a0644f920f20c2431b5b3604ab90b7d882c09`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5985d1edef0613a93f2d7349a7cac2296ec956674df1f96d70d4eb23e83e6f80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85620381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b9e4e79dd10c80e29a2fecb5f9f3cd3e32d7c80f8b4b27fa3fc05d20cabf57`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:46:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jul 2022 02:46:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jul 2022 02:46:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:46:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Jul 2022 02:46:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Jul 2022 02:46:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:46:55 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 12 Jul 2022 02:46:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Jul 2022 02:47:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jul 2022 02:47:15 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jul 2022 02:47:16 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jul 2022 02:47:17 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 12 Jul 2022 02:47:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jul 2022 02:47:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 02:47:19 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jul 2022 02:47:20 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jul 2022 02:47:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7465db9b62d8b48810be110d459aefd7c0ad081513d833783a7562aef41e78d6`  
		Last Modified: Tue, 12 Jul 2022 02:49:11 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a3cff592ded12e484f1d97dcf8f9085ef644409ec4e2f18ad6c98d164e5d92`  
		Last Modified: Tue, 12 Jul 2022 02:49:09 GMT  
		Size: 5.2 MB (5207875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814d3780ef73deb609aa55ea065baba3d62461fab745d182156f44df4f37e219`  
		Last Modified: Tue, 12 Jul 2022 02:49:09 GMT  
		Size: 1.2 MB (1221085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd2b2b81e061ce298724584ab5f3607d132f085d872fdbcc1dd60e522373aa`  
		Last Modified: Tue, 12 Jul 2022 02:49:08 GMT  
		Size: 79.2 KB (79211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff676fcdcdd823ef08a4e8a1d6c970a5251eca7b127e65d1b09d000795e276f`  
		Last Modified: Tue, 12 Jul 2022 02:49:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c9e9d309e749b3822eb0c85e7ac1fe7b0ab46593eada60518f1037359952bd`  
		Last Modified: Tue, 12 Jul 2022 02:49:12 GMT  
		Size: 49.1 MB (49050941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56f7299ebdeade54cc83b0c17918710c993136a0e7d6d507f1db40f4271d455`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51cc2dbe5f24b3287814a216d05c221d724e80a8b62e119ecdd8fe30324a08d`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3df456dccfc3e68a1699f2788eacd3e05451ea656f405247b2ad4609874e31f`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 2.2 KB (2182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7b2d14d653177d0efbeb4d6b5feae31470ea31c924de3eca9c94e52c947358`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f667d0d4bf4acaeade0cf8510a4a1384ccd66c08e4ab0b678afb7f8651b9df41
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93209105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97be31cf5f19a6aab7d3705cac0a30da778d2cbabcc7b65e8e3e83d9ee69130d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jul 2022 01:25:28 GMT
ADD file:9e1afe48f40d94f879aefb12a7e68da2f0772d701e95b8219bd1f79a83e1933a in / 
# Tue, 12 Jul 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 05:07:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jul 2022 05:07:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jul 2022 05:08:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:08:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Jul 2022 05:08:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Jul 2022 05:09:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:09:16 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 12 Jul 2022 05:09:23 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Jul 2022 05:10:03 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jul 2022 05:10:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jul 2022 05:10:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jul 2022 05:10:11 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 12 Jul 2022 05:10:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jul 2022 05:10:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 05:10:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jul 2022 05:10:23 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jul 2022 05:10:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bd3d68d1ce583727f6378a16916795b955cc0ad39e0ebe754a26007ef54744fa`  
		Last Modified: Tue, 12 Jul 2022 01:36:03 GMT  
		Size: 35.3 MB (35272500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a816b1ecbe21c2d3295accb57f0a22f554c6ae767a70a4484a89694de329ad9`  
		Last Modified: Tue, 12 Jul 2022 05:10:57 GMT  
		Size: 3.4 KB (3418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0271d8dbcf501c744e33bf898b77265aca81898b869df5041a1c06d2d83ebe24`  
		Last Modified: Tue, 12 Jul 2022 05:10:55 GMT  
		Size: 6.0 MB (6043843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d3674eea9ced378725126b264323f3f0ff2d6990cec832c16bc105b0b16f5a`  
		Last Modified: Tue, 12 Jul 2022 05:10:55 GMT  
		Size: 1.5 MB (1509243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfd2a8749ad2d263caf1ce37413c496a7e3ade1b931c6b26f4b82f81050103d`  
		Last Modified: Tue, 12 Jul 2022 05:10:54 GMT  
		Size: 295.6 KB (295598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833f3e58c97f3db47bdb1766af1a03ba46192031bb9abbc9ff462c336824e462`  
		Last Modified: Tue, 12 Jul 2022 05:10:54 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfc470b8465c993edaa1fb6e3020c7f3a92508d3d0d83be1129f76b54ca5109`  
		Last Modified: Tue, 12 Jul 2022 05:10:59 GMT  
		Size: 50.1 MB (50080767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897291542ee6f3dbd4072e3c7b03d581285986087d05aa1228d6b8ba0032933`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67268035999ecdd7d95f95dcc3e1b15d74a7f086a262ca5bd93c908a9ade4843`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c09171a9b0a8bdba4afb1e5b703ae97ee3436fb56351df60835ba63cf1416`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ff2a8c18f301fb8ac4ff92fcd9631f382e7282d6483e951f29a82ab8bc08e`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.2`

```console
$ docker pull couchdb@sha256:5206fe4fe9f6b264b3db516efcbbf5f8f9dec6e6670cc6f58fd1d31f6bc4526a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.2` - linux; amd64

```console
$ docker pull couchdb@sha256:3ea7f178b119a1bbd2adbec78486241a087ba35d1d3ec9128a3ada704d55ec97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87498751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9d2dcf03aa6b53788baca7b138c9069926ce70119f77c999d0e2d0858e21d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:06:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:06:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:35 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:06:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:06:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:06:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:06:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:06:50 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:06:50 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:06:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b67ef10ab3031244bf995ed483d30c4423feb9f42f12d55c8511d7497c931`  
		Last Modified: Thu, 23 Jun 2022 01:08:14 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd945ed68b3fecb83857780d70642d81019952136407b87a9f4b6b94711e7dda`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 5.2 MB (5224047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1d67ad9668554764252390c4e5b06fb0f33517e33a831601a00c10a05cfbe7`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 1.6 MB (1553288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b56aaaffae17f3010ab5ba52d88e22126a8b18f5f8fd49ea4a01655c55e20b`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 295.6 KB (295555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e601de752a6ea7ddb9a0b7201437219d647dd0a6555b1d9f48ae8d94004f40`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd769730295be73a2aae5a0882ad80bb9284ad34c68bff96c93ccd15f3cc73`  
		Last Modified: Thu, 23 Jun 2022 01:08:15 GMT  
		Size: 49.0 MB (49039317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0fe21a89a509108c6d599b399458e374353649854cc07814e901deb7030198`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9700366d2b2b831d620b0ee23a1b1ed39c86a91aa69aaad560465e5dd33889`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd356f58092365eb5086db70cc449f1fce114ea73ac0ee9bc18298ac6c579120`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f797d1e3134f5eda53222acba18a0644f920f20c2431b5b3604ab90b7d882c09`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5985d1edef0613a93f2d7349a7cac2296ec956674df1f96d70d4eb23e83e6f80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85620381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b9e4e79dd10c80e29a2fecb5f9f3cd3e32d7c80f8b4b27fa3fc05d20cabf57`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:46:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jul 2022 02:46:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jul 2022 02:46:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:46:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Jul 2022 02:46:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Jul 2022 02:46:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:46:55 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 12 Jul 2022 02:46:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Jul 2022 02:47:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jul 2022 02:47:15 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jul 2022 02:47:16 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jul 2022 02:47:17 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 12 Jul 2022 02:47:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jul 2022 02:47:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 02:47:19 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jul 2022 02:47:20 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jul 2022 02:47:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7465db9b62d8b48810be110d459aefd7c0ad081513d833783a7562aef41e78d6`  
		Last Modified: Tue, 12 Jul 2022 02:49:11 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a3cff592ded12e484f1d97dcf8f9085ef644409ec4e2f18ad6c98d164e5d92`  
		Last Modified: Tue, 12 Jul 2022 02:49:09 GMT  
		Size: 5.2 MB (5207875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814d3780ef73deb609aa55ea065baba3d62461fab745d182156f44df4f37e219`  
		Last Modified: Tue, 12 Jul 2022 02:49:09 GMT  
		Size: 1.2 MB (1221085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd2b2b81e061ce298724584ab5f3607d132f085d872fdbcc1dd60e522373aa`  
		Last Modified: Tue, 12 Jul 2022 02:49:08 GMT  
		Size: 79.2 KB (79211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff676fcdcdd823ef08a4e8a1d6c970a5251eca7b127e65d1b09d000795e276f`  
		Last Modified: Tue, 12 Jul 2022 02:49:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c9e9d309e749b3822eb0c85e7ac1fe7b0ab46593eada60518f1037359952bd`  
		Last Modified: Tue, 12 Jul 2022 02:49:12 GMT  
		Size: 49.1 MB (49050941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56f7299ebdeade54cc83b0c17918710c993136a0e7d6d507f1db40f4271d455`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51cc2dbe5f24b3287814a216d05c221d724e80a8b62e119ecdd8fe30324a08d`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3df456dccfc3e68a1699f2788eacd3e05451ea656f405247b2ad4609874e31f`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 2.2 KB (2182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7b2d14d653177d0efbeb4d6b5feae31470ea31c924de3eca9c94e52c947358`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f667d0d4bf4acaeade0cf8510a4a1384ccd66c08e4ab0b678afb7f8651b9df41
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93209105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97be31cf5f19a6aab7d3705cac0a30da778d2cbabcc7b65e8e3e83d9ee69130d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jul 2022 01:25:28 GMT
ADD file:9e1afe48f40d94f879aefb12a7e68da2f0772d701e95b8219bd1f79a83e1933a in / 
# Tue, 12 Jul 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 05:07:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jul 2022 05:07:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jul 2022 05:08:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:08:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Jul 2022 05:08:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Jul 2022 05:09:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:09:16 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 12 Jul 2022 05:09:23 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Jul 2022 05:10:03 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jul 2022 05:10:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jul 2022 05:10:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jul 2022 05:10:11 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 12 Jul 2022 05:10:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jul 2022 05:10:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 05:10:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jul 2022 05:10:23 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jul 2022 05:10:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bd3d68d1ce583727f6378a16916795b955cc0ad39e0ebe754a26007ef54744fa`  
		Last Modified: Tue, 12 Jul 2022 01:36:03 GMT  
		Size: 35.3 MB (35272500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a816b1ecbe21c2d3295accb57f0a22f554c6ae767a70a4484a89694de329ad9`  
		Last Modified: Tue, 12 Jul 2022 05:10:57 GMT  
		Size: 3.4 KB (3418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0271d8dbcf501c744e33bf898b77265aca81898b869df5041a1c06d2d83ebe24`  
		Last Modified: Tue, 12 Jul 2022 05:10:55 GMT  
		Size: 6.0 MB (6043843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d3674eea9ced378725126b264323f3f0ff2d6990cec832c16bc105b0b16f5a`  
		Last Modified: Tue, 12 Jul 2022 05:10:55 GMT  
		Size: 1.5 MB (1509243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfd2a8749ad2d263caf1ce37413c496a7e3ade1b931c6b26f4b82f81050103d`  
		Last Modified: Tue, 12 Jul 2022 05:10:54 GMT  
		Size: 295.6 KB (295598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833f3e58c97f3db47bdb1766af1a03ba46192031bb9abbc9ff462c336824e462`  
		Last Modified: Tue, 12 Jul 2022 05:10:54 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfc470b8465c993edaa1fb6e3020c7f3a92508d3d0d83be1129f76b54ca5109`  
		Last Modified: Tue, 12 Jul 2022 05:10:59 GMT  
		Size: 50.1 MB (50080767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897291542ee6f3dbd4072e3c7b03d581285986087d05aa1228d6b8ba0032933`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67268035999ecdd7d95f95dcc3e1b15d74a7f086a262ca5bd93c908a9ade4843`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c09171a9b0a8bdba4afb1e5b703ae97ee3436fb56351df60835ba63cf1416`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ff2a8c18f301fb8ac4ff92fcd9631f382e7282d6483e951f29a82ab8bc08e`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:5206fe4fe9f6b264b3db516efcbbf5f8f9dec6e6670cc6f58fd1d31f6bc4526a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:3ea7f178b119a1bbd2adbec78486241a087ba35d1d3ec9128a3ada704d55ec97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87498751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9d2dcf03aa6b53788baca7b138c9069926ce70119f77c999d0e2d0858e21d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:06:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:06:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:35 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:06:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:06:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:06:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:06:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:06:50 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:06:50 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:06:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b67ef10ab3031244bf995ed483d30c4423feb9f42f12d55c8511d7497c931`  
		Last Modified: Thu, 23 Jun 2022 01:08:14 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd945ed68b3fecb83857780d70642d81019952136407b87a9f4b6b94711e7dda`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 5.2 MB (5224047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1d67ad9668554764252390c4e5b06fb0f33517e33a831601a00c10a05cfbe7`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 1.6 MB (1553288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b56aaaffae17f3010ab5ba52d88e22126a8b18f5f8fd49ea4a01655c55e20b`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 295.6 KB (295555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e601de752a6ea7ddb9a0b7201437219d647dd0a6555b1d9f48ae8d94004f40`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd769730295be73a2aae5a0882ad80bb9284ad34c68bff96c93ccd15f3cc73`  
		Last Modified: Thu, 23 Jun 2022 01:08:15 GMT  
		Size: 49.0 MB (49039317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0fe21a89a509108c6d599b399458e374353649854cc07814e901deb7030198`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9700366d2b2b831d620b0ee23a1b1ed39c86a91aa69aaad560465e5dd33889`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd356f58092365eb5086db70cc449f1fce114ea73ac0ee9bc18298ac6c579120`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f797d1e3134f5eda53222acba18a0644f920f20c2431b5b3604ab90b7d882c09`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5985d1edef0613a93f2d7349a7cac2296ec956674df1f96d70d4eb23e83e6f80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85620381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b9e4e79dd10c80e29a2fecb5f9f3cd3e32d7c80f8b4b27fa3fc05d20cabf57`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:46:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jul 2022 02:46:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jul 2022 02:46:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:46:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Jul 2022 02:46:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Jul 2022 02:46:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:46:55 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 12 Jul 2022 02:46:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Jul 2022 02:47:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jul 2022 02:47:15 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jul 2022 02:47:16 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jul 2022 02:47:17 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 12 Jul 2022 02:47:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jul 2022 02:47:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 02:47:19 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jul 2022 02:47:20 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jul 2022 02:47:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7465db9b62d8b48810be110d459aefd7c0ad081513d833783a7562aef41e78d6`  
		Last Modified: Tue, 12 Jul 2022 02:49:11 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a3cff592ded12e484f1d97dcf8f9085ef644409ec4e2f18ad6c98d164e5d92`  
		Last Modified: Tue, 12 Jul 2022 02:49:09 GMT  
		Size: 5.2 MB (5207875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814d3780ef73deb609aa55ea065baba3d62461fab745d182156f44df4f37e219`  
		Last Modified: Tue, 12 Jul 2022 02:49:09 GMT  
		Size: 1.2 MB (1221085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd2b2b81e061ce298724584ab5f3607d132f085d872fdbcc1dd60e522373aa`  
		Last Modified: Tue, 12 Jul 2022 02:49:08 GMT  
		Size: 79.2 KB (79211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff676fcdcdd823ef08a4e8a1d6c970a5251eca7b127e65d1b09d000795e276f`  
		Last Modified: Tue, 12 Jul 2022 02:49:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c9e9d309e749b3822eb0c85e7ac1fe7b0ab46593eada60518f1037359952bd`  
		Last Modified: Tue, 12 Jul 2022 02:49:12 GMT  
		Size: 49.1 MB (49050941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56f7299ebdeade54cc83b0c17918710c993136a0e7d6d507f1db40f4271d455`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51cc2dbe5f24b3287814a216d05c221d724e80a8b62e119ecdd8fe30324a08d`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3df456dccfc3e68a1699f2788eacd3e05451ea656f405247b2ad4609874e31f`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 2.2 KB (2182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7b2d14d653177d0efbeb4d6b5feae31470ea31c924de3eca9c94e52c947358`  
		Last Modified: Tue, 12 Jul 2022 02:49:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f667d0d4bf4acaeade0cf8510a4a1384ccd66c08e4ab0b678afb7f8651b9df41
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93209105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97be31cf5f19a6aab7d3705cac0a30da778d2cbabcc7b65e8e3e83d9ee69130d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jul 2022 01:25:28 GMT
ADD file:9e1afe48f40d94f879aefb12a7e68da2f0772d701e95b8219bd1f79a83e1933a in / 
# Tue, 12 Jul 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 05:07:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jul 2022 05:07:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jul 2022 05:08:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:08:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Jul 2022 05:08:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Jul 2022 05:09:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:09:16 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 12 Jul 2022 05:09:23 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Jul 2022 05:10:03 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jul 2022 05:10:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jul 2022 05:10:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jul 2022 05:10:11 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 12 Jul 2022 05:10:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jul 2022 05:10:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 05:10:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jul 2022 05:10:23 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jul 2022 05:10:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bd3d68d1ce583727f6378a16916795b955cc0ad39e0ebe754a26007ef54744fa`  
		Last Modified: Tue, 12 Jul 2022 01:36:03 GMT  
		Size: 35.3 MB (35272500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a816b1ecbe21c2d3295accb57f0a22f554c6ae767a70a4484a89694de329ad9`  
		Last Modified: Tue, 12 Jul 2022 05:10:57 GMT  
		Size: 3.4 KB (3418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0271d8dbcf501c744e33bf898b77265aca81898b869df5041a1c06d2d83ebe24`  
		Last Modified: Tue, 12 Jul 2022 05:10:55 GMT  
		Size: 6.0 MB (6043843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d3674eea9ced378725126b264323f3f0ff2d6990cec832c16bc105b0b16f5a`  
		Last Modified: Tue, 12 Jul 2022 05:10:55 GMT  
		Size: 1.5 MB (1509243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfd2a8749ad2d263caf1ce37413c496a7e3ade1b931c6b26f4b82f81050103d`  
		Last Modified: Tue, 12 Jul 2022 05:10:54 GMT  
		Size: 295.6 KB (295598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833f3e58c97f3db47bdb1766af1a03ba46192031bb9abbc9ff462c336824e462`  
		Last Modified: Tue, 12 Jul 2022 05:10:54 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfc470b8465c993edaa1fb6e3020c7f3a92508d3d0d83be1129f76b54ca5109`  
		Last Modified: Tue, 12 Jul 2022 05:10:59 GMT  
		Size: 50.1 MB (50080767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897291542ee6f3dbd4072e3c7b03d581285986087d05aa1228d6b8ba0032933`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67268035999ecdd7d95f95dcc3e1b15d74a7f086a262ca5bd93c908a9ade4843`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c09171a9b0a8bdba4afb1e5b703ae97ee3436fb56351df60835ba63cf1416`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ff2a8c18f301fb8ac4ff92fcd9631f382e7282d6483e951f29a82ab8bc08e`  
		Last Modified: Tue, 12 Jul 2022 05:10:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
