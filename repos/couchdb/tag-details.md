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
$ docker pull couchdb@sha256:04c0634787a561546040c61186c89a2bdf268a10abad4a6b07d50473e27d5aa7
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
$ docker pull couchdb@sha256:21fa430aae63671a3127673e38de2e2d071f0d3dbc8a31d8fac62214afc8f59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142051235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3b5c0109cce05b5ad263097797085346efb950cc7f38578fcdbe681a392fd9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:07:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:07:51 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 08 Dec 2025 23:07:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:08:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:08:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:05 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 08 Dec 2025 23:08:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:08:18 GMT
VOLUME [/opt/couchdb/data]
# Mon, 08 Dec 2025 23:08:18 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 08 Dec 2025 23:08:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c9c88e767d5012a0e2dfc399f43404f8f4c3ab262bac734533e8204099be56`  
		Last Modified: Mon, 08 Dec 2025 23:08:40 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716c80c273f8809bbb548458f931e4762b0f447aeca7508e13c19b9c51ff73c0`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 7.9 MB (7881739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609e5bdfa7b1f8218d7dca07b7adde8b80150cda1d87f1f29da51c3a313db82e`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 401.7 KB (401735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d5a41c17903fc51342b98f1560b681035cfe0f7d321a36b50f34de4387824e`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 76.5 KB (76465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b62383183a15d775ce3c4f9430de03b79d6935279d541adfff250dcc8dd91c1`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd726490d7d051e52d86d74f97c293416c4886a83478fc5a2d5b044d81865fee`  
		Last Modified: Mon, 08 Dec 2025 23:08:50 GMT  
		Size: 105.5 MB (105457448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8856ade7c27a5fad19081cfe83a474d6898d1154adff0b08e6d87e98b5c3de45`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2897b671832f132cfb5b6f0c62ea6b5e8c6575868e3a4e361ac25df1f27e196c`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f82cbc9af1f4d32f1432c6cb4d15836c5891f1c431c9a75f8b08dfcd78e027a`  
		Last Modified: Mon, 08 Dec 2025 23:08:42 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b27282aaec507f7fcfa9a1efbb06f1abcd9cf46f8e39f236eb3c9a77a315e3`  
		Last Modified: Mon, 08 Dec 2025 23:08:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:aa6793cd8ef71d7ec06be94d34a9b693f27c315496b3d2778f2a2b406ffae798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087563041a4b7312487736498a1de80ea1d6f4ad2593c2b5efec7ae033626675`

```dockerfile
```

-	Layers:
	-	`sha256:e5384526458d9c66863e4dfe7e78e0b8c04ba19babd32f7e9d6cca6e9e683745`  
		Last Modified: Mon, 08 Dec 2025 23:34:23 GMT  
		Size: 4.2 MB (4184411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb9654333a4a6f0527c5d6d3686a1f350ad41a8b9d6ffa53b3e61c8d0be6a619`  
		Last Modified: Mon, 08 Dec 2025 23:34:24 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5f7127237ffae4f91803c563aca8cab6794b7407a996ff990c8c1b1c2ca53e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141404878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55007689149f254ad0f8f6bd9bf294b0b311c557f7ffb3e9c937f3eb5fc0ab81`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:32:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 03:32:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Nov 2025 03:32:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:32:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 03:32:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 03:32:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:32:44 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 18 Nov 2025 03:32:44 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:32:57 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Nov 2025 03:32:57 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Nov 2025 03:32:57 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1576797ad33df163e9df21eb3631e2cdab5607c35ac9d16b05797a9f0b4f4a62`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79357682a367c4944142ae7161c0dda87bafbfc1efe3ab937561ebdd5750291e`  
		Last Modified: Tue, 18 Nov 2025 03:33:21 GMT  
		Size: 7.7 MB (7692064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce499cb7fc066fc3f76ee116bcaf10c219f3d22ce0e194be90fa33ca7a616dd2`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 370.5 KB (370469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e456ad386d15df751348896749548e4fd781a2023d9b42644fbcc1c2d5d6d1`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 76.4 KB (76437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733cbbeb7fc213083912a6b6196dc4110d4058dfb0a20b6862b95f00d522b4df`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39cd99b3838668bbe1e6b0a1597d16cd159d847fc59fdce20eaab12c82c14b0`  
		Last Modified: Tue, 18 Nov 2025 03:33:30 GMT  
		Size: 105.2 MB (105158266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bbc9cf6f8919e4db1d162042a7f0bdb1899bb499ef0fd2aea33c34279a2de5`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a515d4096222e0e5d1fd051a7bb662d57e2bf1399c5fbe948e586acbd0b2826`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da500d6a31cb08f836c5e8e6b3dd8e6a2627aadd532f9f42b00bff559c48cf7c`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c13fb1a8fa5090d1c8664b8995b33a4d3e90897d58d870a44b4adebda1bd7c`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:fca47f92afd675f23c01b209db15ed17155a120f1d6ba7af7fbe1d109b1131d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9fe471488817a855aab9ca0c86e24330452ebe1a52a1c72441dcdc562b6c19`

```dockerfile
```

-	Layers:
	-	`sha256:e06f7cfcc9ba3ee4ae91e10ca855cd55994ebdb9a3d2538f260b8f486120dccb`  
		Last Modified: Tue, 18 Nov 2025 05:34:31 GMT  
		Size: 4.2 MB (4184704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:147c25b828a6992c4737d8171cf72964b820162b85c9cbcc55f5f7b95e01dbbb`  
		Last Modified: Tue, 18 Nov 2025 05:34:32 GMT  
		Size: 31.9 KB (31930 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:c9a410eba40de845f009bd7e7034f257568c0b2d032050720dc43d773ccbc6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d610f8d7a2c99fd1337112307b105aa162a3c7aa8f7523d2f5097f9b4d352cd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:12:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Dec 2025 00:12:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 09 Dec 2025 00:12:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 09 Dec 2025 00:12:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 09 Dec 2025 00:12:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:14 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 09 Dec 2025 00:12:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:12:31 GMT
VOLUME [/opt/couchdb/data]
# Tue, 09 Dec 2025 00:12:31 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 09 Dec 2025 00:12:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf35cfc495ac6ff70615ca926f57eb6f3961039055b8e0bc78d371b81d66cdcc`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a773213be6f84f3b269baecb1e4cc68f15241c5c383b48b907976c4eb946677`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 7.4 MB (7398139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d5b33ae2cd1bbd5548a76327f0d452ff6f8ba5339ec9c241cbd71a9f453f10`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 372.1 KB (372110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec7e4611c56c4658d750fa9a9cfa1506d45b7d5ad3a68ff8bd891309614c227`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 76.5 KB (76496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fb144940d3c8de5b68011f7c579283d7e04801dd5de76eb64f57bfa89926d3`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e990b9456e92e62ad8b10a958d9038d178a054f7af24c13a64841bba8bc484fe`  
		Last Modified: Tue, 09 Dec 2025 00:13:09 GMT  
		Size: 104.0 MB (104028693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de0c37a96fc881df0e067b4af3e9225be9f50b23eb987ee9b2b6bf242797f41`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845f1a6ee7ce778b2591bbfcde5ad849f34d69c6549c658cfab4f83234163c29`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ab7d725557e60a9b08e9efe0c6be7f3c6a76862af340465be69f3142fe7fd9`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324d82d39cdac56ca6ab5048a5efec1f0303825b13de2695e0014941f79017a2`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:0c524c076ae68a0db10ef651ba126d5920fb123c6c7e6231b335c5b1153dd8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8210e9735ca6eef17803a45249133dedbb0fd46a7f39421c806f22e8329ecff3`

```dockerfile
```

-	Layers:
	-	`sha256:b31d81caa581677e3119d98b84d301af6dff06dc539097e3313a88ee79d4513f`  
		Last Modified: Tue, 09 Dec 2025 02:33:47 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0a65d403bfce6cbe8353b601006c63d5ec489b6ecd9989117ad8bc072515784`  
		Last Modified: Tue, 09 Dec 2025 02:33:48 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:611564b0bee06eddda80a5a2c412b262065a12a9305d09b60ed0b5a3c61fe34e
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
$ docker pull couchdb@sha256:89743ee7151b366d6b28891c88f05210539626294c3321c7345d2efd0e90baae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb0753316d72cc07f4f3abbacfdc4ac02d3c7f4ecd6c71fd7c837e33285365f`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:08:07 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 08 Dec 2025 23:08:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:08:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:08:28 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:28 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:08:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 08 Dec 2025 23:08:34 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 08 Dec 2025 23:08:34 GMT
VOLUME [/opt/nouveau/data]
# Mon, 08 Dec 2025 23:08:34 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 08 Dec 2025 23:08:34 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10769f6e3ca05b0d30f4148aa16e7c13217c6a625a803ea087ee5804768ab4a9`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0703e44e2d7cafd694d8589161e1f5636f76a9b3d970195a5db2aa4b2406a2`  
		Last Modified: Mon, 08 Dec 2025 23:09:01 GMT  
		Size: 7.9 MB (7881795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d787b4bdf36bea424e37ecda03ad1f3ea9805c39521e250c7d97b554b8cd29a3`  
		Last Modified: Mon, 08 Dec 2025 23:09:07 GMT  
		Size: 77.4 MB (77380734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1380eab6cfd83025c297d8099e1247247d56bf95db84862a76d1a5becb1d35f`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 424.1 KB (424123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daf5d2841e907f58723ac0ae3c6fc6078ec51ae8600573953ff5e97445202ad`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 99.5 KB (99518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6cb9bf85b66a1cc208c72599a77b2136ea9d83b7646638973352fec03986fb`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c573270414f2f71a211e02c3a9aacdcc054f37201a785bd7b76d105e0f142c1`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 42.4 MB (42436360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfe2f3d09ee37fa7d61d8b5bc8348ab29b5fbcd32c65e3a0814f1387c4cf010`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:2e4168227791331cacb1f46381af60e5517e8a49edc38ed67a04d517236fed73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f852f63f06fb6a6280ac9e16c490f7f1d4c953810bcd05e1e15444a2153c2e`

```dockerfile
```

-	Layers:
	-	`sha256:1e1592694180e85e28f9f9b10cca96e33f11889b75314b91185faceba2b0a0f1`  
		Last Modified: Mon, 08 Dec 2025 23:34:26 GMT  
		Size: 3.7 MB (3658053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178217fabee2aa3c6d311ebede57eca5ce36fbe5975f4a8d599ad046659d337b`  
		Last Modified: Mon, 08 Dec 2025 23:34:26 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:544fd2610735f66997f2dc3ea47343f29126794307217fdab34cc896292886fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53dda8263a1e2cced1df9591e99bf4e8de27559768d24d1a53dcdf6a6bcf9fc`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:33:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 03:33:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Nov 2025 03:33:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:33:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:33:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 03:33:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 03:34:00 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:34:00 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 03:34:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Nov 2025 03:34:06 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Nov 2025 03:34:06 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Nov 2025 03:34:06 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Nov 2025 03:34:06 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d170929f5122b754e9c3b75c81f5ccce945c639b120cf7fd9f04de497d3351`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d122aab947d7f0b37352ff25d869519635be1a0e7861aea35a7607930d7048`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 7.7 MB (7692053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2712de1723319370a513b2ce6b80dfe68316e938066ef53bd751fb7913363595`  
		Last Modified: Tue, 18 Nov 2025 03:34:37 GMT  
		Size: 76.7 MB (76691571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccbab553627aa3a0f31a1a13d6435b96fa20c948bb8f0a06acd9ce3af5ee46c`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 392.7 KB (392661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4afbad864dfc76385d9a0180412ac0f75762270e3310fb788e9fd11f3b4c72`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 99.4 KB (99437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5123d1a7c8c978a9b8d8ea941fa30415dee531acb7551c51886b2c3eb5403a1`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0409338ca2ef2307306a8c6ce9d0553d3e006645a788373fa0b84faac326d9a`  
		Last Modified: Tue, 18 Nov 2025 03:34:36 GMT  
		Size: 42.3 MB (42339007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3341e7b0042637cf21bf2c7c5d35faa8cf23612d5f81cf113f113d3a1cf06fe1`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7fb5776f8220586ddd041b8b27727ad9eb417b5ae49c98b78444d6d0ed4f4ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08692c5b65246b53c1db3b39b2d49b3982af4f0b68425f674dad749cd5907123`

```dockerfile
```

-	Layers:
	-	`sha256:5b6483cab95ef058cfba5af9eedba8c2f72f1ebc0ee7a7359369b99d70242044`  
		Last Modified: Tue, 18 Nov 2025 05:34:42 GMT  
		Size: 3.7 MB (3656729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc566dff9630765cf5b25f3bb6027d91360ac02f2b43f545da39a7656afd750`  
		Last Modified: Tue, 18 Nov 2025 05:34:43 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:7c12e5c2d11a4e335bc8a826debcde85a8431afeb2d5ded342bc42c376eb1274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150085870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76459a52a9683cd87c99ca9180c3ada00aaf5d7d8038c9914d42a391453dea26`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:12:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Dec 2025 00:12:23 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 09 Dec 2025 00:12:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 09 Dec 2025 00:12:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 09 Dec 2025 00:12:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 09 Dec 2025 00:12:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 09 Dec 2025 00:12:52 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 09 Dec 2025 00:12:52 GMT
VOLUME [/opt/nouveau/data]
# Tue, 09 Dec 2025 00:12:52 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 09 Dec 2025 00:12:52 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c612ddb2613792ba5de7275ede737232c8919bcc9a90ad4dc4a90f42280a0c1`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe05b0e865a4ea871efebb32075b19d70f33e93973dbf638d5e901eacd7440b`  
		Last Modified: Tue, 09 Dec 2025 00:13:20 GMT  
		Size: 7.4 MB (7398109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a18a834e5966996b03bde3dcc826f2b0f461c9717c2a61a157c164bc0035d65`  
		Last Modified: Tue, 09 Dec 2025 00:13:26 GMT  
		Size: 73.1 MB (73142808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508bcd23c82e79bad82091e27743c8746f4b842f6e06556e20c6f6f34a1cf953`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 394.4 KB (394392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbf41a4ae36e10031fc97050f94fbb0ca20081067177751280bee84b46f9584`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 99.6 KB (99616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6092dee6efcbddddabba5653f407f3336d213fc568ad9c6706694ef1f9d439`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a684fa098de563675f00459f674e4c14b2b3edb8dbf71202bc5d7f45c816cd`  
		Last Modified: Tue, 09 Dec 2025 00:13:22 GMT  
		Size: 42.2 MB (42164639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d62053a9e778fc9ff6f26567bed49bc2cc11e771c13d99a53c5014a70c3a393`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:fafb2fb277c2d762056e9587dee834882ec7139cc3b0784d183c8b78e67d1ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e08fae2b3c9cf16c44563ea23595fa688447bc2544e2f2df04f047d64771c55`

```dockerfile
```

-	Layers:
	-	`sha256:c5809d637293d25977e1b07b589b7d0fd3dce59684371058f33db1b61ec2b506`  
		Last Modified: Tue, 09 Dec 2025 02:33:53 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2c29a59962a0f97410221034dec64942903f474ca029dc5e698be9544e54a0`  
		Last Modified: Tue, 09 Dec 2025 02:33:53 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:fabc86f9e37beb192b40bc5358b6d09b6c87627c251d29712ad4dec213805eab
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
$ docker pull couchdb@sha256:65353d9e1fe10e1f7c26f549f7e43aca3e118580a6d1df2ee3014711fbd43680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139013851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934abd1aaaed22697edecf01adb2e0ca5b6b8ce4c2fa8396972aef1777d11cc6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:08:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 08 Dec 2025 23:08:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:08:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:08:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:29 GMT
ENV COUCHDB_VERSION=3.4.3
# Mon, 08 Dec 2025 23:08:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:08:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 08 Dec 2025 23:08:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 08 Dec 2025 23:08:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 08 Dec 2025 23:08:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 08 Dec 2025 23:08:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:08:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:08:43 GMT
VOLUME [/opt/couchdb/data]
# Mon, 08 Dec 2025 23:08:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 08 Dec 2025 23:08:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e153a5f16627de7011b0c4f162810478f37db5725d0d561a2df184feba6a2627`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508f55e79ebecf00ff624029b1029c6c1a8b60dee8e19a19246420bd0b9012b6`  
		Last Modified: Mon, 08 Dec 2025 23:09:06 GMT  
		Size: 7.9 MB (7881840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4491076665d5beb65c9ec3829439587cc9e4ddd7f259c38765680e7949e8bc`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 401.7 KB (401731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85532ceaeaba26872e22bbf0f1a3fa99767dd98e7182c769e3aefc4100691f46`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 76.5 KB (76478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849c8699d4d1a9aa719e7181711909a271582a8203b6892feed93ff1c476c4da`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468c7e062c822fb83b888e84ab29b62abe4e1534cd113ba768518c3faaf529e0`  
		Last Modified: Mon, 08 Dec 2025 23:09:14 GMT  
		Size: 102.4 MB (102419955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244dc957ee0b8da8645558c507ca51e853c4193c8de82b5a2bbc1b438b494328`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85031d190470b34d0f0dc6e93d9aa3ba160e0d58556e1c3e56e8b9540b32cf75`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f4ea18df8af7b5426224b2822d39887e7677d9b308af66b936ae0695371cb1`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55384741dd8773261ad1d6fab337ea9fb1f8019c1ae886e8d44ecd54ef3c48e`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:463b40278b12962ff77d474084fc1146e565523dd49676c917e57de46591e4d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39824ba4ca01d32e22132b3b80d8e093ca4472ee9d061c88a8f9548add430ba`

```dockerfile
```

-	Layers:
	-	`sha256:b2abbee5de78fa0469df35e0da4216b18225b3064858a4bbb779f445865b4cca`  
		Last Modified: Mon, 08 Dec 2025 23:34:34 GMT  
		Size: 4.1 MB (4125385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375895866708619ad4dc1e436db0475a208f38fda7d2f73b0b59c400f835332b`  
		Last Modified: Mon, 08 Dec 2025 23:34:35 GMT  
		Size: 31.1 KB (31147 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9139c0c7111a9365e7cf413d7860d15b8a35a43904bbc34c97693a1eecd428d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138415606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c3a897326a0c94cf580543ce1ca3b86112589d0cfc69495b4ebdc58b128b9d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:32:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 03:32:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Nov 2025 03:32:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:32:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 03:32:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 03:32:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:32:44 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Nov 2025 03:34:35 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 03:34:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Nov 2025 03:34:46 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Nov 2025 03:34:47 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Nov 2025 03:34:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Nov 2025 03:34:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 03:34:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:34:47 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Nov 2025 03:34:47 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Nov 2025 03:34:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1576797ad33df163e9df21eb3631e2cdab5607c35ac9d16b05797a9f0b4f4a62`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79357682a367c4944142ae7161c0dda87bafbfc1efe3ab937561ebdd5750291e`  
		Last Modified: Tue, 18 Nov 2025 03:33:21 GMT  
		Size: 7.7 MB (7692064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce499cb7fc066fc3f76ee116bcaf10c219f3d22ce0e194be90fa33ca7a616dd2`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 370.5 KB (370469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e456ad386d15df751348896749548e4fd781a2023d9b42644fbcc1c2d5d6d1`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 76.4 KB (76437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3898808d638aed5b417a4942960483e67e370760993d1cd8c86975ed1e26467`  
		Last Modified: Tue, 18 Nov 2025 03:35:10 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7a54e9fb8f0290ca44c637738dbd5b3ccf1b628c793095b39fc3505e7fe6d6`  
		Last Modified: Tue, 18 Nov 2025 03:35:22 GMT  
		Size: 102.2 MB (102168996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbf2f2efe6a1cf9c279697652ff0a7eb30eb837656cebc9643418e350b61ccd`  
		Last Modified: Tue, 18 Nov 2025 03:35:09 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b134354da3a709f4d758c8b6728bc311b010c41f68ce1b77ee811c988053f6e`  
		Last Modified: Tue, 18 Nov 2025 03:35:09 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf4400e3572ff0acc7cfd389a158d41b18343b3daad33fdb1b75bbff4a9851`  
		Last Modified: Tue, 18 Nov 2025 03:35:09 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ffe1d819f1a574bfb42aa492417cb4f4de00e6b566733ed1b572d4e88c8af6`  
		Last Modified: Tue, 18 Nov 2025 03:35:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:b1cb55a07039e111cf8afcdcfbb85873d4dd3670f5cfc715d6375f37e99d5762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c447f8928c3d3292d6a86458a1fd0cc8d41dac6b615699f7b433745053579411`

```dockerfile
```

-	Layers:
	-	`sha256:3879517ac6e48a8eaf983a7203263951907fa15e99fbf15566349431b4fdf7f4`  
		Last Modified: Tue, 18 Nov 2025 05:34:51 GMT  
		Size: 4.1 MB (4125654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23e909694eb4ab7950404f7ce1d3928122e710a10a8ec58ce2490b66c2581514`  
		Last Modified: Tue, 18 Nov 2025 05:34:51 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:c2ee35762d461d14bb335199612c1753db6603186de66ff03df525659ad0b9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135792813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116c12eef17237c12f23dbe4717a20f168faa5e8b0f842fb30ca01eb91dc49de`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:12:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Dec 2025 00:12:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 09 Dec 2025 00:12:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 09 Dec 2025 00:12:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 09 Dec 2025 00:12:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:14 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 09 Dec 2025 00:13:23 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:13:53 GMT
VOLUME [/opt/couchdb/data]
# Tue, 09 Dec 2025 00:13:53 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 09 Dec 2025 00:13:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf35cfc495ac6ff70615ca926f57eb6f3961039055b8e0bc78d371b81d66cdcc`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a773213be6f84f3b269baecb1e4cc68f15241c5c383b48b907976c4eb946677`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 7.4 MB (7398139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d5b33ae2cd1bbd5548a76327f0d452ff6f8ba5339ec9c241cbd71a9f453f10`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 372.1 KB (372110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec7e4611c56c4658d750fa9a9cfa1506d45b7d5ad3a68ff8bd891309614c227`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 76.5 KB (76496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b977ec9012a1545cb5c8b2f3569b21a258b52d06f5eea0185749e5e12813e4bc`  
		Last Modified: Tue, 09 Dec 2025 00:14:19 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807809898fd1c7e4a3cb43ce958520d83e97210445db0539ba69f3d127a11987`  
		Last Modified: Tue, 09 Dec 2025 00:14:14 GMT  
		Size: 101.1 MB (101056208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802cf81922757f3883e8ed00bc70a73bbb904464f4ebc44ba568531d871c776b`  
		Last Modified: Tue, 09 Dec 2025 00:14:19 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf624fd3e4c327c1033df936a8f9acb9ae31b7f86a37c12d8c1ee466c069fd4`  
		Last Modified: Tue, 09 Dec 2025 00:14:19 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f9a0d2b0f2ad375a6d2f07899bc1094636c1959a0b26ed9d8eaebe5a55971a`  
		Last Modified: Tue, 09 Dec 2025 00:14:19 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fc65e957cf9baf963af0ec0aaa936ac6b0899833e1436cab5b90c347d69fca`  
		Last Modified: Tue, 09 Dec 2025 00:14:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:7e4fdd0615140282efdc77a2f3c30101ed2cf621fe9f52f20e3a8aa7bea91f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baba6f82ff901aa92ea119e950e1b2ed0b08b380f637f54f9aabd508f27df77e`

```dockerfile
```

-	Layers:
	-	`sha256:eb96eac501647639211a48da1a95bd674e583601b86834be6c3b0a856474e33b`  
		Last Modified: Tue, 09 Dec 2025 02:34:00 GMT  
		Size: 4.1 MB (4121581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43fb5db81001ca44b8d9d6e9ebe6d1d0f85d9477fcedbe588767497c32cd127`  
		Last Modified: Tue, 09 Dec 2025 02:34:01 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:38e815fca2b69e28eec73629b8e39eacf37979528895dc5219e1866cee1e6d52
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
$ docker pull couchdb@sha256:8343c4c7d70f6d6252aa41be193a3d154a5eb6f3382c798c0d4b89734bcd42b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7158e7a7c93c12c5a0fe5825699bf5e0098489f7938d5175a6aa9613b6b1761`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:08:36 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 08 Dec 2025 23:08:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:08:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:08:57 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:57 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:09:03 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 08 Dec 2025 23:09:03 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 08 Dec 2025 23:09:03 GMT
VOLUME [/opt/nouveau/data]
# Mon, 08 Dec 2025 23:09:03 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 08 Dec 2025 23:09:03 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a9da64e20fba1feaeaf2911af6182af957212f954fa7ea7da9df1357ea94b5`  
		Last Modified: Mon, 08 Dec 2025 23:09:27 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf8fbb838bd93ee93d8f6bfb363ee1cff58609dca61684bfea9f5c880a276ff`  
		Last Modified: Mon, 08 Dec 2025 23:09:28 GMT  
		Size: 7.9 MB (7881765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f135b346d93f86adc4875bb150258c76d1e4c92038f72e21f8aa2f0c51981902`  
		Last Modified: Mon, 08 Dec 2025 23:09:37 GMT  
		Size: 77.4 MB (77380761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51942d89b4cb6c8266a73e2f81e49024f563be908a3ff955e7a172e5ac527e29`  
		Last Modified: Mon, 08 Dec 2025 23:09:27 GMT  
		Size: 424.1 KB (424117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08767e4524a36ccb4246b970e1d6f93bd5f9259a288a9bdfbe61b35870de2188`  
		Last Modified: Mon, 08 Dec 2025 23:09:28 GMT  
		Size: 99.5 KB (99490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d3f495cf96f4f25c98f5cda668821580daaa18341e120f5af6b0885cdaef1`  
		Last Modified: Mon, 08 Dec 2025 23:09:27 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c65334a9353144290f50cd8ded8985fa35bca2b05974ad477e378ceecb9288`  
		Last Modified: Mon, 08 Dec 2025 23:09:33 GMT  
		Size: 42.4 MB (42436028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c912113b4f4e8f6bf92b79e93de695bda2dbcc51ea7fe5efa519ba0cdee94fb`  
		Last Modified: Mon, 08 Dec 2025 23:09:27 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:557b41d99683f61bdd7f2c32ef64dcf09540f5b1cc21d852822ef6b0c7d0c5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291f952cedb9d1e62fac1ce6bf3781a6595394b6f6ba38d027f69ffd2488dee2`

```dockerfile
```

-	Layers:
	-	`sha256:7ac47f7d32ef509f56f7d9ece3bf4253e1faea7c43e72cfe0ec3235385107007`  
		Last Modified: Mon, 08 Dec 2025 23:34:39 GMT  
		Size: 3.7 MB (3657747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88cfe7337740ad37177a3cfff4822241730438c26b5de2dc22558ff24975805`  
		Last Modified: Mon, 08 Dec 2025 23:34:40 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5826f64549de938a695a69489c26c3a7fa99624d42f503de818ae006003b483f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155317944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9678857f76bbd6ac34f0a1b12b7814036e8ef11aa4321751077e5d9fb0d0fa`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:33:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 03:33:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Nov 2025 03:33:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:33:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:33:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 03:33:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 03:34:00 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:34:00 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 03:35:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Nov 2025 03:35:34 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Nov 2025 03:35:34 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Nov 2025 03:35:34 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Nov 2025 03:35:34 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d170929f5122b754e9c3b75c81f5ccce945c639b120cf7fd9f04de497d3351`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d122aab947d7f0b37352ff25d869519635be1a0e7861aea35a7607930d7048`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 7.7 MB (7692053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2712de1723319370a513b2ce6b80dfe68316e938066ef53bd751fb7913363595`  
		Last Modified: Tue, 18 Nov 2025 03:34:37 GMT  
		Size: 76.7 MB (76691571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccbab553627aa3a0f31a1a13d6435b96fa20c948bb8f0a06acd9ce3af5ee46c`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 392.7 KB (392661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4afbad864dfc76385d9a0180412ac0f75762270e3310fb788e9fd11f3b4c72`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 99.4 KB (99437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5123d1a7c8c978a9b8d8ea941fa30415dee531acb7551c51886b2c3eb5403a1`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c7bec589009ee727eaf902c1b707504670924d748db00b68559b6a447a5dfa`  
		Last Modified: Tue, 18 Nov 2025 03:35:57 GMT  
		Size: 42.3 MB (42338134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c54fdd31637ae2e354b718b00f0e0dc0e4f0955472f3beb6cb883b1aa08e17`  
		Last Modified: Tue, 18 Nov 2025 03:35:52 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:948cf6ab9747f306442316a812c64284a79ca2ffd9a06ff9fd28cb4131fe7cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fa4f1e49bac173578b617cab72d8a4dbbe10d27965d13ac5a09c9ba8447f47`

```dockerfile
```

-	Layers:
	-	`sha256:100536e0bf5ee858c284c5bfa21cb06a76e0e3af3b5aa5941d858ff26c6f786d`  
		Last Modified: Tue, 18 Nov 2025 05:35:00 GMT  
		Size: 3.7 MB (3656411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5798bf43a465db8ec6ca57248d05fc6ff8225d00418fdea7c723b7665afefbf2`  
		Last Modified: Tue, 18 Nov 2025 05:35:01 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:7e77f511b6be10806f2b050e7d033d8a47802c9eb20f587fb253002cc139cf56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150084168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d39e088956b925a3e02e66a35f5aa1aede57820ff56c9c2eb0aeb64a7c55f1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:12:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Dec 2025 00:12:23 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 09 Dec 2025 00:12:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 09 Dec 2025 00:12:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 09 Dec 2025 00:12:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 09 Dec 2025 00:13:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 09 Dec 2025 00:13:52 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 09 Dec 2025 00:13:52 GMT
VOLUME [/opt/nouveau/data]
# Tue, 09 Dec 2025 00:13:52 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 09 Dec 2025 00:13:52 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c612ddb2613792ba5de7275ede737232c8919bcc9a90ad4dc4a90f42280a0c1`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe05b0e865a4ea871efebb32075b19d70f33e93973dbf638d5e901eacd7440b`  
		Last Modified: Tue, 09 Dec 2025 00:13:20 GMT  
		Size: 7.4 MB (7398109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a18a834e5966996b03bde3dcc826f2b0f461c9717c2a61a157c164bc0035d65`  
		Last Modified: Tue, 09 Dec 2025 00:13:26 GMT  
		Size: 73.1 MB (73142808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508bcd23c82e79bad82091e27743c8746f4b842f6e06556e20c6f6f34a1cf953`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 394.4 KB (394392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbf41a4ae36e10031fc97050f94fbb0ca20081067177751280bee84b46f9584`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 99.6 KB (99616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6092dee6efcbddddabba5653f407f3336d213fc568ad9c6706694ef1f9d439`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9596553058ded6d3b4134adc2777c007800e13e5f2adbaef290cd5705a83d961`  
		Last Modified: Tue, 09 Dec 2025 00:14:17 GMT  
		Size: 42.2 MB (42162940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffea749e0e0b4bc6da57668d2371ac3f1cec4946b3cbeac43742d1d26911a0d`  
		Last Modified: Tue, 09 Dec 2025 00:14:15 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:89aa1dcbd3e110f338daf42aa917d74a060bb7c1810bd4fc692c28e07b7ae06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65f2e47946c9a723619a387ea1f7ddb74e957c43caf3ecb8bd2b3a2c65efc7f`

```dockerfile
```

-	Layers:
	-	`sha256:41096054aa4649a5fe9d7f3bd6058f5b645e73edf1649c493608fee59d985633`  
		Last Modified: Tue, 09 Dec 2025 02:34:04 GMT  
		Size: 3.6 MB (3648276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927d244761c6615e3de03dcead1bfbbf66df28acd2fde38c10ca5f28fa5ab991`  
		Last Modified: Tue, 09 Dec 2025 02:34:05 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:fabc86f9e37beb192b40bc5358b6d09b6c87627c251d29712ad4dec213805eab
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
$ docker pull couchdb@sha256:65353d9e1fe10e1f7c26f549f7e43aca3e118580a6d1df2ee3014711fbd43680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139013851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934abd1aaaed22697edecf01adb2e0ca5b6b8ce4c2fa8396972aef1777d11cc6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:08:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 08 Dec 2025 23:08:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:08:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:08:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:29 GMT
ENV COUCHDB_VERSION=3.4.3
# Mon, 08 Dec 2025 23:08:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:08:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 08 Dec 2025 23:08:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 08 Dec 2025 23:08:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 08 Dec 2025 23:08:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 08 Dec 2025 23:08:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:08:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:08:43 GMT
VOLUME [/opt/couchdb/data]
# Mon, 08 Dec 2025 23:08:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 08 Dec 2025 23:08:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e153a5f16627de7011b0c4f162810478f37db5725d0d561a2df184feba6a2627`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508f55e79ebecf00ff624029b1029c6c1a8b60dee8e19a19246420bd0b9012b6`  
		Last Modified: Mon, 08 Dec 2025 23:09:06 GMT  
		Size: 7.9 MB (7881840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4491076665d5beb65c9ec3829439587cc9e4ddd7f259c38765680e7949e8bc`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 401.7 KB (401731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85532ceaeaba26872e22bbf0f1a3fa99767dd98e7182c769e3aefc4100691f46`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 76.5 KB (76478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849c8699d4d1a9aa719e7181711909a271582a8203b6892feed93ff1c476c4da`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468c7e062c822fb83b888e84ab29b62abe4e1534cd113ba768518c3faaf529e0`  
		Last Modified: Mon, 08 Dec 2025 23:09:14 GMT  
		Size: 102.4 MB (102419955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244dc957ee0b8da8645558c507ca51e853c4193c8de82b5a2bbc1b438b494328`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85031d190470b34d0f0dc6e93d9aa3ba160e0d58556e1c3e56e8b9540b32cf75`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f4ea18df8af7b5426224b2822d39887e7677d9b308af66b936ae0695371cb1`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55384741dd8773261ad1d6fab337ea9fb1f8019c1ae886e8d44ecd54ef3c48e`  
		Last Modified: Mon, 08 Dec 2025 23:09:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:463b40278b12962ff77d474084fc1146e565523dd49676c917e57de46591e4d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39824ba4ca01d32e22132b3b80d8e093ca4472ee9d061c88a8f9548add430ba`

```dockerfile
```

-	Layers:
	-	`sha256:b2abbee5de78fa0469df35e0da4216b18225b3064858a4bbb779f445865b4cca`  
		Last Modified: Mon, 08 Dec 2025 23:34:34 GMT  
		Size: 4.1 MB (4125385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375895866708619ad4dc1e436db0475a208f38fda7d2f73b0b59c400f835332b`  
		Last Modified: Mon, 08 Dec 2025 23:34:35 GMT  
		Size: 31.1 KB (31147 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9139c0c7111a9365e7cf413d7860d15b8a35a43904bbc34c97693a1eecd428d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138415606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c3a897326a0c94cf580543ce1ca3b86112589d0cfc69495b4ebdc58b128b9d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:32:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 03:32:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Nov 2025 03:32:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:32:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 03:32:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 03:32:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:32:44 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Nov 2025 03:34:35 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 03:34:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Nov 2025 03:34:46 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Nov 2025 03:34:47 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Nov 2025 03:34:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Nov 2025 03:34:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 03:34:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:34:47 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Nov 2025 03:34:47 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Nov 2025 03:34:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1576797ad33df163e9df21eb3631e2cdab5607c35ac9d16b05797a9f0b4f4a62`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79357682a367c4944142ae7161c0dda87bafbfc1efe3ab937561ebdd5750291e`  
		Last Modified: Tue, 18 Nov 2025 03:33:21 GMT  
		Size: 7.7 MB (7692064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce499cb7fc066fc3f76ee116bcaf10c219f3d22ce0e194be90fa33ca7a616dd2`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 370.5 KB (370469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e456ad386d15df751348896749548e4fd781a2023d9b42644fbcc1c2d5d6d1`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 76.4 KB (76437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3898808d638aed5b417a4942960483e67e370760993d1cd8c86975ed1e26467`  
		Last Modified: Tue, 18 Nov 2025 03:35:10 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7a54e9fb8f0290ca44c637738dbd5b3ccf1b628c793095b39fc3505e7fe6d6`  
		Last Modified: Tue, 18 Nov 2025 03:35:22 GMT  
		Size: 102.2 MB (102168996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbf2f2efe6a1cf9c279697652ff0a7eb30eb837656cebc9643418e350b61ccd`  
		Last Modified: Tue, 18 Nov 2025 03:35:09 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b134354da3a709f4d758c8b6728bc311b010c41f68ce1b77ee811c988053f6e`  
		Last Modified: Tue, 18 Nov 2025 03:35:09 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf4400e3572ff0acc7cfd389a158d41b18343b3daad33fdb1b75bbff4a9851`  
		Last Modified: Tue, 18 Nov 2025 03:35:09 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ffe1d819f1a574bfb42aa492417cb4f4de00e6b566733ed1b572d4e88c8af6`  
		Last Modified: Tue, 18 Nov 2025 03:35:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:b1cb55a07039e111cf8afcdcfbb85873d4dd3670f5cfc715d6375f37e99d5762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c447f8928c3d3292d6a86458a1fd0cc8d41dac6b615699f7b433745053579411`

```dockerfile
```

-	Layers:
	-	`sha256:3879517ac6e48a8eaf983a7203263951907fa15e99fbf15566349431b4fdf7f4`  
		Last Modified: Tue, 18 Nov 2025 05:34:51 GMT  
		Size: 4.1 MB (4125654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23e909694eb4ab7950404f7ce1d3928122e710a10a8ec58ce2490b66c2581514`  
		Last Modified: Tue, 18 Nov 2025 05:34:51 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:c2ee35762d461d14bb335199612c1753db6603186de66ff03df525659ad0b9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135792813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116c12eef17237c12f23dbe4717a20f168faa5e8b0f842fb30ca01eb91dc49de`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:12:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Dec 2025 00:12:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 09 Dec 2025 00:12:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 09 Dec 2025 00:12:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 09 Dec 2025 00:12:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:14 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 09 Dec 2025 00:13:23 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:13:53 GMT
VOLUME [/opt/couchdb/data]
# Tue, 09 Dec 2025 00:13:53 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 09 Dec 2025 00:13:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf35cfc495ac6ff70615ca926f57eb6f3961039055b8e0bc78d371b81d66cdcc`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a773213be6f84f3b269baecb1e4cc68f15241c5c383b48b907976c4eb946677`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 7.4 MB (7398139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d5b33ae2cd1bbd5548a76327f0d452ff6f8ba5339ec9c241cbd71a9f453f10`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 372.1 KB (372110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec7e4611c56c4658d750fa9a9cfa1506d45b7d5ad3a68ff8bd891309614c227`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 76.5 KB (76496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b977ec9012a1545cb5c8b2f3569b21a258b52d06f5eea0185749e5e12813e4bc`  
		Last Modified: Tue, 09 Dec 2025 00:14:19 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807809898fd1c7e4a3cb43ce958520d83e97210445db0539ba69f3d127a11987`  
		Last Modified: Tue, 09 Dec 2025 00:14:14 GMT  
		Size: 101.1 MB (101056208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802cf81922757f3883e8ed00bc70a73bbb904464f4ebc44ba568531d871c776b`  
		Last Modified: Tue, 09 Dec 2025 00:14:19 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf624fd3e4c327c1033df936a8f9acb9ae31b7f86a37c12d8c1ee466c069fd4`  
		Last Modified: Tue, 09 Dec 2025 00:14:19 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f9a0d2b0f2ad375a6d2f07899bc1094636c1959a0b26ed9d8eaebe5a55971a`  
		Last Modified: Tue, 09 Dec 2025 00:14:19 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fc65e957cf9baf963af0ec0aaa936ac6b0899833e1436cab5b90c347d69fca`  
		Last Modified: Tue, 09 Dec 2025 00:14:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:7e4fdd0615140282efdc77a2f3c30101ed2cf621fe9f52f20e3a8aa7bea91f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baba6f82ff901aa92ea119e950e1b2ed0b08b380f637f54f9aabd508f27df77e`

```dockerfile
```

-	Layers:
	-	`sha256:eb96eac501647639211a48da1a95bd674e583601b86834be6c3b0a856474e33b`  
		Last Modified: Tue, 09 Dec 2025 02:34:00 GMT  
		Size: 4.1 MB (4121581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43fb5db81001ca44b8d9d6e9ebe6d1d0f85d9477fcedbe588767497c32cd127`  
		Last Modified: Tue, 09 Dec 2025 02:34:01 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:38e815fca2b69e28eec73629b8e39eacf37979528895dc5219e1866cee1e6d52
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
$ docker pull couchdb@sha256:8343c4c7d70f6d6252aa41be193a3d154a5eb6f3382c798c0d4b89734bcd42b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7158e7a7c93c12c5a0fe5825699bf5e0098489f7938d5175a6aa9613b6b1761`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:08:36 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 08 Dec 2025 23:08:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:08:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:08:57 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:57 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:09:03 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 08 Dec 2025 23:09:03 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 08 Dec 2025 23:09:03 GMT
VOLUME [/opt/nouveau/data]
# Mon, 08 Dec 2025 23:09:03 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 08 Dec 2025 23:09:03 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a9da64e20fba1feaeaf2911af6182af957212f954fa7ea7da9df1357ea94b5`  
		Last Modified: Mon, 08 Dec 2025 23:09:27 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf8fbb838bd93ee93d8f6bfb363ee1cff58609dca61684bfea9f5c880a276ff`  
		Last Modified: Mon, 08 Dec 2025 23:09:28 GMT  
		Size: 7.9 MB (7881765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f135b346d93f86adc4875bb150258c76d1e4c92038f72e21f8aa2f0c51981902`  
		Last Modified: Mon, 08 Dec 2025 23:09:37 GMT  
		Size: 77.4 MB (77380761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51942d89b4cb6c8266a73e2f81e49024f563be908a3ff955e7a172e5ac527e29`  
		Last Modified: Mon, 08 Dec 2025 23:09:27 GMT  
		Size: 424.1 KB (424117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08767e4524a36ccb4246b970e1d6f93bd5f9259a288a9bdfbe61b35870de2188`  
		Last Modified: Mon, 08 Dec 2025 23:09:28 GMT  
		Size: 99.5 KB (99490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d3f495cf96f4f25c98f5cda668821580daaa18341e120f5af6b0885cdaef1`  
		Last Modified: Mon, 08 Dec 2025 23:09:27 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c65334a9353144290f50cd8ded8985fa35bca2b05974ad477e378ceecb9288`  
		Last Modified: Mon, 08 Dec 2025 23:09:33 GMT  
		Size: 42.4 MB (42436028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c912113b4f4e8f6bf92b79e93de695bda2dbcc51ea7fe5efa519ba0cdee94fb`  
		Last Modified: Mon, 08 Dec 2025 23:09:27 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:557b41d99683f61bdd7f2c32ef64dcf09540f5b1cc21d852822ef6b0c7d0c5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291f952cedb9d1e62fac1ce6bf3781a6595394b6f6ba38d027f69ffd2488dee2`

```dockerfile
```

-	Layers:
	-	`sha256:7ac47f7d32ef509f56f7d9ece3bf4253e1faea7c43e72cfe0ec3235385107007`  
		Last Modified: Mon, 08 Dec 2025 23:34:39 GMT  
		Size: 3.7 MB (3657747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88cfe7337740ad37177a3cfff4822241730438c26b5de2dc22558ff24975805`  
		Last Modified: Mon, 08 Dec 2025 23:34:40 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5826f64549de938a695a69489c26c3a7fa99624d42f503de818ae006003b483f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155317944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9678857f76bbd6ac34f0a1b12b7814036e8ef11aa4321751077e5d9fb0d0fa`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:33:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 03:33:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Nov 2025 03:33:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:33:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:33:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 03:33:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 03:34:00 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:34:00 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 03:35:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Nov 2025 03:35:34 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Nov 2025 03:35:34 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Nov 2025 03:35:34 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Nov 2025 03:35:34 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d170929f5122b754e9c3b75c81f5ccce945c639b120cf7fd9f04de497d3351`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d122aab947d7f0b37352ff25d869519635be1a0e7861aea35a7607930d7048`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 7.7 MB (7692053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2712de1723319370a513b2ce6b80dfe68316e938066ef53bd751fb7913363595`  
		Last Modified: Tue, 18 Nov 2025 03:34:37 GMT  
		Size: 76.7 MB (76691571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccbab553627aa3a0f31a1a13d6435b96fa20c948bb8f0a06acd9ce3af5ee46c`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 392.7 KB (392661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4afbad864dfc76385d9a0180412ac0f75762270e3310fb788e9fd11f3b4c72`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 99.4 KB (99437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5123d1a7c8c978a9b8d8ea941fa30415dee531acb7551c51886b2c3eb5403a1`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c7bec589009ee727eaf902c1b707504670924d748db00b68559b6a447a5dfa`  
		Last Modified: Tue, 18 Nov 2025 03:35:57 GMT  
		Size: 42.3 MB (42338134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c54fdd31637ae2e354b718b00f0e0dc0e4f0955472f3beb6cb883b1aa08e17`  
		Last Modified: Tue, 18 Nov 2025 03:35:52 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:948cf6ab9747f306442316a812c64284a79ca2ffd9a06ff9fd28cb4131fe7cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fa4f1e49bac173578b617cab72d8a4dbbe10d27965d13ac5a09c9ba8447f47`

```dockerfile
```

-	Layers:
	-	`sha256:100536e0bf5ee858c284c5bfa21cb06a76e0e3af3b5aa5941d858ff26c6f786d`  
		Last Modified: Tue, 18 Nov 2025 05:35:00 GMT  
		Size: 3.7 MB (3656411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5798bf43a465db8ec6ca57248d05fc6ff8225d00418fdea7c723b7665afefbf2`  
		Last Modified: Tue, 18 Nov 2025 05:35:01 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:7e77f511b6be10806f2b050e7d033d8a47802c9eb20f587fb253002cc139cf56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150084168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d39e088956b925a3e02e66a35f5aa1aede57820ff56c9c2eb0aeb64a7c55f1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:12:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Dec 2025 00:12:23 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 09 Dec 2025 00:12:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 09 Dec 2025 00:12:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 09 Dec 2025 00:12:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 09 Dec 2025 00:13:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 09 Dec 2025 00:13:52 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 09 Dec 2025 00:13:52 GMT
VOLUME [/opt/nouveau/data]
# Tue, 09 Dec 2025 00:13:52 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 09 Dec 2025 00:13:52 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c612ddb2613792ba5de7275ede737232c8919bcc9a90ad4dc4a90f42280a0c1`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe05b0e865a4ea871efebb32075b19d70f33e93973dbf638d5e901eacd7440b`  
		Last Modified: Tue, 09 Dec 2025 00:13:20 GMT  
		Size: 7.4 MB (7398109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a18a834e5966996b03bde3dcc826f2b0f461c9717c2a61a157c164bc0035d65`  
		Last Modified: Tue, 09 Dec 2025 00:13:26 GMT  
		Size: 73.1 MB (73142808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508bcd23c82e79bad82091e27743c8746f4b842f6e06556e20c6f6f34a1cf953`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 394.4 KB (394392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbf41a4ae36e10031fc97050f94fbb0ca20081067177751280bee84b46f9584`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 99.6 KB (99616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6092dee6efcbddddabba5653f407f3336d213fc568ad9c6706694ef1f9d439`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9596553058ded6d3b4134adc2777c007800e13e5f2adbaef290cd5705a83d961`  
		Last Modified: Tue, 09 Dec 2025 00:14:17 GMT  
		Size: 42.2 MB (42162940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffea749e0e0b4bc6da57668d2371ac3f1cec4946b3cbeac43742d1d26911a0d`  
		Last Modified: Tue, 09 Dec 2025 00:14:15 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:89aa1dcbd3e110f338daf42aa917d74a060bb7c1810bd4fc692c28e07b7ae06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65f2e47946c9a723619a387ea1f7ddb74e957c43caf3ecb8bd2b3a2c65efc7f`

```dockerfile
```

-	Layers:
	-	`sha256:41096054aa4649a5fe9d7f3bd6058f5b645e73edf1649c493608fee59d985633`  
		Last Modified: Tue, 09 Dec 2025 02:34:04 GMT  
		Size: 3.6 MB (3648276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927d244761c6615e3de03dcead1bfbbf66df28acd2fde38c10ca5f28fa5ab991`  
		Last Modified: Tue, 09 Dec 2025 02:34:05 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:04c0634787a561546040c61186c89a2bdf268a10abad4a6b07d50473e27d5aa7
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
$ docker pull couchdb@sha256:21fa430aae63671a3127673e38de2e2d071f0d3dbc8a31d8fac62214afc8f59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142051235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3b5c0109cce05b5ad263097797085346efb950cc7f38578fcdbe681a392fd9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:07:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:07:51 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 08 Dec 2025 23:07:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:08:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:08:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:05 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 08 Dec 2025 23:08:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:08:18 GMT
VOLUME [/opt/couchdb/data]
# Mon, 08 Dec 2025 23:08:18 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 08 Dec 2025 23:08:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c9c88e767d5012a0e2dfc399f43404f8f4c3ab262bac734533e8204099be56`  
		Last Modified: Mon, 08 Dec 2025 23:08:40 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716c80c273f8809bbb548458f931e4762b0f447aeca7508e13c19b9c51ff73c0`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 7.9 MB (7881739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609e5bdfa7b1f8218d7dca07b7adde8b80150cda1d87f1f29da51c3a313db82e`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 401.7 KB (401735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d5a41c17903fc51342b98f1560b681035cfe0f7d321a36b50f34de4387824e`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 76.5 KB (76465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b62383183a15d775ce3c4f9430de03b79d6935279d541adfff250dcc8dd91c1`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd726490d7d051e52d86d74f97c293416c4886a83478fc5a2d5b044d81865fee`  
		Last Modified: Mon, 08 Dec 2025 23:08:50 GMT  
		Size: 105.5 MB (105457448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8856ade7c27a5fad19081cfe83a474d6898d1154adff0b08e6d87e98b5c3de45`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2897b671832f132cfb5b6f0c62ea6b5e8c6575868e3a4e361ac25df1f27e196c`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f82cbc9af1f4d32f1432c6cb4d15836c5891f1c431c9a75f8b08dfcd78e027a`  
		Last Modified: Mon, 08 Dec 2025 23:08:42 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b27282aaec507f7fcfa9a1efbb06f1abcd9cf46f8e39f236eb3c9a77a315e3`  
		Last Modified: Mon, 08 Dec 2025 23:08:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:aa6793cd8ef71d7ec06be94d34a9b693f27c315496b3d2778f2a2b406ffae798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087563041a4b7312487736498a1de80ea1d6f4ad2593c2b5efec7ae033626675`

```dockerfile
```

-	Layers:
	-	`sha256:e5384526458d9c66863e4dfe7e78e0b8c04ba19babd32f7e9d6cca6e9e683745`  
		Last Modified: Mon, 08 Dec 2025 23:34:23 GMT  
		Size: 4.2 MB (4184411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb9654333a4a6f0527c5d6d3686a1f350ad41a8b9d6ffa53b3e61c8d0be6a619`  
		Last Modified: Mon, 08 Dec 2025 23:34:24 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5f7127237ffae4f91803c563aca8cab6794b7407a996ff990c8c1b1c2ca53e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141404878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55007689149f254ad0f8f6bd9bf294b0b311c557f7ffb3e9c937f3eb5fc0ab81`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:32:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 03:32:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Nov 2025 03:32:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:32:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 03:32:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 03:32:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:32:44 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 18 Nov 2025 03:32:44 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:32:57 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Nov 2025 03:32:57 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Nov 2025 03:32:57 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1576797ad33df163e9df21eb3631e2cdab5607c35ac9d16b05797a9f0b4f4a62`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79357682a367c4944142ae7161c0dda87bafbfc1efe3ab937561ebdd5750291e`  
		Last Modified: Tue, 18 Nov 2025 03:33:21 GMT  
		Size: 7.7 MB (7692064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce499cb7fc066fc3f76ee116bcaf10c219f3d22ce0e194be90fa33ca7a616dd2`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 370.5 KB (370469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e456ad386d15df751348896749548e4fd781a2023d9b42644fbcc1c2d5d6d1`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 76.4 KB (76437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733cbbeb7fc213083912a6b6196dc4110d4058dfb0a20b6862b95f00d522b4df`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39cd99b3838668bbe1e6b0a1597d16cd159d847fc59fdce20eaab12c82c14b0`  
		Last Modified: Tue, 18 Nov 2025 03:33:30 GMT  
		Size: 105.2 MB (105158266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bbc9cf6f8919e4db1d162042a7f0bdb1899bb499ef0fd2aea33c34279a2de5`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a515d4096222e0e5d1fd051a7bb662d57e2bf1399c5fbe948e586acbd0b2826`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da500d6a31cb08f836c5e8e6b3dd8e6a2627aadd532f9f42b00bff559c48cf7c`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c13fb1a8fa5090d1c8664b8995b33a4d3e90897d58d870a44b4adebda1bd7c`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:fca47f92afd675f23c01b209db15ed17155a120f1d6ba7af7fbe1d109b1131d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9fe471488817a855aab9ca0c86e24330452ebe1a52a1c72441dcdc562b6c19`

```dockerfile
```

-	Layers:
	-	`sha256:e06f7cfcc9ba3ee4ae91e10ca855cd55994ebdb9a3d2538f260b8f486120dccb`  
		Last Modified: Tue, 18 Nov 2025 05:34:31 GMT  
		Size: 4.2 MB (4184704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:147c25b828a6992c4737d8171cf72964b820162b85c9cbcc55f5f7b95e01dbbb`  
		Last Modified: Tue, 18 Nov 2025 05:34:32 GMT  
		Size: 31.9 KB (31930 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:c9a410eba40de845f009bd7e7034f257568c0b2d032050720dc43d773ccbc6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d610f8d7a2c99fd1337112307b105aa162a3c7aa8f7523d2f5097f9b4d352cd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:12:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Dec 2025 00:12:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 09 Dec 2025 00:12:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 09 Dec 2025 00:12:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 09 Dec 2025 00:12:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:14 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 09 Dec 2025 00:12:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:12:31 GMT
VOLUME [/opt/couchdb/data]
# Tue, 09 Dec 2025 00:12:31 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 09 Dec 2025 00:12:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf35cfc495ac6ff70615ca926f57eb6f3961039055b8e0bc78d371b81d66cdcc`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a773213be6f84f3b269baecb1e4cc68f15241c5c383b48b907976c4eb946677`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 7.4 MB (7398139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d5b33ae2cd1bbd5548a76327f0d452ff6f8ba5339ec9c241cbd71a9f453f10`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 372.1 KB (372110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec7e4611c56c4658d750fa9a9cfa1506d45b7d5ad3a68ff8bd891309614c227`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 76.5 KB (76496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fb144940d3c8de5b68011f7c579283d7e04801dd5de76eb64f57bfa89926d3`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e990b9456e92e62ad8b10a958d9038d178a054f7af24c13a64841bba8bc484fe`  
		Last Modified: Tue, 09 Dec 2025 00:13:09 GMT  
		Size: 104.0 MB (104028693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de0c37a96fc881df0e067b4af3e9225be9f50b23eb987ee9b2b6bf242797f41`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845f1a6ee7ce778b2591bbfcde5ad849f34d69c6549c658cfab4f83234163c29`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ab7d725557e60a9b08e9efe0c6be7f3c6a76862af340465be69f3142fe7fd9`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324d82d39cdac56ca6ab5048a5efec1f0303825b13de2695e0014941f79017a2`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:0c524c076ae68a0db10ef651ba126d5920fb123c6c7e6231b335c5b1153dd8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8210e9735ca6eef17803a45249133dedbb0fd46a7f39421c806f22e8329ecff3`

```dockerfile
```

-	Layers:
	-	`sha256:b31d81caa581677e3119d98b84d301af6dff06dc539097e3313a88ee79d4513f`  
		Last Modified: Tue, 09 Dec 2025 02:33:47 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0a65d403bfce6cbe8353b601006c63d5ec489b6ecd9989117ad8bc072515784`  
		Last Modified: Tue, 09 Dec 2025 02:33:48 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:611564b0bee06eddda80a5a2c412b262065a12a9305d09b60ed0b5a3c61fe34e
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
$ docker pull couchdb@sha256:89743ee7151b366d6b28891c88f05210539626294c3321c7345d2efd0e90baae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb0753316d72cc07f4f3abbacfdc4ac02d3c7f4ecd6c71fd7c837e33285365f`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:08:07 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 08 Dec 2025 23:08:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:08:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:08:28 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:28 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:08:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 08 Dec 2025 23:08:34 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 08 Dec 2025 23:08:34 GMT
VOLUME [/opt/nouveau/data]
# Mon, 08 Dec 2025 23:08:34 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 08 Dec 2025 23:08:34 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10769f6e3ca05b0d30f4148aa16e7c13217c6a625a803ea087ee5804768ab4a9`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0703e44e2d7cafd694d8589161e1f5636f76a9b3d970195a5db2aa4b2406a2`  
		Last Modified: Mon, 08 Dec 2025 23:09:01 GMT  
		Size: 7.9 MB (7881795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d787b4bdf36bea424e37ecda03ad1f3ea9805c39521e250c7d97b554b8cd29a3`  
		Last Modified: Mon, 08 Dec 2025 23:09:07 GMT  
		Size: 77.4 MB (77380734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1380eab6cfd83025c297d8099e1247247d56bf95db84862a76d1a5becb1d35f`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 424.1 KB (424123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daf5d2841e907f58723ac0ae3c6fc6078ec51ae8600573953ff5e97445202ad`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 99.5 KB (99518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6cb9bf85b66a1cc208c72599a77b2136ea9d83b7646638973352fec03986fb`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c573270414f2f71a211e02c3a9aacdcc054f37201a785bd7b76d105e0f142c1`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 42.4 MB (42436360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfe2f3d09ee37fa7d61d8b5bc8348ab29b5fbcd32c65e3a0814f1387c4cf010`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:2e4168227791331cacb1f46381af60e5517e8a49edc38ed67a04d517236fed73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f852f63f06fb6a6280ac9e16c490f7f1d4c953810bcd05e1e15444a2153c2e`

```dockerfile
```

-	Layers:
	-	`sha256:1e1592694180e85e28f9f9b10cca96e33f11889b75314b91185faceba2b0a0f1`  
		Last Modified: Mon, 08 Dec 2025 23:34:26 GMT  
		Size: 3.7 MB (3658053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178217fabee2aa3c6d311ebede57eca5ce36fbe5975f4a8d599ad046659d337b`  
		Last Modified: Mon, 08 Dec 2025 23:34:26 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:544fd2610735f66997f2dc3ea47343f29126794307217fdab34cc896292886fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53dda8263a1e2cced1df9591e99bf4e8de27559768d24d1a53dcdf6a6bcf9fc`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:33:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 03:33:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Nov 2025 03:33:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:33:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:33:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 03:33:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 03:34:00 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:34:00 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 03:34:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Nov 2025 03:34:06 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Nov 2025 03:34:06 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Nov 2025 03:34:06 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Nov 2025 03:34:06 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d170929f5122b754e9c3b75c81f5ccce945c639b120cf7fd9f04de497d3351`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d122aab947d7f0b37352ff25d869519635be1a0e7861aea35a7607930d7048`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 7.7 MB (7692053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2712de1723319370a513b2ce6b80dfe68316e938066ef53bd751fb7913363595`  
		Last Modified: Tue, 18 Nov 2025 03:34:37 GMT  
		Size: 76.7 MB (76691571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccbab553627aa3a0f31a1a13d6435b96fa20c948bb8f0a06acd9ce3af5ee46c`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 392.7 KB (392661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4afbad864dfc76385d9a0180412ac0f75762270e3310fb788e9fd11f3b4c72`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 99.4 KB (99437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5123d1a7c8c978a9b8d8ea941fa30415dee531acb7551c51886b2c3eb5403a1`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0409338ca2ef2307306a8c6ce9d0553d3e006645a788373fa0b84faac326d9a`  
		Last Modified: Tue, 18 Nov 2025 03:34:36 GMT  
		Size: 42.3 MB (42339007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3341e7b0042637cf21bf2c7c5d35faa8cf23612d5f81cf113f113d3a1cf06fe1`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7fb5776f8220586ddd041b8b27727ad9eb417b5ae49c98b78444d6d0ed4f4ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08692c5b65246b53c1db3b39b2d49b3982af4f0b68425f674dad749cd5907123`

```dockerfile
```

-	Layers:
	-	`sha256:5b6483cab95ef058cfba5af9eedba8c2f72f1ebc0ee7a7359369b99d70242044`  
		Last Modified: Tue, 18 Nov 2025 05:34:42 GMT  
		Size: 3.7 MB (3656729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc566dff9630765cf5b25f3bb6027d91360ac02f2b43f545da39a7656afd750`  
		Last Modified: Tue, 18 Nov 2025 05:34:43 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:7c12e5c2d11a4e335bc8a826debcde85a8431afeb2d5ded342bc42c376eb1274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150085870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76459a52a9683cd87c99ca9180c3ada00aaf5d7d8038c9914d42a391453dea26`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:12:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Dec 2025 00:12:23 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 09 Dec 2025 00:12:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 09 Dec 2025 00:12:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 09 Dec 2025 00:12:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 09 Dec 2025 00:12:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 09 Dec 2025 00:12:52 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 09 Dec 2025 00:12:52 GMT
VOLUME [/opt/nouveau/data]
# Tue, 09 Dec 2025 00:12:52 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 09 Dec 2025 00:12:52 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c612ddb2613792ba5de7275ede737232c8919bcc9a90ad4dc4a90f42280a0c1`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe05b0e865a4ea871efebb32075b19d70f33e93973dbf638d5e901eacd7440b`  
		Last Modified: Tue, 09 Dec 2025 00:13:20 GMT  
		Size: 7.4 MB (7398109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a18a834e5966996b03bde3dcc826f2b0f461c9717c2a61a157c164bc0035d65`  
		Last Modified: Tue, 09 Dec 2025 00:13:26 GMT  
		Size: 73.1 MB (73142808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508bcd23c82e79bad82091e27743c8746f4b842f6e06556e20c6f6f34a1cf953`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 394.4 KB (394392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbf41a4ae36e10031fc97050f94fbb0ca20081067177751280bee84b46f9584`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 99.6 KB (99616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6092dee6efcbddddabba5653f407f3336d213fc568ad9c6706694ef1f9d439`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a684fa098de563675f00459f674e4c14b2b3edb8dbf71202bc5d7f45c816cd`  
		Last Modified: Tue, 09 Dec 2025 00:13:22 GMT  
		Size: 42.2 MB (42164639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d62053a9e778fc9ff6f26567bed49bc2cc11e771c13d99a53c5014a70c3a393`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:fafb2fb277c2d762056e9587dee834882ec7139cc3b0784d183c8b78e67d1ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e08fae2b3c9cf16c44563ea23595fa688447bc2544e2f2df04f047d64771c55`

```dockerfile
```

-	Layers:
	-	`sha256:c5809d637293d25977e1b07b589b7d0fd3dce59684371058f33db1b61ec2b506`  
		Last Modified: Tue, 09 Dec 2025 02:33:53 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2c29a59962a0f97410221034dec64942903f474ca029dc5e698be9544e54a0`  
		Last Modified: Tue, 09 Dec 2025 02:33:53 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1`

```console
$ docker pull couchdb@sha256:04c0634787a561546040c61186c89a2bdf268a10abad4a6b07d50473e27d5aa7
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
$ docker pull couchdb@sha256:21fa430aae63671a3127673e38de2e2d071f0d3dbc8a31d8fac62214afc8f59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142051235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3b5c0109cce05b5ad263097797085346efb950cc7f38578fcdbe681a392fd9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:07:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:07:51 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 08 Dec 2025 23:07:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:08:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:08:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:05 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 08 Dec 2025 23:08:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:08:18 GMT
VOLUME [/opt/couchdb/data]
# Mon, 08 Dec 2025 23:08:18 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 08 Dec 2025 23:08:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c9c88e767d5012a0e2dfc399f43404f8f4c3ab262bac734533e8204099be56`  
		Last Modified: Mon, 08 Dec 2025 23:08:40 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716c80c273f8809bbb548458f931e4762b0f447aeca7508e13c19b9c51ff73c0`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 7.9 MB (7881739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609e5bdfa7b1f8218d7dca07b7adde8b80150cda1d87f1f29da51c3a313db82e`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 401.7 KB (401735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d5a41c17903fc51342b98f1560b681035cfe0f7d321a36b50f34de4387824e`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 76.5 KB (76465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b62383183a15d775ce3c4f9430de03b79d6935279d541adfff250dcc8dd91c1`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd726490d7d051e52d86d74f97c293416c4886a83478fc5a2d5b044d81865fee`  
		Last Modified: Mon, 08 Dec 2025 23:08:50 GMT  
		Size: 105.5 MB (105457448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8856ade7c27a5fad19081cfe83a474d6898d1154adff0b08e6d87e98b5c3de45`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2897b671832f132cfb5b6f0c62ea6b5e8c6575868e3a4e361ac25df1f27e196c`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f82cbc9af1f4d32f1432c6cb4d15836c5891f1c431c9a75f8b08dfcd78e027a`  
		Last Modified: Mon, 08 Dec 2025 23:08:42 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b27282aaec507f7fcfa9a1efbb06f1abcd9cf46f8e39f236eb3c9a77a315e3`  
		Last Modified: Mon, 08 Dec 2025 23:08:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:aa6793cd8ef71d7ec06be94d34a9b693f27c315496b3d2778f2a2b406ffae798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087563041a4b7312487736498a1de80ea1d6f4ad2593c2b5efec7ae033626675`

```dockerfile
```

-	Layers:
	-	`sha256:e5384526458d9c66863e4dfe7e78e0b8c04ba19babd32f7e9d6cca6e9e683745`  
		Last Modified: Mon, 08 Dec 2025 23:34:23 GMT  
		Size: 4.2 MB (4184411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb9654333a4a6f0527c5d6d3686a1f350ad41a8b9d6ffa53b3e61c8d0be6a619`  
		Last Modified: Mon, 08 Dec 2025 23:34:24 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5f7127237ffae4f91803c563aca8cab6794b7407a996ff990c8c1b1c2ca53e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141404878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55007689149f254ad0f8f6bd9bf294b0b311c557f7ffb3e9c937f3eb5fc0ab81`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:32:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 03:32:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Nov 2025 03:32:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:32:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 03:32:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 03:32:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:32:44 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 18 Nov 2025 03:32:44 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:32:57 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Nov 2025 03:32:57 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Nov 2025 03:32:57 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1576797ad33df163e9df21eb3631e2cdab5607c35ac9d16b05797a9f0b4f4a62`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79357682a367c4944142ae7161c0dda87bafbfc1efe3ab937561ebdd5750291e`  
		Last Modified: Tue, 18 Nov 2025 03:33:21 GMT  
		Size: 7.7 MB (7692064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce499cb7fc066fc3f76ee116bcaf10c219f3d22ce0e194be90fa33ca7a616dd2`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 370.5 KB (370469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e456ad386d15df751348896749548e4fd781a2023d9b42644fbcc1c2d5d6d1`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 76.4 KB (76437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733cbbeb7fc213083912a6b6196dc4110d4058dfb0a20b6862b95f00d522b4df`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39cd99b3838668bbe1e6b0a1597d16cd159d847fc59fdce20eaab12c82c14b0`  
		Last Modified: Tue, 18 Nov 2025 03:33:30 GMT  
		Size: 105.2 MB (105158266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bbc9cf6f8919e4db1d162042a7f0bdb1899bb499ef0fd2aea33c34279a2de5`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a515d4096222e0e5d1fd051a7bb662d57e2bf1399c5fbe948e586acbd0b2826`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da500d6a31cb08f836c5e8e6b3dd8e6a2627aadd532f9f42b00bff559c48cf7c`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c13fb1a8fa5090d1c8664b8995b33a4d3e90897d58d870a44b4adebda1bd7c`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:fca47f92afd675f23c01b209db15ed17155a120f1d6ba7af7fbe1d109b1131d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9fe471488817a855aab9ca0c86e24330452ebe1a52a1c72441dcdc562b6c19`

```dockerfile
```

-	Layers:
	-	`sha256:e06f7cfcc9ba3ee4ae91e10ca855cd55994ebdb9a3d2538f260b8f486120dccb`  
		Last Modified: Tue, 18 Nov 2025 05:34:31 GMT  
		Size: 4.2 MB (4184704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:147c25b828a6992c4737d8171cf72964b820162b85c9cbcc55f5f7b95e01dbbb`  
		Last Modified: Tue, 18 Nov 2025 05:34:32 GMT  
		Size: 31.9 KB (31930 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; s390x

```console
$ docker pull couchdb@sha256:c9a410eba40de845f009bd7e7034f257568c0b2d032050720dc43d773ccbc6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d610f8d7a2c99fd1337112307b105aa162a3c7aa8f7523d2f5097f9b4d352cd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:12:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Dec 2025 00:12:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 09 Dec 2025 00:12:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 09 Dec 2025 00:12:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 09 Dec 2025 00:12:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:14 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 09 Dec 2025 00:12:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:12:31 GMT
VOLUME [/opt/couchdb/data]
# Tue, 09 Dec 2025 00:12:31 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 09 Dec 2025 00:12:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf35cfc495ac6ff70615ca926f57eb6f3961039055b8e0bc78d371b81d66cdcc`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a773213be6f84f3b269baecb1e4cc68f15241c5c383b48b907976c4eb946677`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 7.4 MB (7398139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d5b33ae2cd1bbd5548a76327f0d452ff6f8ba5339ec9c241cbd71a9f453f10`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 372.1 KB (372110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec7e4611c56c4658d750fa9a9cfa1506d45b7d5ad3a68ff8bd891309614c227`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 76.5 KB (76496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fb144940d3c8de5b68011f7c579283d7e04801dd5de76eb64f57bfa89926d3`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e990b9456e92e62ad8b10a958d9038d178a054f7af24c13a64841bba8bc484fe`  
		Last Modified: Tue, 09 Dec 2025 00:13:09 GMT  
		Size: 104.0 MB (104028693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de0c37a96fc881df0e067b4af3e9225be9f50b23eb987ee9b2b6bf242797f41`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845f1a6ee7ce778b2591bbfcde5ad849f34d69c6549c658cfab4f83234163c29`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ab7d725557e60a9b08e9efe0c6be7f3c6a76862af340465be69f3142fe7fd9`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324d82d39cdac56ca6ab5048a5efec1f0303825b13de2695e0014941f79017a2`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:0c524c076ae68a0db10ef651ba126d5920fb123c6c7e6231b335c5b1153dd8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8210e9735ca6eef17803a45249133dedbb0fd46a7f39421c806f22e8329ecff3`

```dockerfile
```

-	Layers:
	-	`sha256:b31d81caa581677e3119d98b84d301af6dff06dc539097e3313a88ee79d4513f`  
		Last Modified: Tue, 09 Dec 2025 02:33:47 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0a65d403bfce6cbe8353b601006c63d5ec489b6ecd9989117ad8bc072515784`  
		Last Modified: Tue, 09 Dec 2025 02:33:48 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1-nouveau`

```console
$ docker pull couchdb@sha256:611564b0bee06eddda80a5a2c412b262065a12a9305d09b60ed0b5a3c61fe34e
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
$ docker pull couchdb@sha256:89743ee7151b366d6b28891c88f05210539626294c3321c7345d2efd0e90baae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb0753316d72cc07f4f3abbacfdc4ac02d3c7f4ecd6c71fd7c837e33285365f`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:08:07 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 08 Dec 2025 23:08:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:08:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:08:28 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:28 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:08:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 08 Dec 2025 23:08:34 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 08 Dec 2025 23:08:34 GMT
VOLUME [/opt/nouveau/data]
# Mon, 08 Dec 2025 23:08:34 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 08 Dec 2025 23:08:34 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10769f6e3ca05b0d30f4148aa16e7c13217c6a625a803ea087ee5804768ab4a9`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0703e44e2d7cafd694d8589161e1f5636f76a9b3d970195a5db2aa4b2406a2`  
		Last Modified: Mon, 08 Dec 2025 23:09:01 GMT  
		Size: 7.9 MB (7881795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d787b4bdf36bea424e37ecda03ad1f3ea9805c39521e250c7d97b554b8cd29a3`  
		Last Modified: Mon, 08 Dec 2025 23:09:07 GMT  
		Size: 77.4 MB (77380734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1380eab6cfd83025c297d8099e1247247d56bf95db84862a76d1a5becb1d35f`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 424.1 KB (424123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daf5d2841e907f58723ac0ae3c6fc6078ec51ae8600573953ff5e97445202ad`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 99.5 KB (99518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6cb9bf85b66a1cc208c72599a77b2136ea9d83b7646638973352fec03986fb`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c573270414f2f71a211e02c3a9aacdcc054f37201a785bd7b76d105e0f142c1`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 42.4 MB (42436360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfe2f3d09ee37fa7d61d8b5bc8348ab29b5fbcd32c65e3a0814f1387c4cf010`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:2e4168227791331cacb1f46381af60e5517e8a49edc38ed67a04d517236fed73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f852f63f06fb6a6280ac9e16c490f7f1d4c953810bcd05e1e15444a2153c2e`

```dockerfile
```

-	Layers:
	-	`sha256:1e1592694180e85e28f9f9b10cca96e33f11889b75314b91185faceba2b0a0f1`  
		Last Modified: Mon, 08 Dec 2025 23:34:26 GMT  
		Size: 3.7 MB (3658053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178217fabee2aa3c6d311ebede57eca5ce36fbe5975f4a8d599ad046659d337b`  
		Last Modified: Mon, 08 Dec 2025 23:34:26 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:544fd2610735f66997f2dc3ea47343f29126794307217fdab34cc896292886fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53dda8263a1e2cced1df9591e99bf4e8de27559768d24d1a53dcdf6a6bcf9fc`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:33:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 03:33:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Nov 2025 03:33:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:33:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:33:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 03:33:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 03:34:00 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:34:00 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 03:34:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Nov 2025 03:34:06 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Nov 2025 03:34:06 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Nov 2025 03:34:06 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Nov 2025 03:34:06 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d170929f5122b754e9c3b75c81f5ccce945c639b120cf7fd9f04de497d3351`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d122aab947d7f0b37352ff25d869519635be1a0e7861aea35a7607930d7048`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 7.7 MB (7692053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2712de1723319370a513b2ce6b80dfe68316e938066ef53bd751fb7913363595`  
		Last Modified: Tue, 18 Nov 2025 03:34:37 GMT  
		Size: 76.7 MB (76691571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccbab553627aa3a0f31a1a13d6435b96fa20c948bb8f0a06acd9ce3af5ee46c`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 392.7 KB (392661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4afbad864dfc76385d9a0180412ac0f75762270e3310fb788e9fd11f3b4c72`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 99.4 KB (99437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5123d1a7c8c978a9b8d8ea941fa30415dee531acb7551c51886b2c3eb5403a1`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0409338ca2ef2307306a8c6ce9d0553d3e006645a788373fa0b84faac326d9a`  
		Last Modified: Tue, 18 Nov 2025 03:34:36 GMT  
		Size: 42.3 MB (42339007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3341e7b0042637cf21bf2c7c5d35faa8cf23612d5f81cf113f113d3a1cf06fe1`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7fb5776f8220586ddd041b8b27727ad9eb417b5ae49c98b78444d6d0ed4f4ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08692c5b65246b53c1db3b39b2d49b3982af4f0b68425f674dad749cd5907123`

```dockerfile
```

-	Layers:
	-	`sha256:5b6483cab95ef058cfba5af9eedba8c2f72f1ebc0ee7a7359369b99d70242044`  
		Last Modified: Tue, 18 Nov 2025 05:34:42 GMT  
		Size: 3.7 MB (3656729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc566dff9630765cf5b25f3bb6027d91360ac02f2b43f545da39a7656afd750`  
		Last Modified: Tue, 18 Nov 2025 05:34:43 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:7c12e5c2d11a4e335bc8a826debcde85a8431afeb2d5ded342bc42c376eb1274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150085870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76459a52a9683cd87c99ca9180c3ada00aaf5d7d8038c9914d42a391453dea26`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:12:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Dec 2025 00:12:23 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 09 Dec 2025 00:12:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 09 Dec 2025 00:12:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 09 Dec 2025 00:12:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 09 Dec 2025 00:12:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 09 Dec 2025 00:12:52 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 09 Dec 2025 00:12:52 GMT
VOLUME [/opt/nouveau/data]
# Tue, 09 Dec 2025 00:12:52 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 09 Dec 2025 00:12:52 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c612ddb2613792ba5de7275ede737232c8919bcc9a90ad4dc4a90f42280a0c1`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe05b0e865a4ea871efebb32075b19d70f33e93973dbf638d5e901eacd7440b`  
		Last Modified: Tue, 09 Dec 2025 00:13:20 GMT  
		Size: 7.4 MB (7398109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a18a834e5966996b03bde3dcc826f2b0f461c9717c2a61a157c164bc0035d65`  
		Last Modified: Tue, 09 Dec 2025 00:13:26 GMT  
		Size: 73.1 MB (73142808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508bcd23c82e79bad82091e27743c8746f4b842f6e06556e20c6f6f34a1cf953`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 394.4 KB (394392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbf41a4ae36e10031fc97050f94fbb0ca20081067177751280bee84b46f9584`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 99.6 KB (99616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6092dee6efcbddddabba5653f407f3336d213fc568ad9c6706694ef1f9d439`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a684fa098de563675f00459f674e4c14b2b3edb8dbf71202bc5d7f45c816cd`  
		Last Modified: Tue, 09 Dec 2025 00:13:22 GMT  
		Size: 42.2 MB (42164639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d62053a9e778fc9ff6f26567bed49bc2cc11e771c13d99a53c5014a70c3a393`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:fafb2fb277c2d762056e9587dee834882ec7139cc3b0784d183c8b78e67d1ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e08fae2b3c9cf16c44563ea23595fa688447bc2544e2f2df04f047d64771c55`

```dockerfile
```

-	Layers:
	-	`sha256:c5809d637293d25977e1b07b589b7d0fd3dce59684371058f33db1b61ec2b506`  
		Last Modified: Tue, 09 Dec 2025 02:33:53 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2c29a59962a0f97410221034dec64942903f474ca029dc5e698be9544e54a0`  
		Last Modified: Tue, 09 Dec 2025 02:33:53 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:04c0634787a561546040c61186c89a2bdf268a10abad4a6b07d50473e27d5aa7
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
$ docker pull couchdb@sha256:21fa430aae63671a3127673e38de2e2d071f0d3dbc8a31d8fac62214afc8f59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142051235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3b5c0109cce05b5ad263097797085346efb950cc7f38578fcdbe681a392fd9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:07:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:07:51 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 08 Dec 2025 23:07:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:08:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:08:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:05 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 08 Dec 2025 23:08:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:08:18 GMT
VOLUME [/opt/couchdb/data]
# Mon, 08 Dec 2025 23:08:18 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 08 Dec 2025 23:08:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c9c88e767d5012a0e2dfc399f43404f8f4c3ab262bac734533e8204099be56`  
		Last Modified: Mon, 08 Dec 2025 23:08:40 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716c80c273f8809bbb548458f931e4762b0f447aeca7508e13c19b9c51ff73c0`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 7.9 MB (7881739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609e5bdfa7b1f8218d7dca07b7adde8b80150cda1d87f1f29da51c3a313db82e`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 401.7 KB (401735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d5a41c17903fc51342b98f1560b681035cfe0f7d321a36b50f34de4387824e`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 76.5 KB (76465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b62383183a15d775ce3c4f9430de03b79d6935279d541adfff250dcc8dd91c1`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd726490d7d051e52d86d74f97c293416c4886a83478fc5a2d5b044d81865fee`  
		Last Modified: Mon, 08 Dec 2025 23:08:50 GMT  
		Size: 105.5 MB (105457448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8856ade7c27a5fad19081cfe83a474d6898d1154adff0b08e6d87e98b5c3de45`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2897b671832f132cfb5b6f0c62ea6b5e8c6575868e3a4e361ac25df1f27e196c`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f82cbc9af1f4d32f1432c6cb4d15836c5891f1c431c9a75f8b08dfcd78e027a`  
		Last Modified: Mon, 08 Dec 2025 23:08:42 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b27282aaec507f7fcfa9a1efbb06f1abcd9cf46f8e39f236eb3c9a77a315e3`  
		Last Modified: Mon, 08 Dec 2025 23:08:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:aa6793cd8ef71d7ec06be94d34a9b693f27c315496b3d2778f2a2b406ffae798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087563041a4b7312487736498a1de80ea1d6f4ad2593c2b5efec7ae033626675`

```dockerfile
```

-	Layers:
	-	`sha256:e5384526458d9c66863e4dfe7e78e0b8c04ba19babd32f7e9d6cca6e9e683745`  
		Last Modified: Mon, 08 Dec 2025 23:34:23 GMT  
		Size: 4.2 MB (4184411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb9654333a4a6f0527c5d6d3686a1f350ad41a8b9d6ffa53b3e61c8d0be6a619`  
		Last Modified: Mon, 08 Dec 2025 23:34:24 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5f7127237ffae4f91803c563aca8cab6794b7407a996ff990c8c1b1c2ca53e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141404878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55007689149f254ad0f8f6bd9bf294b0b311c557f7ffb3e9c937f3eb5fc0ab81`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:32:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 03:32:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Nov 2025 03:32:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:32:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 03:32:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 03:32:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:32:44 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 18 Nov 2025 03:32:44 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 03:32:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:32:57 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Nov 2025 03:32:57 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Nov 2025 03:32:57 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1576797ad33df163e9df21eb3631e2cdab5607c35ac9d16b05797a9f0b4f4a62`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79357682a367c4944142ae7161c0dda87bafbfc1efe3ab937561ebdd5750291e`  
		Last Modified: Tue, 18 Nov 2025 03:33:21 GMT  
		Size: 7.7 MB (7692064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce499cb7fc066fc3f76ee116bcaf10c219f3d22ce0e194be90fa33ca7a616dd2`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 370.5 KB (370469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e456ad386d15df751348896749548e4fd781a2023d9b42644fbcc1c2d5d6d1`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 76.4 KB (76437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733cbbeb7fc213083912a6b6196dc4110d4058dfb0a20b6862b95f00d522b4df`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39cd99b3838668bbe1e6b0a1597d16cd159d847fc59fdce20eaab12c82c14b0`  
		Last Modified: Tue, 18 Nov 2025 03:33:30 GMT  
		Size: 105.2 MB (105158266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bbc9cf6f8919e4db1d162042a7f0bdb1899bb499ef0fd2aea33c34279a2de5`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a515d4096222e0e5d1fd051a7bb662d57e2bf1399c5fbe948e586acbd0b2826`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da500d6a31cb08f836c5e8e6b3dd8e6a2627aadd532f9f42b00bff559c48cf7c`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c13fb1a8fa5090d1c8664b8995b33a4d3e90897d58d870a44b4adebda1bd7c`  
		Last Modified: Tue, 18 Nov 2025 03:33:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:fca47f92afd675f23c01b209db15ed17155a120f1d6ba7af7fbe1d109b1131d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9fe471488817a855aab9ca0c86e24330452ebe1a52a1c72441dcdc562b6c19`

```dockerfile
```

-	Layers:
	-	`sha256:e06f7cfcc9ba3ee4ae91e10ca855cd55994ebdb9a3d2538f260b8f486120dccb`  
		Last Modified: Tue, 18 Nov 2025 05:34:31 GMT  
		Size: 4.2 MB (4184704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:147c25b828a6992c4737d8171cf72964b820162b85c9cbcc55f5f7b95e01dbbb`  
		Last Modified: Tue, 18 Nov 2025 05:34:32 GMT  
		Size: 31.9 KB (31930 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:c9a410eba40de845f009bd7e7034f257568c0b2d032050720dc43d773ccbc6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d610f8d7a2c99fd1337112307b105aa162a3c7aa8f7523d2f5097f9b4d352cd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:12:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Dec 2025 00:12:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 09 Dec 2025 00:12:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 09 Dec 2025 00:12:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 09 Dec 2025 00:12:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:14 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 09 Dec 2025 00:12:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:12:31 GMT
VOLUME [/opt/couchdb/data]
# Tue, 09 Dec 2025 00:12:31 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 09 Dec 2025 00:12:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf35cfc495ac6ff70615ca926f57eb6f3961039055b8e0bc78d371b81d66cdcc`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a773213be6f84f3b269baecb1e4cc68f15241c5c383b48b907976c4eb946677`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 7.4 MB (7398139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d5b33ae2cd1bbd5548a76327f0d452ff6f8ba5339ec9c241cbd71a9f453f10`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 372.1 KB (372110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec7e4611c56c4658d750fa9a9cfa1506d45b7d5ad3a68ff8bd891309614c227`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 76.5 KB (76496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fb144940d3c8de5b68011f7c579283d7e04801dd5de76eb64f57bfa89926d3`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e990b9456e92e62ad8b10a958d9038d178a054f7af24c13a64841bba8bc484fe`  
		Last Modified: Tue, 09 Dec 2025 00:13:09 GMT  
		Size: 104.0 MB (104028693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de0c37a96fc881df0e067b4af3e9225be9f50b23eb987ee9b2b6bf242797f41`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845f1a6ee7ce778b2591bbfcde5ad849f34d69c6549c658cfab4f83234163c29`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ab7d725557e60a9b08e9efe0c6be7f3c6a76862af340465be69f3142fe7fd9`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324d82d39cdac56ca6ab5048a5efec1f0303825b13de2695e0014941f79017a2`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:0c524c076ae68a0db10ef651ba126d5920fb123c6c7e6231b335c5b1153dd8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8210e9735ca6eef17803a45249133dedbb0fd46a7f39421c806f22e8329ecff3`

```dockerfile
```

-	Layers:
	-	`sha256:b31d81caa581677e3119d98b84d301af6dff06dc539097e3313a88ee79d4513f`  
		Last Modified: Tue, 09 Dec 2025 02:33:47 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0a65d403bfce6cbe8353b601006c63d5ec489b6ecd9989117ad8bc072515784`  
		Last Modified: Tue, 09 Dec 2025 02:33:48 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json
