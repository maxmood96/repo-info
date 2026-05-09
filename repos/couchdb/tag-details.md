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
$ docker pull couchdb@sha256:f931b65dd7406c03e1c83ffc7c04b6d551dc18df1ce8581a04f17cdffcb20e23
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
$ docker pull couchdb@sha256:b4e774adf2b8222bfcd5ccb88dfdca3d8ccbade23c44a5b052b27dca5fa2a0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4854060e48cafa0f1741faa1bf70bb809d0d90aed1c9f63e7a86186467b8f8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:41:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:41:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 19:41:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:41:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:41:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:13 GMT
ENV COUCHDB_VERSION=3.5.1
# Fri, 08 May 2026 19:41:13 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:41:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 19:41:27 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 19:41:27 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 19:41:27 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 19:41:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:41:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:41:27 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 19:41:27 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 19:41:27 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4619b10b6abb0c6e1498cedfc95d38f4c4a0ec385e9e9ebd8c86fc1faf0fa03`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e32228c19e744810ff941d44efdce42b089f2c30deb9057dd768222f6ad5d5`  
		Last Modified: Fri, 08 May 2026 19:41:41 GMT  
		Size: 7.9 MB (7883564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d987204986674deb3f0247644e89099f4e271b1ad27b27b4e819af33dd375ba`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 401.8 KB (401782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe5b1440c65cd5e40e2131e2a01210b449987fe7babb9db4e8232665f4c8e27`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 76.5 KB (76509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a34fa4a7b947dbc66b6bb75f80082e43923d75b15aa892bd5628dc2a2cd024`  
		Last Modified: Fri, 08 May 2026 19:41:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612a697d0527fa1e4c5e621474a561b106e23f96e3f7218762636a1c2a16c48c`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 105.5 MB (105455460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9990217fbeb1bf28489085b2d6c496c05b43ac91cd07bc3d9271831d0a45d55`  
		Last Modified: Fri, 08 May 2026 19:41:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c553ad59996c3c835f4707a465d98c330e0f3f837f8fd7685aeee28a5306d6`  
		Last Modified: Fri, 08 May 2026 19:41:42 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33c3cb69356151284e190eceafdf1a1af7698d22242e0d48fef7924643a5f19`  
		Last Modified: Fri, 08 May 2026 19:41:43 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88011fc5d8e4342ae7ab0f2e409ea625989648da5eacaf3f435b51b008a04ff9`  
		Last Modified: Fri, 08 May 2026 19:41:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d665e41a3958b2c857dffe329418cb0b37a267b847e76ac9676cafec7d473eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403c820e5f8a69976dd97287f8c279a89df210fa8e5a78791f2aee2c114d4ea3`

```dockerfile
```

-	Layers:
	-	`sha256:ed0ec04f88ec623bbc0330c35dcdcd60f1e0372a0a7891103d08301ac002e0d9`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:993c18731410769aa30fa2a6f735e7e559c0b57da4820779fde73acf71d18c2c`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 31.7 KB (31737 bytes)  
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
$ docker pull couchdb@sha256:c17b9c2e29cd7c24179e58c4a37679a612654bdc0724078ab6a7a9b9e8ba4509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a64aa7574803e3c0686efa10943fb8560b0be2b6e1c9a15fe28035491c96431`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:54:00 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 20:54:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 20:54:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 20:54:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 20:54:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:54:16 GMT
ENV COUCHDB_VERSION=3.5.1
# Fri, 08 May 2026 20:54:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 20:54:35 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 20:54:35 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 20:54:35 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 20:54:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 20:54:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:54:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 20:54:35 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 20:54:35 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 20:54:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bffdf210de6acd187924745c5f9c5314f8b55a1712d8bc6ce811afdcaa8e84a`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c217f32eeb936018a0c3c2fd74f2250ea8c6227a3771bb06459662b812496f1`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 7.4 MB (7399519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6302c90d53931f2ac2569cfc71909681a79de3c0e4206ad2f72b0de1377c3a3`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 372.1 KB (372128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2441149aa3bca98c888cb93803232a1d8e227b8f2017b02042133d788e38c412`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 76.6 KB (76560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054fb689d6f1adbe57be588c3e5bc758f6f4c48fb2e57d4d2faef44d9be62cf9`  
		Last Modified: Fri, 08 May 2026 20:54:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b605ada1b3f7a065ce357b7761b6aca4bd7cb73a39b992ec4de6ba0e56f6f2`  
		Last Modified: Fri, 08 May 2026 20:54:58 GMT  
		Size: 104.0 MB (104028251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb74222b0ecd7c2158056d339f503142ac6bfa06bafa618b6c5f0a257656d2f`  
		Last Modified: Fri, 08 May 2026 20:54:56 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0008b3e90609955167dd06800d273d8d91866fbc9e2c81c84eb50a49bc8f27b`  
		Last Modified: Fri, 08 May 2026 20:54:56 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db4bf2f25d8048db6e3e7ea6232159ae2c46ff83f94586d34cd98922ca56e84`  
		Last Modified: Fri, 08 May 2026 20:54:57 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc348bec92209fe9c2c0e01799d2d786221c1befc2801ba468d13ec19427ee15`  
		Last Modified: Fri, 08 May 2026 20:54:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:8d90adb3d3145b44d103b26e9de0c1b0568f86c9f6471b900ad34ff1b817265f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d86237d1a166ca30d9884aa426bf321b0211658e837746110628260cb2ce28`

```dockerfile
```

-	Layers:
	-	`sha256:512c543656a3ebd4aa97b2bd8c2faa305eab0d944b9818281d57463c79d68c82`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa943442d0c72601e50625c99255b86368ad0097049e724d02e0d5a6401b443`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:525c7b6c150f9f3156f292423550dcc9c2a993854d377edf7204746a9ecbbd8d
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
$ docker pull couchdb@sha256:1c8ed68a20598dd0a47725e415f31896306fb5271649a9c2f3c7fcea2c93f2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156560003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03070c7fe084b855af980751395897652d9484ae9c2894931c8b570b1c5d17b`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:41:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:41:03 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 19:41:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:41:19 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:41:23 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:23 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:41:30 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 19:41:30 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 19:41:30 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 19:41:30 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 19:41:30 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c7ab9d7d84ce7427da1600d83e8009cb4f72036cac8e9a138c7505bb63ff51`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231e5c29d488c066806a365cf6bb2d290aeaa545bd367af47436f0ecfa5a68ae`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 7.9 MB (7883617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7503e94334f5e73bc32565e38762c538300f41a45d6a73692e838a342ce60e7d`  
		Last Modified: Fri, 08 May 2026 19:41:47 GMT  
		Size: 77.5 MB (77477951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7160133021d40bd64badd6655f732af1202536e922e37073564653a0f3bd6c1a`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 424.2 KB (424177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cec1429d6b2adacc17f61c8ca26a4cacac478ff6a3d55d14d6d59dcb0dda42c`  
		Last Modified: Fri, 08 May 2026 19:41:46 GMT  
		Size: 99.6 KB (99609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0331cdde4df19f092c9096cfa20ba0f3a7e604f262d5748f1b63967d566f434c`  
		Last Modified: Fri, 08 May 2026 19:41:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8f649c189a4318c0b7e870174aaa0ba4b231fe2fec61d938abbd00f2a8176`  
		Last Modified: Fri, 08 May 2026 19:41:48 GMT  
		Size: 42.4 MB (42436487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e604c15b77c5d906ced67623fc48d60e476012975f560056caed3d6173584`  
		Last Modified: Fri, 08 May 2026 19:41:47 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:65c2afef44a5239797450662121609e95a41d383e1c4972afa6e1013649b8250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3683426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fc2889da0df2dbdd746e2816bc8c997f37ff0e501acb986b08690644d2b666`

```dockerfile
```

-	Layers:
	-	`sha256:7645076ef6b1e13740ce071950ee3be1bc1781448b723d9b4e461c4b249bf721`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 3.7 MB (3658905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f1a071fa129af25c67b27db8f7fde8ea52ab2c7ab4b090bc5c0f057110a4a34`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
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
$ docker pull couchdb@sha256:4e8ce916270d6a33d52e187a6b1f1d2a5611790bf4479221ce113ac2c05c639d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150176402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c869967615fb1ceec6b922141cbb44583aa8637d438ef1eac66cbce43074303e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:54:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 20:54:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 20:54:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 20:55:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 20:55:10 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:10 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 20:55:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 20:55:18 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 20:55:18 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 20:55:18 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 20:55:18 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f53678fa637a5499e3a4c784e7bb9583bd679b5614fbc9ea063ebca22208f7`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e30253fb9558a325c75e8f8cd67d9ba29a4e3d983bc5273c45e7903f35e39c9`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 7.4 MB (7399527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c91ec9cb9119e4e999f79883f51cf69f4e94f5c1c40d673e7184c57b65201a`  
		Last Modified: Fri, 08 May 2026 20:55:43 GMT  
		Size: 73.2 MB (73224500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e09d6b9027e946b15506c40b1e41958b69bbe62fe7cc900c1468b87b5808ec`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 394.5 KB (394514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797e561a1d9086bb1eda68cf769149c66f115a9d365d9a9c76df7609d91d7f42`  
		Last Modified: Fri, 08 May 2026 20:55:42 GMT  
		Size: 99.6 KB (99639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fee3818ac597f228d126b69b2fdc9512433d65517936f182d3ecf7990f74a9`  
		Last Modified: Fri, 08 May 2026 20:55:42 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e9d902cb7040bc7ed5500b783451f3294f473b24615629e74a0a83a9e97277`  
		Last Modified: Fri, 08 May 2026 20:55:43 GMT  
		Size: 42.2 MB (42164737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d9e838a98401c25366b24f102b4ed3dbe7be3b60e29f87dd46fc2887441162`  
		Last Modified: Fri, 08 May 2026 20:55:43 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5201491b408694ede3240ebdf282369ab9cd22edc6f19b433ce6f7864d839cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433a8dd5c2a258926aaa88e2a4787ed2907aeeffe23d3fe2213ec30119c62fd7`

```dockerfile
```

-	Layers:
	-	`sha256:d965b3e99f31ca622604c2a3d04d027e83dd9ee89a720bf2cbd5812cc706b3a1`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 3.6 MB (3649438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3a50adc1e3c135fc555f900a110f8257e34089270903d64a6e59edb4825dd5`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:0e3999e6f460dea5051824c80a8709a877fe4ebe4c31c1490026f1c238deb665
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
$ docker pull couchdb@sha256:f0f4d97618fdc0cdc56d249d1e0050e182ebc12a985bb8f26a32ad7abb702f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139023477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2643635bf9e349f1e0091dcdb1879ed611509fbb41585d70f614bcf0c677d94a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:41:04 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:41:04 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 19:41:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:41:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
ENV COUCHDB_VERSION=3.4.3
# Fri, 08 May 2026 19:41:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:41:30 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 19:41:30 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 19:41:30 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 19:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 19:41:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:41:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:41:30 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 19:41:30 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 19:41:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e64862ee019faabf215dc8e34f93da3603e2eb4b898fe30e05b7b1e8f532a14`  
		Last Modified: Fri, 08 May 2026 19:41:44 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381fa81f8978c7630055998bab4b5abe8fcff01315c91e34035041015aea4666`  
		Last Modified: Fri, 08 May 2026 19:41:44 GMT  
		Size: 7.9 MB (7883475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9e80a4b8c8a477a8e14c6310d215b3d6cf482458ddba467ed231386ea82d1c`  
		Last Modified: Fri, 08 May 2026 19:41:44 GMT  
		Size: 401.8 KB (401784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10e5c7bb8b39cb0034d3e18dbe749438790b7333475d056c3a8818d5458aa90`  
		Last Modified: Fri, 08 May 2026 19:41:44 GMT  
		Size: 76.5 KB (76502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647c9028c3d5b3b7aa7d2f0321b192ad6fd1a25c95cf33e9973ebbd94af53407`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab42673d17d08db468fd00e924615a3b6e217a66db9fd753df962ed8ff6e21a`  
		Last Modified: Fri, 08 May 2026 19:41:48 GMT  
		Size: 102.4 MB (102419993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9ad7da7d3eaceedd95da7113429b8de24f26557db871c56fe9945ac0dbec67`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faaca5d9c610cf9981918e6eece909f00f9954c1a0eabd8c65a23dbd6cfceef`  
		Last Modified: Fri, 08 May 2026 19:41:46 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794097fa0fb65465ff42478f0ee5aee9a3a53f2d15a1406ba344cd85349ebad4`  
		Last Modified: Fri, 08 May 2026 19:41:46 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165f71102f9ef153af852cc65a581b4c522ebde7284920d35f8209e35d6d99ba`  
		Last Modified: Fri, 08 May 2026 19:41:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:eeb935530f75393519f89bbddc27774170d4240805f3a2fe61fc32c73231af0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f2efc46b9d4dc11c080e4bcf7d6baf85403c926a321b4305e417a5a10bb391`

```dockerfile
```

-	Layers:
	-	`sha256:253229fef57d431b70c745566bba94280c734528b244c1213ff6b64785f0d11e`  
		Last Modified: Fri, 08 May 2026 19:41:44 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1013c1b199bb3c16394c154d4ff84b5fd6cbb304647a3c510586543dc4a82040`  
		Last Modified: Fri, 08 May 2026 19:41:44 GMT  
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
$ docker pull couchdb@sha256:2e0db690efeba842536a9da81025e178a05f9fd2d7ed3ea1df84980fd9152f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135801523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6698300bfbf4a94f57ddab362ddf81af7bb0fd8abdf6235a5514e5f8544cfa76`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:54:00 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 20:54:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 20:54:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 20:54:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 20:54:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:54:16 GMT
ENV COUCHDB_VERSION=3.4.3
# Fri, 08 May 2026 20:55:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 20:55:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 20:55:32 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 20:55:32 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 20:55:32 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 20:55:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:55:32 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 20:55:32 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 20:55:32 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 20:55:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bffdf210de6acd187924745c5f9c5314f8b55a1712d8bc6ce811afdcaa8e84a`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c217f32eeb936018a0c3c2fd74f2250ea8c6227a3771bb06459662b812496f1`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 7.4 MB (7399519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6302c90d53931f2ac2569cfc71909681a79de3c0e4206ad2f72b0de1377c3a3`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 372.1 KB (372128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2441149aa3bca98c888cb93803232a1d8e227b8f2017b02042133d788e38c412`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 76.6 KB (76560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba02b68706386ae9f0084523bf108c85a5f1c965826d8c37e8d3cf9205fa81e`  
		Last Modified: Fri, 08 May 2026 20:55:53 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f770b7cd84a544e602dfaf4b03609abd83c2a4e9ec8fddb5cb2ee86f084c4e91`  
		Last Modified: Fri, 08 May 2026 20:55:55 GMT  
		Size: 101.1 MB (101056277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf83af87d0afde258a91922f5fb6db61a143727c64cf843a8519cac7d6e7ca3`  
		Last Modified: Fri, 08 May 2026 20:55:53 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4196f601061499e997d76af1f7828bb7daba965d992d9f9c0f57064edffd1c20`  
		Last Modified: Fri, 08 May 2026 20:55:53 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9c384321576a8d96030de378ae462db27b8bd45e16b5e142ccd553fe467a86`  
		Last Modified: Fri, 08 May 2026 20:55:54 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ebfea0d0232337527793bacd46b1bffef91e6988ccf71ef3636f207eb1de5`  
		Last Modified: Fri, 08 May 2026 20:55:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:df44a512c3340c2dac66d91f12ddb9d8fffa16dc27c0d1695710d225b3168f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396492aaba8f2868601617820c6dd9093dfc1d3863271a1b90e2e97d01d535b5`

```dockerfile
```

-	Layers:
	-	`sha256:f98207dd896ce820b90510a5dcfa66ac6f11d03f5826ca3aa2ebc2696d5c7c7b`  
		Last Modified: Fri, 08 May 2026 20:55:53 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffa650ea671f93b97a290a93854261019000b439725f9763983a036865851b91`  
		Last Modified: Fri, 08 May 2026 20:55:52 GMT  
		Size: 31.1 KB (31147 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:fdc172cebb5343b159a8a8b25aa9ca33e93da41911aaed21cc9a8928b0df14b0
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
$ docker pull couchdb@sha256:ea9d6a76e3c74d6a51b51b25e99d323a5d343d903bf7481775a4c64766dabc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156559456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef416f38d34f483c59daf4b8e84d69848a44b01aa6e633dd2a70e1896fe8bd30`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:41:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:41:06 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 19:41:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:41:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:41:27 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:27 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:41:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 19:41:32 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 19:41:32 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 19:41:32 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 19:41:32 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6fb7f6be18fe20d2e0900d3075f3b0b002e27cf7d0a9b5c8cf8807ecca6d65`  
		Last Modified: Fri, 08 May 2026 19:41:47 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6928e8cba535481b437845f4e2ffbae171db06d759c8bcda4e8ea1ecf7bd93d`  
		Last Modified: Fri, 08 May 2026 19:41:48 GMT  
		Size: 7.9 MB (7883579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1366a26d9023b42a091042f90371594446f426a16940cb83036ecbdda88d3f29`  
		Last Modified: Fri, 08 May 2026 19:41:50 GMT  
		Size: 77.5 MB (77477852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b1f61e56105037ad5d6ca7e8429119e6cc2b69bf474963f73bade4c25f256c`  
		Last Modified: Fri, 08 May 2026 19:41:47 GMT  
		Size: 424.2 KB (424177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f481a3ea7b852abb4b23555a9fa8eee4cb4e93df56ba54670a7e7e7885eaf1ee`  
		Last Modified: Fri, 08 May 2026 19:41:49 GMT  
		Size: 99.6 KB (99562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ae64234583c5f4ca3759604020bcff1e18a1fdd22202d23e946651ad2cbf94`  
		Last Modified: Fri, 08 May 2026 19:41:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d415aa363b4e81fdebb32340e2157da45ebd7f0ac04ef8ae20767e40448f81ee`  
		Last Modified: Fri, 08 May 2026 19:41:51 GMT  
		Size: 42.4 MB (42436121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b903081777986bd9307653ebaddca1d29cbd4cc19f9848ddf47bfbcf6281966`  
		Last Modified: Fri, 08 May 2026 19:41:50 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:afc97efa8a7e10030d36bc42fd5887d851a8b9b39060c143dd96f43ccb8a3485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e6644c08668d778ef5b6dd589271cce027a59b67cb06602a7b9f147ad7557f`

```dockerfile
```

-	Layers:
	-	`sha256:ad45e90621a60beec02dbc72fda74396e6603740add3b160705d6002897feabf`  
		Last Modified: Fri, 08 May 2026 19:41:48 GMT  
		Size: 3.7 MB (3658599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:518fe30626f8b4e448c8d89e577e5853c5752a9be8058d571c0341c40b733620`  
		Last Modified: Fri, 08 May 2026 19:41:47 GMT  
		Size: 24.2 KB (24214 bytes)  
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
$ docker pull couchdb@sha256:1de1521751b7769725fa5397168698eb3454cc8bb79fcae620d60dca6d66eab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150174648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da646382d5435cbefd73a22f910fed04f60e956f62b3af3d116f459739fa4f1a`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:54:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 20:54:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 20:54:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 20:55:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 20:55:10 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:10 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 20:56:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 20:56:10 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 20:56:10 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 20:56:10 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 20:56:10 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f53678fa637a5499e3a4c784e7bb9583bd679b5614fbc9ea063ebca22208f7`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e30253fb9558a325c75e8f8cd67d9ba29a4e3d983bc5273c45e7903f35e39c9`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 7.4 MB (7399527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c91ec9cb9119e4e999f79883f51cf69f4e94f5c1c40d673e7184c57b65201a`  
		Last Modified: Fri, 08 May 2026 20:55:43 GMT  
		Size: 73.2 MB (73224500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e09d6b9027e946b15506c40b1e41958b69bbe62fe7cc900c1468b87b5808ec`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 394.5 KB (394514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797e561a1d9086bb1eda68cf769149c66f115a9d365d9a9c76df7609d91d7f42`  
		Last Modified: Fri, 08 May 2026 20:55:42 GMT  
		Size: 99.6 KB (99639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fee3818ac597f228d126b69b2fdc9512433d65517936f182d3ecf7990f74a9`  
		Last Modified: Fri, 08 May 2026 20:55:42 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c84ccc0442845866606ba196b0edcf0e6bb1d9d581e56790dc8f03a06d53381`  
		Last Modified: Fri, 08 May 2026 20:56:26 GMT  
		Size: 42.2 MB (42162984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ef726f0b9f03625b32f87005f8a7337cad2a0df213fe22733e1bee9e691aba`  
		Last Modified: Fri, 08 May 2026 20:56:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc40d3e0ccfc41cc447d25488094e6a0b3f0c5b1459e5552688eaa2495bfe087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69761afb72786395c7b70e19d864f4ec48fa33b42e3b4bb7b4d7de44c5797eab`

```dockerfile
```

-	Layers:
	-	`sha256:cbfd4f6a7fb0a972da68b511a3e672a9ab5b90efea527ed735192f28c0389c52`  
		Last Modified: Fri, 08 May 2026 20:56:25 GMT  
		Size: 3.6 MB (3649132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:013298f6b17b6beaea2a73ad28e80a47136ef5eb76b74cea4df8a5e7fe69a832`  
		Last Modified: Fri, 08 May 2026 20:56:25 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:0e3999e6f460dea5051824c80a8709a877fe4ebe4c31c1490026f1c238deb665
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
$ docker pull couchdb@sha256:f0f4d97618fdc0cdc56d249d1e0050e182ebc12a985bb8f26a32ad7abb702f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139023477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2643635bf9e349f1e0091dcdb1879ed611509fbb41585d70f614bcf0c677d94a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:41:04 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:41:04 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 19:41:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:41:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
ENV COUCHDB_VERSION=3.4.3
# Fri, 08 May 2026 19:41:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:41:30 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 19:41:30 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 19:41:30 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 19:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 19:41:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:41:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:41:30 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 19:41:30 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 19:41:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e64862ee019faabf215dc8e34f93da3603e2eb4b898fe30e05b7b1e8f532a14`  
		Last Modified: Fri, 08 May 2026 19:41:44 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381fa81f8978c7630055998bab4b5abe8fcff01315c91e34035041015aea4666`  
		Last Modified: Fri, 08 May 2026 19:41:44 GMT  
		Size: 7.9 MB (7883475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9e80a4b8c8a477a8e14c6310d215b3d6cf482458ddba467ed231386ea82d1c`  
		Last Modified: Fri, 08 May 2026 19:41:44 GMT  
		Size: 401.8 KB (401784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10e5c7bb8b39cb0034d3e18dbe749438790b7333475d056c3a8818d5458aa90`  
		Last Modified: Fri, 08 May 2026 19:41:44 GMT  
		Size: 76.5 KB (76502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647c9028c3d5b3b7aa7d2f0321b192ad6fd1a25c95cf33e9973ebbd94af53407`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab42673d17d08db468fd00e924615a3b6e217a66db9fd753df962ed8ff6e21a`  
		Last Modified: Fri, 08 May 2026 19:41:48 GMT  
		Size: 102.4 MB (102419993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9ad7da7d3eaceedd95da7113429b8de24f26557db871c56fe9945ac0dbec67`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faaca5d9c610cf9981918e6eece909f00f9954c1a0eabd8c65a23dbd6cfceef`  
		Last Modified: Fri, 08 May 2026 19:41:46 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794097fa0fb65465ff42478f0ee5aee9a3a53f2d15a1406ba344cd85349ebad4`  
		Last Modified: Fri, 08 May 2026 19:41:46 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165f71102f9ef153af852cc65a581b4c522ebde7284920d35f8209e35d6d99ba`  
		Last Modified: Fri, 08 May 2026 19:41:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:eeb935530f75393519f89bbddc27774170d4240805f3a2fe61fc32c73231af0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f2efc46b9d4dc11c080e4bcf7d6baf85403c926a321b4305e417a5a10bb391`

```dockerfile
```

-	Layers:
	-	`sha256:253229fef57d431b70c745566bba94280c734528b244c1213ff6b64785f0d11e`  
		Last Modified: Fri, 08 May 2026 19:41:44 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1013c1b199bb3c16394c154d4ff84b5fd6cbb304647a3c510586543dc4a82040`  
		Last Modified: Fri, 08 May 2026 19:41:44 GMT  
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
$ docker pull couchdb@sha256:2e0db690efeba842536a9da81025e178a05f9fd2d7ed3ea1df84980fd9152f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135801523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6698300bfbf4a94f57ddab362ddf81af7bb0fd8abdf6235a5514e5f8544cfa76`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:54:00 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 20:54:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 20:54:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 20:54:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 20:54:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:54:16 GMT
ENV COUCHDB_VERSION=3.4.3
# Fri, 08 May 2026 20:55:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 20:55:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 20:55:32 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 20:55:32 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 20:55:32 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 20:55:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:55:32 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 20:55:32 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 20:55:32 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 20:55:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bffdf210de6acd187924745c5f9c5314f8b55a1712d8bc6ce811afdcaa8e84a`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c217f32eeb936018a0c3c2fd74f2250ea8c6227a3771bb06459662b812496f1`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 7.4 MB (7399519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6302c90d53931f2ac2569cfc71909681a79de3c0e4206ad2f72b0de1377c3a3`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 372.1 KB (372128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2441149aa3bca98c888cb93803232a1d8e227b8f2017b02042133d788e38c412`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 76.6 KB (76560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba02b68706386ae9f0084523bf108c85a5f1c965826d8c37e8d3cf9205fa81e`  
		Last Modified: Fri, 08 May 2026 20:55:53 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f770b7cd84a544e602dfaf4b03609abd83c2a4e9ec8fddb5cb2ee86f084c4e91`  
		Last Modified: Fri, 08 May 2026 20:55:55 GMT  
		Size: 101.1 MB (101056277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf83af87d0afde258a91922f5fb6db61a143727c64cf843a8519cac7d6e7ca3`  
		Last Modified: Fri, 08 May 2026 20:55:53 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4196f601061499e997d76af1f7828bb7daba965d992d9f9c0f57064edffd1c20`  
		Last Modified: Fri, 08 May 2026 20:55:53 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9c384321576a8d96030de378ae462db27b8bd45e16b5e142ccd553fe467a86`  
		Last Modified: Fri, 08 May 2026 20:55:54 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ebfea0d0232337527793bacd46b1bffef91e6988ccf71ef3636f207eb1de5`  
		Last Modified: Fri, 08 May 2026 20:55:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:df44a512c3340c2dac66d91f12ddb9d8fffa16dc27c0d1695710d225b3168f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396492aaba8f2868601617820c6dd9093dfc1d3863271a1b90e2e97d01d535b5`

```dockerfile
```

-	Layers:
	-	`sha256:f98207dd896ce820b90510a5dcfa66ac6f11d03f5826ca3aa2ebc2696d5c7c7b`  
		Last Modified: Fri, 08 May 2026 20:55:53 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffa650ea671f93b97a290a93854261019000b439725f9763983a036865851b91`  
		Last Modified: Fri, 08 May 2026 20:55:52 GMT  
		Size: 31.1 KB (31147 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:fdc172cebb5343b159a8a8b25aa9ca33e93da41911aaed21cc9a8928b0df14b0
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
$ docker pull couchdb@sha256:ea9d6a76e3c74d6a51b51b25e99d323a5d343d903bf7481775a4c64766dabc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156559456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef416f38d34f483c59daf4b8e84d69848a44b01aa6e633dd2a70e1896fe8bd30`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:41:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:41:06 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 19:41:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:41:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:41:27 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:27 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:41:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 19:41:32 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 19:41:32 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 19:41:32 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 19:41:32 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6fb7f6be18fe20d2e0900d3075f3b0b002e27cf7d0a9b5c8cf8807ecca6d65`  
		Last Modified: Fri, 08 May 2026 19:41:47 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6928e8cba535481b437845f4e2ffbae171db06d759c8bcda4e8ea1ecf7bd93d`  
		Last Modified: Fri, 08 May 2026 19:41:48 GMT  
		Size: 7.9 MB (7883579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1366a26d9023b42a091042f90371594446f426a16940cb83036ecbdda88d3f29`  
		Last Modified: Fri, 08 May 2026 19:41:50 GMT  
		Size: 77.5 MB (77477852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b1f61e56105037ad5d6ca7e8429119e6cc2b69bf474963f73bade4c25f256c`  
		Last Modified: Fri, 08 May 2026 19:41:47 GMT  
		Size: 424.2 KB (424177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f481a3ea7b852abb4b23555a9fa8eee4cb4e93df56ba54670a7e7e7885eaf1ee`  
		Last Modified: Fri, 08 May 2026 19:41:49 GMT  
		Size: 99.6 KB (99562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ae64234583c5f4ca3759604020bcff1e18a1fdd22202d23e946651ad2cbf94`  
		Last Modified: Fri, 08 May 2026 19:41:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d415aa363b4e81fdebb32340e2157da45ebd7f0ac04ef8ae20767e40448f81ee`  
		Last Modified: Fri, 08 May 2026 19:41:51 GMT  
		Size: 42.4 MB (42436121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b903081777986bd9307653ebaddca1d29cbd4cc19f9848ddf47bfbcf6281966`  
		Last Modified: Fri, 08 May 2026 19:41:50 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:afc97efa8a7e10030d36bc42fd5887d851a8b9b39060c143dd96f43ccb8a3485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e6644c08668d778ef5b6dd589271cce027a59b67cb06602a7b9f147ad7557f`

```dockerfile
```

-	Layers:
	-	`sha256:ad45e90621a60beec02dbc72fda74396e6603740add3b160705d6002897feabf`  
		Last Modified: Fri, 08 May 2026 19:41:48 GMT  
		Size: 3.7 MB (3658599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:518fe30626f8b4e448c8d89e577e5853c5752a9be8058d571c0341c40b733620`  
		Last Modified: Fri, 08 May 2026 19:41:47 GMT  
		Size: 24.2 KB (24214 bytes)  
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
$ docker pull couchdb@sha256:1de1521751b7769725fa5397168698eb3454cc8bb79fcae620d60dca6d66eab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150174648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da646382d5435cbefd73a22f910fed04f60e956f62b3af3d116f459739fa4f1a`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:54:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 20:54:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 20:54:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 20:55:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 20:55:10 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:10 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 20:56:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 20:56:10 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 20:56:10 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 20:56:10 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 20:56:10 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f53678fa637a5499e3a4c784e7bb9583bd679b5614fbc9ea063ebca22208f7`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e30253fb9558a325c75e8f8cd67d9ba29a4e3d983bc5273c45e7903f35e39c9`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 7.4 MB (7399527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c91ec9cb9119e4e999f79883f51cf69f4e94f5c1c40d673e7184c57b65201a`  
		Last Modified: Fri, 08 May 2026 20:55:43 GMT  
		Size: 73.2 MB (73224500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e09d6b9027e946b15506c40b1e41958b69bbe62fe7cc900c1468b87b5808ec`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 394.5 KB (394514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797e561a1d9086bb1eda68cf769149c66f115a9d365d9a9c76df7609d91d7f42`  
		Last Modified: Fri, 08 May 2026 20:55:42 GMT  
		Size: 99.6 KB (99639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fee3818ac597f228d126b69b2fdc9512433d65517936f182d3ecf7990f74a9`  
		Last Modified: Fri, 08 May 2026 20:55:42 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c84ccc0442845866606ba196b0edcf0e6bb1d9d581e56790dc8f03a06d53381`  
		Last Modified: Fri, 08 May 2026 20:56:26 GMT  
		Size: 42.2 MB (42162984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ef726f0b9f03625b32f87005f8a7337cad2a0df213fe22733e1bee9e691aba`  
		Last Modified: Fri, 08 May 2026 20:56:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc40d3e0ccfc41cc447d25488094e6a0b3f0c5b1459e5552688eaa2495bfe087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69761afb72786395c7b70e19d864f4ec48fa33b42e3b4bb7b4d7de44c5797eab`

```dockerfile
```

-	Layers:
	-	`sha256:cbfd4f6a7fb0a972da68b511a3e672a9ab5b90efea527ed735192f28c0389c52`  
		Last Modified: Fri, 08 May 2026 20:56:25 GMT  
		Size: 3.6 MB (3649132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:013298f6b17b6beaea2a73ad28e80a47136ef5eb76b74cea4df8a5e7fe69a832`  
		Last Modified: Fri, 08 May 2026 20:56:25 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:f931b65dd7406c03e1c83ffc7c04b6d551dc18df1ce8581a04f17cdffcb20e23
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
$ docker pull couchdb@sha256:b4e774adf2b8222bfcd5ccb88dfdca3d8ccbade23c44a5b052b27dca5fa2a0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4854060e48cafa0f1741faa1bf70bb809d0d90aed1c9f63e7a86186467b8f8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:41:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:41:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 19:41:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:41:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:41:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:13 GMT
ENV COUCHDB_VERSION=3.5.1
# Fri, 08 May 2026 19:41:13 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:41:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 19:41:27 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 19:41:27 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 19:41:27 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 19:41:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:41:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:41:27 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 19:41:27 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 19:41:27 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4619b10b6abb0c6e1498cedfc95d38f4c4a0ec385e9e9ebd8c86fc1faf0fa03`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e32228c19e744810ff941d44efdce42b089f2c30deb9057dd768222f6ad5d5`  
		Last Modified: Fri, 08 May 2026 19:41:41 GMT  
		Size: 7.9 MB (7883564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d987204986674deb3f0247644e89099f4e271b1ad27b27b4e819af33dd375ba`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 401.8 KB (401782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe5b1440c65cd5e40e2131e2a01210b449987fe7babb9db4e8232665f4c8e27`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 76.5 KB (76509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a34fa4a7b947dbc66b6bb75f80082e43923d75b15aa892bd5628dc2a2cd024`  
		Last Modified: Fri, 08 May 2026 19:41:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612a697d0527fa1e4c5e621474a561b106e23f96e3f7218762636a1c2a16c48c`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 105.5 MB (105455460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9990217fbeb1bf28489085b2d6c496c05b43ac91cd07bc3d9271831d0a45d55`  
		Last Modified: Fri, 08 May 2026 19:41:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c553ad59996c3c835f4707a465d98c330e0f3f837f8fd7685aeee28a5306d6`  
		Last Modified: Fri, 08 May 2026 19:41:42 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33c3cb69356151284e190eceafdf1a1af7698d22242e0d48fef7924643a5f19`  
		Last Modified: Fri, 08 May 2026 19:41:43 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88011fc5d8e4342ae7ab0f2e409ea625989648da5eacaf3f435b51b008a04ff9`  
		Last Modified: Fri, 08 May 2026 19:41:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:d665e41a3958b2c857dffe329418cb0b37a267b847e76ac9676cafec7d473eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403c820e5f8a69976dd97287f8c279a89df210fa8e5a78791f2aee2c114d4ea3`

```dockerfile
```

-	Layers:
	-	`sha256:ed0ec04f88ec623bbc0330c35dcdcd60f1e0372a0a7891103d08301ac002e0d9`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:993c18731410769aa30fa2a6f735e7e559c0b57da4820779fde73acf71d18c2c`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 31.7 KB (31737 bytes)  
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
$ docker pull couchdb@sha256:c17b9c2e29cd7c24179e58c4a37679a612654bdc0724078ab6a7a9b9e8ba4509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a64aa7574803e3c0686efa10943fb8560b0be2b6e1c9a15fe28035491c96431`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:54:00 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 20:54:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 20:54:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 20:54:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 20:54:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:54:16 GMT
ENV COUCHDB_VERSION=3.5.1
# Fri, 08 May 2026 20:54:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 20:54:35 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 20:54:35 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 20:54:35 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 20:54:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 20:54:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:54:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 20:54:35 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 20:54:35 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 20:54:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bffdf210de6acd187924745c5f9c5314f8b55a1712d8bc6ce811afdcaa8e84a`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c217f32eeb936018a0c3c2fd74f2250ea8c6227a3771bb06459662b812496f1`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 7.4 MB (7399519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6302c90d53931f2ac2569cfc71909681a79de3c0e4206ad2f72b0de1377c3a3`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 372.1 KB (372128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2441149aa3bca98c888cb93803232a1d8e227b8f2017b02042133d788e38c412`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 76.6 KB (76560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054fb689d6f1adbe57be588c3e5bc758f6f4c48fb2e57d4d2faef44d9be62cf9`  
		Last Modified: Fri, 08 May 2026 20:54:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b605ada1b3f7a065ce357b7761b6aca4bd7cb73a39b992ec4de6ba0e56f6f2`  
		Last Modified: Fri, 08 May 2026 20:54:58 GMT  
		Size: 104.0 MB (104028251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb74222b0ecd7c2158056d339f503142ac6bfa06bafa618b6c5f0a257656d2f`  
		Last Modified: Fri, 08 May 2026 20:54:56 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0008b3e90609955167dd06800d273d8d91866fbc9e2c81c84eb50a49bc8f27b`  
		Last Modified: Fri, 08 May 2026 20:54:56 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db4bf2f25d8048db6e3e7ea6232159ae2c46ff83f94586d34cd98922ca56e84`  
		Last Modified: Fri, 08 May 2026 20:54:57 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc348bec92209fe9c2c0e01799d2d786221c1befc2801ba468d13ec19427ee15`  
		Last Modified: Fri, 08 May 2026 20:54:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:8d90adb3d3145b44d103b26e9de0c1b0568f86c9f6471b900ad34ff1b817265f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d86237d1a166ca30d9884aa426bf321b0211658e837746110628260cb2ce28`

```dockerfile
```

-	Layers:
	-	`sha256:512c543656a3ebd4aa97b2bd8c2faa305eab0d944b9818281d57463c79d68c82`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa943442d0c72601e50625c99255b86368ad0097049e724d02e0d5a6401b443`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:525c7b6c150f9f3156f292423550dcc9c2a993854d377edf7204746a9ecbbd8d
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
$ docker pull couchdb@sha256:1c8ed68a20598dd0a47725e415f31896306fb5271649a9c2f3c7fcea2c93f2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156560003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03070c7fe084b855af980751395897652d9484ae9c2894931c8b570b1c5d17b`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:41:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:41:03 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 19:41:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:41:19 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:41:23 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:23 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:41:30 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 19:41:30 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 19:41:30 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 19:41:30 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 19:41:30 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c7ab9d7d84ce7427da1600d83e8009cb4f72036cac8e9a138c7505bb63ff51`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231e5c29d488c066806a365cf6bb2d290aeaa545bd367af47436f0ecfa5a68ae`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 7.9 MB (7883617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7503e94334f5e73bc32565e38762c538300f41a45d6a73692e838a342ce60e7d`  
		Last Modified: Fri, 08 May 2026 19:41:47 GMT  
		Size: 77.5 MB (77477951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7160133021d40bd64badd6655f732af1202536e922e37073564653a0f3bd6c1a`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 424.2 KB (424177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cec1429d6b2adacc17f61c8ca26a4cacac478ff6a3d55d14d6d59dcb0dda42c`  
		Last Modified: Fri, 08 May 2026 19:41:46 GMT  
		Size: 99.6 KB (99609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0331cdde4df19f092c9096cfa20ba0f3a7e604f262d5748f1b63967d566f434c`  
		Last Modified: Fri, 08 May 2026 19:41:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8f649c189a4318c0b7e870174aaa0ba4b231fe2fec61d938abbd00f2a8176`  
		Last Modified: Fri, 08 May 2026 19:41:48 GMT  
		Size: 42.4 MB (42436487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e604c15b77c5d906ced67623fc48d60e476012975f560056caed3d6173584`  
		Last Modified: Fri, 08 May 2026 19:41:47 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:65c2afef44a5239797450662121609e95a41d383e1c4972afa6e1013649b8250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3683426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fc2889da0df2dbdd746e2816bc8c997f37ff0e501acb986b08690644d2b666`

```dockerfile
```

-	Layers:
	-	`sha256:7645076ef6b1e13740ce071950ee3be1bc1781448b723d9b4e461c4b249bf721`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 3.7 MB (3658905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f1a071fa129af25c67b27db8f7fde8ea52ab2c7ab4b090bc5c0f057110a4a34`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
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
$ docker pull couchdb@sha256:4e8ce916270d6a33d52e187a6b1f1d2a5611790bf4479221ce113ac2c05c639d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150176402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c869967615fb1ceec6b922141cbb44583aa8637d438ef1eac66cbce43074303e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:54:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 20:54:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 20:54:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 20:55:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 20:55:10 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:10 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 20:55:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 20:55:18 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 20:55:18 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 20:55:18 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 20:55:18 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f53678fa637a5499e3a4c784e7bb9583bd679b5614fbc9ea063ebca22208f7`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e30253fb9558a325c75e8f8cd67d9ba29a4e3d983bc5273c45e7903f35e39c9`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 7.4 MB (7399527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c91ec9cb9119e4e999f79883f51cf69f4e94f5c1c40d673e7184c57b65201a`  
		Last Modified: Fri, 08 May 2026 20:55:43 GMT  
		Size: 73.2 MB (73224500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e09d6b9027e946b15506c40b1e41958b69bbe62fe7cc900c1468b87b5808ec`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 394.5 KB (394514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797e561a1d9086bb1eda68cf769149c66f115a9d365d9a9c76df7609d91d7f42`  
		Last Modified: Fri, 08 May 2026 20:55:42 GMT  
		Size: 99.6 KB (99639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fee3818ac597f228d126b69b2fdc9512433d65517936f182d3ecf7990f74a9`  
		Last Modified: Fri, 08 May 2026 20:55:42 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e9d902cb7040bc7ed5500b783451f3294f473b24615629e74a0a83a9e97277`  
		Last Modified: Fri, 08 May 2026 20:55:43 GMT  
		Size: 42.2 MB (42164737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d9e838a98401c25366b24f102b4ed3dbe7be3b60e29f87dd46fc2887441162`  
		Last Modified: Fri, 08 May 2026 20:55:43 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5201491b408694ede3240ebdf282369ab9cd22edc6f19b433ce6f7864d839cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433a8dd5c2a258926aaa88e2a4787ed2907aeeffe23d3fe2213ec30119c62fd7`

```dockerfile
```

-	Layers:
	-	`sha256:d965b3e99f31ca622604c2a3d04d027e83dd9ee89a720bf2cbd5812cc706b3a1`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 3.6 MB (3649438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3a50adc1e3c135fc555f900a110f8257e34089270903d64a6e59edb4825dd5`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1`

```console
$ docker pull couchdb@sha256:f931b65dd7406c03e1c83ffc7c04b6d551dc18df1ce8581a04f17cdffcb20e23
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
$ docker pull couchdb@sha256:b4e774adf2b8222bfcd5ccb88dfdca3d8ccbade23c44a5b052b27dca5fa2a0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4854060e48cafa0f1741faa1bf70bb809d0d90aed1c9f63e7a86186467b8f8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:41:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:41:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 19:41:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:41:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:41:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:13 GMT
ENV COUCHDB_VERSION=3.5.1
# Fri, 08 May 2026 19:41:13 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:41:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 19:41:27 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 19:41:27 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 19:41:27 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 19:41:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:41:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:41:27 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 19:41:27 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 19:41:27 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4619b10b6abb0c6e1498cedfc95d38f4c4a0ec385e9e9ebd8c86fc1faf0fa03`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e32228c19e744810ff941d44efdce42b089f2c30deb9057dd768222f6ad5d5`  
		Last Modified: Fri, 08 May 2026 19:41:41 GMT  
		Size: 7.9 MB (7883564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d987204986674deb3f0247644e89099f4e271b1ad27b27b4e819af33dd375ba`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 401.8 KB (401782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe5b1440c65cd5e40e2131e2a01210b449987fe7babb9db4e8232665f4c8e27`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 76.5 KB (76509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a34fa4a7b947dbc66b6bb75f80082e43923d75b15aa892bd5628dc2a2cd024`  
		Last Modified: Fri, 08 May 2026 19:41:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612a697d0527fa1e4c5e621474a561b106e23f96e3f7218762636a1c2a16c48c`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 105.5 MB (105455460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9990217fbeb1bf28489085b2d6c496c05b43ac91cd07bc3d9271831d0a45d55`  
		Last Modified: Fri, 08 May 2026 19:41:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c553ad59996c3c835f4707a465d98c330e0f3f837f8fd7685aeee28a5306d6`  
		Last Modified: Fri, 08 May 2026 19:41:42 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33c3cb69356151284e190eceafdf1a1af7698d22242e0d48fef7924643a5f19`  
		Last Modified: Fri, 08 May 2026 19:41:43 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88011fc5d8e4342ae7ab0f2e409ea625989648da5eacaf3f435b51b008a04ff9`  
		Last Modified: Fri, 08 May 2026 19:41:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:d665e41a3958b2c857dffe329418cb0b37a267b847e76ac9676cafec7d473eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403c820e5f8a69976dd97287f8c279a89df210fa8e5a78791f2aee2c114d4ea3`

```dockerfile
```

-	Layers:
	-	`sha256:ed0ec04f88ec623bbc0330c35dcdcd60f1e0372a0a7891103d08301ac002e0d9`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:993c18731410769aa30fa2a6f735e7e559c0b57da4820779fde73acf71d18c2c`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 31.7 KB (31737 bytes)  
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
$ docker pull couchdb@sha256:c17b9c2e29cd7c24179e58c4a37679a612654bdc0724078ab6a7a9b9e8ba4509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a64aa7574803e3c0686efa10943fb8560b0be2b6e1c9a15fe28035491c96431`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:54:00 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 20:54:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 20:54:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 20:54:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 20:54:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:54:16 GMT
ENV COUCHDB_VERSION=3.5.1
# Fri, 08 May 2026 20:54:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 20:54:35 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 20:54:35 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 20:54:35 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 20:54:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 20:54:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:54:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 20:54:35 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 20:54:35 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 20:54:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bffdf210de6acd187924745c5f9c5314f8b55a1712d8bc6ce811afdcaa8e84a`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c217f32eeb936018a0c3c2fd74f2250ea8c6227a3771bb06459662b812496f1`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 7.4 MB (7399519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6302c90d53931f2ac2569cfc71909681a79de3c0e4206ad2f72b0de1377c3a3`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 372.1 KB (372128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2441149aa3bca98c888cb93803232a1d8e227b8f2017b02042133d788e38c412`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 76.6 KB (76560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054fb689d6f1adbe57be588c3e5bc758f6f4c48fb2e57d4d2faef44d9be62cf9`  
		Last Modified: Fri, 08 May 2026 20:54:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b605ada1b3f7a065ce357b7761b6aca4bd7cb73a39b992ec4de6ba0e56f6f2`  
		Last Modified: Fri, 08 May 2026 20:54:58 GMT  
		Size: 104.0 MB (104028251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb74222b0ecd7c2158056d339f503142ac6bfa06bafa618b6c5f0a257656d2f`  
		Last Modified: Fri, 08 May 2026 20:54:56 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0008b3e90609955167dd06800d273d8d91866fbc9e2c81c84eb50a49bc8f27b`  
		Last Modified: Fri, 08 May 2026 20:54:56 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db4bf2f25d8048db6e3e7ea6232159ae2c46ff83f94586d34cd98922ca56e84`  
		Last Modified: Fri, 08 May 2026 20:54:57 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc348bec92209fe9c2c0e01799d2d786221c1befc2801ba468d13ec19427ee15`  
		Last Modified: Fri, 08 May 2026 20:54:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:8d90adb3d3145b44d103b26e9de0c1b0568f86c9f6471b900ad34ff1b817265f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d86237d1a166ca30d9884aa426bf321b0211658e837746110628260cb2ce28`

```dockerfile
```

-	Layers:
	-	`sha256:512c543656a3ebd4aa97b2bd8c2faa305eab0d944b9818281d57463c79d68c82`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa943442d0c72601e50625c99255b86368ad0097049e724d02e0d5a6401b443`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1-nouveau`

```console
$ docker pull couchdb@sha256:525c7b6c150f9f3156f292423550dcc9c2a993854d377edf7204746a9ecbbd8d
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
$ docker pull couchdb@sha256:1c8ed68a20598dd0a47725e415f31896306fb5271649a9c2f3c7fcea2c93f2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156560003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03070c7fe084b855af980751395897652d9484ae9c2894931c8b570b1c5d17b`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:41:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:41:03 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 19:41:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:41:19 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:41:23 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:23 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:41:30 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 19:41:30 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 19:41:30 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 19:41:30 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 19:41:30 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c7ab9d7d84ce7427da1600d83e8009cb4f72036cac8e9a138c7505bb63ff51`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231e5c29d488c066806a365cf6bb2d290aeaa545bd367af47436f0ecfa5a68ae`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 7.9 MB (7883617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7503e94334f5e73bc32565e38762c538300f41a45d6a73692e838a342ce60e7d`  
		Last Modified: Fri, 08 May 2026 19:41:47 GMT  
		Size: 77.5 MB (77477951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7160133021d40bd64badd6655f732af1202536e922e37073564653a0f3bd6c1a`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 424.2 KB (424177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cec1429d6b2adacc17f61c8ca26a4cacac478ff6a3d55d14d6d59dcb0dda42c`  
		Last Modified: Fri, 08 May 2026 19:41:46 GMT  
		Size: 99.6 KB (99609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0331cdde4df19f092c9096cfa20ba0f3a7e604f262d5748f1b63967d566f434c`  
		Last Modified: Fri, 08 May 2026 19:41:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8f649c189a4318c0b7e870174aaa0ba4b231fe2fec61d938abbd00f2a8176`  
		Last Modified: Fri, 08 May 2026 19:41:48 GMT  
		Size: 42.4 MB (42436487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e604c15b77c5d906ced67623fc48d60e476012975f560056caed3d6173584`  
		Last Modified: Fri, 08 May 2026 19:41:47 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:65c2afef44a5239797450662121609e95a41d383e1c4972afa6e1013649b8250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3683426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fc2889da0df2dbdd746e2816bc8c997f37ff0e501acb986b08690644d2b666`

```dockerfile
```

-	Layers:
	-	`sha256:7645076ef6b1e13740ce071950ee3be1bc1781448b723d9b4e461c4b249bf721`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 3.7 MB (3658905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f1a071fa129af25c67b27db8f7fde8ea52ab2c7ab4b090bc5c0f057110a4a34`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
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
$ docker pull couchdb@sha256:4e8ce916270d6a33d52e187a6b1f1d2a5611790bf4479221ce113ac2c05c639d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150176402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c869967615fb1ceec6b922141cbb44583aa8637d438ef1eac66cbce43074303e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:54:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 20:54:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 08 May 2026 20:54:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 20:55:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 20:55:10 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:55:10 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 20:55:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 08 May 2026 20:55:18 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 08 May 2026 20:55:18 GMT
VOLUME [/opt/nouveau/data]
# Fri, 08 May 2026 20:55:18 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 08 May 2026 20:55:18 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f53678fa637a5499e3a4c784e7bb9583bd679b5614fbc9ea063ebca22208f7`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e30253fb9558a325c75e8f8cd67d9ba29a4e3d983bc5273c45e7903f35e39c9`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 7.4 MB (7399527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c91ec9cb9119e4e999f79883f51cf69f4e94f5c1c40d673e7184c57b65201a`  
		Last Modified: Fri, 08 May 2026 20:55:43 GMT  
		Size: 73.2 MB (73224500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e09d6b9027e946b15506c40b1e41958b69bbe62fe7cc900c1468b87b5808ec`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 394.5 KB (394514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797e561a1d9086bb1eda68cf769149c66f115a9d365d9a9c76df7609d91d7f42`  
		Last Modified: Fri, 08 May 2026 20:55:42 GMT  
		Size: 99.6 KB (99639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fee3818ac597f228d126b69b2fdc9512433d65517936f182d3ecf7990f74a9`  
		Last Modified: Fri, 08 May 2026 20:55:42 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e9d902cb7040bc7ed5500b783451f3294f473b24615629e74a0a83a9e97277`  
		Last Modified: Fri, 08 May 2026 20:55:43 GMT  
		Size: 42.2 MB (42164737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d9e838a98401c25366b24f102b4ed3dbe7be3b60e29f87dd46fc2887441162`  
		Last Modified: Fri, 08 May 2026 20:55:43 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5201491b408694ede3240ebdf282369ab9cd22edc6f19b433ce6f7864d839cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433a8dd5c2a258926aaa88e2a4787ed2907aeeffe23d3fe2213ec30119c62fd7`

```dockerfile
```

-	Layers:
	-	`sha256:d965b3e99f31ca622604c2a3d04d027e83dd9ee89a720bf2cbd5812cc706b3a1`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 3.6 MB (3649438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3a50adc1e3c135fc555f900a110f8257e34089270903d64a6e59edb4825dd5`  
		Last Modified: Fri, 08 May 2026 20:55:41 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:f931b65dd7406c03e1c83ffc7c04b6d551dc18df1ce8581a04f17cdffcb20e23
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
$ docker pull couchdb@sha256:b4e774adf2b8222bfcd5ccb88dfdca3d8ccbade23c44a5b052b27dca5fa2a0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4854060e48cafa0f1741faa1bf70bb809d0d90aed1c9f63e7a86186467b8f8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:41:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 19:41:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 19:41:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 19:41:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 19:41:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:13 GMT
ENV COUCHDB_VERSION=3.5.1
# Fri, 08 May 2026 19:41:13 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 19:41:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 19:41:27 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 19:41:27 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 19:41:27 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 19:41:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:41:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:41:27 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 19:41:27 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 19:41:27 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4619b10b6abb0c6e1498cedfc95d38f4c4a0ec385e9e9ebd8c86fc1faf0fa03`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e32228c19e744810ff941d44efdce42b089f2c30deb9057dd768222f6ad5d5`  
		Last Modified: Fri, 08 May 2026 19:41:41 GMT  
		Size: 7.9 MB (7883564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d987204986674deb3f0247644e89099f4e271b1ad27b27b4e819af33dd375ba`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 401.8 KB (401782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe5b1440c65cd5e40e2131e2a01210b449987fe7babb9db4e8232665f4c8e27`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 76.5 KB (76509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a34fa4a7b947dbc66b6bb75f80082e43923d75b15aa892bd5628dc2a2cd024`  
		Last Modified: Fri, 08 May 2026 19:41:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612a697d0527fa1e4c5e621474a561b106e23f96e3f7218762636a1c2a16c48c`  
		Last Modified: Fri, 08 May 2026 19:41:45 GMT  
		Size: 105.5 MB (105455460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9990217fbeb1bf28489085b2d6c496c05b43ac91cd07bc3d9271831d0a45d55`  
		Last Modified: Fri, 08 May 2026 19:41:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c553ad59996c3c835f4707a465d98c330e0f3f837f8fd7685aeee28a5306d6`  
		Last Modified: Fri, 08 May 2026 19:41:42 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33c3cb69356151284e190eceafdf1a1af7698d22242e0d48fef7924643a5f19`  
		Last Modified: Fri, 08 May 2026 19:41:43 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88011fc5d8e4342ae7ab0f2e409ea625989648da5eacaf3f435b51b008a04ff9`  
		Last Modified: Fri, 08 May 2026 19:41:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:d665e41a3958b2c857dffe329418cb0b37a267b847e76ac9676cafec7d473eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403c820e5f8a69976dd97287f8c279a89df210fa8e5a78791f2aee2c114d4ea3`

```dockerfile
```

-	Layers:
	-	`sha256:ed0ec04f88ec623bbc0330c35dcdcd60f1e0372a0a7891103d08301ac002e0d9`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:993c18731410769aa30fa2a6f735e7e559c0b57da4820779fde73acf71d18c2c`  
		Last Modified: Fri, 08 May 2026 19:41:40 GMT  
		Size: 31.7 KB (31737 bytes)  
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
$ docker pull couchdb@sha256:c17b9c2e29cd7c24179e58c4a37679a612654bdc0724078ab6a7a9b9e8ba4509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a64aa7574803e3c0686efa10943fb8560b0be2b6e1c9a15fe28035491c96431`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:54:00 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 08 May 2026 20:54:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 08 May 2026 20:54:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 08 May 2026 20:54:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 08 May 2026 20:54:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:54:16 GMT
ENV COUCHDB_VERSION=3.5.1
# Fri, 08 May 2026 20:54:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 08 May 2026 20:54:35 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 20:54:35 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 08 May 2026 20:54:35 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 08 May 2026 20:54:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 08 May 2026 20:54:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:54:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 May 2026 20:54:35 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 May 2026 20:54:35 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 08 May 2026 20:54:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bffdf210de6acd187924745c5f9c5314f8b55a1712d8bc6ce811afdcaa8e84a`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c217f32eeb936018a0c3c2fd74f2250ea8c6227a3771bb06459662b812496f1`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 7.4 MB (7399519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6302c90d53931f2ac2569cfc71909681a79de3c0e4206ad2f72b0de1377c3a3`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 372.1 KB (372128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2441149aa3bca98c888cb93803232a1d8e227b8f2017b02042133d788e38c412`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 76.6 KB (76560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054fb689d6f1adbe57be588c3e5bc758f6f4c48fb2e57d4d2faef44d9be62cf9`  
		Last Modified: Fri, 08 May 2026 20:54:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b605ada1b3f7a065ce357b7761b6aca4bd7cb73a39b992ec4de6ba0e56f6f2`  
		Last Modified: Fri, 08 May 2026 20:54:58 GMT  
		Size: 104.0 MB (104028251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb74222b0ecd7c2158056d339f503142ac6bfa06bafa618b6c5f0a257656d2f`  
		Last Modified: Fri, 08 May 2026 20:54:56 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0008b3e90609955167dd06800d273d8d91866fbc9e2c81c84eb50a49bc8f27b`  
		Last Modified: Fri, 08 May 2026 20:54:56 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db4bf2f25d8048db6e3e7ea6232159ae2c46ff83f94586d34cd98922ca56e84`  
		Last Modified: Fri, 08 May 2026 20:54:57 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc348bec92209fe9c2c0e01799d2d786221c1befc2801ba468d13ec19427ee15`  
		Last Modified: Fri, 08 May 2026 20:54:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:8d90adb3d3145b44d103b26e9de0c1b0568f86c9f6471b900ad34ff1b817265f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d86237d1a166ca30d9884aa426bf321b0211658e837746110628260cb2ce28`

```dockerfile
```

-	Layers:
	-	`sha256:512c543656a3ebd4aa97b2bd8c2faa305eab0d944b9818281d57463c79d68c82`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa943442d0c72601e50625c99255b86368ad0097049e724d02e0d5a6401b443`  
		Last Modified: Fri, 08 May 2026 20:54:55 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json
