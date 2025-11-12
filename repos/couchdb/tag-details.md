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
$ docker pull couchdb@sha256:3e9c8b7c53ffa4f72aee9946be19ba043c5f1683d1d3513e7ef918c25b0b9e51
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
$ docker pull couchdb@sha256:747f3dd9d0700f2e00b6b23e5225e327c5d0cb32b4228fe554835185ee85238e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141402338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff8fef6b6221df21026e1bf238dabce906eb4b1870b3399664601796d008d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:12:04 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:12:04 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 11 Nov 2025 20:12:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:12:13 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:12:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:19 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 11 Nov 2025 20:12:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 20:12:32 GMT
VOLUME [/opt/couchdb/data]
# Tue, 11 Nov 2025 20:12:32 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 11 Nov 2025 20:12:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e818c14e4504c76b62137ac42128490a9edd0eb981bf5865a5f0a37e8293dcb`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb7b12cd06b04fb526d8f2e897c715e26715a0b1413f341280c5b55e720190c`  
		Last Modified: Tue, 11 Nov 2025 20:12:56 GMT  
		Size: 7.7 MB (7692023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93af127312a86a7727ba7295aa8ecf10726432730090aacd98fefb313b97cb74`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 370.5 KB (370497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2542ebf23d27b05271c174863bbf1c531afcd3c92b354a5864bc0ab1b0dcd2c0`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 76.5 KB (76472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde3e0e108696404fbf186251f687f55b53261087e3d6edb7461bd3cf5e6a50b`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4e83a949c53ba221bf4f83d75fc3fe47de0f63017ba5fd7302d714d42995d5`  
		Last Modified: Tue, 11 Nov 2025 20:13:07 GMT  
		Size: 105.2 MB (105155535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3619ea51b6069a764b242b0afdbb30d9d0b08ff784c5b167f3d4c25c3babef`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086eb28484449b29b005ea287e7debd61acbcdf72c338f935783890b355e9c2c`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d63ab30b28a48901cbc05d83708e0b45bdf8f5c16b30687d8c2f653abd66c`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7692c35f92eaceb5ec01125b3ca4db18305e24eaf641159c0968f5befe5adee8`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:5c3a0ee184ebcc38eea96429109e6ff55dc7349b7bc52ae1d72988680fb0887d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4a357464b37e2bbf44a258c0e5b0faec86bad1b66ba84686fa15038b6edc45`

```dockerfile
```

-	Layers:
	-	`sha256:fa16bc03b59e15874298a7e9c46492386b6ce5bb2e306ec5623add8efacc12d2`  
		Last Modified: Tue, 11 Nov 2025 23:33:30 GMT  
		Size: 4.2 MB (4184704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f66a1df8f2049aa84c8246571c9a471aae459f12582311af1227d6f853c09f`  
		Last Modified: Tue, 11 Nov 2025 23:33:30 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:a7c89f0e3d2759381bb31bf9e6912a85befed86f9afcaf631646bfad0a778c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e82360d747e07b6797d4d48852268a8744de165f6d1efc09920175ff0fb3ff`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:12:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:12:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 11 Nov 2025 20:12:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:12:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:13:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 11 Nov 2025 20:13:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:13:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Nov 2025 20:13:40 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 11 Nov 2025 20:13:41 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 11 Nov 2025 20:13:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 11 Nov 2025 20:13:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 11 Nov 2025 20:13:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 20:13:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 11 Nov 2025 20:13:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 11 Nov 2025 20:13:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf85f69f108bdd7fd8737e2c27f2b519282c682c926e752d7895b95322a3a1f8`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89683817eaac97bd24a904b06852f30efc3f67cc9062e8d6cc5074a518e0de32`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 7.4 MB (7398221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d59a01d46a74b4685f1a0120f88ae0fa22069ebd8446577ac56fdc4be81a78`  
		Last Modified: Tue, 11 Nov 2025 20:14:53 GMT  
		Size: 372.2 KB (372164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da830badeb2c2860661fcd341daa61de0d1c7b7f4e427d958bbf1ad47da60c0`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 76.6 KB (76617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018650cafb141f99a44532fa2e285ef13c5b18b19e9326ededce63a558428de0`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d0f31299fd049816d258cc751714691ad495fc0e9f756387f780c7916f16b2`  
		Last Modified: Tue, 11 Nov 2025 20:15:01 GMT  
		Size: 104.0 MB (104028538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d4ee4d51885d60b2b6b19360366ddef0c308d2dc44dca0945db503f52c9d6`  
		Last Modified: Tue, 11 Nov 2025 20:14:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15273f74fdd408c496548d519baba1d71827da3e8960735deb034c0be1d4857e`  
		Last Modified: Tue, 11 Nov 2025 20:14:55 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d116eca5b93b315310fa7b0067c21c495f2eb27f7b97ef0d8edb2c269c0d6e`  
		Last Modified: Tue, 11 Nov 2025 20:14:55 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7367b93e2dfb059c851e4be053bdfcf168304d052fc63b7739b282fdb9c39884`  
		Last Modified: Tue, 11 Nov 2025 20:14:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:139efc19ebf539a0422f05ca2d4a24977ddcf9c36142421f2d6781cbe44e1e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ea503310d5049caeb7ea967486b7eb49d0b6fde9cc2c1b3364d3cbf6141244`

```dockerfile
```

-	Layers:
	-	`sha256:9ee8592cfac5e571a5b32b86393d262e6b5b6d176c5ae64ab141a14ecf54a685`  
		Last Modified: Tue, 11 Nov 2025 23:33:35 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c8270c42cc0e6ff8640dbbf7380096bb0774c196b33bf02661cc0c0dd4aa2f`  
		Last Modified: Tue, 11 Nov 2025 23:33:36 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:857efe68d371236f1bdc898da343175868b5efeb9cf9934a13c8e173e786a354
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
$ docker pull couchdb@sha256:09aba0fd985d41d85997a5812bc01ea3a6a4bab791e2a00f65fcbef473eee634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7782988f3e89e74a895aaec8f4fa216315d467dc79ab413ad89b9b1b097ff7dd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:11:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:11:10 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 11 Nov 2025 20:11:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:24 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:11:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:11:31 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:31 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:11:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 11 Nov 2025 20:11:38 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 11 Nov 2025 20:11:38 GMT
VOLUME [/opt/nouveau/data]
# Tue, 11 Nov 2025 20:11:38 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 11 Nov 2025 20:11:38 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7dd6974ccd35b0cb52781f6c8f38ebeac7a5d6260ac6ede11f3f8c9f7fc215`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1f8a4ee6f68ed0ad0430ff95a0098ace6d81921806883704460db6aa1dfd1e`  
		Last Modified: Tue, 11 Nov 2025 20:12:18 GMT  
		Size: 7.7 MB (7692012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a18649a57bbd3cbc1c2fda4ecaf7696bada3bac421f257241f528509e9a1ee`  
		Last Modified: Tue, 11 Nov 2025 20:12:27 GMT  
		Size: 76.7 MB (76691503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42568529e1e6429a35c8c262d9019007ac5da91fabf5742ecd65afee0e60e85`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 392.7 KB (392686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c20c9f876f0937864841173cc872d0b40ab7e4b1e874fd150bed14e316c8737`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 99.4 KB (99415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781ab25ac737fdef9c06353f09faae1dbbd846aa22e6257e1df72655b817015`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88308c4f015c5ccafa012b61f255673fca6103af1fcadce254a335a1cc4c0ce1`  
		Last Modified: Tue, 11 Nov 2025 20:12:21 GMT  
		Size: 42.3 MB (42339027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ffc13d91d0ca731e7f6fcf4b27cb78c9e080738696cfcbc946b53d3b4b1c7b`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:954d2c3f512a1932c0826eaf32a7cafce8d74f498b88dcf002d9dc150d9ffbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a396232965fc39a5cef33e08c673a46005c9b24d8261d634c6669a512cea77`

```dockerfile
```

-	Layers:
	-	`sha256:93e8cb72952640bb24278dc2766189898940a409f998cc1523f49e1aa7a3ab04`  
		Last Modified: Tue, 11 Nov 2025 23:33:42 GMT  
		Size: 3.7 MB (3656729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:685e6f2cdaccaf4f44cc143d00ca81ec0005d0e2f61758c9ab557db887643f85`  
		Last Modified: Tue, 11 Nov 2025 23:33:43 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2a59bc3eeaf33c611e6d20198a2d11c347ab3a09cc5f2a194ece87d4cd6917a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150086583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4df85d89689b925f7108cc12b037e552e41f9ce93759a791748679d571f57a`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:14:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:14:55 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 11 Nov 2025 20:15:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:15:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:15:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:15:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:15:47 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:15:47 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:16:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 11 Nov 2025 20:16:03 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 11 Nov 2025 20:16:03 GMT
VOLUME [/opt/nouveau/data]
# Tue, 11 Nov 2025 20:16:03 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 11 Nov 2025 20:16:03 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3c6f64be9bdd3c2601d8e4c2d7c4354853fff0c19e8f7bdf9b09e8860c24e6`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f243593476a0cede547d1c765b50ea8bc5efa48cb91301386dcac9c5051b81`  
		Last Modified: Tue, 11 Nov 2025 20:17:14 GMT  
		Size: 7.4 MB (7398148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0404524878fe3bbf61b798a9732c238278ceef6c536623058c409670c9c43acb`  
		Last Modified: Tue, 11 Nov 2025 20:17:21 GMT  
		Size: 73.1 MB (73143081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e5e1d70ec4cd7686fe1f025560584c71bd57c0d3c71a06189f1017d9bea5e6`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 394.5 KB (394458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b4a7c215085507f09d210801f506b21c980a71e6e0d6dbd25e7b1f030c6046`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 99.7 KB (99676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e9e3fba2322c92147365dab7fb2e4fee6e9a6fb98242badffe51b399fdd0dc`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef31665d30c90ec5abf16e6d176c05980f28aa8a8a3ac0a2b120622b616d813`  
		Last Modified: Tue, 11 Nov 2025 20:17:18 GMT  
		Size: 42.2 MB (42164789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f743239c3077bc286d9a3930ffc95cabb89849d4301bbd7067f7a6f28a7526`  
		Last Modified: Tue, 11 Nov 2025 20:17:12 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5c5b1bddcc346bbcf0737d83ff70de2b0e7a7ea0e9c8368bdd623d334bf5d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8b0a83d57b365c00a69979a736bd7e27430a4d90e6a47d46120b3f05e3b0e6`

```dockerfile
```

-	Layers:
	-	`sha256:9f369884d273c2e87ce29b44b7345886fdda1a13af7ab4872dce6501aad619bc`  
		Last Modified: Tue, 11 Nov 2025 23:33:47 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c740ff0a68a3faca5335b5543295da9494445384b911e1d54d362c5a109dc315`  
		Last Modified: Tue, 11 Nov 2025 23:33:48 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:57aaf1f94039ddae75a3994fc5cef5f06764344fe919ab307acfe522b9ed7995
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
$ docker pull couchdb@sha256:2a7b27021eb330482389d6d0a458365aa3abbf33c95966970dfe473d829362bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138415822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293400da04488d1b9895e016d8aaa255135634d83a12262f02a317bb1df93392`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:30:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 00:31:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:31:07 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:31:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:13 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 04 Nov 2025 00:31:13 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:31:26 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 00:31:26 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 00:31:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa07e0ad136c2d81f08031cacea7cf53591018e635b98792dc196aa25f5ff817`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8530c6a682a670efa2dad1306e54ae7243dde03c298fd4d2314afbe526be8d74`  
		Last Modified: Tue, 04 Nov 2025 00:31:50 GMT  
		Size: 7.7 MB (7692062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbed46138490a32cdc42261c9cc74dbd61554773d5cd1ea6d6a1196313d7633`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 370.5 KB (370474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c6fd493d8273440f4a33bf48cba5e709cecb7890bf493442f3d30c7995927c`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 76.5 KB (76489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5700557c00ad6a97d945d95742339bd0231e8c04c7d53803c425a8ff77a8da64`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82205562d09d1353723fe9dfb290fb140071a479eab8ec17a6a771854f8bdfde`  
		Last Modified: Tue, 04 Nov 2025 00:32:01 GMT  
		Size: 102.2 MB (102169002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075bed437a0f95b0246c5fa38e3ce914b7b19bf0bae1e60b986dfcfaf9ed671e`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50813a568ad5d80449de58f1fa88f33e93d11792b55ab28e527bfa3b1bc9316c`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4b101f7877358209b006590c3cc4c5a30c0a488bf327fd4e8c3d4fc37ee949`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 2.2 KB (2223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba32e7e70af1d2f79e667a87423713201376e2369b85b0f97e7d3fe88c23a30`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:7cb7ee766ece8539a85b77062ae8649036c413e1d2a70493d24ff4fc115e5bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83d91f94a47bb0c4365f76ae4fef42d2e35f877379d22b9962bffea082f1704`

```dockerfile
```

-	Layers:
	-	`sha256:c36180c73e9391c022c084e45caf238e6a8589878bd467fdc26ce5256f33fca7`  
		Last Modified: Tue, 04 Nov 2025 11:33:48 GMT  
		Size: 4.1 MB (4125654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6417cc064e6e4c8735cf98e62c84aae8f155dab00e1888c9f77336417513d71f`  
		Last Modified: Tue, 04 Nov 2025 11:33:49 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:7d0d34b2bd8ccd9a33f1867591d6cf0fa624e3b1006bdbd5654025ac3f31e0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135793031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e587c91bb3579341c572872236fbd4ee2e326b1838d01b1136d13ca436e998`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:17:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:17:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 03:17:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:17:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:28 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 04 Nov 2025 03:19:52 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:20:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 03:20:15 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 03:20:15 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 03:20:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 03:20:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:20:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:20:16 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 03:20:16 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 03:20:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ebf53fbc3e3d769a60213c6f4b514ac2a0bfef8d2cc98e421e7189ae613338`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7269136448c34c9267e49af25de0c0ee12a6b28019ce9018f963e546288181e5`  
		Last Modified: Tue, 04 Nov 2025 03:19:42 GMT  
		Size: 7.4 MB (7398114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d914dba9eba91885244c28bee6394a9e0abe6ffcb48d68e5a1955ad1bc21219e`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 372.1 KB (372121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6479c330dc7ea8c7bce7182bc9a7eb611c9491484db645a0e4f3f8e7885788fa`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 76.5 KB (76504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9470edf29bf6994e89c47deecd6a558a242b0646ca9e3328a885918797f91c7`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b89a5f2d1111c22e5f41446d58663b1d82ab5d0329ba6b08582b2b987220305`  
		Last Modified: Tue, 04 Nov 2025 03:21:10 GMT  
		Size: 101.1 MB (101056323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e010a90a16de6beb0136e22206a21576e2a3e0046e04651d8719c1fa23b732f4`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262cf45231db5237eea2f3dd7dc7ff0edea47f8bc9ea2266a789d998a34952ff`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d0360c36779ed8466cb52e6a129b974f313d35840a7ea23bc8a3b28fa17bdd`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17675d30c8cd72b2e434e73f6c3a1f117f8d4c7c63b46f79e979bcffe1df958a`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:a2418d1f77c38958518731f52885b5971598e6cf401d327840b1ea34d9de9d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbb1adb9c833f0c36f50f5051b969eac60839b7da1b5ca1dc4857bd29d3aa6c`

```dockerfile
```

-	Layers:
	-	`sha256:56aed6f64c043e2e4a34464b6a8d5faf7545147543a4ec9b78c6a511bdfedbad`  
		Last Modified: Tue, 04 Nov 2025 08:33:37 GMT  
		Size: 4.1 MB (4121581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9103d442718ed0821b7b9235f5b81f678192a9d60fa0c28645ae8f1fbef723c`  
		Last Modified: Tue, 04 Nov 2025 08:33:38 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:73cec3233025fca7771de3c210356bb503cb8a4c33a83ad61ec68fa1bfd92003
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
$ docker pull couchdb@sha256:6c9cf3dca020d2f49a7756fe8f8105f86d339d18a18e458d843d93acef026407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f6b5cce950c92e5012360057858e0a99cb68bb8213d701e15825f94bf1a849`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:30:58 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 00:31:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:31:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:31:16 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:16 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:31:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 00:31:21 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 00:31:21 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 00:31:21 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 00:31:21 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edcdf1865838daf6de13d2f54e6059b2ae577054f1243c900c51d96eff25016`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0fff095ff52d0d31ad80dcf98768cff07a53dcdc9e52780584470950235995`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 7.7 MB (7692016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829eaec023c87572eb2d4c890b8c5dc90b1779a07ef7e5b523e2bfa236a0fe3`  
		Last Modified: Tue, 04 Nov 2025 00:31:52 GMT  
		Size: 76.7 MB (76691605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce943843a58567bbdca0d02287165f7ce43c55558b3abd3f67630307fc46f5a`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 392.7 KB (392681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f3f6041487d038917d0260cd126c1e043a39d02c9551a19bd8e652909341d4`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 99.4 KB (99425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018defa4077bcb7effc54eb96363849f037e87acf35482b85943d11d814bbfd`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9066acdcf3de579f128c379ccf334603a47dc20a1a17ae720791ccd7bb4bf255`  
		Last Modified: Tue, 04 Nov 2025 00:31:51 GMT  
		Size: 42.3 MB (42338058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dc773705b3ce38bd572ebe6d6e4160480535d7e8f949f0908fac21ba0a7a6f`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c7dbc1f55361fca496f65603d9749809a1ae3f4743a0f0e089492b9b48c6006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9456edb0f9f0c90e8106370e9782aa17a893fbe04183aac243ab250d51d1d6`

```dockerfile
```

-	Layers:
	-	`sha256:cf84fcc0ed95c4f83de2383072e0a58e4c25b30d1a1686999406e013d4026fac`  
		Last Modified: Tue, 04 Nov 2025 11:33:58 GMT  
		Size: 3.7 MB (3656411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbbf19db69c0dd013c389362a7c08bd6befd9a121255d8b11287230a16f693b5`  
		Last Modified: Tue, 04 Nov 2025 11:33:59 GMT  
		Size: 24.4 KB (24384 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:0145626e7a70b53d323a618d7d58a0d49fbf8a9ae8a6c4e3c14f3a07bbf31845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150084175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7128f59709ed6c5239688d86277670a1411bfdfaa882857f7464c74f52d057`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:18:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:18:35 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 03:18:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:18:57 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:57 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:21:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 03:21:06 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 03:21:06 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 03:21:06 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 03:21:06 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7536539bf1ad715cf2dd300635c28f289b63af1cbb92522e91502eef246923`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526e0a76fba7a4a90e9f82e82a2d36b1fb986318a85518bfc9635401a95de3e9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 7.4 MB (7398078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce039d7896ebedadc57a51103ebe71649e42dcf66503771ad322910999b1c820`  
		Last Modified: Tue, 04 Nov 2025 03:19:46 GMT  
		Size: 73.1 MB (73142672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a2015e06dd327a6fa19c3c6249a4fce7b4de27b48d0ffe99bd89193cdc50d`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 394.4 KB (394429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2edba20a7c1a1e969e4475b2647e6299aa0a17f5c863767efe6b0eba76bd8b9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 99.6 KB (99633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758223be14bf6c71052fd32d6b25ffd5166b527a06b436acc6588a71754d8256`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6861da6c97c304c8e2ed9d94c8e535e0c8458832ddb378851278a924f87d6c42`  
		Last Modified: Tue, 04 Nov 2025 03:21:39 GMT  
		Size: 42.2 MB (42162934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9448ee32852a3a6e4a52afc8f08dd53e824cd98ccac9d74db2c005669ad047a`  
		Last Modified: Tue, 04 Nov 2025 03:21:35 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:42efca8f483cddc63e12d8250d9dd8313f6bc23dfedc3abd3750403804d7b6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e394573be0abf17c648ec23cbf33dcee47e327345de502eb22e4b85fbfb7c3`

```dockerfile
```

-	Layers:
	-	`sha256:3ab20807afc48964b4c227c71583252efe4b22c63ff2a786aadd9701911640d6`  
		Last Modified: Tue, 04 Nov 2025 08:33:43 GMT  
		Size: 3.6 MB (3648276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3169b1aa8b6279ab34ad66ad409146b57db516796ebbafe05a4fcdcea3c45dea`  
		Last Modified: Tue, 04 Nov 2025 08:33:44 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:57aaf1f94039ddae75a3994fc5cef5f06764344fe919ab307acfe522b9ed7995
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
$ docker pull couchdb@sha256:2a7b27021eb330482389d6d0a458365aa3abbf33c95966970dfe473d829362bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138415822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293400da04488d1b9895e016d8aaa255135634d83a12262f02a317bb1df93392`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:30:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 00:31:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:31:07 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:31:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:13 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 04 Nov 2025 00:31:13 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:31:26 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 00:31:26 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 00:31:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa07e0ad136c2d81f08031cacea7cf53591018e635b98792dc196aa25f5ff817`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8530c6a682a670efa2dad1306e54ae7243dde03c298fd4d2314afbe526be8d74`  
		Last Modified: Tue, 04 Nov 2025 00:31:50 GMT  
		Size: 7.7 MB (7692062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbed46138490a32cdc42261c9cc74dbd61554773d5cd1ea6d6a1196313d7633`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 370.5 KB (370474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c6fd493d8273440f4a33bf48cba5e709cecb7890bf493442f3d30c7995927c`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 76.5 KB (76489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5700557c00ad6a97d945d95742339bd0231e8c04c7d53803c425a8ff77a8da64`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82205562d09d1353723fe9dfb290fb140071a479eab8ec17a6a771854f8bdfde`  
		Last Modified: Tue, 04 Nov 2025 00:32:01 GMT  
		Size: 102.2 MB (102169002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075bed437a0f95b0246c5fa38e3ce914b7b19bf0bae1e60b986dfcfaf9ed671e`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50813a568ad5d80449de58f1fa88f33e93d11792b55ab28e527bfa3b1bc9316c`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4b101f7877358209b006590c3cc4c5a30c0a488bf327fd4e8c3d4fc37ee949`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 2.2 KB (2223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba32e7e70af1d2f79e667a87423713201376e2369b85b0f97e7d3fe88c23a30`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:7cb7ee766ece8539a85b77062ae8649036c413e1d2a70493d24ff4fc115e5bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83d91f94a47bb0c4365f76ae4fef42d2e35f877379d22b9962bffea082f1704`

```dockerfile
```

-	Layers:
	-	`sha256:c36180c73e9391c022c084e45caf238e6a8589878bd467fdc26ce5256f33fca7`  
		Last Modified: Tue, 04 Nov 2025 11:33:48 GMT  
		Size: 4.1 MB (4125654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6417cc064e6e4c8735cf98e62c84aae8f155dab00e1888c9f77336417513d71f`  
		Last Modified: Tue, 04 Nov 2025 11:33:49 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:7d0d34b2bd8ccd9a33f1867591d6cf0fa624e3b1006bdbd5654025ac3f31e0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135793031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e587c91bb3579341c572872236fbd4ee2e326b1838d01b1136d13ca436e998`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:17:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:17:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 03:17:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:17:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:28 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 04 Nov 2025 03:19:52 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:20:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 03:20:15 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 03:20:15 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 03:20:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 03:20:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:20:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:20:16 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 03:20:16 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 03:20:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ebf53fbc3e3d769a60213c6f4b514ac2a0bfef8d2cc98e421e7189ae613338`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7269136448c34c9267e49af25de0c0ee12a6b28019ce9018f963e546288181e5`  
		Last Modified: Tue, 04 Nov 2025 03:19:42 GMT  
		Size: 7.4 MB (7398114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d914dba9eba91885244c28bee6394a9e0abe6ffcb48d68e5a1955ad1bc21219e`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 372.1 KB (372121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6479c330dc7ea8c7bce7182bc9a7eb611c9491484db645a0e4f3f8e7885788fa`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 76.5 KB (76504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9470edf29bf6994e89c47deecd6a558a242b0646ca9e3328a885918797f91c7`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b89a5f2d1111c22e5f41446d58663b1d82ab5d0329ba6b08582b2b987220305`  
		Last Modified: Tue, 04 Nov 2025 03:21:10 GMT  
		Size: 101.1 MB (101056323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e010a90a16de6beb0136e22206a21576e2a3e0046e04651d8719c1fa23b732f4`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262cf45231db5237eea2f3dd7dc7ff0edea47f8bc9ea2266a789d998a34952ff`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d0360c36779ed8466cb52e6a129b974f313d35840a7ea23bc8a3b28fa17bdd`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17675d30c8cd72b2e434e73f6c3a1f117f8d4c7c63b46f79e979bcffe1df958a`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a2418d1f77c38958518731f52885b5971598e6cf401d327840b1ea34d9de9d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbb1adb9c833f0c36f50f5051b969eac60839b7da1b5ca1dc4857bd29d3aa6c`

```dockerfile
```

-	Layers:
	-	`sha256:56aed6f64c043e2e4a34464b6a8d5faf7545147543a4ec9b78c6a511bdfedbad`  
		Last Modified: Tue, 04 Nov 2025 08:33:37 GMT  
		Size: 4.1 MB (4121581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9103d442718ed0821b7b9235f5b81f678192a9d60fa0c28645ae8f1fbef723c`  
		Last Modified: Tue, 04 Nov 2025 08:33:38 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:73cec3233025fca7771de3c210356bb503cb8a4c33a83ad61ec68fa1bfd92003
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
$ docker pull couchdb@sha256:6c9cf3dca020d2f49a7756fe8f8105f86d339d18a18e458d843d93acef026407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f6b5cce950c92e5012360057858e0a99cb68bb8213d701e15825f94bf1a849`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:30:58 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 00:31:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:31:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:31:16 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:16 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:31:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 00:31:21 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 00:31:21 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 00:31:21 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 00:31:21 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edcdf1865838daf6de13d2f54e6059b2ae577054f1243c900c51d96eff25016`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0fff095ff52d0d31ad80dcf98768cff07a53dcdc9e52780584470950235995`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 7.7 MB (7692016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829eaec023c87572eb2d4c890b8c5dc90b1779a07ef7e5b523e2bfa236a0fe3`  
		Last Modified: Tue, 04 Nov 2025 00:31:52 GMT  
		Size: 76.7 MB (76691605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce943843a58567bbdca0d02287165f7ce43c55558b3abd3f67630307fc46f5a`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 392.7 KB (392681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f3f6041487d038917d0260cd126c1e043a39d02c9551a19bd8e652909341d4`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 99.4 KB (99425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018defa4077bcb7effc54eb96363849f037e87acf35482b85943d11d814bbfd`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9066acdcf3de579f128c379ccf334603a47dc20a1a17ae720791ccd7bb4bf255`  
		Last Modified: Tue, 04 Nov 2025 00:31:51 GMT  
		Size: 42.3 MB (42338058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dc773705b3ce38bd572ebe6d6e4160480535d7e8f949f0908fac21ba0a7a6f`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c7dbc1f55361fca496f65603d9749809a1ae3f4743a0f0e089492b9b48c6006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9456edb0f9f0c90e8106370e9782aa17a893fbe04183aac243ab250d51d1d6`

```dockerfile
```

-	Layers:
	-	`sha256:cf84fcc0ed95c4f83de2383072e0a58e4c25b30d1a1686999406e013d4026fac`  
		Last Modified: Tue, 04 Nov 2025 11:33:58 GMT  
		Size: 3.7 MB (3656411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbbf19db69c0dd013c389362a7c08bd6befd9a121255d8b11287230a16f693b5`  
		Last Modified: Tue, 04 Nov 2025 11:33:59 GMT  
		Size: 24.4 KB (24384 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:0145626e7a70b53d323a618d7d58a0d49fbf8a9ae8a6c4e3c14f3a07bbf31845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150084175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7128f59709ed6c5239688d86277670a1411bfdfaa882857f7464c74f52d057`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:18:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:18:35 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 03:18:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:18:57 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:57 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:21:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 03:21:06 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 03:21:06 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 03:21:06 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 03:21:06 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7536539bf1ad715cf2dd300635c28f289b63af1cbb92522e91502eef246923`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526e0a76fba7a4a90e9f82e82a2d36b1fb986318a85518bfc9635401a95de3e9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 7.4 MB (7398078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce039d7896ebedadc57a51103ebe71649e42dcf66503771ad322910999b1c820`  
		Last Modified: Tue, 04 Nov 2025 03:19:46 GMT  
		Size: 73.1 MB (73142672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a2015e06dd327a6fa19c3c6249a4fce7b4de27b48d0ffe99bd89193cdc50d`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 394.4 KB (394429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2edba20a7c1a1e969e4475b2647e6299aa0a17f5c863767efe6b0eba76bd8b9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 99.6 KB (99633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758223be14bf6c71052fd32d6b25ffd5166b527a06b436acc6588a71754d8256`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6861da6c97c304c8e2ed9d94c8e535e0c8458832ddb378851278a924f87d6c42`  
		Last Modified: Tue, 04 Nov 2025 03:21:39 GMT  
		Size: 42.2 MB (42162934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9448ee32852a3a6e4a52afc8f08dd53e824cd98ccac9d74db2c005669ad047a`  
		Last Modified: Tue, 04 Nov 2025 03:21:35 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:42efca8f483cddc63e12d8250d9dd8313f6bc23dfedc3abd3750403804d7b6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e394573be0abf17c648ec23cbf33dcee47e327345de502eb22e4b85fbfb7c3`

```dockerfile
```

-	Layers:
	-	`sha256:3ab20807afc48964b4c227c71583252efe4b22c63ff2a786aadd9701911640d6`  
		Last Modified: Tue, 04 Nov 2025 08:33:43 GMT  
		Size: 3.6 MB (3648276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3169b1aa8b6279ab34ad66ad409146b57db516796ebbafe05a4fcdcea3c45dea`  
		Last Modified: Tue, 04 Nov 2025 08:33:44 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:3e9c8b7c53ffa4f72aee9946be19ba043c5f1683d1d3513e7ef918c25b0b9e51
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
$ docker pull couchdb@sha256:747f3dd9d0700f2e00b6b23e5225e327c5d0cb32b4228fe554835185ee85238e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141402338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff8fef6b6221df21026e1bf238dabce906eb4b1870b3399664601796d008d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:12:04 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:12:04 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 11 Nov 2025 20:12:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:12:13 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:12:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:19 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 11 Nov 2025 20:12:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 20:12:32 GMT
VOLUME [/opt/couchdb/data]
# Tue, 11 Nov 2025 20:12:32 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 11 Nov 2025 20:12:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e818c14e4504c76b62137ac42128490a9edd0eb981bf5865a5f0a37e8293dcb`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb7b12cd06b04fb526d8f2e897c715e26715a0b1413f341280c5b55e720190c`  
		Last Modified: Tue, 11 Nov 2025 20:12:56 GMT  
		Size: 7.7 MB (7692023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93af127312a86a7727ba7295aa8ecf10726432730090aacd98fefb313b97cb74`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 370.5 KB (370497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2542ebf23d27b05271c174863bbf1c531afcd3c92b354a5864bc0ab1b0dcd2c0`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 76.5 KB (76472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde3e0e108696404fbf186251f687f55b53261087e3d6edb7461bd3cf5e6a50b`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4e83a949c53ba221bf4f83d75fc3fe47de0f63017ba5fd7302d714d42995d5`  
		Last Modified: Tue, 11 Nov 2025 20:13:07 GMT  
		Size: 105.2 MB (105155535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3619ea51b6069a764b242b0afdbb30d9d0b08ff784c5b167f3d4c25c3babef`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086eb28484449b29b005ea287e7debd61acbcdf72c338f935783890b355e9c2c`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d63ab30b28a48901cbc05d83708e0b45bdf8f5c16b30687d8c2f653abd66c`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7692c35f92eaceb5ec01125b3ca4db18305e24eaf641159c0968f5befe5adee8`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:5c3a0ee184ebcc38eea96429109e6ff55dc7349b7bc52ae1d72988680fb0887d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4a357464b37e2bbf44a258c0e5b0faec86bad1b66ba84686fa15038b6edc45`

```dockerfile
```

-	Layers:
	-	`sha256:fa16bc03b59e15874298a7e9c46492386b6ce5bb2e306ec5623add8efacc12d2`  
		Last Modified: Tue, 11 Nov 2025 23:33:30 GMT  
		Size: 4.2 MB (4184704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f66a1df8f2049aa84c8246571c9a471aae459f12582311af1227d6f853c09f`  
		Last Modified: Tue, 11 Nov 2025 23:33:30 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:a7c89f0e3d2759381bb31bf9e6912a85befed86f9afcaf631646bfad0a778c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e82360d747e07b6797d4d48852268a8744de165f6d1efc09920175ff0fb3ff`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:12:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:12:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 11 Nov 2025 20:12:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:12:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:13:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 11 Nov 2025 20:13:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:13:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Nov 2025 20:13:40 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 11 Nov 2025 20:13:41 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 11 Nov 2025 20:13:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 11 Nov 2025 20:13:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 11 Nov 2025 20:13:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 20:13:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 11 Nov 2025 20:13:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 11 Nov 2025 20:13:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf85f69f108bdd7fd8737e2c27f2b519282c682c926e752d7895b95322a3a1f8`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89683817eaac97bd24a904b06852f30efc3f67cc9062e8d6cc5074a518e0de32`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 7.4 MB (7398221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d59a01d46a74b4685f1a0120f88ae0fa22069ebd8446577ac56fdc4be81a78`  
		Last Modified: Tue, 11 Nov 2025 20:14:53 GMT  
		Size: 372.2 KB (372164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da830badeb2c2860661fcd341daa61de0d1c7b7f4e427d958bbf1ad47da60c0`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 76.6 KB (76617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018650cafb141f99a44532fa2e285ef13c5b18b19e9326ededce63a558428de0`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d0f31299fd049816d258cc751714691ad495fc0e9f756387f780c7916f16b2`  
		Last Modified: Tue, 11 Nov 2025 20:15:01 GMT  
		Size: 104.0 MB (104028538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d4ee4d51885d60b2b6b19360366ddef0c308d2dc44dca0945db503f52c9d6`  
		Last Modified: Tue, 11 Nov 2025 20:14:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15273f74fdd408c496548d519baba1d71827da3e8960735deb034c0be1d4857e`  
		Last Modified: Tue, 11 Nov 2025 20:14:55 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d116eca5b93b315310fa7b0067c21c495f2eb27f7b97ef0d8edb2c269c0d6e`  
		Last Modified: Tue, 11 Nov 2025 20:14:55 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7367b93e2dfb059c851e4be053bdfcf168304d052fc63b7739b282fdb9c39884`  
		Last Modified: Tue, 11 Nov 2025 20:14:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:139efc19ebf539a0422f05ca2d4a24977ddcf9c36142421f2d6781cbe44e1e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ea503310d5049caeb7ea967486b7eb49d0b6fde9cc2c1b3364d3cbf6141244`

```dockerfile
```

-	Layers:
	-	`sha256:9ee8592cfac5e571a5b32b86393d262e6b5b6d176c5ae64ab141a14ecf54a685`  
		Last Modified: Tue, 11 Nov 2025 23:33:35 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c8270c42cc0e6ff8640dbbf7380096bb0774c196b33bf02661cc0c0dd4aa2f`  
		Last Modified: Tue, 11 Nov 2025 23:33:36 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:857efe68d371236f1bdc898da343175868b5efeb9cf9934a13c8e173e786a354
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
$ docker pull couchdb@sha256:09aba0fd985d41d85997a5812bc01ea3a6a4bab791e2a00f65fcbef473eee634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7782988f3e89e74a895aaec8f4fa216315d467dc79ab413ad89b9b1b097ff7dd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:11:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:11:10 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 11 Nov 2025 20:11:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:24 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:11:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:11:31 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:31 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:11:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 11 Nov 2025 20:11:38 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 11 Nov 2025 20:11:38 GMT
VOLUME [/opt/nouveau/data]
# Tue, 11 Nov 2025 20:11:38 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 11 Nov 2025 20:11:38 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7dd6974ccd35b0cb52781f6c8f38ebeac7a5d6260ac6ede11f3f8c9f7fc215`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1f8a4ee6f68ed0ad0430ff95a0098ace6d81921806883704460db6aa1dfd1e`  
		Last Modified: Tue, 11 Nov 2025 20:12:18 GMT  
		Size: 7.7 MB (7692012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a18649a57bbd3cbc1c2fda4ecaf7696bada3bac421f257241f528509e9a1ee`  
		Last Modified: Tue, 11 Nov 2025 20:12:27 GMT  
		Size: 76.7 MB (76691503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42568529e1e6429a35c8c262d9019007ac5da91fabf5742ecd65afee0e60e85`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 392.7 KB (392686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c20c9f876f0937864841173cc872d0b40ab7e4b1e874fd150bed14e316c8737`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 99.4 KB (99415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781ab25ac737fdef9c06353f09faae1dbbd846aa22e6257e1df72655b817015`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88308c4f015c5ccafa012b61f255673fca6103af1fcadce254a335a1cc4c0ce1`  
		Last Modified: Tue, 11 Nov 2025 20:12:21 GMT  
		Size: 42.3 MB (42339027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ffc13d91d0ca731e7f6fcf4b27cb78c9e080738696cfcbc946b53d3b4b1c7b`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:954d2c3f512a1932c0826eaf32a7cafce8d74f498b88dcf002d9dc150d9ffbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a396232965fc39a5cef33e08c673a46005c9b24d8261d634c6669a512cea77`

```dockerfile
```

-	Layers:
	-	`sha256:93e8cb72952640bb24278dc2766189898940a409f998cc1523f49e1aa7a3ab04`  
		Last Modified: Tue, 11 Nov 2025 23:33:42 GMT  
		Size: 3.7 MB (3656729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:685e6f2cdaccaf4f44cc143d00ca81ec0005d0e2f61758c9ab557db887643f85`  
		Last Modified: Tue, 11 Nov 2025 23:33:43 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2a59bc3eeaf33c611e6d20198a2d11c347ab3a09cc5f2a194ece87d4cd6917a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150086583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4df85d89689b925f7108cc12b037e552e41f9ce93759a791748679d571f57a`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:14:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:14:55 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 11 Nov 2025 20:15:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:15:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:15:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:15:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:15:47 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:15:47 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:16:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 11 Nov 2025 20:16:03 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 11 Nov 2025 20:16:03 GMT
VOLUME [/opt/nouveau/data]
# Tue, 11 Nov 2025 20:16:03 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 11 Nov 2025 20:16:03 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3c6f64be9bdd3c2601d8e4c2d7c4354853fff0c19e8f7bdf9b09e8860c24e6`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f243593476a0cede547d1c765b50ea8bc5efa48cb91301386dcac9c5051b81`  
		Last Modified: Tue, 11 Nov 2025 20:17:14 GMT  
		Size: 7.4 MB (7398148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0404524878fe3bbf61b798a9732c238278ceef6c536623058c409670c9c43acb`  
		Last Modified: Tue, 11 Nov 2025 20:17:21 GMT  
		Size: 73.1 MB (73143081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e5e1d70ec4cd7686fe1f025560584c71bd57c0d3c71a06189f1017d9bea5e6`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 394.5 KB (394458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b4a7c215085507f09d210801f506b21c980a71e6e0d6dbd25e7b1f030c6046`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 99.7 KB (99676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e9e3fba2322c92147365dab7fb2e4fee6e9a6fb98242badffe51b399fdd0dc`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef31665d30c90ec5abf16e6d176c05980f28aa8a8a3ac0a2b120622b616d813`  
		Last Modified: Tue, 11 Nov 2025 20:17:18 GMT  
		Size: 42.2 MB (42164789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f743239c3077bc286d9a3930ffc95cabb89849d4301bbd7067f7a6f28a7526`  
		Last Modified: Tue, 11 Nov 2025 20:17:12 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5c5b1bddcc346bbcf0737d83ff70de2b0e7a7ea0e9c8368bdd623d334bf5d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8b0a83d57b365c00a69979a736bd7e27430a4d90e6a47d46120b3f05e3b0e6`

```dockerfile
```

-	Layers:
	-	`sha256:9f369884d273c2e87ce29b44b7345886fdda1a13af7ab4872dce6501aad619bc`  
		Last Modified: Tue, 11 Nov 2025 23:33:47 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c740ff0a68a3faca5335b5543295da9494445384b911e1d54d362c5a109dc315`  
		Last Modified: Tue, 11 Nov 2025 23:33:48 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1`

```console
$ docker pull couchdb@sha256:3e9c8b7c53ffa4f72aee9946be19ba043c5f1683d1d3513e7ef918c25b0b9e51
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
$ docker pull couchdb@sha256:747f3dd9d0700f2e00b6b23e5225e327c5d0cb32b4228fe554835185ee85238e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141402338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff8fef6b6221df21026e1bf238dabce906eb4b1870b3399664601796d008d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:12:04 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:12:04 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 11 Nov 2025 20:12:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:12:13 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:12:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:19 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 11 Nov 2025 20:12:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 20:12:32 GMT
VOLUME [/opt/couchdb/data]
# Tue, 11 Nov 2025 20:12:32 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 11 Nov 2025 20:12:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e818c14e4504c76b62137ac42128490a9edd0eb981bf5865a5f0a37e8293dcb`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb7b12cd06b04fb526d8f2e897c715e26715a0b1413f341280c5b55e720190c`  
		Last Modified: Tue, 11 Nov 2025 20:12:56 GMT  
		Size: 7.7 MB (7692023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93af127312a86a7727ba7295aa8ecf10726432730090aacd98fefb313b97cb74`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 370.5 KB (370497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2542ebf23d27b05271c174863bbf1c531afcd3c92b354a5864bc0ab1b0dcd2c0`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 76.5 KB (76472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde3e0e108696404fbf186251f687f55b53261087e3d6edb7461bd3cf5e6a50b`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4e83a949c53ba221bf4f83d75fc3fe47de0f63017ba5fd7302d714d42995d5`  
		Last Modified: Tue, 11 Nov 2025 20:13:07 GMT  
		Size: 105.2 MB (105155535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3619ea51b6069a764b242b0afdbb30d9d0b08ff784c5b167f3d4c25c3babef`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086eb28484449b29b005ea287e7debd61acbcdf72c338f935783890b355e9c2c`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d63ab30b28a48901cbc05d83708e0b45bdf8f5c16b30687d8c2f653abd66c`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7692c35f92eaceb5ec01125b3ca4db18305e24eaf641159c0968f5befe5adee8`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:5c3a0ee184ebcc38eea96429109e6ff55dc7349b7bc52ae1d72988680fb0887d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4a357464b37e2bbf44a258c0e5b0faec86bad1b66ba84686fa15038b6edc45`

```dockerfile
```

-	Layers:
	-	`sha256:fa16bc03b59e15874298a7e9c46492386b6ce5bb2e306ec5623add8efacc12d2`  
		Last Modified: Tue, 11 Nov 2025 23:33:30 GMT  
		Size: 4.2 MB (4184704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f66a1df8f2049aa84c8246571c9a471aae459f12582311af1227d6f853c09f`  
		Last Modified: Tue, 11 Nov 2025 23:33:30 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; s390x

```console
$ docker pull couchdb@sha256:a7c89f0e3d2759381bb31bf9e6912a85befed86f9afcaf631646bfad0a778c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e82360d747e07b6797d4d48852268a8744de165f6d1efc09920175ff0fb3ff`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:12:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:12:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 11 Nov 2025 20:12:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:12:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:13:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 11 Nov 2025 20:13:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:13:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Nov 2025 20:13:40 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 11 Nov 2025 20:13:41 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 11 Nov 2025 20:13:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 11 Nov 2025 20:13:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 11 Nov 2025 20:13:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 20:13:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 11 Nov 2025 20:13:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 11 Nov 2025 20:13:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf85f69f108bdd7fd8737e2c27f2b519282c682c926e752d7895b95322a3a1f8`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89683817eaac97bd24a904b06852f30efc3f67cc9062e8d6cc5074a518e0de32`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 7.4 MB (7398221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d59a01d46a74b4685f1a0120f88ae0fa22069ebd8446577ac56fdc4be81a78`  
		Last Modified: Tue, 11 Nov 2025 20:14:53 GMT  
		Size: 372.2 KB (372164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da830badeb2c2860661fcd341daa61de0d1c7b7f4e427d958bbf1ad47da60c0`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 76.6 KB (76617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018650cafb141f99a44532fa2e285ef13c5b18b19e9326ededce63a558428de0`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d0f31299fd049816d258cc751714691ad495fc0e9f756387f780c7916f16b2`  
		Last Modified: Tue, 11 Nov 2025 20:15:01 GMT  
		Size: 104.0 MB (104028538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d4ee4d51885d60b2b6b19360366ddef0c308d2dc44dca0945db503f52c9d6`  
		Last Modified: Tue, 11 Nov 2025 20:14:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15273f74fdd408c496548d519baba1d71827da3e8960735deb034c0be1d4857e`  
		Last Modified: Tue, 11 Nov 2025 20:14:55 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d116eca5b93b315310fa7b0067c21c495f2eb27f7b97ef0d8edb2c269c0d6e`  
		Last Modified: Tue, 11 Nov 2025 20:14:55 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7367b93e2dfb059c851e4be053bdfcf168304d052fc63b7739b282fdb9c39884`  
		Last Modified: Tue, 11 Nov 2025 20:14:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:139efc19ebf539a0422f05ca2d4a24977ddcf9c36142421f2d6781cbe44e1e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ea503310d5049caeb7ea967486b7eb49d0b6fde9cc2c1b3364d3cbf6141244`

```dockerfile
```

-	Layers:
	-	`sha256:9ee8592cfac5e571a5b32b86393d262e6b5b6d176c5ae64ab141a14ecf54a685`  
		Last Modified: Tue, 11 Nov 2025 23:33:35 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c8270c42cc0e6ff8640dbbf7380096bb0774c196b33bf02661cc0c0dd4aa2f`  
		Last Modified: Tue, 11 Nov 2025 23:33:36 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1-nouveau`

```console
$ docker pull couchdb@sha256:857efe68d371236f1bdc898da343175868b5efeb9cf9934a13c8e173e786a354
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
$ docker pull couchdb@sha256:09aba0fd985d41d85997a5812bc01ea3a6a4bab791e2a00f65fcbef473eee634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7782988f3e89e74a895aaec8f4fa216315d467dc79ab413ad89b9b1b097ff7dd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:11:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:11:10 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 11 Nov 2025 20:11:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:24 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:11:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:11:31 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:31 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:11:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 11 Nov 2025 20:11:38 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 11 Nov 2025 20:11:38 GMT
VOLUME [/opt/nouveau/data]
# Tue, 11 Nov 2025 20:11:38 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 11 Nov 2025 20:11:38 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7dd6974ccd35b0cb52781f6c8f38ebeac7a5d6260ac6ede11f3f8c9f7fc215`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1f8a4ee6f68ed0ad0430ff95a0098ace6d81921806883704460db6aa1dfd1e`  
		Last Modified: Tue, 11 Nov 2025 20:12:18 GMT  
		Size: 7.7 MB (7692012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a18649a57bbd3cbc1c2fda4ecaf7696bada3bac421f257241f528509e9a1ee`  
		Last Modified: Tue, 11 Nov 2025 20:12:27 GMT  
		Size: 76.7 MB (76691503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42568529e1e6429a35c8c262d9019007ac5da91fabf5742ecd65afee0e60e85`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 392.7 KB (392686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c20c9f876f0937864841173cc872d0b40ab7e4b1e874fd150bed14e316c8737`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 99.4 KB (99415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781ab25ac737fdef9c06353f09faae1dbbd846aa22e6257e1df72655b817015`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88308c4f015c5ccafa012b61f255673fca6103af1fcadce254a335a1cc4c0ce1`  
		Last Modified: Tue, 11 Nov 2025 20:12:21 GMT  
		Size: 42.3 MB (42339027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ffc13d91d0ca731e7f6fcf4b27cb78c9e080738696cfcbc946b53d3b4b1c7b`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:954d2c3f512a1932c0826eaf32a7cafce8d74f498b88dcf002d9dc150d9ffbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a396232965fc39a5cef33e08c673a46005c9b24d8261d634c6669a512cea77`

```dockerfile
```

-	Layers:
	-	`sha256:93e8cb72952640bb24278dc2766189898940a409f998cc1523f49e1aa7a3ab04`  
		Last Modified: Tue, 11 Nov 2025 23:33:42 GMT  
		Size: 3.7 MB (3656729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:685e6f2cdaccaf4f44cc143d00ca81ec0005d0e2f61758c9ab557db887643f85`  
		Last Modified: Tue, 11 Nov 2025 23:33:43 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2a59bc3eeaf33c611e6d20198a2d11c347ab3a09cc5f2a194ece87d4cd6917a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150086583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4df85d89689b925f7108cc12b037e552e41f9ce93759a791748679d571f57a`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:14:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:14:55 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 11 Nov 2025 20:15:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:15:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:15:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:15:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:15:47 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:15:47 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:16:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 11 Nov 2025 20:16:03 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 11 Nov 2025 20:16:03 GMT
VOLUME [/opt/nouveau/data]
# Tue, 11 Nov 2025 20:16:03 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 11 Nov 2025 20:16:03 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3c6f64be9bdd3c2601d8e4c2d7c4354853fff0c19e8f7bdf9b09e8860c24e6`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f243593476a0cede547d1c765b50ea8bc5efa48cb91301386dcac9c5051b81`  
		Last Modified: Tue, 11 Nov 2025 20:17:14 GMT  
		Size: 7.4 MB (7398148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0404524878fe3bbf61b798a9732c238278ceef6c536623058c409670c9c43acb`  
		Last Modified: Tue, 11 Nov 2025 20:17:21 GMT  
		Size: 73.1 MB (73143081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e5e1d70ec4cd7686fe1f025560584c71bd57c0d3c71a06189f1017d9bea5e6`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 394.5 KB (394458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b4a7c215085507f09d210801f506b21c980a71e6e0d6dbd25e7b1f030c6046`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 99.7 KB (99676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e9e3fba2322c92147365dab7fb2e4fee6e9a6fb98242badffe51b399fdd0dc`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef31665d30c90ec5abf16e6d176c05980f28aa8a8a3ac0a2b120622b616d813`  
		Last Modified: Tue, 11 Nov 2025 20:17:18 GMT  
		Size: 42.2 MB (42164789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f743239c3077bc286d9a3930ffc95cabb89849d4301bbd7067f7a6f28a7526`  
		Last Modified: Tue, 11 Nov 2025 20:17:12 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5c5b1bddcc346bbcf0737d83ff70de2b0e7a7ea0e9c8368bdd623d334bf5d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8b0a83d57b365c00a69979a736bd7e27430a4d90e6a47d46120b3f05e3b0e6`

```dockerfile
```

-	Layers:
	-	`sha256:9f369884d273c2e87ce29b44b7345886fdda1a13af7ab4872dce6501aad619bc`  
		Last Modified: Tue, 11 Nov 2025 23:33:47 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c740ff0a68a3faca5335b5543295da9494445384b911e1d54d362c5a109dc315`  
		Last Modified: Tue, 11 Nov 2025 23:33:48 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:3e9c8b7c53ffa4f72aee9946be19ba043c5f1683d1d3513e7ef918c25b0b9e51
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
$ docker pull couchdb@sha256:747f3dd9d0700f2e00b6b23e5225e327c5d0cb32b4228fe554835185ee85238e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141402338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff8fef6b6221df21026e1bf238dabce906eb4b1870b3399664601796d008d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:12:04 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:12:04 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 11 Nov 2025 20:12:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:12:13 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:12:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:19 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 11 Nov 2025 20:12:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 11 Nov 2025 20:12:32 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 20:12:32 GMT
VOLUME [/opt/couchdb/data]
# Tue, 11 Nov 2025 20:12:32 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 11 Nov 2025 20:12:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e818c14e4504c76b62137ac42128490a9edd0eb981bf5865a5f0a37e8293dcb`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb7b12cd06b04fb526d8f2e897c715e26715a0b1413f341280c5b55e720190c`  
		Last Modified: Tue, 11 Nov 2025 20:12:56 GMT  
		Size: 7.7 MB (7692023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93af127312a86a7727ba7295aa8ecf10726432730090aacd98fefb313b97cb74`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 370.5 KB (370497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2542ebf23d27b05271c174863bbf1c531afcd3c92b354a5864bc0ab1b0dcd2c0`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 76.5 KB (76472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde3e0e108696404fbf186251f687f55b53261087e3d6edb7461bd3cf5e6a50b`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4e83a949c53ba221bf4f83d75fc3fe47de0f63017ba5fd7302d714d42995d5`  
		Last Modified: Tue, 11 Nov 2025 20:13:07 GMT  
		Size: 105.2 MB (105155535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3619ea51b6069a764b242b0afdbb30d9d0b08ff784c5b167f3d4c25c3babef`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086eb28484449b29b005ea287e7debd61acbcdf72c338f935783890b355e9c2c`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d63ab30b28a48901cbc05d83708e0b45bdf8f5c16b30687d8c2f653abd66c`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7692c35f92eaceb5ec01125b3ca4db18305e24eaf641159c0968f5befe5adee8`  
		Last Modified: Tue, 11 Nov 2025 20:12:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:5c3a0ee184ebcc38eea96429109e6ff55dc7349b7bc52ae1d72988680fb0887d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4a357464b37e2bbf44a258c0e5b0faec86bad1b66ba84686fa15038b6edc45`

```dockerfile
```

-	Layers:
	-	`sha256:fa16bc03b59e15874298a7e9c46492386b6ce5bb2e306ec5623add8efacc12d2`  
		Last Modified: Tue, 11 Nov 2025 23:33:30 GMT  
		Size: 4.2 MB (4184704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f66a1df8f2049aa84c8246571c9a471aae459f12582311af1227d6f853c09f`  
		Last Modified: Tue, 11 Nov 2025 23:33:30 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:a7c89f0e3d2759381bb31bf9e6912a85befed86f9afcaf631646bfad0a778c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e82360d747e07b6797d4d48852268a8744de165f6d1efc09920175ff0fb3ff`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:12:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:12:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 11 Nov 2025 20:12:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:12:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:13:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 11 Nov 2025 20:13:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:13:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Nov 2025 20:13:40 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 11 Nov 2025 20:13:41 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 11 Nov 2025 20:13:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 11 Nov 2025 20:13:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 11 Nov 2025 20:13:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 20:13:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 11 Nov 2025 20:13:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 11 Nov 2025 20:13:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf85f69f108bdd7fd8737e2c27f2b519282c682c926e752d7895b95322a3a1f8`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89683817eaac97bd24a904b06852f30efc3f67cc9062e8d6cc5074a518e0de32`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 7.4 MB (7398221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d59a01d46a74b4685f1a0120f88ae0fa22069ebd8446577ac56fdc4be81a78`  
		Last Modified: Tue, 11 Nov 2025 20:14:53 GMT  
		Size: 372.2 KB (372164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da830badeb2c2860661fcd341daa61de0d1c7b7f4e427d958bbf1ad47da60c0`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 76.6 KB (76617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018650cafb141f99a44532fa2e285ef13c5b18b19e9326ededce63a558428de0`  
		Last Modified: Tue, 11 Nov 2025 20:14:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d0f31299fd049816d258cc751714691ad495fc0e9f756387f780c7916f16b2`  
		Last Modified: Tue, 11 Nov 2025 20:15:01 GMT  
		Size: 104.0 MB (104028538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d4ee4d51885d60b2b6b19360366ddef0c308d2dc44dca0945db503f52c9d6`  
		Last Modified: Tue, 11 Nov 2025 20:14:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15273f74fdd408c496548d519baba1d71827da3e8960735deb034c0be1d4857e`  
		Last Modified: Tue, 11 Nov 2025 20:14:55 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d116eca5b93b315310fa7b0067c21c495f2eb27f7b97ef0d8edb2c269c0d6e`  
		Last Modified: Tue, 11 Nov 2025 20:14:55 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7367b93e2dfb059c851e4be053bdfcf168304d052fc63b7739b282fdb9c39884`  
		Last Modified: Tue, 11 Nov 2025 20:14:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:139efc19ebf539a0422f05ca2d4a24977ddcf9c36142421f2d6781cbe44e1e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ea503310d5049caeb7ea967486b7eb49d0b6fde9cc2c1b3364d3cbf6141244`

```dockerfile
```

-	Layers:
	-	`sha256:9ee8592cfac5e571a5b32b86393d262e6b5b6d176c5ae64ab141a14ecf54a685`  
		Last Modified: Tue, 11 Nov 2025 23:33:35 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c8270c42cc0e6ff8640dbbf7380096bb0774c196b33bf02661cc0c0dd4aa2f`  
		Last Modified: Tue, 11 Nov 2025 23:33:36 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json
