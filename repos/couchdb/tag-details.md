<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3-nouveau`](#couchdb3-nouveau)
-	[`couchdb:3.4`](#couchdb34)
-	[`couchdb:3.4-nouveau`](#couchdb34-nouveau)
-	[`couchdb:3.4.3`](#couchdb343)
-	[`couchdb:3.4.3-nouveau`](#couchdb343-nouveau)
-	[`couchdb:3.5`](#couchdb35)
-	[`couchdb:3.5-nouveau`](#couchdb35-nouveau)
-	[`couchdb:3.5.1`](#couchdb351)
-	[`couchdb:3.5.1-nouveau`](#couchdb351-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:fa6d5ecadbcec3d20016e5ff78ff938051997859aac9f85a4072706ff25e8af8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:8a1ba2a19a4c6981e0c903c2c3cd4d59602748cae0246666818090091a1645ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142061148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806bab74c1a4fb65ea85eca0df6cbfaf75e633a8fe12b041057efc047f8c1b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:39:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:39:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 01:40:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:08 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 01:40:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:21 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 01:40:21 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 01:40:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a53138b1d134d26fa4d53d9a2683c90141d93b6e7bd622b6f43e87123095de`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d90394d687f0d05c4649b956181d3345b324547ad48051ae0f177b448cbaaed`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 7.9 MB (7883631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de30193b9c2bab17ecfbda0bcf2a02b262bd8ceafd9a031e19a120fd8c8ac1`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 401.8 KB (401802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cdf8fec417a2a0f21a217bd1809c4ea2cc4f135d262f6b0dcc8078c9a7c044`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 76.5 KB (76502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34740f51296d6acfab2fa462e3b8b1803c8737e466de7bbf0fe68db4d70eae7`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9cb5cf3e1dbb2d8da0afe8b27d8c08d85851a5ced23b121452557a3d3c751`  
		Last Modified: Wed, 22 Apr 2026 01:40:55 GMT  
		Size: 105.5 MB (105457531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de039ed6bde8981bad1b825c982292ee098f74b12f1b17c1ba36cfe31305eb3`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a0c60ddabd96476377d89beffea94139f3abd519bfe2f9addbefde09deac10`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731d920f2d4fef22403d1c15d88dd6c5ea16f0ad88cf18a477d7d5b2f9149f63`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408fb10825775c8965247a872391b284439aa7ca55f219ee2b556cd7af7f8cb`  
		Last Modified: Wed, 22 Apr 2026 01:40:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:3401257267e59435bdfe64dbed14ef495900c94738868e5585c90a8b15a0bf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbd66bb44251165fea91e9881fd9bba6ac85de3eb92c8b0575a83327bd36503`

```dockerfile
```

-	Layers:
	-	`sha256:5885b7c7950112751264b2ad2b6bc61f53aa9cf3d431edef5ecfe318a9857788`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf6461ec6d2ed586ec7996683ff351ab2e0289226e87e971668647852e88b16`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3acb3b244848b4ffd238614c6204188d96161de58e6b7c9b2b9c7de222b2e931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141421269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532eec0d6c7fd75306513a9dbdc863b5a5ab09a381fc1d3f71be45d5ea410fb9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:42:47 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 19:42:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:42:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:42:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:00 GMT
ENV COUCHDB_VERSION=3.5.1
# Fri, 08 May 2026 19:43:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:43:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 19:43:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 19:43:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 19:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 19:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:43:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:14 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 19:43:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 19:43:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ba953e3673b93911518c493226c251cc365cdd77c6f876549545639054dabe`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92f6f6706e91bfdfb4e3d908249946bc0dd23581108188076c4b762f669633`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 7.7 MB (7694199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fda1eb9ec2e98980355f7096bdb5fa0e0cc86eb7cfba3f94edf01ca4bac36e6`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 370.5 KB (370536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9d5a29d3a2313f5d79be0a785bca096dff87584599c7921c9c78d8ada69a3c`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdd14c29d7abeffaa6923ffeb66d5ef0400e5057c4d35b358f1053d82a14535`  
		Last Modified: Fri, 08 May 2026 19:43:28 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e2d9fa6ff2962ba383325e4cea1c47d0fc54d34aee23969f9aca08fb7606b0`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 105.2 MB (105158425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b656fbff7ffe21c15b175d9106b8d721ff47e526e319a726238fec2af887a491`  
		Last Modified: Fri, 08 May 2026 19:43:28 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6099ecd94170a7d1fb61ed09b34f5e2c7636c7ea1bdf1a0d92420b074db37712`  
		Last Modified: Fri, 08 May 2026 19:43:29 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1c6dfae50f327fc911f145185f8f7c342667a76aa8e546a5bb4c0d128e0ac6`  
		Last Modified: Fri, 08 May 2026 19:43:29 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be535dad739a0367a13c857220837b7aa02e54a888f3611cad87ad9423e626a`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:2314645392ccdfeadd1be29930c091001214b2ef586e8055f84a5dfc10566667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c884eecfdd4721074439971fe2feda35bab4206d1fa9cab39b28d760ed2f09d`

```dockerfile
```

-	Layers:
	-	`sha256:a122e139a2ecab33684a3fe2b00740464e19b56da6869432b8e9efc1a9ca657f`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d9270ca0635c8e43a137ef9ea2bd3d132f77f36bf563b585c50d43bc67115`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:877bc4f2e9cebde5f6dd5db0625e8c11c1d5fc1450749b8df1ca04eee385183f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225182040bb866da2edada7d68127d3de35b20144022da2ee5092b81a48ff243`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 02:32:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:32:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:54 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 02:32:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:33:12 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 02:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 02:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d77fe6e136fe8121f88c8e24891e2e3ce57d89ace081cd7917cd296bf2781`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c6fd13d86c4615402446553400ddbf811488b8652dfeaf1b30369df23a3d31`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 7.4 MB (7399499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977c5ff033346e1cf892081e6ed41c4dcce967c151c4974c113f4e0406b20fa`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 372.1 KB (372140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28cd61fdf1d3cba5a38ba01f0090a13b851c1b038b6006be4782108f438976`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0df2b1587eda8004175334929323a5430ee32ec7ca0ad93243315dcdfcb1c4d`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d01bd714bd29509eccc7ffd6d42cf54ecb8e91fdd75f00b3a997e6b6adbaf5`  
		Last Modified: Wed, 22 Apr 2026 02:33:35 GMT  
		Size: 104.0 MB (104028166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b90460439c32fbf3c5d889b6093560b179158059ea12b5c62a42ce21380a3fe`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d8c0832e7dbb36e1959f210cc39b9c2f06cded3a0918c38f62da8bb11fe9cc`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846e3f061b916fca388e65c142917fbb47748b12371a1cc92c23fb6caa3881ea`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2a413a15f2d3d0b12253a678fe2d6199c1424fe5ce4d2166204aefde16a81`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:9d0ddb4a733d4cb15d823ccf7fef246af5176b6fbaf3ea6aaef729aa2ddd8e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa74c39c384641d3f8ad817a1c998223d297e3d2453b62a75dbd87fc179ca1c5`

```dockerfile
```

-	Layers:
	-	`sha256:8ae251a1734f9ea12b57e27040fd43078355bb4d78477392c9868f468347d2e5`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cd4bab63ce540f1c9dc037237c27456a1710328cd50cf0b8b3606d11ee6480`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 31.7 KB (31737 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:80c7ba6728048896c1e526f4592e63d45d4aefbb287bb7fbf564a67877591c37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:92cd36a141af320a0e396b3f186e488441d8f5a67a56fac69caf54c5c3c46cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156463311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faeb20718102ff657dc6a855312eda1db690059113db9d85bd5187756618b39`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:40:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:40:01 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 01:40:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 01:40:26 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 01:40:26 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3699c0bcc1c342ae39ac0c5795ee860204401b568e49f81e18539e9709faebc4`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec4bcefbaa2ddc5c5f850b85ffbe49c949b93ad9489b61b3f89cfb34180ffc6`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 7.9 MB (7883583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1541a282306121df04d871433c17b3b800404c707fb599c5a8f234b41af81494`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 77.4 MB (77381418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43036a360cced63fdca47587355730eb6ca55258262dd6b52e46567c797fea4`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 424.1 KB (424148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4a9d479467f6e24a6463d19d8543a2e02c577c849349b0ce23166c5d6413c4`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 99.6 KB (99590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a155df5e2bd3365d2f8221fd2d8deb9cce87e5d7dfe08b67981f61b3a117b392`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc59fcc663abe8a36653dc41b9a13683b410959194a214a77c63a0dfa7bf085`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 42.4 MB (42436440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9545a463d46340f4dc2317a6418c34656c03807cb0c7525ff875b6398b6619c`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7b18530a9ce9367951a915771a5a9595b716fca410e17a0b0ca29f7d32793208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640763ee15e9616ab3dd38c5eeb265cad1434dcea1e1ff5b39533fe8a6382db7`

```dockerfile
```

-	Layers:
	-	`sha256:5e2c3d5c92887b2a975e673d20f4dd218d7c5ffd8478ca1fb73ed1d26c39d70b`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e211ede0fc11c56aa53817d66bfbfdc5b86629c700866acedf8bf91383dbabdd`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5c3cff7893382c994ca21184edafd3b247ec816e7e4ecf3736559bc67d7a0663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155436880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b4459e54907be8150236e42457c0a4d6db8b77490dd864c51bdca201cb5b0e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:42:48 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 19:42:55 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:43:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:43:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:43:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 19:43:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 19:43:15 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 19:43:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 19:43:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ddef996fe46367e2532460479664c8214a0203b0017240e68afb176e5a36b0`  
		Last Modified: Fri, 08 May 2026 19:43:29 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91044b2437e171b8dd7c095eedfc11308cb2a9f62f671f20f5bb40210f725941`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 7.7 MB (7694258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a67db7d7b579aeb5e777fd75e9e8c9eda206c7bcc17baecb8fc21903b12aa4`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 76.8 MB (76793314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cc61a58dbda4a2dab5da91216f2f4d3633c5a18511efa3f61478c1b6cc0ac0`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 392.8 KB (392751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85de5c3a4c1869ae15b1c563fdcf036be0407d5b08c08a0192952ca8ba3f821e`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 99.5 KB (99464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5042cab76c65435d560ab84199463e521cfc1f63110116f2120772b191edd2b6`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1c003b9db67f94b31cc11d1e9e0be6b8fe811953ea5bf63c43ed6a18f68718`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 42.3 MB (42339047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8634ce406e9ee484c07d482bbb415be6761aea93923e92c7f15cf47127734c`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:228d76562da373dcc20f3cc04378060492a9ced87347124344bff7b607fb8899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55567f184556c31ccc8ce34cbfb5195caf7b0655eb8e24bc679042a2930605cc`

```dockerfile
```

-	Layers:
	-	`sha256:a9bd9b0aa6d61067296a75cfbde0992b1ab39d241bf6ecc31de5b56c50102587`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 3.7 MB (3657585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6098c7702cb94cec334bedfbc24b951ad3d7c6843959b70679095dbcc9fa664`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:cf725f5fc333ce5583c3a1bdc5c493b3ff2f80035acfe396b5d72fd91f07d765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150105066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1ee5ed95bc2b90e3a3e93630af5058bed2be6512d46323fed497d83ca3e700`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:42 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:42 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 02:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:33:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:33:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:33:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:33:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 02:33:14 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 02:33:14 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c72ad32031623d24cb015f06ba762b3e2605190b489f63556f5c5c54c26a174`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431023707f5f79b1f184ccc237ab2f994f164119af3c3c206647fa1a55b73464`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 7.4 MB (7399462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2ad2d5f20f69c12b06d18d0949dc33bc5c537de9fb95aed5c4c65874835f3f`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 73.2 MB (73153273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5a19190ca30575a8918e6cdfed0b8b8c654e027d95ebe94ec24fe7ec5dda88`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 394.5 KB (394500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a7dee933c23aaf5e57248fcb5d87c1681d5a3a500d396b2f887a7ad0cac2c1`  
		Last Modified: Wed, 22 Apr 2026 02:33:37 GMT  
		Size: 99.7 KB (99663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48cd1f38f663b0e9a746ae67a2609d0a3ca9beab4247f6c3c7a23d7bdfdddd3`  
		Last Modified: Wed, 22 Apr 2026 02:33:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69bf6b994e3969bc5a4a0775754d5e7e81ac5cef4e04e5b8a6af9fa2c1b111`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 42.2 MB (42164727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84df84af6c868bcfbf2fb72ac4d14ad4512360969fabab4f072bda72b3f84fe`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f219414bd8b1573e72b97f12aafa8a21443e21307c127870d5bbe6ca5c90b09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf901c9bcaad01ea643fb50cb373264849c48824372fd6cba1d9291c92aed21`

```dockerfile
```

-	Layers:
	-	`sha256:1deb324532a176476ff3b667e706dcf1f8598d923bdfb9840aa5c45a076f4312`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6937c36d9e12093fba3ca6879d372458ad4f0a5f2e8f698c480182ab3c45c58`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:e09c992bb6c1f6d6955975d4115e0d579bdd842ba57a90b69dd90b1f39df4c05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4` - linux; amd64

```console
$ docker pull couchdb@sha256:5428814b65a4e51c61950aacb1eb9f0547e7aa6813e82b5d758c6d01259c6230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139023493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac80a991e305b8c9783e99fe1f055d345c7f4e6bd982f6679d8b3e4e2b31ac4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:40:04 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:40:04 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 01:40:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:17 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 22 Apr 2026 01:40:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 01:40:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:40:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:30 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 01:40:30 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 01:40:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85e89b64bb046d626a907734ef7a9b40ff6c4ef8a01deedcdfc36dd6782d464`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b9cc78d51139e05e4e4b210d2e65d57a180a134a39598cf1ae533d15928ed7`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 7.9 MB (7883540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316153b895f76daaab8076cf011b6c8e5a177f55e48562af0e7a05283d8503fd`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 401.8 KB (401794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e805a04eabbeedab61d24437ad992d1f1fcec69bb934507f7d5e504ff607197`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 76.5 KB (76512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b66b657a671ac4a21dbfc6ae4cdcd7dcb43c9b2da99f8e926cd64c3a10382e`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f68875914be9bcaff4d3c42cf902b182678731d00e048ad985576031262b0f`  
		Last Modified: Wed, 22 Apr 2026 01:40:45 GMT  
		Size: 102.4 MB (102419968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423a9813d2f3ec90378081d6ad677feb6bab0cc43f7e777eb0b996eb78c92634`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d00bc280812ffb50673789dd6057b5c98f5d6bfb7b45b3ec18f9f32ed69e600`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ecd9d2ecd1bbff49f937712a0b920aad8ff0b3999ccd9b353d7685810cf96`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e6be45ae454f7dcb0b9845c58bceee7bdbc6668b3e1a70821c2eb35e3d0bc`  
		Last Modified: Wed, 22 Apr 2026 01:40:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:048c65e3a362c69f9cb3f18fd552ac18243e9d2e061d5f2768860080a1a6c3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b491106a4e23d95588bfd3c1184cb6e02336be9456a5ce7231db016b58c32012`

```dockerfile
```

-	Layers:
	-	`sha256:9ce1ad516d4e59603081f39ace6f4d622459aa4e9c14613dc9741c903b8c1d13`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb217b54b7504de5ae3d779581e2bb214209e93e933552a6b6f84ea8d375037`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a8930f568af04abfa9b4dbc44a83fe620e758d39ad8845177e28de8c31cf35c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138432019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc01ef956f79c2bc699c0a74674017031f792ad429ae3ae20643da2de8eb0aeb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:52 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:42:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 19:42:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:43:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:06 GMT
ENV COUCHDB_VERSION=3.4.3
# Fri, 08 May 2026 19:43:06 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:43:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 19:43:18 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 19:43:18 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 19:43:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 19:43:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:43:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:18 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 19:43:18 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 19:43:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa3c48685d75fc305dcd37f8385450c237538fba7a9e019d1e6227f09e9b391`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a1b28a34ce3ec8a8e75f7cda34d57e469260f8a05cc9c5f9e09533a1ff191b`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 7.7 MB (7694300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac413a51a63ba6d6d11b4688bd9951b6307d102be6e4519e1aa74d29d3328dd`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 370.5 KB (370545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb086805b0472f13279dc83348302a49206f252bd2bad67441861c45a181de2`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 76.5 KB (76508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f9b758f88d12248c4ded2f0084c3eb297cedcdf62f715a1223912ccfc95182`  
		Last Modified: Fri, 08 May 2026 19:43:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b08ccc8cf9423ce6c09ad193f68fca975d1a0d64b163ee7976cbe21318a37d`  
		Last Modified: Fri, 08 May 2026 19:43:37 GMT  
		Size: 102.2 MB (102169066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89716ef593ad5d4ebbc2e01046680df65f60b46fdf472928f6cebb331cba0c5c`  
		Last Modified: Fri, 08 May 2026 19:43:34 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bb5eb18c2bf59fbff16cd96439b0f9d4b1b95bf5b0b75ae4f03112b0492a18`  
		Last Modified: Fri, 08 May 2026 19:43:35 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a90b736432506016527dda4dc4a088ef61aef15e962681da1831008efa9c4ed`  
		Last Modified: Fri, 08 May 2026 19:43:35 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b59e69dc239c8649dd6251b08a48125e8a045ebc70b04874643d9c9d7b16d7`  
		Last Modified: Fri, 08 May 2026 19:43:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:3ac697f377b3fe90a04528430983fa4e66826f08fb8c1128fa4ffd5965b09eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47db07212995e06aa8b03cdd013cc1874e58606a623dd9c59d1180754456fee7`

```dockerfile
```

-	Layers:
	-	`sha256:543c0d8ec6575cbace2452d06a83b0fb10651a8367734dfd8343c9250166a02a`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 4.1 MB (4125664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6c827e3530c87d814098791c5817e4bc54e8da1368da126b696fc7caf2f626f`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:fe69688f8a8a9fc7e558a72a4ac5cbead8abdc92ed794bdff5d2f857bad642ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135801559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0db4c4038cfbb749e099a7e7d629ac585ff220f732a490ed133003b519f36b8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 02:32:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:32:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:54 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 22 Apr 2026 02:33:09 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:33:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 02:33:25 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 02:33:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d77fe6e136fe8121f88c8e24891e2e3ce57d89ace081cd7917cd296bf2781`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c6fd13d86c4615402446553400ddbf811488b8652dfeaf1b30369df23a3d31`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 7.4 MB (7399499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977c5ff033346e1cf892081e6ed41c4dcce967c151c4974c113f4e0406b20fa`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 372.1 KB (372140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28cd61fdf1d3cba5a38ba01f0090a13b851c1b038b6006be4782108f438976`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51021d0991e21fdae5f82d151b8818f1a910d821b0e80cb74fe15fc244a157a`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd3c1758f3d8b894c1ccb4b9432456ec5f332ca1c028a3e5278050de5d9c034`  
		Last Modified: Wed, 22 Apr 2026 02:33:47 GMT  
		Size: 101.1 MB (101056387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1965c3cd4dcf03b89b4dcb613be010d7ad5bbebabff5b10e81f148444a4cf608`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6177a75af20c10e9eb4655cd66317f4b2a301ea9b0e8c6e3abe07b5764b33c3c`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f72a9ff25a97ad60e552b712c9bfc05a9ab2fd0d6801b33a3f77dcb8404fee1`  
		Last Modified: Wed, 22 Apr 2026 02:33:46 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf942b5dda4ee12459bead808567170200716b81bd5d5c791a10ca115b84c57`  
		Last Modified: Wed, 22 Apr 2026 02:33:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:ad5ccbec04df2f72fba8d7aeaa688573aba52ead2f2695672ab053b1fa88fee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3c5cbe3d0f03b9458aa22af27bbc6a0c259bb83ad5d180c6bbec5aca90b63e`

```dockerfile
```

-	Layers:
	-	`sha256:906b1434453c91788d486dd4a8dfd300a2576c794da0ae58cac2badd47a5530e`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2848d89da3b96589c1887032f7faf2ffb3ee0c02eee8826a01e50839cac6e44c`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:1e8fc2e10f189d8e5aba8c83a986559f8e34e58d2abfa5e70b78de071be3d5a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:6bef3997a59a7cb2920cd0a39773e7dac18a2a3f22b328a06ad1b3cabc1ac171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5637cb95392efea21d281e2b5aeabe64617798d49764037e46f57ae8048e6fab`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:40:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:40:06 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 01:40:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:23 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:23 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 01:40:27 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 01:40:27 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 01:40:27 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 01:40:27 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74980224cf758de90dca7d23ae81256f9bea075d12f56a4c3d2b1a37cf9a06c`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d04cecb0b1c5f6c24ed1d7536d1046e510e60e76d1ac9e79ca3e909c3085ed8`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 7.9 MB (7883603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e1af881e02d1c55b51d883ccf7f355c8e5e11d844edc411bd7c313527476cc`  
		Last Modified: Wed, 22 Apr 2026 01:40:50 GMT  
		Size: 77.4 MB (77381391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a31b79bfbbb57e9748c5a1f401e54713de3df23116b590290f1c6340452cc8`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 424.1 KB (424149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca78edf048bf6db58a97238f1a19c1bd6b5641ce16e15d2339754848a609a07`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 99.6 KB (99563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fc33302856959d39043c6a3f8956473a95630fbfa3497f5da8281bd1de8461`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356f9514689b1e9a5798e4606de863da2fa12c9e2625197bc67ed0cd8d4881c`  
		Last Modified: Wed, 22 Apr 2026 01:40:53 GMT  
		Size: 42.4 MB (42436138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31b4d7022e7af9a70b856a7c10e7e57ae93b7cb2caf9a72081413cd2d1b0e9f`  
		Last Modified: Wed, 22 Apr 2026 01:40:45 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:2cc08aa418b8ab792b15bbab673b9a5cf6e04dd8321db4c45db679beb118fba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54357c6db70c52095c0fa62fa4b956c14c004b21cfaf5dcb73cd8bbdedcae88`

```dockerfile
```

-	Layers:
	-	`sha256:ab5ea45e715310cad5acbfa29412e9118bc79c53a09eadd100588313927e5e3d`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 3.7 MB (3657789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a977a4cf972d069555b80ca29d7f9f6b1f205edfd4242931bf82d4436772bdb1`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:82e666914aaf407a9c7f6d8a59c54577b9ae23432db3be52b537263bf2c5e6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155436068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ebdc56ae845cfcb2f7de80b751b3773b5af509c06516bf818edab1da642032`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:52 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:42:52 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 19:42:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:43:07 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:43:11 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:11 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:43:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 19:43:16 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 19:43:16 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 19:43:16 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 19:43:16 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41408173867b8a3854f9a5c4a312ec8e614f4e7c489fb7a84656944d7185158a`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bbee753ce3011172cb45ff56d1f2d295dc271f9fb3d0111fb2de8678b5e334`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 7.7 MB (7694290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab25a57666d303d5f5309461c90c8cad38f2ecf5aaa4897357631b0d72c0eb48`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 76.8 MB (76793325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3294b800f6b67e405f2c09d056c3083606ffaf8ffe0283539cecd3edcdb65e`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 392.8 KB (392758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75878dba833386f5a3c9a41b111da708c714d086106fecb16f3187be8f59b89`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 99.5 KB (99477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1277aea04b936dd2bbbe5c45b05bd4f52bd5e37ecf0cff642f0b381078e294`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5902554cfb2819a9f5e4493d0ab12604ec295d9b4494ea39cce1dc49b459b2a4`  
		Last Modified: Fri, 08 May 2026 19:43:34 GMT  
		Size: 42.3 MB (42338170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b20aa0f2b669cc6d984f4e5ca5228f064207fc4d14ba5687300911b223c6026`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c73d010159e0685cfa7faedd676eb5bf76fd23c5e1546ad9ced98709db19e88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1b0d8a07da0470ecf69221710b967c14a11d47eeeedefc128bd02d648f6d41`

```dockerfile
```

-	Layers:
	-	`sha256:22583c7a4f6c5084005f2258a9a683b7b745c86b381a3bd16158ae5131cb5db8`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 3.7 MB (3657267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a958c1f5354a35cfea93932ef6c7a64a9c89bfe9bcedddf949b545cae557e596`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:87d62235c5899f6b8907d6d4d6052e86ee6f8be2877b17b0af7052abc6c4042c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150103452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124203b7fdd33c82e55e3019842da1b15a5aadf747dbed322f77acb8361e075b`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:33:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:33:53 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 02:33:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:34:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:34:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:34:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:34:15 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:34:16 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:34:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 02:34:26 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 02:34:26 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 02:34:26 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 02:34:26 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914b93210cd7104243e5ef6ab5d6244ddaaa8e4de085d219730706cca0fe3d94`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dc676250eb3edb1c12ff88d7c3c575684b2b29286cc757826511fe4e5c3b0c`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 7.4 MB (7399490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d64a4027355a4a1e6262832fd770bc7012502c2b8fb82b11c7aa24f61cb3eae`  
		Last Modified: Wed, 22 Apr 2026 02:34:51 GMT  
		Size: 73.2 MB (73153346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b93a5b58af5fadbdabc90fd9607a01b6bca90a9c02603eae57979ebbd6eb6f8`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 394.5 KB (394515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504f5f76d401a46b2de1aac91467563b4e016283bd372f4f827c4ee31a4c5a49`  
		Last Modified: Wed, 22 Apr 2026 02:34:50 GMT  
		Size: 99.6 KB (99649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ad49d758a4bf3d10640373f237ee766837d40f3e80ac364ea8d6b014e5af8e`  
		Last Modified: Wed, 22 Apr 2026 02:34:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c474d8ca8378054e459b4a6a175057200e4e5828617e831437708f80e8073b`  
		Last Modified: Wed, 22 Apr 2026 02:34:52 GMT  
		Size: 42.2 MB (42163011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cce7429a46657a931d21e39205ddf60884e8a4843d28e80299597da82c7ba4d`  
		Last Modified: Wed, 22 Apr 2026 02:34:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c93092bd194fec0fd074d3d576df7bed91f15f4c7bb55bfd1528bcf0c8165594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d455e39274286509abd19f51cd4e94639bb87b113642f3be88adab47df5b060`

```dockerfile
```

-	Layers:
	-	`sha256:1a9ff45b41bfd52d342877ae4a67e32edb70f7d551bf260c870ccd22a27e31fb`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 3.6 MB (3648318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e65e2d2a818933f9de43c39f59679a82b6fb23b52b14ea074e9cd26464d9c295`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:e09c992bb6c1f6d6955975d4115e0d579bdd842ba57a90b69dd90b1f39df4c05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.3` - linux; amd64

```console
$ docker pull couchdb@sha256:5428814b65a4e51c61950aacb1eb9f0547e7aa6813e82b5d758c6d01259c6230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139023493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac80a991e305b8c9783e99fe1f055d345c7f4e6bd982f6679d8b3e4e2b31ac4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:40:04 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:40:04 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 01:40:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:17 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 22 Apr 2026 01:40:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 01:40:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:40:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:30 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 01:40:30 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 01:40:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85e89b64bb046d626a907734ef7a9b40ff6c4ef8a01deedcdfc36dd6782d464`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b9cc78d51139e05e4e4b210d2e65d57a180a134a39598cf1ae533d15928ed7`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 7.9 MB (7883540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316153b895f76daaab8076cf011b6c8e5a177f55e48562af0e7a05283d8503fd`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 401.8 KB (401794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e805a04eabbeedab61d24437ad992d1f1fcec69bb934507f7d5e504ff607197`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 76.5 KB (76512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b66b657a671ac4a21dbfc6ae4cdcd7dcb43c9b2da99f8e926cd64c3a10382e`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f68875914be9bcaff4d3c42cf902b182678731d00e048ad985576031262b0f`  
		Last Modified: Wed, 22 Apr 2026 01:40:45 GMT  
		Size: 102.4 MB (102419968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423a9813d2f3ec90378081d6ad677feb6bab0cc43f7e777eb0b996eb78c92634`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d00bc280812ffb50673789dd6057b5c98f5d6bfb7b45b3ec18f9f32ed69e600`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ecd9d2ecd1bbff49f937712a0b920aad8ff0b3999ccd9b353d7685810cf96`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e6be45ae454f7dcb0b9845c58bceee7bdbc6668b3e1a70821c2eb35e3d0bc`  
		Last Modified: Wed, 22 Apr 2026 01:40:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:048c65e3a362c69f9cb3f18fd552ac18243e9d2e061d5f2768860080a1a6c3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b491106a4e23d95588bfd3c1184cb6e02336be9456a5ce7231db016b58c32012`

```dockerfile
```

-	Layers:
	-	`sha256:9ce1ad516d4e59603081f39ace6f4d622459aa4e9c14613dc9741c903b8c1d13`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb217b54b7504de5ae3d779581e2bb214209e93e933552a6b6f84ea8d375037`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a8930f568af04abfa9b4dbc44a83fe620e758d39ad8845177e28de8c31cf35c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138432019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc01ef956f79c2bc699c0a74674017031f792ad429ae3ae20643da2de8eb0aeb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:52 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:42:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 19:42:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:43:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:06 GMT
ENV COUCHDB_VERSION=3.4.3
# Fri, 08 May 2026 19:43:06 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:43:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 19:43:18 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 19:43:18 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 19:43:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 19:43:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:43:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:18 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 19:43:18 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 19:43:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa3c48685d75fc305dcd37f8385450c237538fba7a9e019d1e6227f09e9b391`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a1b28a34ce3ec8a8e75f7cda34d57e469260f8a05cc9c5f9e09533a1ff191b`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 7.7 MB (7694300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac413a51a63ba6d6d11b4688bd9951b6307d102be6e4519e1aa74d29d3328dd`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 370.5 KB (370545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb086805b0472f13279dc83348302a49206f252bd2bad67441861c45a181de2`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 76.5 KB (76508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f9b758f88d12248c4ded2f0084c3eb297cedcdf62f715a1223912ccfc95182`  
		Last Modified: Fri, 08 May 2026 19:43:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b08ccc8cf9423ce6c09ad193f68fca975d1a0d64b163ee7976cbe21318a37d`  
		Last Modified: Fri, 08 May 2026 19:43:37 GMT  
		Size: 102.2 MB (102169066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89716ef593ad5d4ebbc2e01046680df65f60b46fdf472928f6cebb331cba0c5c`  
		Last Modified: Fri, 08 May 2026 19:43:34 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bb5eb18c2bf59fbff16cd96439b0f9d4b1b95bf5b0b75ae4f03112b0492a18`  
		Last Modified: Fri, 08 May 2026 19:43:35 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a90b736432506016527dda4dc4a088ef61aef15e962681da1831008efa9c4ed`  
		Last Modified: Fri, 08 May 2026 19:43:35 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b59e69dc239c8649dd6251b08a48125e8a045ebc70b04874643d9c9d7b16d7`  
		Last Modified: Fri, 08 May 2026 19:43:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:3ac697f377b3fe90a04528430983fa4e66826f08fb8c1128fa4ffd5965b09eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47db07212995e06aa8b03cdd013cc1874e58606a623dd9c59d1180754456fee7`

```dockerfile
```

-	Layers:
	-	`sha256:543c0d8ec6575cbace2452d06a83b0fb10651a8367734dfd8343c9250166a02a`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 4.1 MB (4125664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6c827e3530c87d814098791c5817e4bc54e8da1368da126b696fc7caf2f626f`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:fe69688f8a8a9fc7e558a72a4ac5cbead8abdc92ed794bdff5d2f857bad642ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135801559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0db4c4038cfbb749e099a7e7d629ac585ff220f732a490ed133003b519f36b8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 02:32:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:32:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:54 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 22 Apr 2026 02:33:09 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:33:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 02:33:25 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 02:33:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d77fe6e136fe8121f88c8e24891e2e3ce57d89ace081cd7917cd296bf2781`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c6fd13d86c4615402446553400ddbf811488b8652dfeaf1b30369df23a3d31`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 7.4 MB (7399499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977c5ff033346e1cf892081e6ed41c4dcce967c151c4974c113f4e0406b20fa`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 372.1 KB (372140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28cd61fdf1d3cba5a38ba01f0090a13b851c1b038b6006be4782108f438976`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51021d0991e21fdae5f82d151b8818f1a910d821b0e80cb74fe15fc244a157a`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd3c1758f3d8b894c1ccb4b9432456ec5f332ca1c028a3e5278050de5d9c034`  
		Last Modified: Wed, 22 Apr 2026 02:33:47 GMT  
		Size: 101.1 MB (101056387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1965c3cd4dcf03b89b4dcb613be010d7ad5bbebabff5b10e81f148444a4cf608`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6177a75af20c10e9eb4655cd66317f4b2a301ea9b0e8c6e3abe07b5764b33c3c`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f72a9ff25a97ad60e552b712c9bfc05a9ab2fd0d6801b33a3f77dcb8404fee1`  
		Last Modified: Wed, 22 Apr 2026 02:33:46 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf942b5dda4ee12459bead808567170200716b81bd5d5c791a10ca115b84c57`  
		Last Modified: Wed, 22 Apr 2026 02:33:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ad5ccbec04df2f72fba8d7aeaa688573aba52ead2f2695672ab053b1fa88fee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3c5cbe3d0f03b9458aa22af27bbc6a0c259bb83ad5d180c6bbec5aca90b63e`

```dockerfile
```

-	Layers:
	-	`sha256:906b1434453c91788d486dd4a8dfd300a2576c794da0ae58cac2badd47a5530e`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2848d89da3b96589c1887032f7faf2ffb3ee0c02eee8826a01e50839cac6e44c`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:1e8fc2e10f189d8e5aba8c83a986559f8e34e58d2abfa5e70b78de071be3d5a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:6bef3997a59a7cb2920cd0a39773e7dac18a2a3f22b328a06ad1b3cabc1ac171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5637cb95392efea21d281e2b5aeabe64617798d49764037e46f57ae8048e6fab`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:40:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:40:06 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 01:40:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:23 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:23 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 01:40:27 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 01:40:27 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 01:40:27 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 01:40:27 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74980224cf758de90dca7d23ae81256f9bea075d12f56a4c3d2b1a37cf9a06c`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d04cecb0b1c5f6c24ed1d7536d1046e510e60e76d1ac9e79ca3e909c3085ed8`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 7.9 MB (7883603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e1af881e02d1c55b51d883ccf7f355c8e5e11d844edc411bd7c313527476cc`  
		Last Modified: Wed, 22 Apr 2026 01:40:50 GMT  
		Size: 77.4 MB (77381391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a31b79bfbbb57e9748c5a1f401e54713de3df23116b590290f1c6340452cc8`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 424.1 KB (424149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca78edf048bf6db58a97238f1a19c1bd6b5641ce16e15d2339754848a609a07`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 99.6 KB (99563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fc33302856959d39043c6a3f8956473a95630fbfa3497f5da8281bd1de8461`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356f9514689b1e9a5798e4606de863da2fa12c9e2625197bc67ed0cd8d4881c`  
		Last Modified: Wed, 22 Apr 2026 01:40:53 GMT  
		Size: 42.4 MB (42436138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31b4d7022e7af9a70b856a7c10e7e57ae93b7cb2caf9a72081413cd2d1b0e9f`  
		Last Modified: Wed, 22 Apr 2026 01:40:45 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:2cc08aa418b8ab792b15bbab673b9a5cf6e04dd8321db4c45db679beb118fba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54357c6db70c52095c0fa62fa4b956c14c004b21cfaf5dcb73cd8bbdedcae88`

```dockerfile
```

-	Layers:
	-	`sha256:ab5ea45e715310cad5acbfa29412e9118bc79c53a09eadd100588313927e5e3d`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 3.7 MB (3657789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a977a4cf972d069555b80ca29d7f9f6b1f205edfd4242931bf82d4436772bdb1`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:82e666914aaf407a9c7f6d8a59c54577b9ae23432db3be52b537263bf2c5e6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155436068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ebdc56ae845cfcb2f7de80b751b3773b5af509c06516bf818edab1da642032`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:52 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:42:52 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 19:42:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:43:07 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:43:11 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:11 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:43:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 19:43:16 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 19:43:16 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 19:43:16 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 19:43:16 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41408173867b8a3854f9a5c4a312ec8e614f4e7c489fb7a84656944d7185158a`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bbee753ce3011172cb45ff56d1f2d295dc271f9fb3d0111fb2de8678b5e334`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 7.7 MB (7694290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab25a57666d303d5f5309461c90c8cad38f2ecf5aaa4897357631b0d72c0eb48`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 76.8 MB (76793325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3294b800f6b67e405f2c09d056c3083606ffaf8ffe0283539cecd3edcdb65e`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 392.8 KB (392758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75878dba833386f5a3c9a41b111da708c714d086106fecb16f3187be8f59b89`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 99.5 KB (99477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1277aea04b936dd2bbbe5c45b05bd4f52bd5e37ecf0cff642f0b381078e294`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5902554cfb2819a9f5e4493d0ab12604ec295d9b4494ea39cce1dc49b459b2a4`  
		Last Modified: Fri, 08 May 2026 19:43:34 GMT  
		Size: 42.3 MB (42338170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b20aa0f2b669cc6d984f4e5ca5228f064207fc4d14ba5687300911b223c6026`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c73d010159e0685cfa7faedd676eb5bf76fd23c5e1546ad9ced98709db19e88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1b0d8a07da0470ecf69221710b967c14a11d47eeeedefc128bd02d648f6d41`

```dockerfile
```

-	Layers:
	-	`sha256:22583c7a4f6c5084005f2258a9a683b7b745c86b381a3bd16158ae5131cb5db8`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 3.7 MB (3657267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a958c1f5354a35cfea93932ef6c7a64a9c89bfe9bcedddf949b545cae557e596`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:87d62235c5899f6b8907d6d4d6052e86ee6f8be2877b17b0af7052abc6c4042c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150103452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124203b7fdd33c82e55e3019842da1b15a5aadf747dbed322f77acb8361e075b`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:33:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:33:53 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 02:33:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:34:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:34:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:34:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:34:15 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:34:16 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:34:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 02:34:26 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 02:34:26 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 02:34:26 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 02:34:26 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914b93210cd7104243e5ef6ab5d6244ddaaa8e4de085d219730706cca0fe3d94`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dc676250eb3edb1c12ff88d7c3c575684b2b29286cc757826511fe4e5c3b0c`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 7.4 MB (7399490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d64a4027355a4a1e6262832fd770bc7012502c2b8fb82b11c7aa24f61cb3eae`  
		Last Modified: Wed, 22 Apr 2026 02:34:51 GMT  
		Size: 73.2 MB (73153346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b93a5b58af5fadbdabc90fd9607a01b6bca90a9c02603eae57979ebbd6eb6f8`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 394.5 KB (394515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504f5f76d401a46b2de1aac91467563b4e016283bd372f4f827c4ee31a4c5a49`  
		Last Modified: Wed, 22 Apr 2026 02:34:50 GMT  
		Size: 99.6 KB (99649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ad49d758a4bf3d10640373f237ee766837d40f3e80ac364ea8d6b014e5af8e`  
		Last Modified: Wed, 22 Apr 2026 02:34:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c474d8ca8378054e459b4a6a175057200e4e5828617e831437708f80e8073b`  
		Last Modified: Wed, 22 Apr 2026 02:34:52 GMT  
		Size: 42.2 MB (42163011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cce7429a46657a931d21e39205ddf60884e8a4843d28e80299597da82c7ba4d`  
		Last Modified: Wed, 22 Apr 2026 02:34:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c93092bd194fec0fd074d3d576df7bed91f15f4c7bb55bfd1528bcf0c8165594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d455e39274286509abd19f51cd4e94639bb87b113642f3be88adab47df5b060`

```dockerfile
```

-	Layers:
	-	`sha256:1a9ff45b41bfd52d342877ae4a67e32edb70f7d551bf260c870ccd22a27e31fb`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 3.6 MB (3648318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e65e2d2a818933f9de43c39f59679a82b6fb23b52b14ea074e9cd26464d9c295`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:fa6d5ecadbcec3d20016e5ff78ff938051997859aac9f85a4072706ff25e8af8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5` - linux; amd64

```console
$ docker pull couchdb@sha256:8a1ba2a19a4c6981e0c903c2c3cd4d59602748cae0246666818090091a1645ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142061148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806bab74c1a4fb65ea85eca0df6cbfaf75e633a8fe12b041057efc047f8c1b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:39:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:39:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 01:40:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:08 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 01:40:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:21 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 01:40:21 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 01:40:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a53138b1d134d26fa4d53d9a2683c90141d93b6e7bd622b6f43e87123095de`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d90394d687f0d05c4649b956181d3345b324547ad48051ae0f177b448cbaaed`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 7.9 MB (7883631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de30193b9c2bab17ecfbda0bcf2a02b262bd8ceafd9a031e19a120fd8c8ac1`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 401.8 KB (401802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cdf8fec417a2a0f21a217bd1809c4ea2cc4f135d262f6b0dcc8078c9a7c044`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 76.5 KB (76502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34740f51296d6acfab2fa462e3b8b1803c8737e466de7bbf0fe68db4d70eae7`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9cb5cf3e1dbb2d8da0afe8b27d8c08d85851a5ced23b121452557a3d3c751`  
		Last Modified: Wed, 22 Apr 2026 01:40:55 GMT  
		Size: 105.5 MB (105457531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de039ed6bde8981bad1b825c982292ee098f74b12f1b17c1ba36cfe31305eb3`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a0c60ddabd96476377d89beffea94139f3abd519bfe2f9addbefde09deac10`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731d920f2d4fef22403d1c15d88dd6c5ea16f0ad88cf18a477d7d5b2f9149f63`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408fb10825775c8965247a872391b284439aa7ca55f219ee2b556cd7af7f8cb`  
		Last Modified: Wed, 22 Apr 2026 01:40:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:3401257267e59435bdfe64dbed14ef495900c94738868e5585c90a8b15a0bf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbd66bb44251165fea91e9881fd9bba6ac85de3eb92c8b0575a83327bd36503`

```dockerfile
```

-	Layers:
	-	`sha256:5885b7c7950112751264b2ad2b6bc61f53aa9cf3d431edef5ecfe318a9857788`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf6461ec6d2ed586ec7996683ff351ab2e0289226e87e971668647852e88b16`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3acb3b244848b4ffd238614c6204188d96161de58e6b7c9b2b9c7de222b2e931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141421269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532eec0d6c7fd75306513a9dbdc863b5a5ab09a381fc1d3f71be45d5ea410fb9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:42:47 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 19:42:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:42:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:42:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:00 GMT
ENV COUCHDB_VERSION=3.5.1
# Fri, 08 May 2026 19:43:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:43:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 19:43:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 19:43:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 19:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 19:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:43:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:14 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 19:43:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 19:43:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ba953e3673b93911518c493226c251cc365cdd77c6f876549545639054dabe`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92f6f6706e91bfdfb4e3d908249946bc0dd23581108188076c4b762f669633`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 7.7 MB (7694199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fda1eb9ec2e98980355f7096bdb5fa0e0cc86eb7cfba3f94edf01ca4bac36e6`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 370.5 KB (370536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9d5a29d3a2313f5d79be0a785bca096dff87584599c7921c9c78d8ada69a3c`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdd14c29d7abeffaa6923ffeb66d5ef0400e5057c4d35b358f1053d82a14535`  
		Last Modified: Fri, 08 May 2026 19:43:28 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e2d9fa6ff2962ba383325e4cea1c47d0fc54d34aee23969f9aca08fb7606b0`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 105.2 MB (105158425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b656fbff7ffe21c15b175d9106b8d721ff47e526e319a726238fec2af887a491`  
		Last Modified: Fri, 08 May 2026 19:43:28 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6099ecd94170a7d1fb61ed09b34f5e2c7636c7ea1bdf1a0d92420b074db37712`  
		Last Modified: Fri, 08 May 2026 19:43:29 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1c6dfae50f327fc911f145185f8f7c342667a76aa8e546a5bb4c0d128e0ac6`  
		Last Modified: Fri, 08 May 2026 19:43:29 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be535dad739a0367a13c857220837b7aa02e54a888f3611cad87ad9423e626a`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:2314645392ccdfeadd1be29930c091001214b2ef586e8055f84a5dfc10566667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c884eecfdd4721074439971fe2feda35bab4206d1fa9cab39b28d760ed2f09d`

```dockerfile
```

-	Layers:
	-	`sha256:a122e139a2ecab33684a3fe2b00740464e19b56da6869432b8e9efc1a9ca657f`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d9270ca0635c8e43a137ef9ea2bd3d132f77f36bf563b585c50d43bc67115`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:877bc4f2e9cebde5f6dd5db0625e8c11c1d5fc1450749b8df1ca04eee385183f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225182040bb866da2edada7d68127d3de35b20144022da2ee5092b81a48ff243`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 02:32:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:32:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:54 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 02:32:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:33:12 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 02:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 02:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d77fe6e136fe8121f88c8e24891e2e3ce57d89ace081cd7917cd296bf2781`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c6fd13d86c4615402446553400ddbf811488b8652dfeaf1b30369df23a3d31`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 7.4 MB (7399499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977c5ff033346e1cf892081e6ed41c4dcce967c151c4974c113f4e0406b20fa`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 372.1 KB (372140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28cd61fdf1d3cba5a38ba01f0090a13b851c1b038b6006be4782108f438976`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0df2b1587eda8004175334929323a5430ee32ec7ca0ad93243315dcdfcb1c4d`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d01bd714bd29509eccc7ffd6d42cf54ecb8e91fdd75f00b3a997e6b6adbaf5`  
		Last Modified: Wed, 22 Apr 2026 02:33:35 GMT  
		Size: 104.0 MB (104028166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b90460439c32fbf3c5d889b6093560b179158059ea12b5c62a42ce21380a3fe`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d8c0832e7dbb36e1959f210cc39b9c2f06cded3a0918c38f62da8bb11fe9cc`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846e3f061b916fca388e65c142917fbb47748b12371a1cc92c23fb6caa3881ea`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2a413a15f2d3d0b12253a678fe2d6199c1424fe5ce4d2166204aefde16a81`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:9d0ddb4a733d4cb15d823ccf7fef246af5176b6fbaf3ea6aaef729aa2ddd8e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa74c39c384641d3f8ad817a1c998223d297e3d2453b62a75dbd87fc179ca1c5`

```dockerfile
```

-	Layers:
	-	`sha256:8ae251a1734f9ea12b57e27040fd43078355bb4d78477392c9868f468347d2e5`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cd4bab63ce540f1c9dc037237c27456a1710328cd50cf0b8b3606d11ee6480`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 31.7 KB (31737 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:80c7ba6728048896c1e526f4592e63d45d4aefbb287bb7fbf564a67877591c37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:92cd36a141af320a0e396b3f186e488441d8f5a67a56fac69caf54c5c3c46cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156463311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faeb20718102ff657dc6a855312eda1db690059113db9d85bd5187756618b39`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:40:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:40:01 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 01:40:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 01:40:26 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 01:40:26 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3699c0bcc1c342ae39ac0c5795ee860204401b568e49f81e18539e9709faebc4`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec4bcefbaa2ddc5c5f850b85ffbe49c949b93ad9489b61b3f89cfb34180ffc6`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 7.9 MB (7883583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1541a282306121df04d871433c17b3b800404c707fb599c5a8f234b41af81494`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 77.4 MB (77381418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43036a360cced63fdca47587355730eb6ca55258262dd6b52e46567c797fea4`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 424.1 KB (424148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4a9d479467f6e24a6463d19d8543a2e02c577c849349b0ce23166c5d6413c4`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 99.6 KB (99590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a155df5e2bd3365d2f8221fd2d8deb9cce87e5d7dfe08b67981f61b3a117b392`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc59fcc663abe8a36653dc41b9a13683b410959194a214a77c63a0dfa7bf085`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 42.4 MB (42436440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9545a463d46340f4dc2317a6418c34656c03807cb0c7525ff875b6398b6619c`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7b18530a9ce9367951a915771a5a9595b716fca410e17a0b0ca29f7d32793208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640763ee15e9616ab3dd38c5eeb265cad1434dcea1e1ff5b39533fe8a6382db7`

```dockerfile
```

-	Layers:
	-	`sha256:5e2c3d5c92887b2a975e673d20f4dd218d7c5ffd8478ca1fb73ed1d26c39d70b`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e211ede0fc11c56aa53817d66bfbfdc5b86629c700866acedf8bf91383dbabdd`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5c3cff7893382c994ca21184edafd3b247ec816e7e4ecf3736559bc67d7a0663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155436880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b4459e54907be8150236e42457c0a4d6db8b77490dd864c51bdca201cb5b0e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:42:48 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 19:42:55 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:43:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:43:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:43:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 19:43:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 19:43:15 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 19:43:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 19:43:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ddef996fe46367e2532460479664c8214a0203b0017240e68afb176e5a36b0`  
		Last Modified: Fri, 08 May 2026 19:43:29 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91044b2437e171b8dd7c095eedfc11308cb2a9f62f671f20f5bb40210f725941`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 7.7 MB (7694258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a67db7d7b579aeb5e777fd75e9e8c9eda206c7bcc17baecb8fc21903b12aa4`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 76.8 MB (76793314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cc61a58dbda4a2dab5da91216f2f4d3633c5a18511efa3f61478c1b6cc0ac0`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 392.8 KB (392751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85de5c3a4c1869ae15b1c563fdcf036be0407d5b08c08a0192952ca8ba3f821e`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 99.5 KB (99464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5042cab76c65435d560ab84199463e521cfc1f63110116f2120772b191edd2b6`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1c003b9db67f94b31cc11d1e9e0be6b8fe811953ea5bf63c43ed6a18f68718`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 42.3 MB (42339047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8634ce406e9ee484c07d482bbb415be6761aea93923e92c7f15cf47127734c`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:228d76562da373dcc20f3cc04378060492a9ced87347124344bff7b607fb8899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55567f184556c31ccc8ce34cbfb5195caf7b0655eb8e24bc679042a2930605cc`

```dockerfile
```

-	Layers:
	-	`sha256:a9bd9b0aa6d61067296a75cfbde0992b1ab39d241bf6ecc31de5b56c50102587`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 3.7 MB (3657585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6098c7702cb94cec334bedfbc24b951ad3d7c6843959b70679095dbcc9fa664`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:cf725f5fc333ce5583c3a1bdc5c493b3ff2f80035acfe396b5d72fd91f07d765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150105066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1ee5ed95bc2b90e3a3e93630af5058bed2be6512d46323fed497d83ca3e700`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:42 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:42 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 02:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:33:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:33:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:33:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:33:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 02:33:14 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 02:33:14 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c72ad32031623d24cb015f06ba762b3e2605190b489f63556f5c5c54c26a174`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431023707f5f79b1f184ccc237ab2f994f164119af3c3c206647fa1a55b73464`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 7.4 MB (7399462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2ad2d5f20f69c12b06d18d0949dc33bc5c537de9fb95aed5c4c65874835f3f`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 73.2 MB (73153273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5a19190ca30575a8918e6cdfed0b8b8c654e027d95ebe94ec24fe7ec5dda88`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 394.5 KB (394500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a7dee933c23aaf5e57248fcb5d87c1681d5a3a500d396b2f887a7ad0cac2c1`  
		Last Modified: Wed, 22 Apr 2026 02:33:37 GMT  
		Size: 99.7 KB (99663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48cd1f38f663b0e9a746ae67a2609d0a3ca9beab4247f6c3c7a23d7bdfdddd3`  
		Last Modified: Wed, 22 Apr 2026 02:33:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69bf6b994e3969bc5a4a0775754d5e7e81ac5cef4e04e5b8a6af9fa2c1b111`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 42.2 MB (42164727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84df84af6c868bcfbf2fb72ac4d14ad4512360969fabab4f072bda72b3f84fe`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f219414bd8b1573e72b97f12aafa8a21443e21307c127870d5bbe6ca5c90b09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf901c9bcaad01ea643fb50cb373264849c48824372fd6cba1d9291c92aed21`

```dockerfile
```

-	Layers:
	-	`sha256:1deb324532a176476ff3b667e706dcf1f8598d923bdfb9840aa5c45a076f4312`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6937c36d9e12093fba3ca6879d372458ad4f0a5f2e8f698c480182ab3c45c58`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1`

```console
$ docker pull couchdb@sha256:fa6d5ecadbcec3d20016e5ff78ff938051997859aac9f85a4072706ff25e8af8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.1` - linux; amd64

```console
$ docker pull couchdb@sha256:8a1ba2a19a4c6981e0c903c2c3cd4d59602748cae0246666818090091a1645ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142061148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806bab74c1a4fb65ea85eca0df6cbfaf75e633a8fe12b041057efc047f8c1b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:39:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:39:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 01:40:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:08 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 01:40:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:21 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 01:40:21 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 01:40:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a53138b1d134d26fa4d53d9a2683c90141d93b6e7bd622b6f43e87123095de`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d90394d687f0d05c4649b956181d3345b324547ad48051ae0f177b448cbaaed`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 7.9 MB (7883631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de30193b9c2bab17ecfbda0bcf2a02b262bd8ceafd9a031e19a120fd8c8ac1`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 401.8 KB (401802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cdf8fec417a2a0f21a217bd1809c4ea2cc4f135d262f6b0dcc8078c9a7c044`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 76.5 KB (76502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34740f51296d6acfab2fa462e3b8b1803c8737e466de7bbf0fe68db4d70eae7`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9cb5cf3e1dbb2d8da0afe8b27d8c08d85851a5ced23b121452557a3d3c751`  
		Last Modified: Wed, 22 Apr 2026 01:40:55 GMT  
		Size: 105.5 MB (105457531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de039ed6bde8981bad1b825c982292ee098f74b12f1b17c1ba36cfe31305eb3`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a0c60ddabd96476377d89beffea94139f3abd519bfe2f9addbefde09deac10`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731d920f2d4fef22403d1c15d88dd6c5ea16f0ad88cf18a477d7d5b2f9149f63`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408fb10825775c8965247a872391b284439aa7ca55f219ee2b556cd7af7f8cb`  
		Last Modified: Wed, 22 Apr 2026 01:40:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:3401257267e59435bdfe64dbed14ef495900c94738868e5585c90a8b15a0bf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbd66bb44251165fea91e9881fd9bba6ac85de3eb92c8b0575a83327bd36503`

```dockerfile
```

-	Layers:
	-	`sha256:5885b7c7950112751264b2ad2b6bc61f53aa9cf3d431edef5ecfe318a9857788`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf6461ec6d2ed586ec7996683ff351ab2e0289226e87e971668647852e88b16`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3acb3b244848b4ffd238614c6204188d96161de58e6b7c9b2b9c7de222b2e931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141421269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532eec0d6c7fd75306513a9dbdc863b5a5ab09a381fc1d3f71be45d5ea410fb9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:42:47 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 19:42:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:42:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:42:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:00 GMT
ENV COUCHDB_VERSION=3.5.1
# Fri, 08 May 2026 19:43:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:43:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 19:43:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 19:43:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 19:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 19:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:43:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:14 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 19:43:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 19:43:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ba953e3673b93911518c493226c251cc365cdd77c6f876549545639054dabe`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92f6f6706e91bfdfb4e3d908249946bc0dd23581108188076c4b762f669633`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 7.7 MB (7694199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fda1eb9ec2e98980355f7096bdb5fa0e0cc86eb7cfba3f94edf01ca4bac36e6`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 370.5 KB (370536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9d5a29d3a2313f5d79be0a785bca096dff87584599c7921c9c78d8ada69a3c`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdd14c29d7abeffaa6923ffeb66d5ef0400e5057c4d35b358f1053d82a14535`  
		Last Modified: Fri, 08 May 2026 19:43:28 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e2d9fa6ff2962ba383325e4cea1c47d0fc54d34aee23969f9aca08fb7606b0`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 105.2 MB (105158425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b656fbff7ffe21c15b175d9106b8d721ff47e526e319a726238fec2af887a491`  
		Last Modified: Fri, 08 May 2026 19:43:28 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6099ecd94170a7d1fb61ed09b34f5e2c7636c7ea1bdf1a0d92420b074db37712`  
		Last Modified: Fri, 08 May 2026 19:43:29 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1c6dfae50f327fc911f145185f8f7c342667a76aa8e546a5bb4c0d128e0ac6`  
		Last Modified: Fri, 08 May 2026 19:43:29 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be535dad739a0367a13c857220837b7aa02e54a888f3611cad87ad9423e626a`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:2314645392ccdfeadd1be29930c091001214b2ef586e8055f84a5dfc10566667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c884eecfdd4721074439971fe2feda35bab4206d1fa9cab39b28d760ed2f09d`

```dockerfile
```

-	Layers:
	-	`sha256:a122e139a2ecab33684a3fe2b00740464e19b56da6869432b8e9efc1a9ca657f`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d9270ca0635c8e43a137ef9ea2bd3d132f77f36bf563b585c50d43bc67115`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; s390x

```console
$ docker pull couchdb@sha256:877bc4f2e9cebde5f6dd5db0625e8c11c1d5fc1450749b8df1ca04eee385183f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225182040bb866da2edada7d68127d3de35b20144022da2ee5092b81a48ff243`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 02:32:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:32:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:54 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 02:32:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:33:12 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 02:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 02:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d77fe6e136fe8121f88c8e24891e2e3ce57d89ace081cd7917cd296bf2781`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c6fd13d86c4615402446553400ddbf811488b8652dfeaf1b30369df23a3d31`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 7.4 MB (7399499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977c5ff033346e1cf892081e6ed41c4dcce967c151c4974c113f4e0406b20fa`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 372.1 KB (372140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28cd61fdf1d3cba5a38ba01f0090a13b851c1b038b6006be4782108f438976`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0df2b1587eda8004175334929323a5430ee32ec7ca0ad93243315dcdfcb1c4d`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d01bd714bd29509eccc7ffd6d42cf54ecb8e91fdd75f00b3a997e6b6adbaf5`  
		Last Modified: Wed, 22 Apr 2026 02:33:35 GMT  
		Size: 104.0 MB (104028166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b90460439c32fbf3c5d889b6093560b179158059ea12b5c62a42ce21380a3fe`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d8c0832e7dbb36e1959f210cc39b9c2f06cded3a0918c38f62da8bb11fe9cc`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846e3f061b916fca388e65c142917fbb47748b12371a1cc92c23fb6caa3881ea`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2a413a15f2d3d0b12253a678fe2d6199c1424fe5ce4d2166204aefde16a81`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:9d0ddb4a733d4cb15d823ccf7fef246af5176b6fbaf3ea6aaef729aa2ddd8e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa74c39c384641d3f8ad817a1c998223d297e3d2453b62a75dbd87fc179ca1c5`

```dockerfile
```

-	Layers:
	-	`sha256:8ae251a1734f9ea12b57e27040fd43078355bb4d78477392c9868f468347d2e5`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cd4bab63ce540f1c9dc037237c27456a1710328cd50cf0b8b3606d11ee6480`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 31.7 KB (31737 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1-nouveau`

```console
$ docker pull couchdb@sha256:80c7ba6728048896c1e526f4592e63d45d4aefbb287bb7fbf564a67877591c37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.1-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:92cd36a141af320a0e396b3f186e488441d8f5a67a56fac69caf54c5c3c46cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156463311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faeb20718102ff657dc6a855312eda1db690059113db9d85bd5187756618b39`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:40:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:40:01 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 01:40:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 01:40:26 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 01:40:26 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3699c0bcc1c342ae39ac0c5795ee860204401b568e49f81e18539e9709faebc4`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec4bcefbaa2ddc5c5f850b85ffbe49c949b93ad9489b61b3f89cfb34180ffc6`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 7.9 MB (7883583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1541a282306121df04d871433c17b3b800404c707fb599c5a8f234b41af81494`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 77.4 MB (77381418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43036a360cced63fdca47587355730eb6ca55258262dd6b52e46567c797fea4`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 424.1 KB (424148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4a9d479467f6e24a6463d19d8543a2e02c577c849349b0ce23166c5d6413c4`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 99.6 KB (99590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a155df5e2bd3365d2f8221fd2d8deb9cce87e5d7dfe08b67981f61b3a117b392`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc59fcc663abe8a36653dc41b9a13683b410959194a214a77c63a0dfa7bf085`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 42.4 MB (42436440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9545a463d46340f4dc2317a6418c34656c03807cb0c7525ff875b6398b6619c`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7b18530a9ce9367951a915771a5a9595b716fca410e17a0b0ca29f7d32793208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640763ee15e9616ab3dd38c5eeb265cad1434dcea1e1ff5b39533fe8a6382db7`

```dockerfile
```

-	Layers:
	-	`sha256:5e2c3d5c92887b2a975e673d20f4dd218d7c5ffd8478ca1fb73ed1d26c39d70b`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e211ede0fc11c56aa53817d66bfbfdc5b86629c700866acedf8bf91383dbabdd`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5c3cff7893382c994ca21184edafd3b247ec816e7e4ecf3736559bc67d7a0663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155436880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b4459e54907be8150236e42457c0a4d6db8b77490dd864c51bdca201cb5b0e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:42:48 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 19:42:55 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:43:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:43:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:43:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 19:43:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 19:43:15 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 19:43:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 19:43:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ddef996fe46367e2532460479664c8214a0203b0017240e68afb176e5a36b0`  
		Last Modified: Fri, 08 May 2026 19:43:29 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91044b2437e171b8dd7c095eedfc11308cb2a9f62f671f20f5bb40210f725941`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 7.7 MB (7694258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a67db7d7b579aeb5e777fd75e9e8c9eda206c7bcc17baecb8fc21903b12aa4`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 76.8 MB (76793314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cc61a58dbda4a2dab5da91216f2f4d3633c5a18511efa3f61478c1b6cc0ac0`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 392.8 KB (392751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85de5c3a4c1869ae15b1c563fdcf036be0407d5b08c08a0192952ca8ba3f821e`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 99.5 KB (99464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5042cab76c65435d560ab84199463e521cfc1f63110116f2120772b191edd2b6`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1c003b9db67f94b31cc11d1e9e0be6b8fe811953ea5bf63c43ed6a18f68718`  
		Last Modified: Fri, 08 May 2026 19:43:33 GMT  
		Size: 42.3 MB (42339047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8634ce406e9ee484c07d482bbb415be6761aea93923e92c7f15cf47127734c`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:228d76562da373dcc20f3cc04378060492a9ced87347124344bff7b607fb8899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55567f184556c31ccc8ce34cbfb5195caf7b0655eb8e24bc679042a2930605cc`

```dockerfile
```

-	Layers:
	-	`sha256:a9bd9b0aa6d61067296a75cfbde0992b1ab39d241bf6ecc31de5b56c50102587`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 3.7 MB (3657585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6098c7702cb94cec334bedfbc24b951ad3d7c6843959b70679095dbcc9fa664`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:cf725f5fc333ce5583c3a1bdc5c493b3ff2f80035acfe396b5d72fd91f07d765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150105066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1ee5ed95bc2b90e3a3e93630af5058bed2be6512d46323fed497d83ca3e700`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:42 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:42 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 02:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:33:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:33:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:33:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:33:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 02:33:14 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 02:33:14 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c72ad32031623d24cb015f06ba762b3e2605190b489f63556f5c5c54c26a174`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431023707f5f79b1f184ccc237ab2f994f164119af3c3c206647fa1a55b73464`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 7.4 MB (7399462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2ad2d5f20f69c12b06d18d0949dc33bc5c537de9fb95aed5c4c65874835f3f`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 73.2 MB (73153273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5a19190ca30575a8918e6cdfed0b8b8c654e027d95ebe94ec24fe7ec5dda88`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 394.5 KB (394500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a7dee933c23aaf5e57248fcb5d87c1681d5a3a500d396b2f887a7ad0cac2c1`  
		Last Modified: Wed, 22 Apr 2026 02:33:37 GMT  
		Size: 99.7 KB (99663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48cd1f38f663b0e9a746ae67a2609d0a3ca9beab4247f6c3c7a23d7bdfdddd3`  
		Last Modified: Wed, 22 Apr 2026 02:33:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69bf6b994e3969bc5a4a0775754d5e7e81ac5cef4e04e5b8a6af9fa2c1b111`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 42.2 MB (42164727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84df84af6c868bcfbf2fb72ac4d14ad4512360969fabab4f072bda72b3f84fe`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f219414bd8b1573e72b97f12aafa8a21443e21307c127870d5bbe6ca5c90b09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf901c9bcaad01ea643fb50cb373264849c48824372fd6cba1d9291c92aed21`

```dockerfile
```

-	Layers:
	-	`sha256:1deb324532a176476ff3b667e706dcf1f8598d923bdfb9840aa5c45a076f4312`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6937c36d9e12093fba3ca6879d372458ad4f0a5f2e8f698c480182ab3c45c58`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:fa6d5ecadbcec3d20016e5ff78ff938051997859aac9f85a4072706ff25e8af8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:8a1ba2a19a4c6981e0c903c2c3cd4d59602748cae0246666818090091a1645ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142061148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806bab74c1a4fb65ea85eca0df6cbfaf75e633a8fe12b041057efc047f8c1b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:39:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:39:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 01:40:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:08 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 01:40:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:21 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 01:40:21 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 01:40:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a53138b1d134d26fa4d53d9a2683c90141d93b6e7bd622b6f43e87123095de`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d90394d687f0d05c4649b956181d3345b324547ad48051ae0f177b448cbaaed`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 7.9 MB (7883631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de30193b9c2bab17ecfbda0bcf2a02b262bd8ceafd9a031e19a120fd8c8ac1`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 401.8 KB (401802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cdf8fec417a2a0f21a217bd1809c4ea2cc4f135d262f6b0dcc8078c9a7c044`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 76.5 KB (76502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34740f51296d6acfab2fa462e3b8b1803c8737e466de7bbf0fe68db4d70eae7`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9cb5cf3e1dbb2d8da0afe8b27d8c08d85851a5ced23b121452557a3d3c751`  
		Last Modified: Wed, 22 Apr 2026 01:40:55 GMT  
		Size: 105.5 MB (105457531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de039ed6bde8981bad1b825c982292ee098f74b12f1b17c1ba36cfe31305eb3`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a0c60ddabd96476377d89beffea94139f3abd519bfe2f9addbefde09deac10`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731d920f2d4fef22403d1c15d88dd6c5ea16f0ad88cf18a477d7d5b2f9149f63`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408fb10825775c8965247a872391b284439aa7ca55f219ee2b556cd7af7f8cb`  
		Last Modified: Wed, 22 Apr 2026 01:40:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:3401257267e59435bdfe64dbed14ef495900c94738868e5585c90a8b15a0bf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbd66bb44251165fea91e9881fd9bba6ac85de3eb92c8b0575a83327bd36503`

```dockerfile
```

-	Layers:
	-	`sha256:5885b7c7950112751264b2ad2b6bc61f53aa9cf3d431edef5ecfe318a9857788`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf6461ec6d2ed586ec7996683ff351ab2e0289226e87e971668647852e88b16`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3acb3b244848b4ffd238614c6204188d96161de58e6b7c9b2b9c7de222b2e931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141421269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532eec0d6c7fd75306513a9dbdc863b5a5ab09a381fc1d3f71be45d5ea410fb9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:42:47 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 19:42:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:42:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:42:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:00 GMT
ENV COUCHDB_VERSION=3.5.1
# Fri, 08 May 2026 19:43:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:43:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 19:43:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 19:43:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 19:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 19:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:43:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:14 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 19:43:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 19:43:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ba953e3673b93911518c493226c251cc365cdd77c6f876549545639054dabe`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92f6f6706e91bfdfb4e3d908249946bc0dd23581108188076c4b762f669633`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 7.7 MB (7694199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fda1eb9ec2e98980355f7096bdb5fa0e0cc86eb7cfba3f94edf01ca4bac36e6`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 370.5 KB (370536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9d5a29d3a2313f5d79be0a785bca096dff87584599c7921c9c78d8ada69a3c`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdd14c29d7abeffaa6923ffeb66d5ef0400e5057c4d35b358f1053d82a14535`  
		Last Modified: Fri, 08 May 2026 19:43:28 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e2d9fa6ff2962ba383325e4cea1c47d0fc54d34aee23969f9aca08fb7606b0`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 105.2 MB (105158425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b656fbff7ffe21c15b175d9106b8d721ff47e526e319a726238fec2af887a491`  
		Last Modified: Fri, 08 May 2026 19:43:28 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6099ecd94170a7d1fb61ed09b34f5e2c7636c7ea1bdf1a0d92420b074db37712`  
		Last Modified: Fri, 08 May 2026 19:43:29 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1c6dfae50f327fc911f145185f8f7c342667a76aa8e546a5bb4c0d128e0ac6`  
		Last Modified: Fri, 08 May 2026 19:43:29 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be535dad739a0367a13c857220837b7aa02e54a888f3611cad87ad9423e626a`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:2314645392ccdfeadd1be29930c091001214b2ef586e8055f84a5dfc10566667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c884eecfdd4721074439971fe2feda35bab4206d1fa9cab39b28d760ed2f09d`

```dockerfile
```

-	Layers:
	-	`sha256:a122e139a2ecab33684a3fe2b00740464e19b56da6869432b8e9efc1a9ca657f`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d9270ca0635c8e43a137ef9ea2bd3d132f77f36bf563b585c50d43bc67115`  
		Last Modified: Fri, 08 May 2026 19:43:27 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:877bc4f2e9cebde5f6dd5db0625e8c11c1d5fc1450749b8df1ca04eee385183f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225182040bb866da2edada7d68127d3de35b20144022da2ee5092b81a48ff243`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 02:32:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:32:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:54 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 02:32:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:33:12 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 02:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 02:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d77fe6e136fe8121f88c8e24891e2e3ce57d89ace081cd7917cd296bf2781`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c6fd13d86c4615402446553400ddbf811488b8652dfeaf1b30369df23a3d31`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 7.4 MB (7399499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977c5ff033346e1cf892081e6ed41c4dcce967c151c4974c113f4e0406b20fa`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 372.1 KB (372140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28cd61fdf1d3cba5a38ba01f0090a13b851c1b038b6006be4782108f438976`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0df2b1587eda8004175334929323a5430ee32ec7ca0ad93243315dcdfcb1c4d`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d01bd714bd29509eccc7ffd6d42cf54ecb8e91fdd75f00b3a997e6b6adbaf5`  
		Last Modified: Wed, 22 Apr 2026 02:33:35 GMT  
		Size: 104.0 MB (104028166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b90460439c32fbf3c5d889b6093560b179158059ea12b5c62a42ce21380a3fe`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d8c0832e7dbb36e1959f210cc39b9c2f06cded3a0918c38f62da8bb11fe9cc`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846e3f061b916fca388e65c142917fbb47748b12371a1cc92c23fb6caa3881ea`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2a413a15f2d3d0b12253a678fe2d6199c1424fe5ce4d2166204aefde16a81`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:9d0ddb4a733d4cb15d823ccf7fef246af5176b6fbaf3ea6aaef729aa2ddd8e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa74c39c384641d3f8ad817a1c998223d297e3d2453b62a75dbd87fc179ca1c5`

```dockerfile
```

-	Layers:
	-	`sha256:8ae251a1734f9ea12b57e27040fd43078355bb4d78477392c9868f468347d2e5`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cd4bab63ce540f1c9dc037237c27456a1710328cd50cf0b8b3606d11ee6480`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 31.7 KB (31737 bytes)  
		MIME: application/vnd.in-toto+json
