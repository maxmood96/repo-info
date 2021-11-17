<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.2`](#couchdb312)
-	[`couchdb:3.2`](#couchdb32)
-	[`couchdb:3.2.0`](#couchdb320)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:ba616d371f4a840cd6f2601af2954da9a371910687a33b1284971e8be819cafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:6e2232e6e2c4d7fff955ed8373ce99f91703bf99d8d1a3550b1ce0282331616f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef89ef79d29cc4c912824d323c7a17658e616b6205f438be9dfdfac1ec5fe2ec`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:36:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:36:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:36:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:36:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:36:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:37:46 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 17 Nov 2021 03:37:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:38:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:38:11 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:38:11 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:38:11 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 17 Nov 2021 03:38:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:38:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:38:13 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:38:13 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:38:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa9620155d936e98f43252dadc4e586951619a4986135c8f8b2088f0c651867`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31474bb5de7990ab6e7451ab4ebe08ab585ed87effb09bf982e13e41133da5f3`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 6.7 MB (6691326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5918906c341559cdc91df9aaccee014f9677ee7af9918df48c0f65880a6e4fbf`  
		Last Modified: Wed, 17 Nov 2021 03:38:36 GMT  
		Size: 1.3 MB (1258351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b07f325620694878eeead65f0dde169fbe2dbc20b052636e40b2345bfc0ce29`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 293.0 KB (292981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28ed6dc654ad2528e0eb7de424ad67bbd5087908448f821c7711f8deb5e3a4d`  
		Last Modified: Wed, 17 Nov 2021 03:39:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f138b38ade0d5c5f3354be4b86a2be8bae9e22ff92409df06bd1c3c44b54daa3`  
		Last Modified: Wed, 17 Nov 2021 03:39:19 GMT  
		Size: 49.1 MB (49113816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8196bf2917cf118f3c8890a5587a6f05e2c075ba3c332464207c6efa8b2d9`  
		Last Modified: Wed, 17 Nov 2021 03:39:12 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d91a5ad7e2067bdffbdc5b9b2cad669ca6d3ef58e25132e6bf69e4aeaca7c7`  
		Last Modified: Wed, 17 Nov 2021 03:39:12 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7368323eb80a50ef02f60e816a9e28c4885b3f041531571ae9ba4c1095c94ffa`  
		Last Modified: Wed, 17 Nov 2021 03:39:12 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffbfa9181f5687694199083926dbefe7ba73633e3d0b7a9e757d744fcde5105`  
		Last Modified: Wed, 17 Nov 2021 03:39:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a2234d5ef9cfaf5250ea7fe5c5aace9f2970510e264c192437d43bb7f50b1124
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87390f597386e9612170756997a4b24dad965808b0a0563b78a74535774c0fef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:14:06 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 17 Nov 2021 03:14:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:14:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:14:27 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:14:28 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:14:29 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 17 Nov 2021 03:14:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:14:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:14:31 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:14:32 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:14:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde381ec5a1278d2a68005ae0d1fae341c35a340efb3d9b90be4fe049c4ef8a`  
		Last Modified: Wed, 17 Nov 2021 03:15:42 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5474d94037945201cc5d7571f55def71d28fc890d3bc387495108a7a0bee632d`  
		Last Modified: Wed, 17 Nov 2021 03:15:45 GMT  
		Size: 39.0 MB (39011901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3b7c8996739229afa8080719316aa93ea6f0cba82b9d12e581dcb4999f345`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09df975511d34ed7f321268c943fd807a0e9fe1458bdd8bb4fd7ec82dffcfd03`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5607f62215bb22d77ff6f9f8bb4949ab62b0980260bf0e4c49e1a7567ccf128a`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e953c19ec4cff6a88215e2380d9df7cd5907027ea651ffece0a60c7b7a3302`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:ba616d371f4a840cd6f2601af2954da9a371910687a33b1284971e8be819cafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:6e2232e6e2c4d7fff955ed8373ce99f91703bf99d8d1a3550b1ce0282331616f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef89ef79d29cc4c912824d323c7a17658e616b6205f438be9dfdfac1ec5fe2ec`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:36:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:36:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:36:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:36:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:36:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:37:46 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 17 Nov 2021 03:37:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:38:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:38:11 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:38:11 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:38:11 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 17 Nov 2021 03:38:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:38:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:38:13 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:38:13 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:38:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa9620155d936e98f43252dadc4e586951619a4986135c8f8b2088f0c651867`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31474bb5de7990ab6e7451ab4ebe08ab585ed87effb09bf982e13e41133da5f3`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 6.7 MB (6691326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5918906c341559cdc91df9aaccee014f9677ee7af9918df48c0f65880a6e4fbf`  
		Last Modified: Wed, 17 Nov 2021 03:38:36 GMT  
		Size: 1.3 MB (1258351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b07f325620694878eeead65f0dde169fbe2dbc20b052636e40b2345bfc0ce29`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 293.0 KB (292981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28ed6dc654ad2528e0eb7de424ad67bbd5087908448f821c7711f8deb5e3a4d`  
		Last Modified: Wed, 17 Nov 2021 03:39:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f138b38ade0d5c5f3354be4b86a2be8bae9e22ff92409df06bd1c3c44b54daa3`  
		Last Modified: Wed, 17 Nov 2021 03:39:19 GMT  
		Size: 49.1 MB (49113816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8196bf2917cf118f3c8890a5587a6f05e2c075ba3c332464207c6efa8b2d9`  
		Last Modified: Wed, 17 Nov 2021 03:39:12 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d91a5ad7e2067bdffbdc5b9b2cad669ca6d3ef58e25132e6bf69e4aeaca7c7`  
		Last Modified: Wed, 17 Nov 2021 03:39:12 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7368323eb80a50ef02f60e816a9e28c4885b3f041531571ae9ba4c1095c94ffa`  
		Last Modified: Wed, 17 Nov 2021 03:39:12 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffbfa9181f5687694199083926dbefe7ba73633e3d0b7a9e757d744fcde5105`  
		Last Modified: Wed, 17 Nov 2021 03:39:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a2234d5ef9cfaf5250ea7fe5c5aace9f2970510e264c192437d43bb7f50b1124
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87390f597386e9612170756997a4b24dad965808b0a0563b78a74535774c0fef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:14:06 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 17 Nov 2021 03:14:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:14:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:14:27 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:14:28 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:14:29 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 17 Nov 2021 03:14:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:14:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:14:31 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:14:32 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:14:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde381ec5a1278d2a68005ae0d1fae341c35a340efb3d9b90be4fe049c4ef8a`  
		Last Modified: Wed, 17 Nov 2021 03:15:42 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5474d94037945201cc5d7571f55def71d28fc890d3bc387495108a7a0bee632d`  
		Last Modified: Wed, 17 Nov 2021 03:15:45 GMT  
		Size: 39.0 MB (39011901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3b7c8996739229afa8080719316aa93ea6f0cba82b9d12e581dcb4999f345`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09df975511d34ed7f321268c943fd807a0e9fe1458bdd8bb4fd7ec82dffcfd03`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5607f62215bb22d77ff6f9f8bb4949ab62b0980260bf0e4c49e1a7567ccf128a`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e953c19ec4cff6a88215e2380d9df7cd5907027ea651ffece0a60c7b7a3302`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:ba616d371f4a840cd6f2601af2954da9a371910687a33b1284971e8be819cafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:6e2232e6e2c4d7fff955ed8373ce99f91703bf99d8d1a3550b1ce0282331616f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef89ef79d29cc4c912824d323c7a17658e616b6205f438be9dfdfac1ec5fe2ec`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:36:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:36:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:36:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:36:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:36:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:37:46 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 17 Nov 2021 03:37:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:38:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:38:11 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:38:11 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:38:11 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 17 Nov 2021 03:38:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:38:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:38:13 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:38:13 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:38:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa9620155d936e98f43252dadc4e586951619a4986135c8f8b2088f0c651867`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31474bb5de7990ab6e7451ab4ebe08ab585ed87effb09bf982e13e41133da5f3`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 6.7 MB (6691326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5918906c341559cdc91df9aaccee014f9677ee7af9918df48c0f65880a6e4fbf`  
		Last Modified: Wed, 17 Nov 2021 03:38:36 GMT  
		Size: 1.3 MB (1258351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b07f325620694878eeead65f0dde169fbe2dbc20b052636e40b2345bfc0ce29`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 293.0 KB (292981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28ed6dc654ad2528e0eb7de424ad67bbd5087908448f821c7711f8deb5e3a4d`  
		Last Modified: Wed, 17 Nov 2021 03:39:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f138b38ade0d5c5f3354be4b86a2be8bae9e22ff92409df06bd1c3c44b54daa3`  
		Last Modified: Wed, 17 Nov 2021 03:39:19 GMT  
		Size: 49.1 MB (49113816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8196bf2917cf118f3c8890a5587a6f05e2c075ba3c332464207c6efa8b2d9`  
		Last Modified: Wed, 17 Nov 2021 03:39:12 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d91a5ad7e2067bdffbdc5b9b2cad669ca6d3ef58e25132e6bf69e4aeaca7c7`  
		Last Modified: Wed, 17 Nov 2021 03:39:12 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7368323eb80a50ef02f60e816a9e28c4885b3f041531571ae9ba4c1095c94ffa`  
		Last Modified: Wed, 17 Nov 2021 03:39:12 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffbfa9181f5687694199083926dbefe7ba73633e3d0b7a9e757d744fcde5105`  
		Last Modified: Wed, 17 Nov 2021 03:39:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a2234d5ef9cfaf5250ea7fe5c5aace9f2970510e264c192437d43bb7f50b1124
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87390f597386e9612170756997a4b24dad965808b0a0563b78a74535774c0fef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:14:06 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 17 Nov 2021 03:14:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:14:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:14:27 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:14:28 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:14:29 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 17 Nov 2021 03:14:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:14:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:14:31 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:14:32 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:14:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde381ec5a1278d2a68005ae0d1fae341c35a340efb3d9b90be4fe049c4ef8a`  
		Last Modified: Wed, 17 Nov 2021 03:15:42 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5474d94037945201cc5d7571f55def71d28fc890d3bc387495108a7a0bee632d`  
		Last Modified: Wed, 17 Nov 2021 03:15:45 GMT  
		Size: 39.0 MB (39011901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3b7c8996739229afa8080719316aa93ea6f0cba82b9d12e581dcb4999f345`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09df975511d34ed7f321268c943fd807a0e9fe1458bdd8bb4fd7ec82dffcfd03`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5607f62215bb22d77ff6f9f8bb4949ab62b0980260bf0e4c49e1a7567ccf128a`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e953c19ec4cff6a88215e2380d9df7cd5907027ea651ffece0a60c7b7a3302`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:b5a62a68fbe6e37401736f5da9c9bdb47975b20c3b04816f8410bcdfd711959b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:d44ca1317fa02802757690c4006115ce59183c87c019da95c9823cecef20902a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80555231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b72edd8b1ad67c4847fa458541026d4d4960f98c26e4665faf16f241f18346`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:36:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:36:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:36:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:36:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:36:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:49 GMT
ENV COUCHDB_VERSION=3.2.0
# Wed, 17 Nov 2021 03:36:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:37:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:37:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:37:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:37:09 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:37:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:37:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:37:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:37:11 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:37:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa9620155d936e98f43252dadc4e586951619a4986135c8f8b2088f0c651867`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31474bb5de7990ab6e7451ab4ebe08ab585ed87effb09bf982e13e41133da5f3`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 6.7 MB (6691326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5918906c341559cdc91df9aaccee014f9677ee7af9918df48c0f65880a6e4fbf`  
		Last Modified: Wed, 17 Nov 2021 03:38:36 GMT  
		Size: 1.3 MB (1258351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b07f325620694878eeead65f0dde169fbe2dbc20b052636e40b2345bfc0ce29`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 293.0 KB (292981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fced536466abc950895abafa11cb0321801b50d0b88972774d621dcfeebd5048`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7372d4c41a2b14f6c1f5a562ceaa27cf9df18aad065b51a7f924eb88b0639c4`  
		Last Modified: Wed, 17 Nov 2021 03:38:39 GMT  
		Size: 45.2 MB (45151883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbcf15db1a866454cfee77ce904e73f33156d24384d99aba1fcd8fe91736381`  
		Last Modified: Wed, 17 Nov 2021 03:38:33 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37394932887976e4d6098fffa582e2312d7a6066d8d27e2179d0611e37663cb0`  
		Last Modified: Wed, 17 Nov 2021 03:38:32 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3a1135068494686c93ce341d735e8d498ec132b550f0b709dbb1abb9f4bde5`  
		Last Modified: Wed, 17 Nov 2021 03:38:32 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cd74753ae8a80e23a9433a800a678704eca6d66c3939bd6d0f98c9a1547e75`  
		Last Modified: Wed, 17 Nov 2021 03:38:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f2030d9ddbcb3ed7120aeeebdc4b089b0d969ad833a1a792297c0797c08bf33d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75231135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f19af1927bdddc0bceb963c64ece13b6daa206f047105a8a225966ffa901bcb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:58 GMT
ENV COUCHDB_VERSION=3.2.0
# Wed, 17 Nov 2021 03:12:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:13:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:13:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:13:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:13:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:13:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:13:23 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:13:24 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:13:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f10d6d3037836c6c8aa5c296f0f70e385564599dbbafe34639ded032c0e9c6`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95555d888dc786cead48d13eadcb9e9fc7e69b2ad36a9b2bd3ee118469e0dd7c`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 41.7 MB (41720155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922085445cffcaed101abaf1c2aed29901463589f4ca49f7be8dac5d197e12f`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0e02dae87f84ebee883fd339617c2324b116a2439ae1a225d22ce5dce53b11`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78060cecbefc0e301d5732233088293e426decdfb208b0e80307ba8c2ad95355`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9c11ef87ada6fcbf0f410909cc4aa6f1d28ed15ac59d1787f5624afdfb073e`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:69dcac2b2149b7540d54188779c865a33f425c6b146bca1ff3a57af83c310f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:9f234b9ce4d544eb99bd730d375dbbb0ed23738000039b5433a31eb5d7b5c54c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80003298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0184c1fca810d56d31875de1c89a5cbbd218301af3cc30c5271ea4ba1ed6ae`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:36:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:36:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:36:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:36:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:36:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:37:18 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 17 Nov 2021 03:37:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:37:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:37:39 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:37:39 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:37:39 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:37:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:37:40 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:37:41 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:37:41 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:37:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa9620155d936e98f43252dadc4e586951619a4986135c8f8b2088f0c651867`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31474bb5de7990ab6e7451ab4ebe08ab585ed87effb09bf982e13e41133da5f3`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 6.7 MB (6691326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5918906c341559cdc91df9aaccee014f9677ee7af9918df48c0f65880a6e4fbf`  
		Last Modified: Wed, 17 Nov 2021 03:38:36 GMT  
		Size: 1.3 MB (1258351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b07f325620694878eeead65f0dde169fbe2dbc20b052636e40b2345bfc0ce29`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 293.0 KB (292981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae37f29a6727fbc017899df29dbf435b1adb02a7037945a36dd212208a9e708`  
		Last Modified: Wed, 17 Nov 2021 03:38:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3c2d6b2e685cd2e974fb452c96be6a6a093fde22766ce3af431ce227e726e9`  
		Last Modified: Wed, 17 Nov 2021 03:39:02 GMT  
		Size: 44.6 MB (44599951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f145d10d4072ad82eec6f57e97529819b2978b251a397e77664b72509b39589`  
		Last Modified: Wed, 17 Nov 2021 03:38:57 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de48a6fff725be1ed755b629b9a19702ad654817d7825590695457517f2d9d84`  
		Last Modified: Wed, 17 Nov 2021 03:38:57 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178ddf1c8218eb4d3a556a658b82bf3c69a52efdeb989fab3375a185c6aa5b5`  
		Last Modified: Wed, 17 Nov 2021 03:38:57 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa532811a69ab48bc62aafbd38cd96eb46d9590bc83eeac77c4d325ca4af3f0`  
		Last Modified: Wed, 17 Nov 2021 03:38:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c4d8a1503ca18c1599eba18e97ea21f228e920c878c5a5f7b1d69be01e1fa028
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74612278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89f734b1ac6c68282b0b172ad767b2a25e273b044473eec4cb7799c1d5d8de7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:13:35 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 17 Nov 2021 03:13:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:13:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:13:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:13:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:13:57 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:13:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:13:58 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:13:59 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:14:00 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:14:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d364f5670abffa7a117aff9a0b2fee592035bd61977f33d207385acea580116`  
		Last Modified: Wed, 17 Nov 2021 03:15:25 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f10831ac14d41ed907e4f278276ba6e26edbb08cc2e0b5e7bb5d9bcc6ea445`  
		Last Modified: Wed, 17 Nov 2021 03:15:28 GMT  
		Size: 41.1 MB (41101292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948b99fd9aa4a4e910f342b607ef4b97636f303a5418b495c5f688f3651bd008`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0137091501598bb5ba6d1bc7177f360aebd145dd89b4f66b3ffe64d74926807`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7725280cc9bcd2bd19da4451bb3639ebf0acabd14b68b947205d63a6203b12`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd45677a03cb8eac3e45939d3b2e2428af023d360c11760a0e1f40e5c162486`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:69dcac2b2149b7540d54188779c865a33f425c6b146bca1ff3a57af83c310f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:9f234b9ce4d544eb99bd730d375dbbb0ed23738000039b5433a31eb5d7b5c54c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80003298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0184c1fca810d56d31875de1c89a5cbbd218301af3cc30c5271ea4ba1ed6ae`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:36:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:36:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:36:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:36:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:36:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:37:18 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 17 Nov 2021 03:37:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:37:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:37:39 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:37:39 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:37:39 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:37:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:37:40 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:37:41 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:37:41 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:37:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa9620155d936e98f43252dadc4e586951619a4986135c8f8b2088f0c651867`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31474bb5de7990ab6e7451ab4ebe08ab585ed87effb09bf982e13e41133da5f3`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 6.7 MB (6691326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5918906c341559cdc91df9aaccee014f9677ee7af9918df48c0f65880a6e4fbf`  
		Last Modified: Wed, 17 Nov 2021 03:38:36 GMT  
		Size: 1.3 MB (1258351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b07f325620694878eeead65f0dde169fbe2dbc20b052636e40b2345bfc0ce29`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 293.0 KB (292981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae37f29a6727fbc017899df29dbf435b1adb02a7037945a36dd212208a9e708`  
		Last Modified: Wed, 17 Nov 2021 03:38:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3c2d6b2e685cd2e974fb452c96be6a6a093fde22766ce3af431ce227e726e9`  
		Last Modified: Wed, 17 Nov 2021 03:39:02 GMT  
		Size: 44.6 MB (44599951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f145d10d4072ad82eec6f57e97529819b2978b251a397e77664b72509b39589`  
		Last Modified: Wed, 17 Nov 2021 03:38:57 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de48a6fff725be1ed755b629b9a19702ad654817d7825590695457517f2d9d84`  
		Last Modified: Wed, 17 Nov 2021 03:38:57 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178ddf1c8218eb4d3a556a658b82bf3c69a52efdeb989fab3375a185c6aa5b5`  
		Last Modified: Wed, 17 Nov 2021 03:38:57 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa532811a69ab48bc62aafbd38cd96eb46d9590bc83eeac77c4d325ca4af3f0`  
		Last Modified: Wed, 17 Nov 2021 03:38:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c4d8a1503ca18c1599eba18e97ea21f228e920c878c5a5f7b1d69be01e1fa028
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74612278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89f734b1ac6c68282b0b172ad767b2a25e273b044473eec4cb7799c1d5d8de7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:13:35 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 17 Nov 2021 03:13:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:13:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:13:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:13:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:13:57 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:13:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:13:58 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:13:59 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:14:00 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:14:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d364f5670abffa7a117aff9a0b2fee592035bd61977f33d207385acea580116`  
		Last Modified: Wed, 17 Nov 2021 03:15:25 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f10831ac14d41ed907e4f278276ba6e26edbb08cc2e0b5e7bb5d9bcc6ea445`  
		Last Modified: Wed, 17 Nov 2021 03:15:28 GMT  
		Size: 41.1 MB (41101292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948b99fd9aa4a4e910f342b607ef4b97636f303a5418b495c5f688f3651bd008`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0137091501598bb5ba6d1bc7177f360aebd145dd89b4f66b3ffe64d74926807`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7725280cc9bcd2bd19da4451bb3639ebf0acabd14b68b947205d63a6203b12`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd45677a03cb8eac3e45939d3b2e2428af023d360c11760a0e1f40e5c162486`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:b5a62a68fbe6e37401736f5da9c9bdb47975b20c3b04816f8410bcdfd711959b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:d44ca1317fa02802757690c4006115ce59183c87c019da95c9823cecef20902a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80555231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b72edd8b1ad67c4847fa458541026d4d4960f98c26e4665faf16f241f18346`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:36:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:36:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:36:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:36:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:36:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:49 GMT
ENV COUCHDB_VERSION=3.2.0
# Wed, 17 Nov 2021 03:36:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:37:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:37:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:37:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:37:09 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:37:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:37:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:37:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:37:11 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:37:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa9620155d936e98f43252dadc4e586951619a4986135c8f8b2088f0c651867`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31474bb5de7990ab6e7451ab4ebe08ab585ed87effb09bf982e13e41133da5f3`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 6.7 MB (6691326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5918906c341559cdc91df9aaccee014f9677ee7af9918df48c0f65880a6e4fbf`  
		Last Modified: Wed, 17 Nov 2021 03:38:36 GMT  
		Size: 1.3 MB (1258351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b07f325620694878eeead65f0dde169fbe2dbc20b052636e40b2345bfc0ce29`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 293.0 KB (292981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fced536466abc950895abafa11cb0321801b50d0b88972774d621dcfeebd5048`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7372d4c41a2b14f6c1f5a562ceaa27cf9df18aad065b51a7f924eb88b0639c4`  
		Last Modified: Wed, 17 Nov 2021 03:38:39 GMT  
		Size: 45.2 MB (45151883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbcf15db1a866454cfee77ce904e73f33156d24384d99aba1fcd8fe91736381`  
		Last Modified: Wed, 17 Nov 2021 03:38:33 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37394932887976e4d6098fffa582e2312d7a6066d8d27e2179d0611e37663cb0`  
		Last Modified: Wed, 17 Nov 2021 03:38:32 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3a1135068494686c93ce341d735e8d498ec132b550f0b709dbb1abb9f4bde5`  
		Last Modified: Wed, 17 Nov 2021 03:38:32 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cd74753ae8a80e23a9433a800a678704eca6d66c3939bd6d0f98c9a1547e75`  
		Last Modified: Wed, 17 Nov 2021 03:38:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f2030d9ddbcb3ed7120aeeebdc4b089b0d969ad833a1a792297c0797c08bf33d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75231135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f19af1927bdddc0bceb963c64ece13b6daa206f047105a8a225966ffa901bcb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:58 GMT
ENV COUCHDB_VERSION=3.2.0
# Wed, 17 Nov 2021 03:12:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:13:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:13:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:13:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:13:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:13:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:13:23 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:13:24 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:13:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f10d6d3037836c6c8aa5c296f0f70e385564599dbbafe34639ded032c0e9c6`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95555d888dc786cead48d13eadcb9e9fc7e69b2ad36a9b2bd3ee118469e0dd7c`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 41.7 MB (41720155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922085445cffcaed101abaf1c2aed29901463589f4ca49f7be8dac5d197e12f`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0e02dae87f84ebee883fd339617c2324b116a2439ae1a225d22ce5dce53b11`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78060cecbefc0e301d5732233088293e426decdfb208b0e80307ba8c2ad95355`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9c11ef87ada6fcbf0f410909cc4aa6f1d28ed15ac59d1787f5624afdfb073e`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.0`

```console
$ docker pull couchdb@sha256:b5a62a68fbe6e37401736f5da9c9bdb47975b20c3b04816f8410bcdfd711959b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.2.0` - linux; amd64

```console
$ docker pull couchdb@sha256:d44ca1317fa02802757690c4006115ce59183c87c019da95c9823cecef20902a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80555231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b72edd8b1ad67c4847fa458541026d4d4960f98c26e4665faf16f241f18346`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:36:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:36:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:36:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:36:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:36:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:49 GMT
ENV COUCHDB_VERSION=3.2.0
# Wed, 17 Nov 2021 03:36:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:37:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:37:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:37:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:37:09 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:37:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:37:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:37:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:37:11 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:37:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa9620155d936e98f43252dadc4e586951619a4986135c8f8b2088f0c651867`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31474bb5de7990ab6e7451ab4ebe08ab585ed87effb09bf982e13e41133da5f3`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 6.7 MB (6691326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5918906c341559cdc91df9aaccee014f9677ee7af9918df48c0f65880a6e4fbf`  
		Last Modified: Wed, 17 Nov 2021 03:38:36 GMT  
		Size: 1.3 MB (1258351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b07f325620694878eeead65f0dde169fbe2dbc20b052636e40b2345bfc0ce29`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 293.0 KB (292981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fced536466abc950895abafa11cb0321801b50d0b88972774d621dcfeebd5048`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7372d4c41a2b14f6c1f5a562ceaa27cf9df18aad065b51a7f924eb88b0639c4`  
		Last Modified: Wed, 17 Nov 2021 03:38:39 GMT  
		Size: 45.2 MB (45151883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbcf15db1a866454cfee77ce904e73f33156d24384d99aba1fcd8fe91736381`  
		Last Modified: Wed, 17 Nov 2021 03:38:33 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37394932887976e4d6098fffa582e2312d7a6066d8d27e2179d0611e37663cb0`  
		Last Modified: Wed, 17 Nov 2021 03:38:32 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3a1135068494686c93ce341d735e8d498ec132b550f0b709dbb1abb9f4bde5`  
		Last Modified: Wed, 17 Nov 2021 03:38:32 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cd74753ae8a80e23a9433a800a678704eca6d66c3939bd6d0f98c9a1547e75`  
		Last Modified: Wed, 17 Nov 2021 03:38:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f2030d9ddbcb3ed7120aeeebdc4b089b0d969ad833a1a792297c0797c08bf33d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75231135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f19af1927bdddc0bceb963c64ece13b6daa206f047105a8a225966ffa901bcb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:58 GMT
ENV COUCHDB_VERSION=3.2.0
# Wed, 17 Nov 2021 03:12:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:13:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:13:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:13:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:13:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:13:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:13:23 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:13:24 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:13:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f10d6d3037836c6c8aa5c296f0f70e385564599dbbafe34639ded032c0e9c6`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95555d888dc786cead48d13eadcb9e9fc7e69b2ad36a9b2bd3ee118469e0dd7c`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 41.7 MB (41720155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922085445cffcaed101abaf1c2aed29901463589f4ca49f7be8dac5d197e12f`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0e02dae87f84ebee883fd339617c2324b116a2439ae1a225d22ce5dce53b11`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78060cecbefc0e301d5732233088293e426decdfb208b0e80307ba8c2ad95355`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9c11ef87ada6fcbf0f410909cc4aa6f1d28ed15ac59d1787f5624afdfb073e`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:b5a62a68fbe6e37401736f5da9c9bdb47975b20c3b04816f8410bcdfd711959b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:d44ca1317fa02802757690c4006115ce59183c87c019da95c9823cecef20902a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80555231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b72edd8b1ad67c4847fa458541026d4d4960f98c26e4665faf16f241f18346`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:36:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:36:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:36:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:36:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:36:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:49 GMT
ENV COUCHDB_VERSION=3.2.0
# Wed, 17 Nov 2021 03:36:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:37:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:37:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:37:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:37:09 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:37:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:37:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:37:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:37:11 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:37:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa9620155d936e98f43252dadc4e586951619a4986135c8f8b2088f0c651867`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31474bb5de7990ab6e7451ab4ebe08ab585ed87effb09bf982e13e41133da5f3`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 6.7 MB (6691326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5918906c341559cdc91df9aaccee014f9677ee7af9918df48c0f65880a6e4fbf`  
		Last Modified: Wed, 17 Nov 2021 03:38:36 GMT  
		Size: 1.3 MB (1258351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b07f325620694878eeead65f0dde169fbe2dbc20b052636e40b2345bfc0ce29`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 293.0 KB (292981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fced536466abc950895abafa11cb0321801b50d0b88972774d621dcfeebd5048`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7372d4c41a2b14f6c1f5a562ceaa27cf9df18aad065b51a7f924eb88b0639c4`  
		Last Modified: Wed, 17 Nov 2021 03:38:39 GMT  
		Size: 45.2 MB (45151883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbcf15db1a866454cfee77ce904e73f33156d24384d99aba1fcd8fe91736381`  
		Last Modified: Wed, 17 Nov 2021 03:38:33 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37394932887976e4d6098fffa582e2312d7a6066d8d27e2179d0611e37663cb0`  
		Last Modified: Wed, 17 Nov 2021 03:38:32 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3a1135068494686c93ce341d735e8d498ec132b550f0b709dbb1abb9f4bde5`  
		Last Modified: Wed, 17 Nov 2021 03:38:32 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cd74753ae8a80e23a9433a800a678704eca6d66c3939bd6d0f98c9a1547e75`  
		Last Modified: Wed, 17 Nov 2021 03:38:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f2030d9ddbcb3ed7120aeeebdc4b089b0d969ad833a1a792297c0797c08bf33d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75231135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f19af1927bdddc0bceb963c64ece13b6daa206f047105a8a225966ffa901bcb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:58 GMT
ENV COUCHDB_VERSION=3.2.0
# Wed, 17 Nov 2021 03:12:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:13:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:13:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:13:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:13:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:13:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:13:23 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:13:24 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:13:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f10d6d3037836c6c8aa5c296f0f70e385564599dbbafe34639ded032c0e9c6`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95555d888dc786cead48d13eadcb9e9fc7e69b2ad36a9b2bd3ee118469e0dd7c`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 41.7 MB (41720155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922085445cffcaed101abaf1c2aed29901463589f4ca49f7be8dac5d197e12f`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0e02dae87f84ebee883fd339617c2324b116a2439ae1a225d22ce5dce53b11`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78060cecbefc0e301d5732233088293e426decdfb208b0e80307ba8c2ad95355`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9c11ef87ada6fcbf0f410909cc4aa6f1d28ed15ac59d1787f5624afdfb073e`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
