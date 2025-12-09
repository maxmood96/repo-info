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
$ docker pull couchdb@sha256:979671a0e5ca8b8700b954c5cb602c85d3060dcd5f1f9bc4bc890fb66702b6d6
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
$ docker pull couchdb@sha256:75ada75abb92681c395e8f4167b308909290c4fb26f0323616d36387bce7bab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138764853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dce8d4eaaa998757f14ce4c6b32f6e50a1f6511e35513edb3ef04b12d098eb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:06:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 04:06:26 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Nov 2025 04:06:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 04:06:35 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 04:06:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:06:39 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 18 Nov 2025 04:06:39 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:06:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Nov 2025 04:06:56 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Nov 2025 04:06:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c697228032ca02a0caaa4f4add3225ee449f1f25a2160b49abf37fcfd510b822`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af41536559239b6a3e4d2436a9e9dc36226ff8021b52c3db5e02ab33c7758ea6`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 7.4 MB (7398082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb3826996122228cee174dc0bb7ac7e7f64a62027d6b2dcb374adc50d08d085`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 372.1 KB (372109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72a2f3bd584dacf20be452f9eae9845aa4294c738cf6db4a40d88427dc1b308`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 76.5 KB (76517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186e1666c4ab29c6d36e98fdbaa97d622cc9e48ef35bf17c3ba06825e00b574e`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc4889f7e2df67455952b41c36ca299a5bf2d6a226836d6d0a9bf53ed80ccc7`  
		Last Modified: Tue, 18 Nov 2025 04:07:34 GMT  
		Size: 104.0 MB (104028328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3274038af5d95859fdf25989f0fd9524a45fb1a2f0cc1fda762fd5f5256e68d6`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33c4e8d23ccdc79f2d869c87aa35cf397d7c0cd592dfacc137e7b155b3cdba8`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584886fc763992aa0636dac1eb7fe5413ea822630f064ab3322d44aa175574df`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4de580aabdabd943d9c997e193f69bff695cbc5717278e4df22dc5fb88f51c3`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:09958c2baf31ac6d8089fe9bce53d52a08dba1b9ed08723ece784b00ea14c7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0706effaee2f10eb06db73814d4ae51fcd6153f48cc92367e7499a3bd0617276`

```dockerfile
```

-	Layers:
	-	`sha256:77f980d289de80d9fa70030da79e6852c465474a2a2c4ec86c9f3a1219cd484e`  
		Last Modified: Tue, 18 Nov 2025 05:34:37 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccfcb618e6ad781845a60d27ed302fef9e457926b372bcb95b63721a38df6a4`  
		Last Modified: Tue, 18 Nov 2025 05:34:37 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:3128745752000c2e150e7810133026b61c6dc56ece7766faebc3aa4315e3935b
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
$ docker pull couchdb@sha256:6d105ae4c3cfb487453dc42ebb84bca2d760070072cd8b8ba81a7f2c31a0dadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150086141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb4ce24ab1a4f47af64aee459172c19dc5667f1c122869b8bbc9af97e1a28a0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:07:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 04:07:23 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Nov 2025 04:07:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 04:07:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 04:07:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Nov 2025 04:07:52 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Nov 2025 04:07:52 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2e87e61b486b2674141864f4363d98ded26c8f54e991336ad1d12e326c3a16`  
		Last Modified: Tue, 18 Nov 2025 04:08:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31b605a2e7b31da747e5753f0ddab47bf42a62e40cee69c1047dc0c2d30f6b1`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 7.4 MB (7398114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d58478a99282a2368ea67171ded7641e1b0038caa802b2fe1670fb2deb9f8d`  
		Last Modified: Tue, 18 Nov 2025 04:08:30 GMT  
		Size: 73.1 MB (73143056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f06a849564a0186d5596762b9c12ee8747f037baef6d3e1ba2c83a743389eb0`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 394.4 KB (394411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a0e427d83599ac4b811cfd58210ecdb8178a62036d472729b26fc7d415de53`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 99.6 KB (99624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9210fddd0e0bc63c40f7d261245d3fbd05b4d939788283eb1d1a8daa30f9785d`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d59dccc95cb6f79dba3e6eb7001aedb61689abf7d6a7615729fad6451968d2`  
		Last Modified: Tue, 18 Nov 2025 04:08:25 GMT  
		Size: 42.2 MB (42164660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2e79e6b7ddf0949aaf0d3c54dcebc276d1c2bf91c6cd77d8b0a437ebe5ffc4`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:65e9e7614841fe27093ee627cfd01d6cc4373d76d7d6ee532430ce5c714310cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889ef69b339c0e8c0d511f4836014ae41b4de63f97c676e2e651ea26f39787e6`

```dockerfile
```

-	Layers:
	-	`sha256:949aba49bddf11115bacb751c3bd35f64dd18029e6a267d5bbdffd283f33afd6`  
		Last Modified: Tue, 18 Nov 2025 05:34:46 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c6e59512c24b1e04b0c745da36168da8df9ae6ba95ba224c9ebd714bafbffa0`  
		Last Modified: Tue, 18 Nov 2025 05:34:47 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:c937f6794767270f522f6db3e1debc58d762e8bb7ae512360dd9b5b964e85f4b
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
$ docker pull couchdb@sha256:09dee9d5715f81d3021408dde28b5f976a131bc73a239441465689339c616976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135792909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e04d87f5af4d99fc8513ab9448541760bcdddee17b336dbe81ad0d18a69477`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:07:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 04:07:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Nov 2025 04:07:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 04:07:31 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 04:07:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:36 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Nov 2025 04:07:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 04:07:51 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Nov 2025 04:07:51 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Nov 2025 04:07:51 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Nov 2025 04:07:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Nov 2025 04:07:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 04:07:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:07:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Nov 2025 04:07:51 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Nov 2025 04:07:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5ec0b5de516d100d84500f37f0ba167e00853f5eafd57daab361f2d7b6037b`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a680bd909664622c1abf9e1ad74db577b5fe75275e5a9fa5c8dbe42e69d7f91`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 7.4 MB (7398107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c868a84cf8d870354569057e49223a0da12a537f28320a5b679497d287e02017`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 372.1 KB (372099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fb6d295012c12abae2c4c66f02c92759924cb2bd1bf52e811e58787549e200`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 76.5 KB (76486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4031bbf3d52cc5297383bb361573f3a8b6761e14523755039c0a0bfb1343ae1e`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3211ffe814d01e6208fe37e970d20eccc5d19167217c5d177b388e2274f2a90`  
		Last Modified: Tue, 18 Nov 2025 04:08:29 GMT  
		Size: 101.1 MB (101056399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321f74709b35d8f3d5c252701b381c9338e6bba1d833e7a30a78440b3ae0954a`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae07e7c469cd12079197cc8b32f4f7d48a1dbc160ea91dbe638ac3e87299bfb5`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c5257aae19934c975df8e7313243a956b5abc10b326451387c9f944cdf5d38`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdb6a86e8ac75ea51fe4e514e6041924dcf100b5acff507d570e505ab49df43`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:f5afee39925a39af1a3c6c5e7b6ea2a16ea3d38b9b792aece8ffbdfbb6056031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ee031334b89845dd5bcfdd9a4dbd4bfb72c757fb67aeab63fe4f6961ad18cb`

```dockerfile
```

-	Layers:
	-	`sha256:368066a18a33faf02a8effa62d18d678f24ceafefe3b13d14d75cdc307bc51fb`  
		Last Modified: Tue, 18 Nov 2025 05:34:55 GMT  
		Size: 4.1 MB (4121581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a48d9bf4660f3b0e1ad01cc5acc4868184de368b35ffe334901b42964c88458d`  
		Last Modified: Tue, 18 Nov 2025 05:34:56 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:c6e721b1b406ce6e344c3cf5055adaa8244d02e6f6dbf1fc0c72de93503e4522
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
$ docker pull couchdb@sha256:65ed756bbba7ec876c14c37f1c50e68fb59072ca9c677221c59941a4c5ae700c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150084189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d85e7a54a8419e9ffc3529b842914a65f871dd871be48ac70020c5d27dbdb4`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:07:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 04:07:37 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Nov 2025 04:07:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 04:07:56 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:56 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 04:08:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Nov 2025 04:08:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Nov 2025 04:08:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Nov 2025 04:08:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Nov 2025 04:08:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4556ec8d4568ad8c355385978ae2a28adc8ed9208426e3c922a49b674d04c2bc`  
		Last Modified: Tue, 18 Nov 2025 04:08:34 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04b233a7dded2e1a95e0b520607136bfb1f15b85d74b8c9a5af6210937d4d88`  
		Last Modified: Tue, 18 Nov 2025 04:08:35 GMT  
		Size: 7.4 MB (7398056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11339ca7d68166534a604a19379c38ae7267e01fe266194daae3fb00641bfae`  
		Last Modified: Tue, 18 Nov 2025 04:08:44 GMT  
		Size: 73.1 MB (73142948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803da9afe463668337fa4eedae506235ca5e48e37e6aafd0996824d642eaaf5b`  
		Last Modified: Tue, 18 Nov 2025 04:08:34 GMT  
		Size: 394.4 KB (394398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84698facd73a4c733d30b5108920d36bfea6417d9f32336f1034f7aed126364`  
		Last Modified: Tue, 18 Nov 2025 04:08:34 GMT  
		Size: 99.6 KB (99615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810611a4d3c5703a2b1cb57c0bd7fdfe2573180dbb05e8cfb2c3fcb96bd0c819`  
		Last Modified: Tue, 18 Nov 2025 04:08:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83baa034868a988011b2df92e15016ba0b4ace500f6b0af4ef5c90c5209cf0fb`  
		Last Modified: Tue, 18 Nov 2025 04:08:59 GMT  
		Size: 42.2 MB (42162900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5980aa99b7f43c37f0b70989ff4b4ad64131b0ca9805c93fd206c8ecd345f0ad`  
		Last Modified: Tue, 18 Nov 2025 04:08:34 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:13a7a30cd41ea87ff507c74d9a4b0e2ee0d1cb1dd0080e92e03ff05cd8fc7390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0aead4b471b7c6790627870770ecba46aebf9540de650d038ef5cc0f2971e0c`

```dockerfile
```

-	Layers:
	-	`sha256:19c4cfe1011d6b6d4169f047fefb33d86d28cd8615bd4266de476c38bfb707b5`  
		Last Modified: Tue, 18 Nov 2025 05:35:05 GMT  
		Size: 3.6 MB (3648276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e6bbd17b7da4d840c7bf89cd613f45143fcc5af2dcd5490381c08417c864c37`  
		Last Modified: Tue, 18 Nov 2025 05:35:06 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:c937f6794767270f522f6db3e1debc58d762e8bb7ae512360dd9b5b964e85f4b
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
$ docker pull couchdb@sha256:09dee9d5715f81d3021408dde28b5f976a131bc73a239441465689339c616976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135792909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e04d87f5af4d99fc8513ab9448541760bcdddee17b336dbe81ad0d18a69477`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:07:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 04:07:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Nov 2025 04:07:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 04:07:31 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 04:07:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:36 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Nov 2025 04:07:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 04:07:51 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Nov 2025 04:07:51 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Nov 2025 04:07:51 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Nov 2025 04:07:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Nov 2025 04:07:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 04:07:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:07:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Nov 2025 04:07:51 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Nov 2025 04:07:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5ec0b5de516d100d84500f37f0ba167e00853f5eafd57daab361f2d7b6037b`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a680bd909664622c1abf9e1ad74db577b5fe75275e5a9fa5c8dbe42e69d7f91`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 7.4 MB (7398107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c868a84cf8d870354569057e49223a0da12a537f28320a5b679497d287e02017`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 372.1 KB (372099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fb6d295012c12abae2c4c66f02c92759924cb2bd1bf52e811e58787549e200`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 76.5 KB (76486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4031bbf3d52cc5297383bb361573f3a8b6761e14523755039c0a0bfb1343ae1e`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3211ffe814d01e6208fe37e970d20eccc5d19167217c5d177b388e2274f2a90`  
		Last Modified: Tue, 18 Nov 2025 04:08:29 GMT  
		Size: 101.1 MB (101056399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321f74709b35d8f3d5c252701b381c9338e6bba1d833e7a30a78440b3ae0954a`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae07e7c469cd12079197cc8b32f4f7d48a1dbc160ea91dbe638ac3e87299bfb5`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c5257aae19934c975df8e7313243a956b5abc10b326451387c9f944cdf5d38`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdb6a86e8ac75ea51fe4e514e6041924dcf100b5acff507d570e505ab49df43`  
		Last Modified: Tue, 18 Nov 2025 04:08:20 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f5afee39925a39af1a3c6c5e7b6ea2a16ea3d38b9b792aece8ffbdfbb6056031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ee031334b89845dd5bcfdd9a4dbd4bfb72c757fb67aeab63fe4f6961ad18cb`

```dockerfile
```

-	Layers:
	-	`sha256:368066a18a33faf02a8effa62d18d678f24ceafefe3b13d14d75cdc307bc51fb`  
		Last Modified: Tue, 18 Nov 2025 05:34:55 GMT  
		Size: 4.1 MB (4121581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a48d9bf4660f3b0e1ad01cc5acc4868184de368b35ffe334901b42964c88458d`  
		Last Modified: Tue, 18 Nov 2025 05:34:56 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:c6e721b1b406ce6e344c3cf5055adaa8244d02e6f6dbf1fc0c72de93503e4522
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
$ docker pull couchdb@sha256:65ed756bbba7ec876c14c37f1c50e68fb59072ca9c677221c59941a4c5ae700c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150084189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d85e7a54a8419e9ffc3529b842914a65f871dd871be48ac70020c5d27dbdb4`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:07:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 04:07:37 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Nov 2025 04:07:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 04:07:56 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:56 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 04:08:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Nov 2025 04:08:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Nov 2025 04:08:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Nov 2025 04:08:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Nov 2025 04:08:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4556ec8d4568ad8c355385978ae2a28adc8ed9208426e3c922a49b674d04c2bc`  
		Last Modified: Tue, 18 Nov 2025 04:08:34 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04b233a7dded2e1a95e0b520607136bfb1f15b85d74b8c9a5af6210937d4d88`  
		Last Modified: Tue, 18 Nov 2025 04:08:35 GMT  
		Size: 7.4 MB (7398056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11339ca7d68166534a604a19379c38ae7267e01fe266194daae3fb00641bfae`  
		Last Modified: Tue, 18 Nov 2025 04:08:44 GMT  
		Size: 73.1 MB (73142948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803da9afe463668337fa4eedae506235ca5e48e37e6aafd0996824d642eaaf5b`  
		Last Modified: Tue, 18 Nov 2025 04:08:34 GMT  
		Size: 394.4 KB (394398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84698facd73a4c733d30b5108920d36bfea6417d9f32336f1034f7aed126364`  
		Last Modified: Tue, 18 Nov 2025 04:08:34 GMT  
		Size: 99.6 KB (99615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810611a4d3c5703a2b1cb57c0bd7fdfe2573180dbb05e8cfb2c3fcb96bd0c819`  
		Last Modified: Tue, 18 Nov 2025 04:08:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83baa034868a988011b2df92e15016ba0b4ace500f6b0af4ef5c90c5209cf0fb`  
		Last Modified: Tue, 18 Nov 2025 04:08:59 GMT  
		Size: 42.2 MB (42162900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5980aa99b7f43c37f0b70989ff4b4ad64131b0ca9805c93fd206c8ecd345f0ad`  
		Last Modified: Tue, 18 Nov 2025 04:08:34 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:13a7a30cd41ea87ff507c74d9a4b0e2ee0d1cb1dd0080e92e03ff05cd8fc7390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0aead4b471b7c6790627870770ecba46aebf9540de650d038ef5cc0f2971e0c`

```dockerfile
```

-	Layers:
	-	`sha256:19c4cfe1011d6b6d4169f047fefb33d86d28cd8615bd4266de476c38bfb707b5`  
		Last Modified: Tue, 18 Nov 2025 05:35:05 GMT  
		Size: 3.6 MB (3648276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e6bbd17b7da4d840c7bf89cd613f45143fcc5af2dcd5490381c08417c864c37`  
		Last Modified: Tue, 18 Nov 2025 05:35:06 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:979671a0e5ca8b8700b954c5cb602c85d3060dcd5f1f9bc4bc890fb66702b6d6
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
$ docker pull couchdb@sha256:75ada75abb92681c395e8f4167b308909290c4fb26f0323616d36387bce7bab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138764853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dce8d4eaaa998757f14ce4c6b32f6e50a1f6511e35513edb3ef04b12d098eb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:06:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 04:06:26 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Nov 2025 04:06:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 04:06:35 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 04:06:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:06:39 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 18 Nov 2025 04:06:39 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:06:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Nov 2025 04:06:56 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Nov 2025 04:06:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c697228032ca02a0caaa4f4add3225ee449f1f25a2160b49abf37fcfd510b822`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af41536559239b6a3e4d2436a9e9dc36226ff8021b52c3db5e02ab33c7758ea6`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 7.4 MB (7398082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb3826996122228cee174dc0bb7ac7e7f64a62027d6b2dcb374adc50d08d085`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 372.1 KB (372109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72a2f3bd584dacf20be452f9eae9845aa4294c738cf6db4a40d88427dc1b308`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 76.5 KB (76517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186e1666c4ab29c6d36e98fdbaa97d622cc9e48ef35bf17c3ba06825e00b574e`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc4889f7e2df67455952b41c36ca299a5bf2d6a226836d6d0a9bf53ed80ccc7`  
		Last Modified: Tue, 18 Nov 2025 04:07:34 GMT  
		Size: 104.0 MB (104028328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3274038af5d95859fdf25989f0fd9524a45fb1a2f0cc1fda762fd5f5256e68d6`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33c4e8d23ccdc79f2d869c87aa35cf397d7c0cd592dfacc137e7b155b3cdba8`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584886fc763992aa0636dac1eb7fe5413ea822630f064ab3322d44aa175574df`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4de580aabdabd943d9c997e193f69bff695cbc5717278e4df22dc5fb88f51c3`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:09958c2baf31ac6d8089fe9bce53d52a08dba1b9ed08723ece784b00ea14c7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0706effaee2f10eb06db73814d4ae51fcd6153f48cc92367e7499a3bd0617276`

```dockerfile
```

-	Layers:
	-	`sha256:77f980d289de80d9fa70030da79e6852c465474a2a2c4ec86c9f3a1219cd484e`  
		Last Modified: Tue, 18 Nov 2025 05:34:37 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccfcb618e6ad781845a60d27ed302fef9e457926b372bcb95b63721a38df6a4`  
		Last Modified: Tue, 18 Nov 2025 05:34:37 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:3128745752000c2e150e7810133026b61c6dc56ece7766faebc3aa4315e3935b
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
$ docker pull couchdb@sha256:6d105ae4c3cfb487453dc42ebb84bca2d760070072cd8b8ba81a7f2c31a0dadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150086141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb4ce24ab1a4f47af64aee459172c19dc5667f1c122869b8bbc9af97e1a28a0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:07:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 04:07:23 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Nov 2025 04:07:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 04:07:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 04:07:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Nov 2025 04:07:52 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Nov 2025 04:07:52 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2e87e61b486b2674141864f4363d98ded26c8f54e991336ad1d12e326c3a16`  
		Last Modified: Tue, 18 Nov 2025 04:08:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31b605a2e7b31da747e5753f0ddab47bf42a62e40cee69c1047dc0c2d30f6b1`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 7.4 MB (7398114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d58478a99282a2368ea67171ded7641e1b0038caa802b2fe1670fb2deb9f8d`  
		Last Modified: Tue, 18 Nov 2025 04:08:30 GMT  
		Size: 73.1 MB (73143056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f06a849564a0186d5596762b9c12ee8747f037baef6d3e1ba2c83a743389eb0`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 394.4 KB (394411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a0e427d83599ac4b811cfd58210ecdb8178a62036d472729b26fc7d415de53`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 99.6 KB (99624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9210fddd0e0bc63c40f7d261245d3fbd05b4d939788283eb1d1a8daa30f9785d`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d59dccc95cb6f79dba3e6eb7001aedb61689abf7d6a7615729fad6451968d2`  
		Last Modified: Tue, 18 Nov 2025 04:08:25 GMT  
		Size: 42.2 MB (42164660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2e79e6b7ddf0949aaf0d3c54dcebc276d1c2bf91c6cd77d8b0a437ebe5ffc4`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:65e9e7614841fe27093ee627cfd01d6cc4373d76d7d6ee532430ce5c714310cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889ef69b339c0e8c0d511f4836014ae41b4de63f97c676e2e651ea26f39787e6`

```dockerfile
```

-	Layers:
	-	`sha256:949aba49bddf11115bacb751c3bd35f64dd18029e6a267d5bbdffd283f33afd6`  
		Last Modified: Tue, 18 Nov 2025 05:34:46 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c6e59512c24b1e04b0c745da36168da8df9ae6ba95ba224c9ebd714bafbffa0`  
		Last Modified: Tue, 18 Nov 2025 05:34:47 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1`

```console
$ docker pull couchdb@sha256:979671a0e5ca8b8700b954c5cb602c85d3060dcd5f1f9bc4bc890fb66702b6d6
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
$ docker pull couchdb@sha256:75ada75abb92681c395e8f4167b308909290c4fb26f0323616d36387bce7bab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138764853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dce8d4eaaa998757f14ce4c6b32f6e50a1f6511e35513edb3ef04b12d098eb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:06:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 04:06:26 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Nov 2025 04:06:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 04:06:35 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 04:06:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:06:39 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 18 Nov 2025 04:06:39 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:06:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Nov 2025 04:06:56 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Nov 2025 04:06:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c697228032ca02a0caaa4f4add3225ee449f1f25a2160b49abf37fcfd510b822`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af41536559239b6a3e4d2436a9e9dc36226ff8021b52c3db5e02ab33c7758ea6`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 7.4 MB (7398082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb3826996122228cee174dc0bb7ac7e7f64a62027d6b2dcb374adc50d08d085`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 372.1 KB (372109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72a2f3bd584dacf20be452f9eae9845aa4294c738cf6db4a40d88427dc1b308`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 76.5 KB (76517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186e1666c4ab29c6d36e98fdbaa97d622cc9e48ef35bf17c3ba06825e00b574e`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc4889f7e2df67455952b41c36ca299a5bf2d6a226836d6d0a9bf53ed80ccc7`  
		Last Modified: Tue, 18 Nov 2025 04:07:34 GMT  
		Size: 104.0 MB (104028328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3274038af5d95859fdf25989f0fd9524a45fb1a2f0cc1fda762fd5f5256e68d6`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33c4e8d23ccdc79f2d869c87aa35cf397d7c0cd592dfacc137e7b155b3cdba8`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584886fc763992aa0636dac1eb7fe5413ea822630f064ab3322d44aa175574df`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4de580aabdabd943d9c997e193f69bff695cbc5717278e4df22dc5fb88f51c3`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:09958c2baf31ac6d8089fe9bce53d52a08dba1b9ed08723ece784b00ea14c7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0706effaee2f10eb06db73814d4ae51fcd6153f48cc92367e7499a3bd0617276`

```dockerfile
```

-	Layers:
	-	`sha256:77f980d289de80d9fa70030da79e6852c465474a2a2c4ec86c9f3a1219cd484e`  
		Last Modified: Tue, 18 Nov 2025 05:34:37 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccfcb618e6ad781845a60d27ed302fef9e457926b372bcb95b63721a38df6a4`  
		Last Modified: Tue, 18 Nov 2025 05:34:37 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1-nouveau`

```console
$ docker pull couchdb@sha256:3128745752000c2e150e7810133026b61c6dc56ece7766faebc3aa4315e3935b
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
$ docker pull couchdb@sha256:6d105ae4c3cfb487453dc42ebb84bca2d760070072cd8b8ba81a7f2c31a0dadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150086141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb4ce24ab1a4f47af64aee459172c19dc5667f1c122869b8bbc9af97e1a28a0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:07:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 04:07:23 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Nov 2025 04:07:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 04:07:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 04:07:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Nov 2025 04:07:52 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Nov 2025 04:07:52 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2e87e61b486b2674141864f4363d98ded26c8f54e991336ad1d12e326c3a16`  
		Last Modified: Tue, 18 Nov 2025 04:08:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31b605a2e7b31da747e5753f0ddab47bf42a62e40cee69c1047dc0c2d30f6b1`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 7.4 MB (7398114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d58478a99282a2368ea67171ded7641e1b0038caa802b2fe1670fb2deb9f8d`  
		Last Modified: Tue, 18 Nov 2025 04:08:30 GMT  
		Size: 73.1 MB (73143056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f06a849564a0186d5596762b9c12ee8747f037baef6d3e1ba2c83a743389eb0`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 394.4 KB (394411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a0e427d83599ac4b811cfd58210ecdb8178a62036d472729b26fc7d415de53`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 99.6 KB (99624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9210fddd0e0bc63c40f7d261245d3fbd05b4d939788283eb1d1a8daa30f9785d`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d59dccc95cb6f79dba3e6eb7001aedb61689abf7d6a7615729fad6451968d2`  
		Last Modified: Tue, 18 Nov 2025 04:08:25 GMT  
		Size: 42.2 MB (42164660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2e79e6b7ddf0949aaf0d3c54dcebc276d1c2bf91c6cd77d8b0a437ebe5ffc4`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:65e9e7614841fe27093ee627cfd01d6cc4373d76d7d6ee532430ce5c714310cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889ef69b339c0e8c0d511f4836014ae41b4de63f97c676e2e651ea26f39787e6`

```dockerfile
```

-	Layers:
	-	`sha256:949aba49bddf11115bacb751c3bd35f64dd18029e6a267d5bbdffd283f33afd6`  
		Last Modified: Tue, 18 Nov 2025 05:34:46 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c6e59512c24b1e04b0c745da36168da8df9ae6ba95ba224c9ebd714bafbffa0`  
		Last Modified: Tue, 18 Nov 2025 05:34:47 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:979671a0e5ca8b8700b954c5cb602c85d3060dcd5f1f9bc4bc890fb66702b6d6
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
$ docker pull couchdb@sha256:75ada75abb92681c395e8f4167b308909290c4fb26f0323616d36387bce7bab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138764853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dce8d4eaaa998757f14ce4c6b32f6e50a1f6511e35513edb3ef04b12d098eb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:06:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 04:06:26 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Nov 2025 04:06:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 04:06:35 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 04:06:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:06:39 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 18 Nov 2025 04:06:39 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 04:06:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:06:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Nov 2025 04:06:56 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Nov 2025 04:06:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c697228032ca02a0caaa4f4add3225ee449f1f25a2160b49abf37fcfd510b822`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af41536559239b6a3e4d2436a9e9dc36226ff8021b52c3db5e02ab33c7758ea6`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 7.4 MB (7398082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb3826996122228cee174dc0bb7ac7e7f64a62027d6b2dcb374adc50d08d085`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 372.1 KB (372109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72a2f3bd584dacf20be452f9eae9845aa4294c738cf6db4a40d88427dc1b308`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 76.5 KB (76517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186e1666c4ab29c6d36e98fdbaa97d622cc9e48ef35bf17c3ba06825e00b574e`  
		Last Modified: Tue, 18 Nov 2025 04:07:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc4889f7e2df67455952b41c36ca299a5bf2d6a226836d6d0a9bf53ed80ccc7`  
		Last Modified: Tue, 18 Nov 2025 04:07:34 GMT  
		Size: 104.0 MB (104028328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3274038af5d95859fdf25989f0fd9524a45fb1a2f0cc1fda762fd5f5256e68d6`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33c4e8d23ccdc79f2d869c87aa35cf397d7c0cd592dfacc137e7b155b3cdba8`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584886fc763992aa0636dac1eb7fe5413ea822630f064ab3322d44aa175574df`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4de580aabdabd943d9c997e193f69bff695cbc5717278e4df22dc5fb88f51c3`  
		Last Modified: Tue, 18 Nov 2025 04:07:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:09958c2baf31ac6d8089fe9bce53d52a08dba1b9ed08723ece784b00ea14c7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0706effaee2f10eb06db73814d4ae51fcd6153f48cc92367e7499a3bd0617276`

```dockerfile
```

-	Layers:
	-	`sha256:77f980d289de80d9fa70030da79e6852c465474a2a2c4ec86c9f3a1219cd484e`  
		Last Modified: Tue, 18 Nov 2025 05:34:37 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccfcb618e6ad781845a60d27ed302fef9e457926b372bcb95b63721a38df6a4`  
		Last Modified: Tue, 18 Nov 2025 05:34:37 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json
