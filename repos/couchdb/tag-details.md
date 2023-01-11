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
-	[`couchdb:3.3.0`](#couchdb330)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:967b9980952e8e9b2be90d2bf0bd99ca5afc699e0e2c97f5ac6b9afc609012de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:2d081271605809a59a90231c2c77ad5bd0863c5baf8b34b1a64a445ecc8adcc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84536978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a905e3beb38e0854b0e3ad9e24d0242bb021071794b6747b2cad1d9e09e2662`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:43:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:43:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:43:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:43:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:43:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:43:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:43:47 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 11 Jan 2023 03:43:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:44:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:44:08 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:44:08 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:44:08 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 11 Jan 2023 03:44:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:44:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:44:09 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:44:09 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:44:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bfa3ff9f71a5a4f932b800f82439d71d57495a2d9fef430c966ab306016b76`  
		Last Modified: Wed, 11 Jan 2023 03:45:07 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3290d729cfecae377ea085ca44e04eb92eca928b7491aafe36ac68d874206264`  
		Last Modified: Wed, 11 Jan 2023 03:45:07 GMT  
		Size: 6.7 MB (6703741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e90f7ff778b0a21552053c8ff003e422e360385f0c4d5cf5e3f508e0da53f62`  
		Last Modified: Wed, 11 Jan 2023 03:45:06 GMT  
		Size: 1.3 MB (1259602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227c2aabc12d137f66b5d7237b4d29bba9cf30c14a47efe01dcec783040b3de8`  
		Last Modified: Wed, 11 Jan 2023 03:45:05 GMT  
		Size: 294.3 KB (294300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f097e5a917d6019cbe1c7c24f62b2ee942e5f7c346482b995b5a7d8187118540`  
		Last Modified: Wed, 11 Jan 2023 03:45:18 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf57ec82db0f605f77d4bbeedc35d088f3e9a8bb56e5fd9c16481633101aa2`  
		Last Modified: Wed, 11 Jan 2023 03:45:23 GMT  
		Size: 49.1 MB (49131968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b50c6247989f42be0488ad9df1128d6cb0dc8d6b5353253144a141568b8ad65`  
		Last Modified: Wed, 11 Jan 2023 03:45:16 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d6dad00e8b3089f0b860c83c9dadf40c830f2cb94058597d3f99243145fcd2`  
		Last Modified: Wed, 11 Jan 2023 03:45:16 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d083b1aa9704c36eb085c1a7faa286a16b801eec9c3f38a3f757727aac6b8f6`  
		Last Modified: Wed, 11 Jan 2023 03:45:16 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c9d5b1b790873824910abe91cd41edc325de48311e2640cfcfc28dfd93412b`  
		Last Modified: Wed, 11 Jan 2023 03:45:16 GMT  
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
$ docker pull couchdb@sha256:967b9980952e8e9b2be90d2bf0bd99ca5afc699e0e2c97f5ac6b9afc609012de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:2d081271605809a59a90231c2c77ad5bd0863c5baf8b34b1a64a445ecc8adcc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84536978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a905e3beb38e0854b0e3ad9e24d0242bb021071794b6747b2cad1d9e09e2662`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:43:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:43:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:43:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:43:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:43:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:43:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:43:47 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 11 Jan 2023 03:43:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:44:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:44:08 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:44:08 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:44:08 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 11 Jan 2023 03:44:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:44:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:44:09 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:44:09 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:44:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bfa3ff9f71a5a4f932b800f82439d71d57495a2d9fef430c966ab306016b76`  
		Last Modified: Wed, 11 Jan 2023 03:45:07 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3290d729cfecae377ea085ca44e04eb92eca928b7491aafe36ac68d874206264`  
		Last Modified: Wed, 11 Jan 2023 03:45:07 GMT  
		Size: 6.7 MB (6703741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e90f7ff778b0a21552053c8ff003e422e360385f0c4d5cf5e3f508e0da53f62`  
		Last Modified: Wed, 11 Jan 2023 03:45:06 GMT  
		Size: 1.3 MB (1259602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227c2aabc12d137f66b5d7237b4d29bba9cf30c14a47efe01dcec783040b3de8`  
		Last Modified: Wed, 11 Jan 2023 03:45:05 GMT  
		Size: 294.3 KB (294300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f097e5a917d6019cbe1c7c24f62b2ee942e5f7c346482b995b5a7d8187118540`  
		Last Modified: Wed, 11 Jan 2023 03:45:18 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf57ec82db0f605f77d4bbeedc35d088f3e9a8bb56e5fd9c16481633101aa2`  
		Last Modified: Wed, 11 Jan 2023 03:45:23 GMT  
		Size: 49.1 MB (49131968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b50c6247989f42be0488ad9df1128d6cb0dc8d6b5353253144a141568b8ad65`  
		Last Modified: Wed, 11 Jan 2023 03:45:16 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d6dad00e8b3089f0b860c83c9dadf40c830f2cb94058597d3f99243145fcd2`  
		Last Modified: Wed, 11 Jan 2023 03:45:16 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d083b1aa9704c36eb085c1a7faa286a16b801eec9c3f38a3f757727aac6b8f6`  
		Last Modified: Wed, 11 Jan 2023 03:45:16 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c9d5b1b790873824910abe91cd41edc325de48311e2640cfcfc28dfd93412b`  
		Last Modified: Wed, 11 Jan 2023 03:45:16 GMT  
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
$ docker pull couchdb@sha256:967b9980952e8e9b2be90d2bf0bd99ca5afc699e0e2c97f5ac6b9afc609012de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:2d081271605809a59a90231c2c77ad5bd0863c5baf8b34b1a64a445ecc8adcc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84536978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a905e3beb38e0854b0e3ad9e24d0242bb021071794b6747b2cad1d9e09e2662`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:43:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:43:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:43:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:43:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:43:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:43:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:43:47 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 11 Jan 2023 03:43:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:44:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:44:08 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:44:08 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:44:08 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 11 Jan 2023 03:44:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:44:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:44:09 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:44:09 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:44:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bfa3ff9f71a5a4f932b800f82439d71d57495a2d9fef430c966ab306016b76`  
		Last Modified: Wed, 11 Jan 2023 03:45:07 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3290d729cfecae377ea085ca44e04eb92eca928b7491aafe36ac68d874206264`  
		Last Modified: Wed, 11 Jan 2023 03:45:07 GMT  
		Size: 6.7 MB (6703741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e90f7ff778b0a21552053c8ff003e422e360385f0c4d5cf5e3f508e0da53f62`  
		Last Modified: Wed, 11 Jan 2023 03:45:06 GMT  
		Size: 1.3 MB (1259602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227c2aabc12d137f66b5d7237b4d29bba9cf30c14a47efe01dcec783040b3de8`  
		Last Modified: Wed, 11 Jan 2023 03:45:05 GMT  
		Size: 294.3 KB (294300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f097e5a917d6019cbe1c7c24f62b2ee942e5f7c346482b995b5a7d8187118540`  
		Last Modified: Wed, 11 Jan 2023 03:45:18 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf57ec82db0f605f77d4bbeedc35d088f3e9a8bb56e5fd9c16481633101aa2`  
		Last Modified: Wed, 11 Jan 2023 03:45:23 GMT  
		Size: 49.1 MB (49131968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b50c6247989f42be0488ad9df1128d6cb0dc8d6b5353253144a141568b8ad65`  
		Last Modified: Wed, 11 Jan 2023 03:45:16 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d6dad00e8b3089f0b860c83c9dadf40c830f2cb94058597d3f99243145fcd2`  
		Last Modified: Wed, 11 Jan 2023 03:45:16 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d083b1aa9704c36eb085c1a7faa286a16b801eec9c3f38a3f757727aac6b8f6`  
		Last Modified: Wed, 11 Jan 2023 03:45:16 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c9d5b1b790873824910abe91cd41edc325de48311e2640cfcfc28dfd93412b`  
		Last Modified: Wed, 11 Jan 2023 03:45:16 GMT  
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
$ docker pull couchdb@sha256:2cb4cacb5b2e8b8ee60b692f42c63f02d23cae0ea1a5e324e26737bf328f335e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:3f3704ddfb6014435f2611a611efcfe465f04d56bc3d5f92c9955493a3cdb3af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91170738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799ba382589148b50a50959977441a8f86654f60b0a06ac5ee1284c35a19e033`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:42:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:42:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:42:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:42:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:42:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:42:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:42:24 GMT
ENV COUCHDB_VERSION=3.3.0
# Wed, 11 Jan 2023 03:42:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:42:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:42:38 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:42:38 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:42:38 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 03:42:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:42:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:42:39 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:42:39 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:42:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b54fc1f41d9e17df7d49c1f5111f508dcb398b5196ebba6d187873dc3480ac6`  
		Last Modified: Wed, 11 Jan 2023 03:44:34 GMT  
		Size: 3.4 KB (3407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb927a4266fd4cede9f246cd7618acfdc3616eb4317e9cb36336d6c1cc6fd06`  
		Last Modified: Wed, 11 Jan 2023 03:44:33 GMT  
		Size: 5.2 MB (5224274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4e44b11124abc70dfa0c6427e095db1f27f6dde701d1f7189b11da9493502c`  
		Last Modified: Wed, 11 Jan 2023 03:44:32 GMT  
		Size: 1.6 MB (1553321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef2a9c48048ec5db36fe98ca1615725d8b2ffae3208912b30f46d66350d567c`  
		Last Modified: Wed, 11 Jan 2023 03:44:32 GMT  
		Size: 295.6 KB (295572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1733bf1e1f601845827b5e2fbaea7f2787c0a1569115aebe2409b21c75e844e7`  
		Last Modified: Wed, 11 Jan 2023 03:44:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad41b48fc6b9e5728cf2a545800c04c14be2aed0ab458dc16950b9d147e1fb3`  
		Last Modified: Wed, 11 Jan 2023 03:44:35 GMT  
		Size: 52.7 MB (52693469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfd0f547079ce8a04faf5ecf4aaf0101e801cba0b16becec736bc8f097ccfa6`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6296a2f8c0c9d1836022dfeaca4678825180d16ff3a991aef1fc41f235afb0ff`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c775ec994f746eae7f636d0bfb61cbbeb0f6519e95956936e9266d06eab1f2`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2509d15830b488026e0b012f58465b22e97bb86522fe7bcf12fdf50ec1abdb37`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f4406d33306fe49a7a2e30f35b5dbd5cbfa273d862a666d4eeade997434ba124
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d525ca39e94698fcf20b7b2375614336e6667fa8df217e74fd18d84aa59ec7b1`
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
# Wed, 11 Jan 2023 03:57:50 GMT
ENV COUCHDB_VERSION=3.3.0
# Wed, 11 Jan 2023 03:57:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:58:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:58:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:58:02 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:58:02 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 03:58:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:58:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:58:03 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:58:03 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:58:03 GMT
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
	-	`sha256:30f094d764575f750f083741eef9b006b2b8f38377066123276183970c9f4b9c`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d18c7d73142c458e120afbad0b523afbea47c5dd64c907c36f3eadbe1ab4f5b`  
		Last Modified: Wed, 11 Jan 2023 03:59:35 GMT  
		Size: 52.5 MB (52549696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812134a97ce41f8f31052309638b75bb6aaa642f97c7651ad4de14d3ae8367c5`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c887f3198f5407ad0f3df301a53ecb084eb9ce4b962b72db984d1aea1aa401`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d3dce85443993cd688868bce0e21e6bbe5e1d91ea7478a3c41fc55d23be5f3`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe79279fcda944111b666bef5e8fcd9e17a0ffc5bb460227e37a4e0e6d3f3562`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:4d6b05042044225fc1ff9532c1edd602d0fc750d35cac8ff858a8ff06205e1d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96677789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3598983d07c56e8d4b91d1e40075e104c3cb7e9af92e4c200b6291d8c8a1b3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 03:49:30 GMT
ADD file:3c7553fb5eda606d574ff6c08bc2213f9e6a68910043fe3087e4c1a04b65a18e in / 
# Wed, 11 Jan 2023 03:49:32 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 04:17:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 04:17:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 04:18:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:18:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 04:18:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 04:18:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:18:23 GMT
ENV COUCHDB_VERSION=3.3.0
# Wed, 11 Jan 2023 04:18:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 04:18:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 04:18:50 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 04:18:50 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 04:18:50 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 04:18:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 04:18:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 04:18:52 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 04:18:52 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 04:18:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bbf81328aca90b7ddb122fc175443f5323674a9e51bbb00d5b1d683ef0b858f4`  
		Last Modified: Wed, 11 Jan 2023 03:55:33 GMT  
		Size: 35.3 MB (35268773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d4b7dfde57dc3b711e2273da5a61a5829a57b9d58474f1d5ffd21634458f5e`  
		Last Modified: Wed, 11 Jan 2023 04:19:54 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e0b83a7c039dc80fa7b1d8424d0c1a059fbd972e127d4bb4845181526ca907`  
		Last Modified: Wed, 11 Jan 2023 04:19:54 GMT  
		Size: 6.0 MB (6043874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2673661962247aa7e2f981fd8bfb91ba790a2cf92ab3c5c63e6e1340e5f5bc5b`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 1.5 MB (1509211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c497897d6b3b0e80026e3b729b1d0d01cb112a46c93249841c7394cb4930e3`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 295.5 KB (295534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e147edb3c0e81852fd5b883ae96cae30c9de2f81a7057e45188be3e1059e0aca`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc6f7e67309c7cde8911e23783a30f691fe986cf9b79e185f3cc904877134a6`  
		Last Modified: Wed, 11 Jan 2023 04:19:59 GMT  
		Size: 53.6 MB (53553258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d38eb64d280ea68213c9f68e36c544e73c614d8487daf917414f5e4d3f3cbe2`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77b0769427d4085a204e9b363d301ee1da0315634e0ff4f8df8daba91998694`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c49240b3d78c657c4c382b920923ac4a3db5bb640b05e7f674969ccefbced46`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250b59b18ccba5cb48d1c83a196a4b40629090ba7751356fe560871529379183`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:0fd2e1f2a20d81099f98d8e1f8063205cc9ea127011f57008c1ed4c208817e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:2e0760b86a82074aa79c9104d478d84ed477f507391d0d4e95b61a31aa63ba23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80023658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02aed577f568d149628975ba99aee714fe693ddb06651627e1f35bff566545cc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:43:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:43:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:43:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:43:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:43:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:43:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:43:28 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 11 Jan 2023 03:43:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:43:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:43:43 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:43:43 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:43:43 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 11 Jan 2023 03:43:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:43:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:43:44 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:43:44 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:43:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bfa3ff9f71a5a4f932b800f82439d71d57495a2d9fef430c966ab306016b76`  
		Last Modified: Wed, 11 Jan 2023 03:45:07 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3290d729cfecae377ea085ca44e04eb92eca928b7491aafe36ac68d874206264`  
		Last Modified: Wed, 11 Jan 2023 03:45:07 GMT  
		Size: 6.7 MB (6703741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e90f7ff778b0a21552053c8ff003e422e360385f0c4d5cf5e3f508e0da53f62`  
		Last Modified: Wed, 11 Jan 2023 03:45:06 GMT  
		Size: 1.3 MB (1259602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227c2aabc12d137f66b5d7237b4d29bba9cf30c14a47efe01dcec783040b3de8`  
		Last Modified: Wed, 11 Jan 2023 03:45:05 GMT  
		Size: 294.3 KB (294300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb521ebad65b8d60789e8b7b832e1de7bcb6759425ec2cfcc8c2bbd0bbec235`  
		Last Modified: Wed, 11 Jan 2023 03:45:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536b1182382b88dc17e41d1479b38feef0728f72e89e2b6c57c1bbd2dbc03dee`  
		Last Modified: Wed, 11 Jan 2023 03:45:08 GMT  
		Size: 44.6 MB (44618659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f343af23026d2dd84092b385dd0cbaa4021aa7e855657309dd3fe9eb1eae9b`  
		Last Modified: Wed, 11 Jan 2023 03:45:03 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de829366d196f7bc8dd8424e1de688e7cbec3bb172ed7939a4d0a9c4c1b56a2`  
		Last Modified: Wed, 11 Jan 2023 03:45:03 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e8aafd68e4dfc15a48688295522d15d6b44e41acbff5e5d536075414252283`  
		Last Modified: Wed, 11 Jan 2023 03:45:04 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aa7915d25c1b19cb7b06c0434a33b6d37b949aa7bc3cc8502b67d726b38712`  
		Last Modified: Wed, 11 Jan 2023 03:45:03 GMT  
		Size: 121.0 B  
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
$ docker pull couchdb@sha256:0fd2e1f2a20d81099f98d8e1f8063205cc9ea127011f57008c1ed4c208817e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:2e0760b86a82074aa79c9104d478d84ed477f507391d0d4e95b61a31aa63ba23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80023658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02aed577f568d149628975ba99aee714fe693ddb06651627e1f35bff566545cc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:43:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:43:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:43:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:43:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:43:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:43:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:43:28 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 11 Jan 2023 03:43:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:43:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:43:43 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:43:43 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:43:43 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 11 Jan 2023 03:43:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:43:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:43:44 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:43:44 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:43:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bfa3ff9f71a5a4f932b800f82439d71d57495a2d9fef430c966ab306016b76`  
		Last Modified: Wed, 11 Jan 2023 03:45:07 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3290d729cfecae377ea085ca44e04eb92eca928b7491aafe36ac68d874206264`  
		Last Modified: Wed, 11 Jan 2023 03:45:07 GMT  
		Size: 6.7 MB (6703741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e90f7ff778b0a21552053c8ff003e422e360385f0c4d5cf5e3f508e0da53f62`  
		Last Modified: Wed, 11 Jan 2023 03:45:06 GMT  
		Size: 1.3 MB (1259602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227c2aabc12d137f66b5d7237b4d29bba9cf30c14a47efe01dcec783040b3de8`  
		Last Modified: Wed, 11 Jan 2023 03:45:05 GMT  
		Size: 294.3 KB (294300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb521ebad65b8d60789e8b7b832e1de7bcb6759425ec2cfcc8c2bbd0bbec235`  
		Last Modified: Wed, 11 Jan 2023 03:45:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536b1182382b88dc17e41d1479b38feef0728f72e89e2b6c57c1bbd2dbc03dee`  
		Last Modified: Wed, 11 Jan 2023 03:45:08 GMT  
		Size: 44.6 MB (44618659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f343af23026d2dd84092b385dd0cbaa4021aa7e855657309dd3fe9eb1eae9b`  
		Last Modified: Wed, 11 Jan 2023 03:45:03 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de829366d196f7bc8dd8424e1de688e7cbec3bb172ed7939a4d0a9c4c1b56a2`  
		Last Modified: Wed, 11 Jan 2023 03:45:03 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e8aafd68e4dfc15a48688295522d15d6b44e41acbff5e5d536075414252283`  
		Last Modified: Wed, 11 Jan 2023 03:45:04 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aa7915d25c1b19cb7b06c0434a33b6d37b949aa7bc3cc8502b67d726b38712`  
		Last Modified: Wed, 11 Jan 2023 03:45:03 GMT  
		Size: 121.0 B  
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
$ docker pull couchdb@sha256:e0dd3b7b4413e8ee165343aedb07334da0df850d296e32a234b7e4b93762f57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:8983f5e09207dbccbd7d8e057cbb495281a0218319de11f9e85863d34601e08d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87524708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f404712cecd44f80b4d7e216fa9e00cca4def28fad4b37e420e34fab817b689b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:42:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:42:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:42:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:42:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:42:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:42:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:42:47 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 11 Jan 2023 03:42:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:43:01 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:43:01 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:43:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:43:01 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 03:43:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:43:02 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:43:02 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:43:02 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:43:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b54fc1f41d9e17df7d49c1f5111f508dcb398b5196ebba6d187873dc3480ac6`  
		Last Modified: Wed, 11 Jan 2023 03:44:34 GMT  
		Size: 3.4 KB (3407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb927a4266fd4cede9f246cd7618acfdc3616eb4317e9cb36336d6c1cc6fd06`  
		Last Modified: Wed, 11 Jan 2023 03:44:33 GMT  
		Size: 5.2 MB (5224274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4e44b11124abc70dfa0c6427e095db1f27f6dde701d1f7189b11da9493502c`  
		Last Modified: Wed, 11 Jan 2023 03:44:32 GMT  
		Size: 1.6 MB (1553321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef2a9c48048ec5db36fe98ca1615725d8b2ffae3208912b30f46d66350d567c`  
		Last Modified: Wed, 11 Jan 2023 03:44:32 GMT  
		Size: 295.6 KB (295572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dec427ed6b4455de2ebe5130af154b902f1981b7e58f0e51ed70dcb9a39dd4`  
		Last Modified: Wed, 11 Jan 2023 03:44:50 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6161a938b5bb2789dd250d87e3328b22951727e139fef17f5553d9a093ffeac7`  
		Last Modified: Wed, 11 Jan 2023 03:44:54 GMT  
		Size: 49.0 MB (49047433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e96fc640cf54e08437bebbdc2fa62fb7c4cbc081ef46c6e11eb3a319018ae0`  
		Last Modified: Wed, 11 Jan 2023 03:44:49 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f9ffc7ef4d826629fa8f29ec33fa4e5dd7861cdf5dcafc1970b5337ac88bab`  
		Last Modified: Wed, 11 Jan 2023 03:44:49 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71345c4510bf637fa1f7c0f277bd14c51dfc68124496a84b8d1e2e4729d886a`  
		Last Modified: Wed, 11 Jan 2023 03:44:49 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443896036cf7a84ca6619299969209d03a666bf2ea14b849e0716c7db3ca6867`  
		Last Modified: Wed, 11 Jan 2023 03:44:49 GMT  
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
$ docker pull couchdb@sha256:75850eff81cebbc5c66f290d5fbc8deb6a39d8f6d5a753c2bb54efb9f68a0d2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93210528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908496914c04ea5ed686a19445d87e37784ee7173c3fe8aa1580049b2132764`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 03:49:30 GMT
ADD file:3c7553fb5eda606d574ff6c08bc2213f9e6a68910043fe3087e4c1a04b65a18e in / 
# Wed, 11 Jan 2023 03:49:32 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 04:17:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 04:17:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 04:18:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:18:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 04:18:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 04:18:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:18:58 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 11 Jan 2023 04:18:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 04:19:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 04:19:23 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 04:19:23 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 04:19:23 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 04:19:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 04:19:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 04:19:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 04:19:25 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 04:19:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bbf81328aca90b7ddb122fc175443f5323674a9e51bbb00d5b1d683ef0b858f4`  
		Last Modified: Wed, 11 Jan 2023 03:55:33 GMT  
		Size: 35.3 MB (35268773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d4b7dfde57dc3b711e2273da5a61a5829a57b9d58474f1d5ffd21634458f5e`  
		Last Modified: Wed, 11 Jan 2023 04:19:54 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e0b83a7c039dc80fa7b1d8424d0c1a059fbd972e127d4bb4845181526ca907`  
		Last Modified: Wed, 11 Jan 2023 04:19:54 GMT  
		Size: 6.0 MB (6043874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2673661962247aa7e2f981fd8bfb91ba790a2cf92ab3c5c63e6e1340e5f5bc5b`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 1.5 MB (1509211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c497897d6b3b0e80026e3b729b1d0d01cb112a46c93249841c7394cb4930e3`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 295.5 KB (295534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28015fe227fccfe108c2228326f4f86acd95b321c246ce68385f84a2f69e08d8`  
		Last Modified: Wed, 11 Jan 2023 04:20:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2673c190fd453dfabe57ebbb3fc2961eec3153ad007a5e2cd2ccff212f3a0c8e`  
		Last Modified: Wed, 11 Jan 2023 04:20:28 GMT  
		Size: 50.1 MB (50085993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b8a5b0bbdbf782871d7299c9ee8863978972dc8a210da3afd21174370d7ece`  
		Last Modified: Wed, 11 Jan 2023 04:20:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c7768733a08358b7de0ddb016dc8fa2d6a97ae2bc6180368a1cf92a9abeb3a`  
		Last Modified: Wed, 11 Jan 2023 04:20:19 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89dd72912ecd2d2693913736074f5afb3d88884d8ed648fdb300ee9d9e0f2a8`  
		Last Modified: Wed, 11 Jan 2023 04:20:19 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e2ed4a1ec1d9cba539192afdceb7781d11860ea43646355685c8796a6221c`  
		Last Modified: Wed, 11 Jan 2023 04:20:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.2`

```console
$ docker pull couchdb@sha256:e0dd3b7b4413e8ee165343aedb07334da0df850d296e32a234b7e4b93762f57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.2` - linux; amd64

```console
$ docker pull couchdb@sha256:8983f5e09207dbccbd7d8e057cbb495281a0218319de11f9e85863d34601e08d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87524708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f404712cecd44f80b4d7e216fa9e00cca4def28fad4b37e420e34fab817b689b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:42:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:42:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:42:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:42:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:42:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:42:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:42:47 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 11 Jan 2023 03:42:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:43:01 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:43:01 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:43:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:43:01 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 03:43:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:43:02 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:43:02 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:43:02 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:43:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b54fc1f41d9e17df7d49c1f5111f508dcb398b5196ebba6d187873dc3480ac6`  
		Last Modified: Wed, 11 Jan 2023 03:44:34 GMT  
		Size: 3.4 KB (3407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb927a4266fd4cede9f246cd7618acfdc3616eb4317e9cb36336d6c1cc6fd06`  
		Last Modified: Wed, 11 Jan 2023 03:44:33 GMT  
		Size: 5.2 MB (5224274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4e44b11124abc70dfa0c6427e095db1f27f6dde701d1f7189b11da9493502c`  
		Last Modified: Wed, 11 Jan 2023 03:44:32 GMT  
		Size: 1.6 MB (1553321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef2a9c48048ec5db36fe98ca1615725d8b2ffae3208912b30f46d66350d567c`  
		Last Modified: Wed, 11 Jan 2023 03:44:32 GMT  
		Size: 295.6 KB (295572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dec427ed6b4455de2ebe5130af154b902f1981b7e58f0e51ed70dcb9a39dd4`  
		Last Modified: Wed, 11 Jan 2023 03:44:50 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6161a938b5bb2789dd250d87e3328b22951727e139fef17f5553d9a093ffeac7`  
		Last Modified: Wed, 11 Jan 2023 03:44:54 GMT  
		Size: 49.0 MB (49047433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e96fc640cf54e08437bebbdc2fa62fb7c4cbc081ef46c6e11eb3a319018ae0`  
		Last Modified: Wed, 11 Jan 2023 03:44:49 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f9ffc7ef4d826629fa8f29ec33fa4e5dd7861cdf5dcafc1970b5337ac88bab`  
		Last Modified: Wed, 11 Jan 2023 03:44:49 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71345c4510bf637fa1f7c0f277bd14c51dfc68124496a84b8d1e2e4729d886a`  
		Last Modified: Wed, 11 Jan 2023 03:44:49 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443896036cf7a84ca6619299969209d03a666bf2ea14b849e0716c7db3ca6867`  
		Last Modified: Wed, 11 Jan 2023 03:44:49 GMT  
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
$ docker pull couchdb@sha256:75850eff81cebbc5c66f290d5fbc8deb6a39d8f6d5a753c2bb54efb9f68a0d2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93210528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908496914c04ea5ed686a19445d87e37784ee7173c3fe8aa1580049b2132764`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 03:49:30 GMT
ADD file:3c7553fb5eda606d574ff6c08bc2213f9e6a68910043fe3087e4c1a04b65a18e in / 
# Wed, 11 Jan 2023 03:49:32 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 04:17:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 04:17:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 04:18:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:18:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 04:18:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 04:18:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:18:58 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 11 Jan 2023 04:18:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 04:19:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 04:19:23 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 04:19:23 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 04:19:23 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 04:19:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 04:19:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 04:19:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 04:19:25 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 04:19:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bbf81328aca90b7ddb122fc175443f5323674a9e51bbb00d5b1d683ef0b858f4`  
		Last Modified: Wed, 11 Jan 2023 03:55:33 GMT  
		Size: 35.3 MB (35268773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d4b7dfde57dc3b711e2273da5a61a5829a57b9d58474f1d5ffd21634458f5e`  
		Last Modified: Wed, 11 Jan 2023 04:19:54 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e0b83a7c039dc80fa7b1d8424d0c1a059fbd972e127d4bb4845181526ca907`  
		Last Modified: Wed, 11 Jan 2023 04:19:54 GMT  
		Size: 6.0 MB (6043874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2673661962247aa7e2f981fd8bfb91ba790a2cf92ab3c5c63e6e1340e5f5bc5b`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 1.5 MB (1509211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c497897d6b3b0e80026e3b729b1d0d01cb112a46c93249841c7394cb4930e3`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 295.5 KB (295534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28015fe227fccfe108c2228326f4f86acd95b321c246ce68385f84a2f69e08d8`  
		Last Modified: Wed, 11 Jan 2023 04:20:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2673c190fd453dfabe57ebbb3fc2961eec3153ad007a5e2cd2ccff212f3a0c8e`  
		Last Modified: Wed, 11 Jan 2023 04:20:28 GMT  
		Size: 50.1 MB (50085993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b8a5b0bbdbf782871d7299c9ee8863978972dc8a210da3afd21174370d7ece`  
		Last Modified: Wed, 11 Jan 2023 04:20:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c7768733a08358b7de0ddb016dc8fa2d6a97ae2bc6180368a1cf92a9abeb3a`  
		Last Modified: Wed, 11 Jan 2023 04:20:19 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89dd72912ecd2d2693913736074f5afb3d88884d8ed648fdb300ee9d9e0f2a8`  
		Last Modified: Wed, 11 Jan 2023 04:20:19 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e2ed4a1ec1d9cba539192afdceb7781d11860ea43646355685c8796a6221c`  
		Last Modified: Wed, 11 Jan 2023 04:20:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:2cb4cacb5b2e8b8ee60b692f42c63f02d23cae0ea1a5e324e26737bf328f335e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:3f3704ddfb6014435f2611a611efcfe465f04d56bc3d5f92c9955493a3cdb3af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91170738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799ba382589148b50a50959977441a8f86654f60b0a06ac5ee1284c35a19e033`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:42:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:42:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:42:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:42:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:42:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:42:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:42:24 GMT
ENV COUCHDB_VERSION=3.3.0
# Wed, 11 Jan 2023 03:42:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:42:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:42:38 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:42:38 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:42:38 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 03:42:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:42:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:42:39 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:42:39 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:42:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b54fc1f41d9e17df7d49c1f5111f508dcb398b5196ebba6d187873dc3480ac6`  
		Last Modified: Wed, 11 Jan 2023 03:44:34 GMT  
		Size: 3.4 KB (3407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb927a4266fd4cede9f246cd7618acfdc3616eb4317e9cb36336d6c1cc6fd06`  
		Last Modified: Wed, 11 Jan 2023 03:44:33 GMT  
		Size: 5.2 MB (5224274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4e44b11124abc70dfa0c6427e095db1f27f6dde701d1f7189b11da9493502c`  
		Last Modified: Wed, 11 Jan 2023 03:44:32 GMT  
		Size: 1.6 MB (1553321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef2a9c48048ec5db36fe98ca1615725d8b2ffae3208912b30f46d66350d567c`  
		Last Modified: Wed, 11 Jan 2023 03:44:32 GMT  
		Size: 295.6 KB (295572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1733bf1e1f601845827b5e2fbaea7f2787c0a1569115aebe2409b21c75e844e7`  
		Last Modified: Wed, 11 Jan 2023 03:44:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad41b48fc6b9e5728cf2a545800c04c14be2aed0ab458dc16950b9d147e1fb3`  
		Last Modified: Wed, 11 Jan 2023 03:44:35 GMT  
		Size: 52.7 MB (52693469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfd0f547079ce8a04faf5ecf4aaf0101e801cba0b16becec736bc8f097ccfa6`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6296a2f8c0c9d1836022dfeaca4678825180d16ff3a991aef1fc41f235afb0ff`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c775ec994f746eae7f636d0bfb61cbbeb0f6519e95956936e9266d06eab1f2`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2509d15830b488026e0b012f58465b22e97bb86522fe7bcf12fdf50ec1abdb37`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f4406d33306fe49a7a2e30f35b5dbd5cbfa273d862a666d4eeade997434ba124
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d525ca39e94698fcf20b7b2375614336e6667fa8df217e74fd18d84aa59ec7b1`
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
# Wed, 11 Jan 2023 03:57:50 GMT
ENV COUCHDB_VERSION=3.3.0
# Wed, 11 Jan 2023 03:57:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:58:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:58:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:58:02 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:58:02 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 03:58:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:58:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:58:03 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:58:03 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:58:03 GMT
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
	-	`sha256:30f094d764575f750f083741eef9b006b2b8f38377066123276183970c9f4b9c`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d18c7d73142c458e120afbad0b523afbea47c5dd64c907c36f3eadbe1ab4f5b`  
		Last Modified: Wed, 11 Jan 2023 03:59:35 GMT  
		Size: 52.5 MB (52549696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812134a97ce41f8f31052309638b75bb6aaa642f97c7651ad4de14d3ae8367c5`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c887f3198f5407ad0f3df301a53ecb084eb9ce4b962b72db984d1aea1aa401`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d3dce85443993cd688868bce0e21e6bbe5e1d91ea7478a3c41fc55d23be5f3`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe79279fcda944111b666bef5e8fcd9e17a0ffc5bb460227e37a4e0e6d3f3562`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:4d6b05042044225fc1ff9532c1edd602d0fc750d35cac8ff858a8ff06205e1d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96677789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3598983d07c56e8d4b91d1e40075e104c3cb7e9af92e4c200b6291d8c8a1b3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 03:49:30 GMT
ADD file:3c7553fb5eda606d574ff6c08bc2213f9e6a68910043fe3087e4c1a04b65a18e in / 
# Wed, 11 Jan 2023 03:49:32 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 04:17:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 04:17:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 04:18:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:18:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 04:18:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 04:18:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:18:23 GMT
ENV COUCHDB_VERSION=3.3.0
# Wed, 11 Jan 2023 04:18:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 04:18:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 04:18:50 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 04:18:50 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 04:18:50 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 04:18:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 04:18:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 04:18:52 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 04:18:52 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 04:18:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bbf81328aca90b7ddb122fc175443f5323674a9e51bbb00d5b1d683ef0b858f4`  
		Last Modified: Wed, 11 Jan 2023 03:55:33 GMT  
		Size: 35.3 MB (35268773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d4b7dfde57dc3b711e2273da5a61a5829a57b9d58474f1d5ffd21634458f5e`  
		Last Modified: Wed, 11 Jan 2023 04:19:54 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e0b83a7c039dc80fa7b1d8424d0c1a059fbd972e127d4bb4845181526ca907`  
		Last Modified: Wed, 11 Jan 2023 04:19:54 GMT  
		Size: 6.0 MB (6043874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2673661962247aa7e2f981fd8bfb91ba790a2cf92ab3c5c63e6e1340e5f5bc5b`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 1.5 MB (1509211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c497897d6b3b0e80026e3b729b1d0d01cb112a46c93249841c7394cb4930e3`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 295.5 KB (295534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e147edb3c0e81852fd5b883ae96cae30c9de2f81a7057e45188be3e1059e0aca`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc6f7e67309c7cde8911e23783a30f691fe986cf9b79e185f3cc904877134a6`  
		Last Modified: Wed, 11 Jan 2023 04:19:59 GMT  
		Size: 53.6 MB (53553258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d38eb64d280ea68213c9f68e36c544e73c614d8487daf917414f5e4d3f3cbe2`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77b0769427d4085a204e9b363d301ee1da0315634e0ff4f8df8daba91998694`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c49240b3d78c657c4c382b920923ac4a3db5bb640b05e7f674969ccefbced46`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250b59b18ccba5cb48d1c83a196a4b40629090ba7751356fe560871529379183`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3.0`

```console
$ docker pull couchdb@sha256:2cb4cacb5b2e8b8ee60b692f42c63f02d23cae0ea1a5e324e26737bf328f335e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.3.0` - linux; amd64

```console
$ docker pull couchdb@sha256:3f3704ddfb6014435f2611a611efcfe465f04d56bc3d5f92c9955493a3cdb3af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91170738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799ba382589148b50a50959977441a8f86654f60b0a06ac5ee1284c35a19e033`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:42:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:42:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:42:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:42:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:42:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:42:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:42:24 GMT
ENV COUCHDB_VERSION=3.3.0
# Wed, 11 Jan 2023 03:42:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:42:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:42:38 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:42:38 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:42:38 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 03:42:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:42:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:42:39 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:42:39 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:42:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b54fc1f41d9e17df7d49c1f5111f508dcb398b5196ebba6d187873dc3480ac6`  
		Last Modified: Wed, 11 Jan 2023 03:44:34 GMT  
		Size: 3.4 KB (3407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb927a4266fd4cede9f246cd7618acfdc3616eb4317e9cb36336d6c1cc6fd06`  
		Last Modified: Wed, 11 Jan 2023 03:44:33 GMT  
		Size: 5.2 MB (5224274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4e44b11124abc70dfa0c6427e095db1f27f6dde701d1f7189b11da9493502c`  
		Last Modified: Wed, 11 Jan 2023 03:44:32 GMT  
		Size: 1.6 MB (1553321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef2a9c48048ec5db36fe98ca1615725d8b2ffae3208912b30f46d66350d567c`  
		Last Modified: Wed, 11 Jan 2023 03:44:32 GMT  
		Size: 295.6 KB (295572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1733bf1e1f601845827b5e2fbaea7f2787c0a1569115aebe2409b21c75e844e7`  
		Last Modified: Wed, 11 Jan 2023 03:44:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad41b48fc6b9e5728cf2a545800c04c14be2aed0ab458dc16950b9d147e1fb3`  
		Last Modified: Wed, 11 Jan 2023 03:44:35 GMT  
		Size: 52.7 MB (52693469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfd0f547079ce8a04faf5ecf4aaf0101e801cba0b16becec736bc8f097ccfa6`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6296a2f8c0c9d1836022dfeaca4678825180d16ff3a991aef1fc41f235afb0ff`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c775ec994f746eae7f636d0bfb61cbbeb0f6519e95956936e9266d06eab1f2`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2509d15830b488026e0b012f58465b22e97bb86522fe7bcf12fdf50ec1abdb37`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f4406d33306fe49a7a2e30f35b5dbd5cbfa273d862a666d4eeade997434ba124
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d525ca39e94698fcf20b7b2375614336e6667fa8df217e74fd18d84aa59ec7b1`
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
# Wed, 11 Jan 2023 03:57:50 GMT
ENV COUCHDB_VERSION=3.3.0
# Wed, 11 Jan 2023 03:57:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:58:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:58:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:58:02 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:58:02 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 03:58:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:58:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:58:03 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:58:03 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:58:03 GMT
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
	-	`sha256:30f094d764575f750f083741eef9b006b2b8f38377066123276183970c9f4b9c`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d18c7d73142c458e120afbad0b523afbea47c5dd64c907c36f3eadbe1ab4f5b`  
		Last Modified: Wed, 11 Jan 2023 03:59:35 GMT  
		Size: 52.5 MB (52549696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812134a97ce41f8f31052309638b75bb6aaa642f97c7651ad4de14d3ae8367c5`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c887f3198f5407ad0f3df301a53ecb084eb9ce4b962b72db984d1aea1aa401`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d3dce85443993cd688868bce0e21e6bbe5e1d91ea7478a3c41fc55d23be5f3`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe79279fcda944111b666bef5e8fcd9e17a0ffc5bb460227e37a4e0e6d3f3562`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.0` - linux; ppc64le

```console
$ docker pull couchdb@sha256:4d6b05042044225fc1ff9532c1edd602d0fc750d35cac8ff858a8ff06205e1d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96677789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3598983d07c56e8d4b91d1e40075e104c3cb7e9af92e4c200b6291d8c8a1b3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 03:49:30 GMT
ADD file:3c7553fb5eda606d574ff6c08bc2213f9e6a68910043fe3087e4c1a04b65a18e in / 
# Wed, 11 Jan 2023 03:49:32 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 04:17:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 04:17:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 04:18:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:18:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 04:18:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 04:18:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:18:23 GMT
ENV COUCHDB_VERSION=3.3.0
# Wed, 11 Jan 2023 04:18:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 04:18:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 04:18:50 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 04:18:50 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 04:18:50 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 04:18:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 04:18:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 04:18:52 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 04:18:52 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 04:18:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bbf81328aca90b7ddb122fc175443f5323674a9e51bbb00d5b1d683ef0b858f4`  
		Last Modified: Wed, 11 Jan 2023 03:55:33 GMT  
		Size: 35.3 MB (35268773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d4b7dfde57dc3b711e2273da5a61a5829a57b9d58474f1d5ffd21634458f5e`  
		Last Modified: Wed, 11 Jan 2023 04:19:54 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e0b83a7c039dc80fa7b1d8424d0c1a059fbd972e127d4bb4845181526ca907`  
		Last Modified: Wed, 11 Jan 2023 04:19:54 GMT  
		Size: 6.0 MB (6043874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2673661962247aa7e2f981fd8bfb91ba790a2cf92ab3c5c63e6e1340e5f5bc5b`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 1.5 MB (1509211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c497897d6b3b0e80026e3b729b1d0d01cb112a46c93249841c7394cb4930e3`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 295.5 KB (295534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e147edb3c0e81852fd5b883ae96cae30c9de2f81a7057e45188be3e1059e0aca`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc6f7e67309c7cde8911e23783a30f691fe986cf9b79e185f3cc904877134a6`  
		Last Modified: Wed, 11 Jan 2023 04:19:59 GMT  
		Size: 53.6 MB (53553258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d38eb64d280ea68213c9f68e36c544e73c614d8487daf917414f5e4d3f3cbe2`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77b0769427d4085a204e9b363d301ee1da0315634e0ff4f8df8daba91998694`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c49240b3d78c657c4c382b920923ac4a3db5bb640b05e7f674969ccefbced46`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250b59b18ccba5cb48d1c83a196a4b40629090ba7751356fe560871529379183`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:2cb4cacb5b2e8b8ee60b692f42c63f02d23cae0ea1a5e324e26737bf328f335e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:3f3704ddfb6014435f2611a611efcfe465f04d56bc3d5f92c9955493a3cdb3af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91170738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799ba382589148b50a50959977441a8f86654f60b0a06ac5ee1284c35a19e033`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:42:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 03:42:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 03:42:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:42:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 03:42:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 03:42:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:42:24 GMT
ENV COUCHDB_VERSION=3.3.0
# Wed, 11 Jan 2023 03:42:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:42:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:42:38 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:42:38 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:42:38 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 03:42:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:42:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:42:39 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:42:39 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:42:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b54fc1f41d9e17df7d49c1f5111f508dcb398b5196ebba6d187873dc3480ac6`  
		Last Modified: Wed, 11 Jan 2023 03:44:34 GMT  
		Size: 3.4 KB (3407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb927a4266fd4cede9f246cd7618acfdc3616eb4317e9cb36336d6c1cc6fd06`  
		Last Modified: Wed, 11 Jan 2023 03:44:33 GMT  
		Size: 5.2 MB (5224274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4e44b11124abc70dfa0c6427e095db1f27f6dde701d1f7189b11da9493502c`  
		Last Modified: Wed, 11 Jan 2023 03:44:32 GMT  
		Size: 1.6 MB (1553321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef2a9c48048ec5db36fe98ca1615725d8b2ffae3208912b30f46d66350d567c`  
		Last Modified: Wed, 11 Jan 2023 03:44:32 GMT  
		Size: 295.6 KB (295572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1733bf1e1f601845827b5e2fbaea7f2787c0a1569115aebe2409b21c75e844e7`  
		Last Modified: Wed, 11 Jan 2023 03:44:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad41b48fc6b9e5728cf2a545800c04c14be2aed0ab458dc16950b9d147e1fb3`  
		Last Modified: Wed, 11 Jan 2023 03:44:35 GMT  
		Size: 52.7 MB (52693469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfd0f547079ce8a04faf5ecf4aaf0101e801cba0b16becec736bc8f097ccfa6`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6296a2f8c0c9d1836022dfeaca4678825180d16ff3a991aef1fc41f235afb0ff`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c775ec994f746eae7f636d0bfb61cbbeb0f6519e95956936e9266d06eab1f2`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2509d15830b488026e0b012f58465b22e97bb86522fe7bcf12fdf50ec1abdb37`  
		Last Modified: Wed, 11 Jan 2023 03:44:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f4406d33306fe49a7a2e30f35b5dbd5cbfa273d862a666d4eeade997434ba124
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d525ca39e94698fcf20b7b2375614336e6667fa8df217e74fd18d84aa59ec7b1`
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
# Wed, 11 Jan 2023 03:57:50 GMT
ENV COUCHDB_VERSION=3.3.0
# Wed, 11 Jan 2023 03:57:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 03:58:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 03:58:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 03:58:02 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 03:58:02 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 03:58:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 03:58:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:58:03 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 03:58:03 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 03:58:03 GMT
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
	-	`sha256:30f094d764575f750f083741eef9b006b2b8f38377066123276183970c9f4b9c`  
		Last Modified: Wed, 11 Jan 2023 03:59:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d18c7d73142c458e120afbad0b523afbea47c5dd64c907c36f3eadbe1ab4f5b`  
		Last Modified: Wed, 11 Jan 2023 03:59:35 GMT  
		Size: 52.5 MB (52549696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812134a97ce41f8f31052309638b75bb6aaa642f97c7651ad4de14d3ae8367c5`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c887f3198f5407ad0f3df301a53ecb084eb9ce4b962b72db984d1aea1aa401`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d3dce85443993cd688868bce0e21e6bbe5e1d91ea7478a3c41fc55d23be5f3`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe79279fcda944111b666bef5e8fcd9e17a0ffc5bb460227e37a4e0e6d3f3562`  
		Last Modified: Wed, 11 Jan 2023 03:59:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:4d6b05042044225fc1ff9532c1edd602d0fc750d35cac8ff858a8ff06205e1d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96677789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3598983d07c56e8d4b91d1e40075e104c3cb7e9af92e4c200b6291d8c8a1b3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Jan 2023 03:49:30 GMT
ADD file:3c7553fb5eda606d574ff6c08bc2213f9e6a68910043fe3087e4c1a04b65a18e in / 
# Wed, 11 Jan 2023 03:49:32 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 04:17:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Jan 2023 04:17:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Jan 2023 04:18:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:18:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Jan 2023 04:18:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Jan 2023 04:18:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:18:23 GMT
ENV COUCHDB_VERSION=3.3.0
# Wed, 11 Jan 2023 04:18:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Jan 2023 04:18:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Jan 2023 04:18:50 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Jan 2023 04:18:50 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Jan 2023 04:18:50 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 Jan 2023 04:18:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Jan 2023 04:18:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 04:18:52 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Jan 2023 04:18:52 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Jan 2023 04:18:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bbf81328aca90b7ddb122fc175443f5323674a9e51bbb00d5b1d683ef0b858f4`  
		Last Modified: Wed, 11 Jan 2023 03:55:33 GMT  
		Size: 35.3 MB (35268773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d4b7dfde57dc3b711e2273da5a61a5829a57b9d58474f1d5ffd21634458f5e`  
		Last Modified: Wed, 11 Jan 2023 04:19:54 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e0b83a7c039dc80fa7b1d8424d0c1a059fbd972e127d4bb4845181526ca907`  
		Last Modified: Wed, 11 Jan 2023 04:19:54 GMT  
		Size: 6.0 MB (6043874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2673661962247aa7e2f981fd8bfb91ba790a2cf92ab3c5c63e6e1340e5f5bc5b`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 1.5 MB (1509211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c497897d6b3b0e80026e3b729b1d0d01cb112a46c93249841c7394cb4930e3`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 295.5 KB (295534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e147edb3c0e81852fd5b883ae96cae30c9de2f81a7057e45188be3e1059e0aca`  
		Last Modified: Wed, 11 Jan 2023 04:19:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc6f7e67309c7cde8911e23783a30f691fe986cf9b79e185f3cc904877134a6`  
		Last Modified: Wed, 11 Jan 2023 04:19:59 GMT  
		Size: 53.6 MB (53553258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d38eb64d280ea68213c9f68e36c544e73c614d8487daf917414f5e4d3f3cbe2`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77b0769427d4085a204e9b363d301ee1da0315634e0ff4f8df8daba91998694`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c49240b3d78c657c4c382b920923ac4a3db5bb640b05e7f674969ccefbced46`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250b59b18ccba5cb48d1c83a196a4b40629090ba7751356fe560871529379183`  
		Last Modified: Wed, 11 Jan 2023 04:19:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
