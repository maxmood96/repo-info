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
$ docker pull couchdb@sha256:d8bd3c3eb34c621096f4d2837be7f246128814f34ad0ada8a6280e71da8e2885
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
$ docker pull couchdb@sha256:b4f0b214477ea89489da9d4001cb8eac7d259e113b44603c57cfc94a3d008e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142049914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e493d383d26977710c0749ed769f8af1b2477b0298047b08eb44d409a1ba32`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:11:50 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:11:50 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 11 Nov 2025 20:11:56 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:11:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:12:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:03 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 11 Nov 2025 20:12:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 20:12:16 GMT
VOLUME [/opt/couchdb/data]
# Tue, 11 Nov 2025 20:12:16 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 11 Nov 2025 20:12:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d274f1c08381bf79eeb842fb97a61b254cfade7b44d978eaf71f4c639725ea4b`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0bb58d39055c8e5f9cd829ae5145f2d096176b6ee2cff83eba6156c3e07ff6`  
		Last Modified: Tue, 11 Nov 2025 20:12:45 GMT  
		Size: 7.9 MB (7881754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26343153c3ea04a23236a9d1583932b81c6438b6207cf64b4d5b3f53564cee93`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 401.7 KB (401726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b90245eeddcd781e96e60a2a8f6c3577ca5e847663d5214fd7814fa06e92f26`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 76.5 KB (76493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ba965190fc68e68e942085ecc664e51d04bd603b9dec0ce07ab6251ac8758`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a59fb0b9169398073160f35b57b1496ae69826d16b74c1b4e3ab2844fb5525d`  
		Last Modified: Tue, 11 Nov 2025 20:12:57 GMT  
		Size: 105.5 MB (105455944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dd169b0f4a6523413ec8242e7568a2e7dd7a4d2eacfbc963471b6d8cf6fb89`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8b456496aaec87c0693ad6583722dafd823752a83215c82f1b5571aa029574`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6f255d3954734536507fb9b1df986db1efe0ddc7f7785823819a7c03071f3a`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53956994f9d7834ac7d9f501da791134da93568c9fd52624c28c2132c73b32fc`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:80da6917e9bbc790ef79a634800825719b7e3fc92bc4ca0b11be7bf068ba3956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c0723948db0c0e9064bdf851696cf9002f189cfa532bc0a2ce41d74b0c2d28`

```dockerfile
```

-	Layers:
	-	`sha256:1d86db9e4bf6a0561b493dbb01967046c5fd93c40e1aba4122d041d3f87860f7`  
		Last Modified: Tue, 11 Nov 2025 23:33:24 GMT  
		Size: 4.2 MB (4184411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8080e21939e4646d48e99f6919137484c87a4d688e9bc13a06a9a3bcec3e806a`  
		Last Modified: Tue, 11 Nov 2025 23:33:25 GMT  
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
$ docker pull couchdb@sha256:0db9109afaf2e76be1b0a866c68c6da1d1395ec0468b2baad046268729cc3f2e
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
$ docker pull couchdb@sha256:d73248e18a72d47573e1dea801a54fb37b52dd63e8e119bc0e3c42652bd75250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3109071ca4993e06ad0d4d6b1e786c48365329326ee7287ede57b68d35188d51`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:12:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:12:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 11 Nov 2025 20:12:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:12:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:12:58 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:58 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 11 Nov 2025 20:13:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 11 Nov 2025 20:13:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4753a07d81ae29a1f5c07d626bbc1509aee278e77e3aaab375ab94890e9aeb9`  
		Last Modified: Tue, 11 Nov 2025 20:13:26 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605d123a589ba69a28cfc4dc492c43c5442935e8f6f784dc9144946ed0ff830e`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 7.9 MB (7881782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1870aa4ea49712c48611828f9cc0d818149d5a1fb397d52253c79553ba04011b`  
		Last Modified: Tue, 11 Nov 2025 20:13:37 GMT  
		Size: 77.4 MB (77380766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fc3432c653b53a299e44685232f09f7b0809334dee2657458cc70fc82018ed`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 424.1 KB (424112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894fa5b8d29848991cf9186656a612b7126749b77dafddb9091cafd934f3f14a`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 99.5 KB (99510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f414fe051f965c8439ad7dd45b3d5e0f60fde782301d3d8b39b11063417be90`  
		Last Modified: Tue, 11 Nov 2025 20:13:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3341fb5bd5d5a909f909eea6e9a7411f41de72e5fdb5eb82b5cec97a2e247671`  
		Last Modified: Tue, 11 Nov 2025 20:13:31 GMT  
		Size: 42.4 MB (42436337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6603e804abc967e250d9c8e5ea60352fb09cd05188ab4a0e930148cef296b`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d7b9a35fd9a8869c1c492ed858d55401fc8c539a4ecbb224d91f32a7796d7c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568857b4ebfd0100253c3aa4b17612124b10b5097410fd4cf6ea9e76a13db09c`

```dockerfile
```

-	Layers:
	-	`sha256:5beab407beb102095b5ffab57cf238fe0f9a40f8695b2a9d63b3960f912bb269`  
		Last Modified: Tue, 11 Nov 2025 23:33:37 GMT  
		Size: 3.7 MB (3658053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9ca515fdb2f9e12bf53a92941f03d3aec40b3cccf1d47c1b93e54f7f324c4f7`  
		Last Modified: Tue, 11 Nov 2025 23:33:38 GMT  
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
$ docker pull couchdb@sha256:fde8795f545acc4d10d9ec8f9623068e0e1ef86d9d4effb4dbc8eb77f3d045b7
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
$ docker pull couchdb@sha256:ae92649b1de2af5a30ea16afa0a15662287b1e906887234d1c40962f9bd396e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139013957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc040e8ea83945c4fd839a438c8fad3ee6237c167c82854bacd1143932162fed`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:28:47 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 00:28:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:28:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:29:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:01 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 04 Nov 2025 00:29:01 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:29:14 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 00:29:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 00:29:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c309e0064c83abaec532030cb896235be9913190de769e3856c578805467b1`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af37cbb4228b62b8a25984f56f3f1f6319ca4778a1e53dcadbef7ae9f60a76ca`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 7.9 MB (7881768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8b88432ef4a069404a98fc7da5da7daf4a41a71d6fa95d4e6775d383a87022`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 401.7 KB (401731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb078d567a91f2796daf6f979be6c01b370b303f417e407fdfb4bc2f5bc30c1e`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 76.5 KB (76510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b69adfad93090a275d6c5a6d35ad956857ddd317072a9d11b3c10357b1a0af`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa90b6b09fb165d3e3814d34725623133d8be304b59bbce9f1a15eec4bf55900`  
		Last Modified: Tue, 04 Nov 2025 00:29:48 GMT  
		Size: 102.4 MB (102419951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed773c86bcdb74d35e017d30c3201992f06144929c2d0ccb1dc10247f0d3f2b4`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4665b492d7528f234f5daf4aa405248fe5d6fc4dcb551d648ef67285b73f5121`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cde999ba539c4da994f46b8f03a176ef7cbb5ea82043469c322980720364d53`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a941d5a3854a0c9c1c25c9291b5f3eac8757408e365b0847d958abe30050b6f`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:0feb279ca88f41023331ad038a92457ce8e7be8f0cae73efe99ce6a24bdd648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517b5fcaadb85aaaeae3b6487482cee64014e781c108ff47d7277ac6bfc9f004`

```dockerfile
```

-	Layers:
	-	`sha256:46003e629c9efbaf1be067b184be32150c504a46ecb93b9117ba0805e01c313e`  
		Last Modified: Tue, 04 Nov 2025 11:33:42 GMT  
		Size: 4.1 MB (4125385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee11a78b0c7bfe5d99115d2cf9017a3a5cfaabf8ec850f49a897635c355b286b`  
		Last Modified: Tue, 04 Nov 2025 11:33:43 GMT  
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
$ docker pull couchdb@sha256:3b23ac5eedfba5b3e71582c31fa146d6e7898fda4b96a6d108e7cae86b565b17
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
$ docker pull couchdb@sha256:e89c1ca28509ef58d06eb69437b051ba82525209ef897d97ebd0f9538bad6d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07014dc088587ea17b296479e2301b20674dd791e8d144dac636d676017b1ff4`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:28:51 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 00:28:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:29:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:29:12 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:12 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:29:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 00:29:17 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 00:29:17 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 00:29:17 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 00:29:17 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1baa3f34f1f0b416fc635d8528859a4ace4a710155adb7bab7162be3d9c01ef`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc47a29a3aeceec28033eefdeef21ec52824e831c80a0b2082afb8dfcd1b143`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 7.9 MB (7881827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e654e32c73e5f166e000959eb66293ca86d969a50765309ae2577d2e199ce`  
		Last Modified: Tue, 04 Nov 2025 00:29:46 GMT  
		Size: 77.4 MB (77380777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2baca22c5b5dcb16d7d8b9090aef401fea173970ac366fc29058a0bd7ec82417`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 424.1 KB (424100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e38882bf6bf9d5eab34d9b24fc53c80b9f2f36381de70a135f97248d8add`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 99.5 KB (99509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec31032200367531e6dc5f66facb9b3f12f89c141af119373f883b866126a3d`  
		Last Modified: Tue, 04 Nov 2025 00:29:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3534afae21db3a85bdf3c2b158c1d794313c431cf94e5048291aca218dae7fbc`  
		Last Modified: Tue, 04 Nov 2025 00:29:46 GMT  
		Size: 42.4 MB (42436072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc445fc3dd6d577af95062e01bc783f112dbcc379c8dac4c52acfa983b5880c`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5e6190d3030c7e418be905a3d2918ccd4f2b335e3792f7e3f2965bb4f5a55043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821a21457ebebe2398298513512b18dc25e8d3bc87e89902e97ff42338fbd7f1`

```dockerfile
```

-	Layers:
	-	`sha256:3df563e514f63d880a008e1aa29d70ceeb0c130054aba118d127778031cd5531`  
		Last Modified: Tue, 04 Nov 2025 11:33:53 GMT  
		Size: 3.7 MB (3657747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b349c809c80936be658fef724eff8631b4e18eb7401d78066fcab5855c852541`  
		Last Modified: Tue, 04 Nov 2025 11:33:54 GMT  
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
$ docker pull couchdb@sha256:fde8795f545acc4d10d9ec8f9623068e0e1ef86d9d4effb4dbc8eb77f3d045b7
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
$ docker pull couchdb@sha256:ae92649b1de2af5a30ea16afa0a15662287b1e906887234d1c40962f9bd396e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139013957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc040e8ea83945c4fd839a438c8fad3ee6237c167c82854bacd1143932162fed`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:28:47 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 00:28:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:28:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:29:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:01 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 04 Nov 2025 00:29:01 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:29:14 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 00:29:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 00:29:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c309e0064c83abaec532030cb896235be9913190de769e3856c578805467b1`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af37cbb4228b62b8a25984f56f3f1f6319ca4778a1e53dcadbef7ae9f60a76ca`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 7.9 MB (7881768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8b88432ef4a069404a98fc7da5da7daf4a41a71d6fa95d4e6775d383a87022`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 401.7 KB (401731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb078d567a91f2796daf6f979be6c01b370b303f417e407fdfb4bc2f5bc30c1e`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 76.5 KB (76510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b69adfad93090a275d6c5a6d35ad956857ddd317072a9d11b3c10357b1a0af`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa90b6b09fb165d3e3814d34725623133d8be304b59bbce9f1a15eec4bf55900`  
		Last Modified: Tue, 04 Nov 2025 00:29:48 GMT  
		Size: 102.4 MB (102419951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed773c86bcdb74d35e017d30c3201992f06144929c2d0ccb1dc10247f0d3f2b4`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4665b492d7528f234f5daf4aa405248fe5d6fc4dcb551d648ef67285b73f5121`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cde999ba539c4da994f46b8f03a176ef7cbb5ea82043469c322980720364d53`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a941d5a3854a0c9c1c25c9291b5f3eac8757408e365b0847d958abe30050b6f`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:0feb279ca88f41023331ad038a92457ce8e7be8f0cae73efe99ce6a24bdd648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517b5fcaadb85aaaeae3b6487482cee64014e781c108ff47d7277ac6bfc9f004`

```dockerfile
```

-	Layers:
	-	`sha256:46003e629c9efbaf1be067b184be32150c504a46ecb93b9117ba0805e01c313e`  
		Last Modified: Tue, 04 Nov 2025 11:33:42 GMT  
		Size: 4.1 MB (4125385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee11a78b0c7bfe5d99115d2cf9017a3a5cfaabf8ec850f49a897635c355b286b`  
		Last Modified: Tue, 04 Nov 2025 11:33:43 GMT  
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
$ docker pull couchdb@sha256:3b23ac5eedfba5b3e71582c31fa146d6e7898fda4b96a6d108e7cae86b565b17
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
$ docker pull couchdb@sha256:e89c1ca28509ef58d06eb69437b051ba82525209ef897d97ebd0f9538bad6d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07014dc088587ea17b296479e2301b20674dd791e8d144dac636d676017b1ff4`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:28:51 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 00:28:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:29:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:29:12 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:12 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:29:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 00:29:17 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 00:29:17 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 00:29:17 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 00:29:17 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1baa3f34f1f0b416fc635d8528859a4ace4a710155adb7bab7162be3d9c01ef`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc47a29a3aeceec28033eefdeef21ec52824e831c80a0b2082afb8dfcd1b143`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 7.9 MB (7881827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e654e32c73e5f166e000959eb66293ca86d969a50765309ae2577d2e199ce`  
		Last Modified: Tue, 04 Nov 2025 00:29:46 GMT  
		Size: 77.4 MB (77380777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2baca22c5b5dcb16d7d8b9090aef401fea173970ac366fc29058a0bd7ec82417`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 424.1 KB (424100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e38882bf6bf9d5eab34d9b24fc53c80b9f2f36381de70a135f97248d8add`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 99.5 KB (99509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec31032200367531e6dc5f66facb9b3f12f89c141af119373f883b866126a3d`  
		Last Modified: Tue, 04 Nov 2025 00:29:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3534afae21db3a85bdf3c2b158c1d794313c431cf94e5048291aca218dae7fbc`  
		Last Modified: Tue, 04 Nov 2025 00:29:46 GMT  
		Size: 42.4 MB (42436072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc445fc3dd6d577af95062e01bc783f112dbcc379c8dac4c52acfa983b5880c`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5e6190d3030c7e418be905a3d2918ccd4f2b335e3792f7e3f2965bb4f5a55043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821a21457ebebe2398298513512b18dc25e8d3bc87e89902e97ff42338fbd7f1`

```dockerfile
```

-	Layers:
	-	`sha256:3df563e514f63d880a008e1aa29d70ceeb0c130054aba118d127778031cd5531`  
		Last Modified: Tue, 04 Nov 2025 11:33:53 GMT  
		Size: 3.7 MB (3657747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b349c809c80936be658fef724eff8631b4e18eb7401d78066fcab5855c852541`  
		Last Modified: Tue, 04 Nov 2025 11:33:54 GMT  
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
$ docker pull couchdb@sha256:d8bd3c3eb34c621096f4d2837be7f246128814f34ad0ada8a6280e71da8e2885
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
$ docker pull couchdb@sha256:b4f0b214477ea89489da9d4001cb8eac7d259e113b44603c57cfc94a3d008e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142049914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e493d383d26977710c0749ed769f8af1b2477b0298047b08eb44d409a1ba32`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:11:50 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:11:50 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 11 Nov 2025 20:11:56 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:11:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:12:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:03 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 11 Nov 2025 20:12:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 20:12:16 GMT
VOLUME [/opt/couchdb/data]
# Tue, 11 Nov 2025 20:12:16 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 11 Nov 2025 20:12:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d274f1c08381bf79eeb842fb97a61b254cfade7b44d978eaf71f4c639725ea4b`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0bb58d39055c8e5f9cd829ae5145f2d096176b6ee2cff83eba6156c3e07ff6`  
		Last Modified: Tue, 11 Nov 2025 20:12:45 GMT  
		Size: 7.9 MB (7881754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26343153c3ea04a23236a9d1583932b81c6438b6207cf64b4d5b3f53564cee93`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 401.7 KB (401726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b90245eeddcd781e96e60a2a8f6c3577ca5e847663d5214fd7814fa06e92f26`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 76.5 KB (76493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ba965190fc68e68e942085ecc664e51d04bd603b9dec0ce07ab6251ac8758`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a59fb0b9169398073160f35b57b1496ae69826d16b74c1b4e3ab2844fb5525d`  
		Last Modified: Tue, 11 Nov 2025 20:12:57 GMT  
		Size: 105.5 MB (105455944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dd169b0f4a6523413ec8242e7568a2e7dd7a4d2eacfbc963471b6d8cf6fb89`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8b456496aaec87c0693ad6583722dafd823752a83215c82f1b5571aa029574`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6f255d3954734536507fb9b1df986db1efe0ddc7f7785823819a7c03071f3a`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53956994f9d7834ac7d9f501da791134da93568c9fd52624c28c2132c73b32fc`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:80da6917e9bbc790ef79a634800825719b7e3fc92bc4ca0b11be7bf068ba3956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c0723948db0c0e9064bdf851696cf9002f189cfa532bc0a2ce41d74b0c2d28`

```dockerfile
```

-	Layers:
	-	`sha256:1d86db9e4bf6a0561b493dbb01967046c5fd93c40e1aba4122d041d3f87860f7`  
		Last Modified: Tue, 11 Nov 2025 23:33:24 GMT  
		Size: 4.2 MB (4184411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8080e21939e4646d48e99f6919137484c87a4d688e9bc13a06a9a3bcec3e806a`  
		Last Modified: Tue, 11 Nov 2025 23:33:25 GMT  
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
$ docker pull couchdb@sha256:0db9109afaf2e76be1b0a866c68c6da1d1395ec0468b2baad046268729cc3f2e
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
$ docker pull couchdb@sha256:d73248e18a72d47573e1dea801a54fb37b52dd63e8e119bc0e3c42652bd75250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3109071ca4993e06ad0d4d6b1e786c48365329326ee7287ede57b68d35188d51`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:12:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:12:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 11 Nov 2025 20:12:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:12:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:12:58 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:58 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 11 Nov 2025 20:13:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 11 Nov 2025 20:13:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4753a07d81ae29a1f5c07d626bbc1509aee278e77e3aaab375ab94890e9aeb9`  
		Last Modified: Tue, 11 Nov 2025 20:13:26 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605d123a589ba69a28cfc4dc492c43c5442935e8f6f784dc9144946ed0ff830e`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 7.9 MB (7881782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1870aa4ea49712c48611828f9cc0d818149d5a1fb397d52253c79553ba04011b`  
		Last Modified: Tue, 11 Nov 2025 20:13:37 GMT  
		Size: 77.4 MB (77380766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fc3432c653b53a299e44685232f09f7b0809334dee2657458cc70fc82018ed`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 424.1 KB (424112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894fa5b8d29848991cf9186656a612b7126749b77dafddb9091cafd934f3f14a`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 99.5 KB (99510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f414fe051f965c8439ad7dd45b3d5e0f60fde782301d3d8b39b11063417be90`  
		Last Modified: Tue, 11 Nov 2025 20:13:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3341fb5bd5d5a909f909eea6e9a7411f41de72e5fdb5eb82b5cec97a2e247671`  
		Last Modified: Tue, 11 Nov 2025 20:13:31 GMT  
		Size: 42.4 MB (42436337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6603e804abc967e250d9c8e5ea60352fb09cd05188ab4a0e930148cef296b`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d7b9a35fd9a8869c1c492ed858d55401fc8c539a4ecbb224d91f32a7796d7c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568857b4ebfd0100253c3aa4b17612124b10b5097410fd4cf6ea9e76a13db09c`

```dockerfile
```

-	Layers:
	-	`sha256:5beab407beb102095b5ffab57cf238fe0f9a40f8695b2a9d63b3960f912bb269`  
		Last Modified: Tue, 11 Nov 2025 23:33:37 GMT  
		Size: 3.7 MB (3658053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9ca515fdb2f9e12bf53a92941f03d3aec40b3cccf1d47c1b93e54f7f324c4f7`  
		Last Modified: Tue, 11 Nov 2025 23:33:38 GMT  
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
$ docker pull couchdb@sha256:d8bd3c3eb34c621096f4d2837be7f246128814f34ad0ada8a6280e71da8e2885
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
$ docker pull couchdb@sha256:b4f0b214477ea89489da9d4001cb8eac7d259e113b44603c57cfc94a3d008e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142049914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e493d383d26977710c0749ed769f8af1b2477b0298047b08eb44d409a1ba32`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:11:50 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:11:50 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 11 Nov 2025 20:11:56 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:11:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:12:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:03 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 11 Nov 2025 20:12:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 20:12:16 GMT
VOLUME [/opt/couchdb/data]
# Tue, 11 Nov 2025 20:12:16 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 11 Nov 2025 20:12:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d274f1c08381bf79eeb842fb97a61b254cfade7b44d978eaf71f4c639725ea4b`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0bb58d39055c8e5f9cd829ae5145f2d096176b6ee2cff83eba6156c3e07ff6`  
		Last Modified: Tue, 11 Nov 2025 20:12:45 GMT  
		Size: 7.9 MB (7881754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26343153c3ea04a23236a9d1583932b81c6438b6207cf64b4d5b3f53564cee93`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 401.7 KB (401726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b90245eeddcd781e96e60a2a8f6c3577ca5e847663d5214fd7814fa06e92f26`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 76.5 KB (76493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ba965190fc68e68e942085ecc664e51d04bd603b9dec0ce07ab6251ac8758`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a59fb0b9169398073160f35b57b1496ae69826d16b74c1b4e3ab2844fb5525d`  
		Last Modified: Tue, 11 Nov 2025 20:12:57 GMT  
		Size: 105.5 MB (105455944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dd169b0f4a6523413ec8242e7568a2e7dd7a4d2eacfbc963471b6d8cf6fb89`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8b456496aaec87c0693ad6583722dafd823752a83215c82f1b5571aa029574`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6f255d3954734536507fb9b1df986db1efe0ddc7f7785823819a7c03071f3a`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53956994f9d7834ac7d9f501da791134da93568c9fd52624c28c2132c73b32fc`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:80da6917e9bbc790ef79a634800825719b7e3fc92bc4ca0b11be7bf068ba3956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c0723948db0c0e9064bdf851696cf9002f189cfa532bc0a2ce41d74b0c2d28`

```dockerfile
```

-	Layers:
	-	`sha256:1d86db9e4bf6a0561b493dbb01967046c5fd93c40e1aba4122d041d3f87860f7`  
		Last Modified: Tue, 11 Nov 2025 23:33:24 GMT  
		Size: 4.2 MB (4184411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8080e21939e4646d48e99f6919137484c87a4d688e9bc13a06a9a3bcec3e806a`  
		Last Modified: Tue, 11 Nov 2025 23:33:25 GMT  
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
$ docker pull couchdb@sha256:0db9109afaf2e76be1b0a866c68c6da1d1395ec0468b2baad046268729cc3f2e
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
$ docker pull couchdb@sha256:d73248e18a72d47573e1dea801a54fb37b52dd63e8e119bc0e3c42652bd75250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3109071ca4993e06ad0d4d6b1e786c48365329326ee7287ede57b68d35188d51`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:12:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:12:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 11 Nov 2025 20:12:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:12:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:12:58 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:58 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 11 Nov 2025 20:13:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 11 Nov 2025 20:13:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4753a07d81ae29a1f5c07d626bbc1509aee278e77e3aaab375ab94890e9aeb9`  
		Last Modified: Tue, 11 Nov 2025 20:13:26 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605d123a589ba69a28cfc4dc492c43c5442935e8f6f784dc9144946ed0ff830e`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 7.9 MB (7881782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1870aa4ea49712c48611828f9cc0d818149d5a1fb397d52253c79553ba04011b`  
		Last Modified: Tue, 11 Nov 2025 20:13:37 GMT  
		Size: 77.4 MB (77380766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fc3432c653b53a299e44685232f09f7b0809334dee2657458cc70fc82018ed`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 424.1 KB (424112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894fa5b8d29848991cf9186656a612b7126749b77dafddb9091cafd934f3f14a`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 99.5 KB (99510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f414fe051f965c8439ad7dd45b3d5e0f60fde782301d3d8b39b11063417be90`  
		Last Modified: Tue, 11 Nov 2025 20:13:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3341fb5bd5d5a909f909eea6e9a7411f41de72e5fdb5eb82b5cec97a2e247671`  
		Last Modified: Tue, 11 Nov 2025 20:13:31 GMT  
		Size: 42.4 MB (42436337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6603e804abc967e250d9c8e5ea60352fb09cd05188ab4a0e930148cef296b`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d7b9a35fd9a8869c1c492ed858d55401fc8c539a4ecbb224d91f32a7796d7c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568857b4ebfd0100253c3aa4b17612124b10b5097410fd4cf6ea9e76a13db09c`

```dockerfile
```

-	Layers:
	-	`sha256:5beab407beb102095b5ffab57cf238fe0f9a40f8695b2a9d63b3960f912bb269`  
		Last Modified: Tue, 11 Nov 2025 23:33:37 GMT  
		Size: 3.7 MB (3658053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9ca515fdb2f9e12bf53a92941f03d3aec40b3cccf1d47c1b93e54f7f324c4f7`  
		Last Modified: Tue, 11 Nov 2025 23:33:38 GMT  
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
$ docker pull couchdb@sha256:d8bd3c3eb34c621096f4d2837be7f246128814f34ad0ada8a6280e71da8e2885
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
$ docker pull couchdb@sha256:b4f0b214477ea89489da9d4001cb8eac7d259e113b44603c57cfc94a3d008e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142049914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e493d383d26977710c0749ed769f8af1b2477b0298047b08eb44d409a1ba32`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:11:50 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:11:50 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 11 Nov 2025 20:11:56 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:11:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:12:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:03 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 11 Nov 2025 20:12:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 11 Nov 2025 20:12:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 20:12:16 GMT
VOLUME [/opt/couchdb/data]
# Tue, 11 Nov 2025 20:12:16 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 11 Nov 2025 20:12:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d274f1c08381bf79eeb842fb97a61b254cfade7b44d978eaf71f4c639725ea4b`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0bb58d39055c8e5f9cd829ae5145f2d096176b6ee2cff83eba6156c3e07ff6`  
		Last Modified: Tue, 11 Nov 2025 20:12:45 GMT  
		Size: 7.9 MB (7881754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26343153c3ea04a23236a9d1583932b81c6438b6207cf64b4d5b3f53564cee93`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 401.7 KB (401726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b90245eeddcd781e96e60a2a8f6c3577ca5e847663d5214fd7814fa06e92f26`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 76.5 KB (76493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ba965190fc68e68e942085ecc664e51d04bd603b9dec0ce07ab6251ac8758`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a59fb0b9169398073160f35b57b1496ae69826d16b74c1b4e3ab2844fb5525d`  
		Last Modified: Tue, 11 Nov 2025 20:12:57 GMT  
		Size: 105.5 MB (105455944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dd169b0f4a6523413ec8242e7568a2e7dd7a4d2eacfbc963471b6d8cf6fb89`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8b456496aaec87c0693ad6583722dafd823752a83215c82f1b5571aa029574`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6f255d3954734536507fb9b1df986db1efe0ddc7f7785823819a7c03071f3a`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53956994f9d7834ac7d9f501da791134da93568c9fd52624c28c2132c73b32fc`  
		Last Modified: Tue, 11 Nov 2025 20:12:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:80da6917e9bbc790ef79a634800825719b7e3fc92bc4ca0b11be7bf068ba3956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c0723948db0c0e9064bdf851696cf9002f189cfa532bc0a2ce41d74b0c2d28`

```dockerfile
```

-	Layers:
	-	`sha256:1d86db9e4bf6a0561b493dbb01967046c5fd93c40e1aba4122d041d3f87860f7`  
		Last Modified: Tue, 11 Nov 2025 23:33:24 GMT  
		Size: 4.2 MB (4184411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8080e21939e4646d48e99f6919137484c87a4d688e9bc13a06a9a3bcec3e806a`  
		Last Modified: Tue, 11 Nov 2025 23:33:25 GMT  
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
