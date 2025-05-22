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
-	[`couchdb:3.5.0`](#couchdb350)
-	[`couchdb:3.5.0-nouveau`](#couchdb350-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:6ec7bea4222980f4630b91614ef668e75042c0fdf1a2c6dd153c34f5c2522d2f
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
$ docker pull couchdb@sha256:48461e712eb19a62999037cecd2592b579cd2a099aff546bffd354d4a4981503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139819073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457042a730fbb82c61566ed8e79d453f3a2b8b3b4f1caacf640675f0b7d967cf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db76d6e1c7998fb7ae0ccb603376f72d1b2018fc3301cdf33f421573621423`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796832cf42a2afc1527f14d3835cb90abc5d314cbb4eb381fef0e2953985377c`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 7.9 MB (7876592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c546028bb904f5fd511313dc39d6843111f3a6e0f8466d9d6d021b2a23e9a6d`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 392.1 KB (392129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb8ea8809565d82d409be15bb0a487592feb0f0f45a1a9f85ff4eaf4de21225`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 76.3 KB (76283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587baf2d1aec5aecdd448d026ad54ff5c007d7060b808956f70d6f7a9bd14340`  
		Last Modified: Wed, 21 May 2025 23:21:19 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496680db7db212dcc94ccbce6034c0f0791a93a26474a3fee2fa192a624cc7dd`  
		Last Modified: Wed, 21 May 2025 23:21:21 GMT  
		Size: 103.2 MB (103243310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588b33ca1e68b6ff6bf8acb7508583394d58125f6223688c34370302ecc14411`  
		Last Modified: Wed, 21 May 2025 23:21:19 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b863b579a751a6b5cbe57b4c53895d5078b68b027d26e71de5b951d9bcc23b04`  
		Last Modified: Wed, 21 May 2025 23:21:20 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711bcfe1ad83602d399128ff2639b813736951b0469a95ba7e5d4bc87cc7bdbe`  
		Last Modified: Wed, 21 May 2025 23:21:20 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66f91f3e055f54abdbf7b7c953477bd00bc4af34ec3fcfe884b8622aee2c30f`  
		Last Modified: Wed, 21 May 2025 23:21:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:984ceb992e4fae3bfe805ef41aae42ff8c56bdd05b11f97b3f91aeb74287d2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4037092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cadb37b6ecf8b6b8916ca50c9b249a8dac3cdca7772600f52d1498fc1993da`

```dockerfile
```

-	Layers:
	-	`sha256:fe5b854cbd1b60d14e82a3922af523976763eecef3b1e94d773d249cbd8c5136`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 4.0 MB (4005311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f2d4dd498de68b34125f3c8cf7cf8b06b23533a94545eb9f97858fc055533de`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2e5d6e31ba5b9b92989e29faa365e2bffb92af2c68d74ece6a2ca43016ba6648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139041917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11de94aa647367ba5fe5a4ea744897e9a6e24f0ab3c0db12740c8cafca9ee4d4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fda7edaf9e5fa4bff22f8647fc45ace1dec9a2413c557a56f3d209571bb03d3`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f44d3c9be40e352cbd13efebb94c5b86d4cd047a37cb05e1470b3799da491`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 7.7 MB (7654565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77c2f410b4ff91dda61e7492f539cf3280b1e296b0f87b974582537e952a860`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 348.9 KB (348949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f245645ed55f34a29dc8f3628a26a2df51feae716273e621d28255c5cd0366fc`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 76.3 KB (76313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5710c3924976aed640fb8f738d4e47e35ecd4a5fcf0b2511f68afe7d1146528`  
		Last Modified: Tue, 06 May 2025 17:58:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0454c720549b1dcd1cdef601206f434cdd971e17c9a772d65ba3975f97b969`  
		Last Modified: Tue, 06 May 2025 17:58:05 GMT  
		Size: 102.9 MB (102890031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a994b43877b24b8e8eb646784ca98c6cc75ae1c83f06754649a2bd484c7b1831`  
		Last Modified: Tue, 06 May 2025 17:58:02 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c16e2d34057757eb1428efb7c184e238c3794dd98268e3bd294f2f244475f`  
		Last Modified: Tue, 06 May 2025 17:58:02 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc5813c77ab5a6b2305995bddd3c3e4d7a17f36fc53dbf8de965c6d9d85f0a`  
		Last Modified: Tue, 06 May 2025 17:58:03 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc85c73a0cbd10b91c9982c83b79f58e9b9deab4cf54e563375a8a928c2dffa`  
		Last Modified: Tue, 06 May 2025 17:58:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:fe60acaabade72ceee44fb2665c04f57bc8c5b0c47358f52c9b5043925401920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b478e56c588977ce65a82fb0d0c0f20cc1f87c7ea3af87f9bbd3fdaeae84d40c`

```dockerfile
```

-	Layers:
	-	`sha256:89d3e99d85d7bb933bd62e346a0a1620c97bdf09d7c859d291d8a37233ee45df`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 4.0 MB (3977764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:112e82b651057c0dc11627c3143fd48ca8640c788a42c40bdf853c248d46e608`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:aa073d5b2899110636aa11b4ccab6e222f76ee8d6066a8d595b6932a31f35352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136508976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5d7eb1088b9aeadc82c9d60d973705ecad3e5cfbe2233370486d9318bce329`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae941489b0da77e1ee8a58c546530f92eb369117b11a80bba562437bc949405`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215e6a02cfb983cdf525705ca0c858e32481b6d88effe8dd5638e254428c9bc1`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 7.4 MB (7390952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea51146f220497d66074837aed4d4957b378c092326bae49eb2d25956a7124ed`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 355.6 KB (355621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8ebfd7a69c538a6ea4a568bbcbd2d09dbe7dc0cb1c8ad80b5013567bf9c77`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 76.3 KB (76309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f6d65faf14a43908fc64a3f7c5b8a0093df475ab99ccd1d0fbb4cb1856eabf`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8bc5ef397d902964b72e93ad3785ed5674999751e96c4039ef937aecb8127d`  
		Last Modified: Thu, 22 May 2025 01:04:40 GMT  
		Size: 101.8 MB (101797850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa33ac6d9246fc0b0be7672444d9e70ff24dae5519016facb02368cdf4db1d1a`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62df8f16139eddb5120f8765468175dd99b130d830b7d9f1d53f4935dc7ed44`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c74ac65654aa3b3e84aaa87876e05096485f3682d04333e26366ac6161fe75`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a4f71afa5a484da6c2c13331d63e07dfe4c47964b692716adf42caeab50c9`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:636b405f48663602370accde8d8bdac3d47d86051471d1734ec16114c16d8098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4036180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a640caec505c17fdd7c1ef70a9b01903be51d0432e21c40889962ba68ea7094a`

```dockerfile
```

-	Layers:
	-	`sha256:c8cb70efa326f50969856150cf5c10d1b1700062b0465df1ef7c61d992759afc`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 4.0 MB (4004399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa0b8b821b8a67c0bf0425f63deb4111df467de46101259a3c149b787203648`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:69f0862d6fce32301cecfb5b1c3c1e4f9b3b762d725766e83dcc731a79ea94ce
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
$ docker pull couchdb@sha256:0e9d627a82619751cc0d6f42f899aa11e8b0fd01afa5f06cbc2de5dbc0151e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156377003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f486850fee961991297613cd422a46f6df9bf60911d27619b99ab996d1a18ef`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9499470c9acbc00bcc886054c1cda3f5c8c36fbf550a642960f2726c99f7cccd`  
		Last Modified: Wed, 21 May 2025 23:21:31 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0590250af4762255b25cff955958f055fdfcafdeb9007c8e4b4f571432bc98cc`  
		Last Modified: Wed, 21 May 2025 23:21:32 GMT  
		Size: 7.9 MB (7876617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffa6110867a1df8c941ceb29416c301977da6dcc8a82ce3dbf7d4931009ac58`  
		Last Modified: Wed, 21 May 2025 23:21:34 GMT  
		Size: 77.3 MB (77324631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5f96efa9cf3073c2562091ffd7f4ef6b7934631bc159dee2cda56169bb3c37`  
		Last Modified: Wed, 21 May 2025 23:21:31 GMT  
		Size: 415.0 KB (414987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98d8ddcf13047ccfd1fc7c4747bc785c5cb1a0459ff93c5263a96defebe4d42`  
		Last Modified: Wed, 21 May 2025 23:21:32 GMT  
		Size: 99.3 KB (99323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733d973b08d70309f6af91291d0d69983e350cf6377bd9a4649c156c22827d6`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749f6475cadf4afd508e15603543c680150a2dcf6641c3d8a64a766c1bc71bc`  
		Last Modified: Wed, 21 May 2025 23:21:35 GMT  
		Size: 42.4 MB (42434239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002a25bfa7ceaa38750737429b07cefd358da6cdc7699c3062c6602c8a5db5bc`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:e06b980a13665020a73a39fbad472958d45e6c263edc8c901c8c6782efd65326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3527788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e8f86012d808409684a3638c5fcf10b5cc3c3250ea82df6f6bc0c3cb24aaef`

```dockerfile
```

-	Layers:
	-	`sha256:6b81beb7bb8f78ee184908beda66bcd1024e3a72659520cb1cf1e11b7b3cc114`  
		Last Modified: Wed, 21 May 2025 23:21:32 GMT  
		Size: 3.5 MB (3503225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e797f8a70670a8c360e264c6b98942981c8680eb266df741b8e284dd2db0f5a`  
		Last Modified: Wed, 21 May 2025 23:21:31 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7fdb1df7e89b35ae184e2975f8ed5d5c72acd6e651588d7854923639ea383648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155180531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90792137fb7d00afa09943655aa32c8b56afb2ed23f9ca819aef6c02127e89b0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104637e2eb67ec32ff000f153eebca995c5a32bdca49fe1b16015251fd887842`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc58e96c4d79f04a31e09066efeea0f21f93f87a60cd80b537546b799ebbff9`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 7.7 MB (7654542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f58f87545a1ea3e85e36bc4f13c6528480a4d096cabe6e23b6919d84a3a21fa`  
		Last Modified: Tue, 06 May 2025 17:58:59 GMT  
		Size: 76.7 MB (76653670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886a375283a50138292c4ab34c2a2cd473c86f479a0657d206917439b9293ef4`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 371.7 KB (371732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccf50ebfde2d6eb28578d23558bec7ad3fcf33ed5edbbda390b0c02b37636ab`  
		Last Modified: Tue, 06 May 2025 17:58:56 GMT  
		Size: 99.3 KB (99262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a67aafe8a97aa0a8dd806d49d1da627072a88c7e466a6957064c3b1ac9f579`  
		Last Modified: Tue, 06 May 2025 17:58:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd40dddaef0fcda5c486a0d107b1aeac5eae87d112d92a7f8babc07a9c2bc5b`  
		Last Modified: Tue, 06 May 2025 17:58:59 GMT  
		Size: 42.3 MB (42332820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ead4ac28d2805b9ad7d4bc386937a7df61b55d7493ee5c9fa48d6eab8baa75c`  
		Last Modified: Tue, 06 May 2025 17:58:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc0f7d743c3b12042d2363c435ba9a3136bffb0e8741d2777c0e9501b34fb0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b851a388ca66506c60d98b25da2535df558b509b5464f97e568dcd7055452f`

```dockerfile
```

-	Layers:
	-	`sha256:926a4dc0d56e3c9be08d364b9e30b94d534c9a7d479ce49b32d9a7fac0b85348`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 3.5 MB (3467148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22075a440bd6b34723136a723584525e19f147bda33189d33a6d6199161fb556`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:c144920a1f33f2407cb3611ea12b4e80ceebd4fa134fe745503729ed901bbe2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149990045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e2d1ccfff6600840e8ab5f7799ad12211edb132dddf6c0f6f05b11f2e47fd8`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26396a1c92d005f1f73ce8a5a786829b16fd7bfeea83b11aab47577c79125a6`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474be071a26fc29b13f67d8e56c399b46d3b8233fba772eddf197a41e47b3ce`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 7.4 MB (7391039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7557a7943629e9a5e09974b851cd3f71af7ae009a3c979a57c2005e05a04ae`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 73.1 MB (73075902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364ab5de64b0f27b98361254033eb8e64dab17927d0d5ed36673abde5d5a1116`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 378.1 KB (378082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9582aebb38d001676e191f1d1739f9651fb01da8c1d4099e8e0eb6e86e453`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 99.4 KB (99441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15939d7d9273f1580bd4614a899539324dde9b46bb9c958cb5ecd8b6e118b3b7`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9ca0b94e18b2399600f2856dafbb9e4ad3d61ca982c486d68ee6f2f8e2f845`  
		Last Modified: Thu, 22 May 2025 01:05:47 GMT  
		Size: 42.2 MB (42160892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afc856a01f3eda18d2caeeef10985ba6f113d6e40fa30d36627cffd35c50895`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:9026af3d06aa014b566e394abb7e54e49cf289dcb09ad6c4bc2363b87545ace7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbed73861a10a7185fb0f4d338c33bb2b7b13941e243ef568f46cd7853f1b44`

```dockerfile
```

-	Layers:
	-	`sha256:50da05748a9be431439b8d33cd60430c479b3050bc095b88e787d64e1bfbbbbc`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 3.5 MB (3496646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b67689b0e1b9ff33b91e6f02f0d07c8551e1671ab573b630d590e1607976d665`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:03e8b34b1a5b8f5247023b008fb9b8782bfd2cc9f891a53cc51820373f21a14e
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
$ docker pull couchdb@sha256:4b3d2d2327ebe2e2a71fceb9e592a9311fa91b47a29d502de0cb55c62e289784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138996956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343bec67ba9e53b1c7875f8faacd948f3b8484923d4eb5389629130b3f86f851`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fe6910cb13319c2f21da90f20788c730c261c6947a1610602755895ad9ba6e`  
		Last Modified: Wed, 21 May 2025 23:21:38 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d320c854faeea21abf0e3e8e9a416bc07f0c3e8062115e487ccd97f5ba47553`  
		Last Modified: Wed, 21 May 2025 23:21:38 GMT  
		Size: 7.9 MB (7876583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9881916f5a820676368755d769cd40b7e0e9df48c6ef2a0562e88f45e776ec`  
		Last Modified: Wed, 21 May 2025 23:21:38 GMT  
		Size: 392.1 KB (392131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84abbeff469e281c4068dc7dc6c3ed242eef8ede5e85715c5fa399657bb71c6`  
		Last Modified: Wed, 21 May 2025 23:21:38 GMT  
		Size: 76.3 KB (76293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b47390cd854b3fade658b434b169b4e9374c8a2e39ae485fb3e79f56b35eaa2`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f440703289eb36095d7d6dd12351d0112340ba8139904a0f99ea3bd9b340573e`  
		Last Modified: Wed, 21 May 2025 23:21:42 GMT  
		Size: 102.4 MB (102421180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad8887225b7196f8689f6ceae8e7ee1e65b3fa361d14bc231a0293b00ed259a`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a672aa636d853ecc57c05c5d7dabcd678d45e19a918073464387b191c7fd8f`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361648ea7136a2a8dd5f99092cfa11ea4051598b711011625e14fa6336295959`  
		Last Modified: Wed, 21 May 2025 23:21:40 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55450775d2f4f5c70ab37c8b96405115946e0b919d095dd90bc2c9e01d596203`  
		Last Modified: Wed, 21 May 2025 23:21:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:c019c491c429ee2be1514aaab5093b32b924a3acbdc7c408ca313758abb2177d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ecd354a84054d72c56f2e0def88ce183b0b3ffa38ad85fd24745f6864c95b9`

```dockerfile
```

-	Layers:
	-	`sha256:90142802e757b2297600bde997a2557c09465e2b60ded163ed735c23c2c6b6e4`  
		Last Modified: Wed, 21 May 2025 23:21:38 GMT  
		Size: 4.0 MB (3989444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3043e001adaa538399030483dda9d4deea1a121c98989f3a8f1892411432536`  
		Last Modified: Wed, 21 May 2025 23:21:38 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:15729596c86dda15cc99edf750fc425cb57ef4edce5babce54d068a426a45a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138301136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cf79497d5220986281ff560d275803bb04fb7bc51e1cbb7a936f6d973a73c8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2633edfbe42095655e8e06326a2bb09e72f60054163cab4d32ecdf090a957da`  
		Last Modified: Tue, 29 Apr 2025 01:50:52 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0cf2efaa368539937e0c9e20e80322a37f0973ca6529dc176891bc2b6b4343`  
		Last Modified: Tue, 29 Apr 2025 01:50:53 GMT  
		Size: 7.7 MB (7654571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb956e71c0e68ceaea25a9a17c3479c71593de51c3e3883402da9bddd458ce9`  
		Last Modified: Tue, 29 Apr 2025 01:50:53 GMT  
		Size: 348.9 KB (348927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a6383735d775aae8622e383ef33c77472eab8ffce56113ccda5df7ac6cfa1c`  
		Last Modified: Tue, 29 Apr 2025 01:50:53 GMT  
		Size: 76.3 KB (76324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f979f73832f1924be9ae9da8592cf4f4e6c7eadc7cb4338f2bd8e4ce317e44`  
		Last Modified: Tue, 29 Apr 2025 01:50:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16239f6235a9d3bcdaf9c38f9927cd1e232df55ee863031a4353daadfea769b9`  
		Last Modified: Tue, 29 Apr 2025 01:50:57 GMT  
		Size: 102.1 MB (102149270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8220ab79af616850c33eb5221da223f95894f9c6a1ae7da136c296c3d03b510`  
		Last Modified: Tue, 29 Apr 2025 01:50:54 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6e43f89922d88c83e3806dff1d4bf75ccc80c4a4d308b57a4de073a5a1eca1`  
		Last Modified: Tue, 29 Apr 2025 01:50:54 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3804f08bee9c27c0fece5ba72adbe467bd4b68926d439c1c516309ffa3e74a2e`  
		Last Modified: Tue, 29 Apr 2025 01:50:55 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b49f429faf76187d67cc6f28f9db32073e600dab35eb869191557acfa4cde4`  
		Last Modified: Tue, 29 Apr 2025 01:50:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:df8ec2e03ec5c103efc80684aae3d7a53433bb17f2c2714e448b58288d74630b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fe7f0e4c9ec3c47ecda169839158b3abbe56f06752386e568d2c2c5df04c0e`

```dockerfile
```

-	Layers:
	-	`sha256:92ed9cd6274d1b94036200dcd5171f298f315f6db22e8327bba08ebd9992df49`  
		Last Modified: Tue, 29 Apr 2025 01:50:53 GMT  
		Size: 4.0 MB (3962487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:425cc3db72cabb981f4a91737562f7be0699079a61ccb18f8f8fe8d4369a21ab`  
		Last Modified: Tue, 29 Apr 2025 01:50:53 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:7819b07037fe98ec994ca26a121fbb8c9a601772df54fa0f3af9f7ba85e50a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135766171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220713081441f1810d0218f5900376c97d27ed09c05e86c7476f16287ab5794`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c8a4385111079823034d1e8ed702e9672cd681f79562137fa525d16803eea`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c0f7f5b2751909f18f45844094309abfc54100ace7c37207440666c3dd916`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 7.4 MB (7387937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b6aeef9cd48451c7352e0d027a4ab68782567fd1af8b1aeed4283756407f74`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 355.6 KB (355644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a016c259437b9920b9c085f993abedb656356821d7571071cb17db40433ce23`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf854b3c69326f429e568061da038a651efb11e32516f8571b1eb6c2fa4f676`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63c8fe755b51ffd8fbe51e653149697f4db50ec5f2e547f3cdacddcf23a8cc`  
		Last Modified: Tue, 29 Apr 2025 00:03:42 GMT  
		Size: 101.1 MB (101055957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702504975d7b1931a864c2373bbe22a5a0c200b6689e356d0e589bee6a061932`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c449b40f1681890fb4190af1efe37d7714370d105e051af05596c701a932f57`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094a79dad673e9d7ae35052d26551314238c734e732e0fb16915e7266b6547ad`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1480727e9ec140937813aea1076b6378bf266665e18b0e20314a588367868a3b`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:88af6693555cb508b2d025acdc1cf32ed693329c7425a63e3ca33fcae9d6527d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cd21e53513802102079ed3d78030c64a5a73292fb437f3f01cd3c37abebb08`

```dockerfile
```

-	Layers:
	-	`sha256:899e8cbc1e36d790e687a9f1f9b1b0d69e11609f8e383484c7a552377bdc224b`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 4.0 MB (3961282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5195173997f32afdbc21e62b738eca6b36722bdcbe2527bfd1b80cc09e348e`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:d8d3d9f9db0623f3d300e629a75a90b83cf4f886e64cab807c301d4a492a1bcb
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
$ docker pull couchdb@sha256:baeee2679298fb6a68701e1240a5d722d9bde10891d2df481064cd43fda8d9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156376138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5763e930c1db2b91f95e20cc0e3819eb2a12d3bc43e6fd26192425f7d65eb3ce`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26c958d6c4d447f8a8d0364934ad1fbe3d621b0994241e7a1bc6c1da675ef26`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82037acdce809e8a6d5d7fa667076515748e41198ffffdd5dabd86155d68096`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 7.9 MB (7876476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967602685befc4ac9e1ceae20f9d0eeb0956b55362a1ccda2bbd753b546259a`  
		Last Modified: Wed, 21 May 2025 23:21:34 GMT  
		Size: 77.3 MB (77324664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ce896791c198afced5bc9fc81a882ee6e098bbcb817c5810f7ab3bf31f210f`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 415.0 KB (414989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37afc41665e2753cece416555d49bd6203a19478d97edd2f0c7f4adb4ce8a3c`  
		Last Modified: Wed, 21 May 2025 23:21:34 GMT  
		Size: 99.3 KB (99327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94186914076559a29762b6e9db34b4506a3a448b2c25e8e267c92b403ccb2e69`  
		Last Modified: Wed, 21 May 2025 23:21:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686b78b0943f21f1810832f2ba2d33fbda1c4d95ad356d919d7eb3ae5ffbb029`  
		Last Modified: Wed, 21 May 2025 23:21:34 GMT  
		Size: 42.4 MB (42433470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed2cc40c96c6da96e95777a48ccf4730d0b5574288e2e9332bd620aa4112510`  
		Last Modified: Wed, 21 May 2025 23:21:34 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f7523d310e8e8e4ed80112562db7595085f60356d19bf9451a58c5e6f7b5ae19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3527177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125c5b6e6ffd5112963fc4d2101c2f68a1926b4ce68729008c5b9281c50aadd7`

```dockerfile
```

-	Layers:
	-	`sha256:9ff0fa278dd93ae3168a16479a214b2ba0f249118ce041e7c2305c53583b7498`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 3.5 MB (3502919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a05f5531efd5204ae9926a29d2f8794374993f7809bb0801abfe00f252b5e91b`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 24.3 KB (24258 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0fc5bf7f8656c738548765f26d845e06e1f397e2ba7769a12f072ed480ea2192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155151224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5839b1b3d1b63e9c6218041f808c4f01c7d9c791f10d4af997c8168ace78fd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac2fb37a32e5d32440fe31bf070b4f898cd1be575a07c97cb79545c9b0185ba`  
		Last Modified: Tue, 29 Apr 2025 01:51:45 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01d9b43b431ef17b69173455b60689597c4625f6f6c4f7eb221a030ab004321`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 7.7 MB (7654523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3825b273ce4e5eb6867f90ff56927c439343cdddf5b9851536108096d71a168f`  
		Last Modified: Tue, 29 Apr 2025 01:51:48 GMT  
		Size: 76.6 MB (76624178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6a8d76ed8c03ee5297cc4c2d41c92edfb6fa1335a48b18b7dd5b4bd3c123b`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 371.7 KB (371743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19359905d9ad3145a133462b7a4bb5f7b0ec3e6fdba00b937fd82721789cf935`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 99.3 KB (99267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e15435482689c2ae429169c378e85e1689ad1fcbf407d2afc7d57623eed71a`  
		Last Modified: Tue, 29 Apr 2025 01:51:47 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad50cd5577f3297510ebe03234b653c4bda90d45cc8ca400513aca09e0446e0`  
		Last Modified: Tue, 29 Apr 2025 01:51:48 GMT  
		Size: 42.3 MB (42333012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a49280d94a95e153d3e016076b7e5188cfdc8ab11ad546a46ab8a4c31f8340`  
		Last Modified: Tue, 29 Apr 2025 01:51:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:02e17f86ce17541e3ff54b18c1e75db26776c37e7a0f04eb985686e8706efd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb40c217bb4ab0e4de428c0aba3fc79410576e35dcd21a2d1e4f0df951d7348`

```dockerfile
```

-	Layers:
	-	`sha256:e1a0a1588545666af4b5a0101d887a0dae635f9389deab9ea94282c17c799abd`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 3.5 MB (3467148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f6b2e21e354c6da21bec28182224c1de6a2a046a3b09e39131690d219a25642`  
		Last Modified: Tue, 29 Apr 2025 01:51:45 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:567f3e53824961c5f506118d23c53e6c44333ede5da72ca9fc0453ee8df3559f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149977892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d2af33615aa36bcba2719f0280f43028b632981cf48362c439c8774e5a7e08`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeb9febea926497c6b73a956a66c5ec7705a80ed96a88acd22e023a12bb07b9`  
		Last Modified: Tue, 29 Apr 2025 00:04:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb3720e0f56a097c25a4a4a982b82bafb5b5cd40ac87ffefca40556227f213f`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 7.4 MB (7387952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce679ce7dd142ab1209f6b1e198804851164e290d7c9412f489110386d84a3c4`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 73.1 MB (73065225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ea5e69fb0ac2e8ec68ad79d4ed32a98475e57dec15e01433a7aac1c8d2bcff`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 378.1 KB (378103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8084ad1ebf84dff15753e78e53bdc8cfdccdcb39266f1bf8e231f251d78a64e3`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 99.4 KB (99449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a49819b32ddd9c0fe27e1ed0f760870d4d9170232838540cc48f818ef2606e`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cd8bce374995c6a118e0965c0b2ebf3fa93ae834354a829cc1b3cd0f830219`  
		Last Modified: Tue, 29 Apr 2025 00:04:49 GMT  
		Size: 42.2 MB (42160416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55bbc492280b5c45b056b641e8fec35f5fb54bc50068de783a4c110b4beb376`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:77c04fe246e4b659963c87d866f2678b43426ef3984aac6cc092e602b0dc0ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f22a5e7194519b1d9eff220c23222179736285e22078c6328ae14eda1ca0b0`

```dockerfile
```

-	Layers:
	-	`sha256:e581491861b03880116342ed4b02be1373f61f3ac37d5e781506fac9e30a02d5`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 3.5 MB (3461893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e144eeff7b03258ac15dcb32b9ea1e2ff7892643f844b7df4a7b15118c6c87e3`  
		Last Modified: Tue, 29 Apr 2025 00:04:46 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:03e8b34b1a5b8f5247023b008fb9b8782bfd2cc9f891a53cc51820373f21a14e
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
$ docker pull couchdb@sha256:4b3d2d2327ebe2e2a71fceb9e592a9311fa91b47a29d502de0cb55c62e289784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138996956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343bec67ba9e53b1c7875f8faacd948f3b8484923d4eb5389629130b3f86f851`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fe6910cb13319c2f21da90f20788c730c261c6947a1610602755895ad9ba6e`  
		Last Modified: Wed, 21 May 2025 23:21:38 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d320c854faeea21abf0e3e8e9a416bc07f0c3e8062115e487ccd97f5ba47553`  
		Last Modified: Wed, 21 May 2025 23:21:38 GMT  
		Size: 7.9 MB (7876583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9881916f5a820676368755d769cd40b7e0e9df48c6ef2a0562e88f45e776ec`  
		Last Modified: Wed, 21 May 2025 23:21:38 GMT  
		Size: 392.1 KB (392131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84abbeff469e281c4068dc7dc6c3ed242eef8ede5e85715c5fa399657bb71c6`  
		Last Modified: Wed, 21 May 2025 23:21:38 GMT  
		Size: 76.3 KB (76293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b47390cd854b3fade658b434b169b4e9374c8a2e39ae485fb3e79f56b35eaa2`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f440703289eb36095d7d6dd12351d0112340ba8139904a0f99ea3bd9b340573e`  
		Last Modified: Wed, 21 May 2025 23:21:42 GMT  
		Size: 102.4 MB (102421180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad8887225b7196f8689f6ceae8e7ee1e65b3fa361d14bc231a0293b00ed259a`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a672aa636d853ecc57c05c5d7dabcd678d45e19a918073464387b191c7fd8f`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361648ea7136a2a8dd5f99092cfa11ea4051598b711011625e14fa6336295959`  
		Last Modified: Wed, 21 May 2025 23:21:40 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55450775d2f4f5c70ab37c8b96405115946e0b919d095dd90bc2c9e01d596203`  
		Last Modified: Wed, 21 May 2025 23:21:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c019c491c429ee2be1514aaab5093b32b924a3acbdc7c408ca313758abb2177d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ecd354a84054d72c56f2e0def88ce183b0b3ffa38ad85fd24745f6864c95b9`

```dockerfile
```

-	Layers:
	-	`sha256:90142802e757b2297600bde997a2557c09465e2b60ded163ed735c23c2c6b6e4`  
		Last Modified: Wed, 21 May 2025 23:21:38 GMT  
		Size: 4.0 MB (3989444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3043e001adaa538399030483dda9d4deea1a121c98989f3a8f1892411432536`  
		Last Modified: Wed, 21 May 2025 23:21:38 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:15729596c86dda15cc99edf750fc425cb57ef4edce5babce54d068a426a45a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138301136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cf79497d5220986281ff560d275803bb04fb7bc51e1cbb7a936f6d973a73c8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2633edfbe42095655e8e06326a2bb09e72f60054163cab4d32ecdf090a957da`  
		Last Modified: Tue, 29 Apr 2025 01:50:52 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0cf2efaa368539937e0c9e20e80322a37f0973ca6529dc176891bc2b6b4343`  
		Last Modified: Tue, 29 Apr 2025 01:50:53 GMT  
		Size: 7.7 MB (7654571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb956e71c0e68ceaea25a9a17c3479c71593de51c3e3883402da9bddd458ce9`  
		Last Modified: Tue, 29 Apr 2025 01:50:53 GMT  
		Size: 348.9 KB (348927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a6383735d775aae8622e383ef33c77472eab8ffce56113ccda5df7ac6cfa1c`  
		Last Modified: Tue, 29 Apr 2025 01:50:53 GMT  
		Size: 76.3 KB (76324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f979f73832f1924be9ae9da8592cf4f4e6c7eadc7cb4338f2bd8e4ce317e44`  
		Last Modified: Tue, 29 Apr 2025 01:50:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16239f6235a9d3bcdaf9c38f9927cd1e232df55ee863031a4353daadfea769b9`  
		Last Modified: Tue, 29 Apr 2025 01:50:57 GMT  
		Size: 102.1 MB (102149270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8220ab79af616850c33eb5221da223f95894f9c6a1ae7da136c296c3d03b510`  
		Last Modified: Tue, 29 Apr 2025 01:50:54 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6e43f89922d88c83e3806dff1d4bf75ccc80c4a4d308b57a4de073a5a1eca1`  
		Last Modified: Tue, 29 Apr 2025 01:50:54 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3804f08bee9c27c0fece5ba72adbe467bd4b68926d439c1c516309ffa3e74a2e`  
		Last Modified: Tue, 29 Apr 2025 01:50:55 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b49f429faf76187d67cc6f28f9db32073e600dab35eb869191557acfa4cde4`  
		Last Modified: Tue, 29 Apr 2025 01:50:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:df8ec2e03ec5c103efc80684aae3d7a53433bb17f2c2714e448b58288d74630b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fe7f0e4c9ec3c47ecda169839158b3abbe56f06752386e568d2c2c5df04c0e`

```dockerfile
```

-	Layers:
	-	`sha256:92ed9cd6274d1b94036200dcd5171f298f315f6db22e8327bba08ebd9992df49`  
		Last Modified: Tue, 29 Apr 2025 01:50:53 GMT  
		Size: 4.0 MB (3962487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:425cc3db72cabb981f4a91737562f7be0699079a61ccb18f8f8fe8d4369a21ab`  
		Last Modified: Tue, 29 Apr 2025 01:50:53 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:7819b07037fe98ec994ca26a121fbb8c9a601772df54fa0f3af9f7ba85e50a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135766171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220713081441f1810d0218f5900376c97d27ed09c05e86c7476f16287ab5794`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c8a4385111079823034d1e8ed702e9672cd681f79562137fa525d16803eea`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c0f7f5b2751909f18f45844094309abfc54100ace7c37207440666c3dd916`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 7.4 MB (7387937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b6aeef9cd48451c7352e0d027a4ab68782567fd1af8b1aeed4283756407f74`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 355.6 KB (355644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a016c259437b9920b9c085f993abedb656356821d7571071cb17db40433ce23`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf854b3c69326f429e568061da038a651efb11e32516f8571b1eb6c2fa4f676`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63c8fe755b51ffd8fbe51e653149697f4db50ec5f2e547f3cdacddcf23a8cc`  
		Last Modified: Tue, 29 Apr 2025 00:03:42 GMT  
		Size: 101.1 MB (101055957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702504975d7b1931a864c2373bbe22a5a0c200b6689e356d0e589bee6a061932`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c449b40f1681890fb4190af1efe37d7714370d105e051af05596c701a932f57`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094a79dad673e9d7ae35052d26551314238c734e732e0fb16915e7266b6547ad`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1480727e9ec140937813aea1076b6378bf266665e18b0e20314a588367868a3b`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:88af6693555cb508b2d025acdc1cf32ed693329c7425a63e3ca33fcae9d6527d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cd21e53513802102079ed3d78030c64a5a73292fb437f3f01cd3c37abebb08`

```dockerfile
```

-	Layers:
	-	`sha256:899e8cbc1e36d790e687a9f1f9b1b0d69e11609f8e383484c7a552377bdc224b`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 4.0 MB (3961282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5195173997f32afdbc21e62b738eca6b36722bdcbe2527bfd1b80cc09e348e`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:d8d3d9f9db0623f3d300e629a75a90b83cf4f886e64cab807c301d4a492a1bcb
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
$ docker pull couchdb@sha256:baeee2679298fb6a68701e1240a5d722d9bde10891d2df481064cd43fda8d9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156376138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5763e930c1db2b91f95e20cc0e3819eb2a12d3bc43e6fd26192425f7d65eb3ce`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26c958d6c4d447f8a8d0364934ad1fbe3d621b0994241e7a1bc6c1da675ef26`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82037acdce809e8a6d5d7fa667076515748e41198ffffdd5dabd86155d68096`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 7.9 MB (7876476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967602685befc4ac9e1ceae20f9d0eeb0956b55362a1ccda2bbd753b546259a`  
		Last Modified: Wed, 21 May 2025 23:21:34 GMT  
		Size: 77.3 MB (77324664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ce896791c198afced5bc9fc81a882ee6e098bbcb817c5810f7ab3bf31f210f`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 415.0 KB (414989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37afc41665e2753cece416555d49bd6203a19478d97edd2f0c7f4adb4ce8a3c`  
		Last Modified: Wed, 21 May 2025 23:21:34 GMT  
		Size: 99.3 KB (99327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94186914076559a29762b6e9db34b4506a3a448b2c25e8e267c92b403ccb2e69`  
		Last Modified: Wed, 21 May 2025 23:21:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686b78b0943f21f1810832f2ba2d33fbda1c4d95ad356d919d7eb3ae5ffbb029`  
		Last Modified: Wed, 21 May 2025 23:21:34 GMT  
		Size: 42.4 MB (42433470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed2cc40c96c6da96e95777a48ccf4730d0b5574288e2e9332bd620aa4112510`  
		Last Modified: Wed, 21 May 2025 23:21:34 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f7523d310e8e8e4ed80112562db7595085f60356d19bf9451a58c5e6f7b5ae19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3527177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125c5b6e6ffd5112963fc4d2101c2f68a1926b4ce68729008c5b9281c50aadd7`

```dockerfile
```

-	Layers:
	-	`sha256:9ff0fa278dd93ae3168a16479a214b2ba0f249118ce041e7c2305c53583b7498`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 3.5 MB (3502919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a05f5531efd5204ae9926a29d2f8794374993f7809bb0801abfe00f252b5e91b`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 24.3 KB (24258 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0fc5bf7f8656c738548765f26d845e06e1f397e2ba7769a12f072ed480ea2192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155151224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5839b1b3d1b63e9c6218041f808c4f01c7d9c791f10d4af997c8168ace78fd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac2fb37a32e5d32440fe31bf070b4f898cd1be575a07c97cb79545c9b0185ba`  
		Last Modified: Tue, 29 Apr 2025 01:51:45 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01d9b43b431ef17b69173455b60689597c4625f6f6c4f7eb221a030ab004321`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 7.7 MB (7654523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3825b273ce4e5eb6867f90ff56927c439343cdddf5b9851536108096d71a168f`  
		Last Modified: Tue, 29 Apr 2025 01:51:48 GMT  
		Size: 76.6 MB (76624178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6a8d76ed8c03ee5297cc4c2d41c92edfb6fa1335a48b18b7dd5b4bd3c123b`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 371.7 KB (371743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19359905d9ad3145a133462b7a4bb5f7b0ec3e6fdba00b937fd82721789cf935`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 99.3 KB (99267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e15435482689c2ae429169c378e85e1689ad1fcbf407d2afc7d57623eed71a`  
		Last Modified: Tue, 29 Apr 2025 01:51:47 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad50cd5577f3297510ebe03234b653c4bda90d45cc8ca400513aca09e0446e0`  
		Last Modified: Tue, 29 Apr 2025 01:51:48 GMT  
		Size: 42.3 MB (42333012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a49280d94a95e153d3e016076b7e5188cfdc8ab11ad546a46ab8a4c31f8340`  
		Last Modified: Tue, 29 Apr 2025 01:51:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:02e17f86ce17541e3ff54b18c1e75db26776c37e7a0f04eb985686e8706efd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb40c217bb4ab0e4de428c0aba3fc79410576e35dcd21a2d1e4f0df951d7348`

```dockerfile
```

-	Layers:
	-	`sha256:e1a0a1588545666af4b5a0101d887a0dae635f9389deab9ea94282c17c799abd`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 3.5 MB (3467148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f6b2e21e354c6da21bec28182224c1de6a2a046a3b09e39131690d219a25642`  
		Last Modified: Tue, 29 Apr 2025 01:51:45 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:567f3e53824961c5f506118d23c53e6c44333ede5da72ca9fc0453ee8df3559f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149977892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d2af33615aa36bcba2719f0280f43028b632981cf48362c439c8774e5a7e08`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeb9febea926497c6b73a956a66c5ec7705a80ed96a88acd22e023a12bb07b9`  
		Last Modified: Tue, 29 Apr 2025 00:04:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb3720e0f56a097c25a4a4a982b82bafb5b5cd40ac87ffefca40556227f213f`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 7.4 MB (7387952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce679ce7dd142ab1209f6b1e198804851164e290d7c9412f489110386d84a3c4`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 73.1 MB (73065225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ea5e69fb0ac2e8ec68ad79d4ed32a98475e57dec15e01433a7aac1c8d2bcff`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 378.1 KB (378103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8084ad1ebf84dff15753e78e53bdc8cfdccdcb39266f1bf8e231f251d78a64e3`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 99.4 KB (99449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a49819b32ddd9c0fe27e1ed0f760870d4d9170232838540cc48f818ef2606e`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cd8bce374995c6a118e0965c0b2ebf3fa93ae834354a829cc1b3cd0f830219`  
		Last Modified: Tue, 29 Apr 2025 00:04:49 GMT  
		Size: 42.2 MB (42160416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55bbc492280b5c45b056b641e8fec35f5fb54bc50068de783a4c110b4beb376`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:77c04fe246e4b659963c87d866f2678b43426ef3984aac6cc092e602b0dc0ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f22a5e7194519b1d9eff220c23222179736285e22078c6328ae14eda1ca0b0`

```dockerfile
```

-	Layers:
	-	`sha256:e581491861b03880116342ed4b02be1373f61f3ac37d5e781506fac9e30a02d5`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 3.5 MB (3461893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e144eeff7b03258ac15dcb32b9ea1e2ff7892643f844b7df4a7b15118c6c87e3`  
		Last Modified: Tue, 29 Apr 2025 00:04:46 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:6ec7bea4222980f4630b91614ef668e75042c0fdf1a2c6dd153c34f5c2522d2f
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
$ docker pull couchdb@sha256:48461e712eb19a62999037cecd2592b579cd2a099aff546bffd354d4a4981503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139819073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457042a730fbb82c61566ed8e79d453f3a2b8b3b4f1caacf640675f0b7d967cf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db76d6e1c7998fb7ae0ccb603376f72d1b2018fc3301cdf33f421573621423`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796832cf42a2afc1527f14d3835cb90abc5d314cbb4eb381fef0e2953985377c`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 7.9 MB (7876592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c546028bb904f5fd511313dc39d6843111f3a6e0f8466d9d6d021b2a23e9a6d`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 392.1 KB (392129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb8ea8809565d82d409be15bb0a487592feb0f0f45a1a9f85ff4eaf4de21225`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 76.3 KB (76283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587baf2d1aec5aecdd448d026ad54ff5c007d7060b808956f70d6f7a9bd14340`  
		Last Modified: Wed, 21 May 2025 23:21:19 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496680db7db212dcc94ccbce6034c0f0791a93a26474a3fee2fa192a624cc7dd`  
		Last Modified: Wed, 21 May 2025 23:21:21 GMT  
		Size: 103.2 MB (103243310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588b33ca1e68b6ff6bf8acb7508583394d58125f6223688c34370302ecc14411`  
		Last Modified: Wed, 21 May 2025 23:21:19 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b863b579a751a6b5cbe57b4c53895d5078b68b027d26e71de5b951d9bcc23b04`  
		Last Modified: Wed, 21 May 2025 23:21:20 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711bcfe1ad83602d399128ff2639b813736951b0469a95ba7e5d4bc87cc7bdbe`  
		Last Modified: Wed, 21 May 2025 23:21:20 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66f91f3e055f54abdbf7b7c953477bd00bc4af34ec3fcfe884b8622aee2c30f`  
		Last Modified: Wed, 21 May 2025 23:21:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:984ceb992e4fae3bfe805ef41aae42ff8c56bdd05b11f97b3f91aeb74287d2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4037092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cadb37b6ecf8b6b8916ca50c9b249a8dac3cdca7772600f52d1498fc1993da`

```dockerfile
```

-	Layers:
	-	`sha256:fe5b854cbd1b60d14e82a3922af523976763eecef3b1e94d773d249cbd8c5136`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 4.0 MB (4005311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f2d4dd498de68b34125f3c8cf7cf8b06b23533a94545eb9f97858fc055533de`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2e5d6e31ba5b9b92989e29faa365e2bffb92af2c68d74ece6a2ca43016ba6648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139041917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11de94aa647367ba5fe5a4ea744897e9a6e24f0ab3c0db12740c8cafca9ee4d4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fda7edaf9e5fa4bff22f8647fc45ace1dec9a2413c557a56f3d209571bb03d3`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f44d3c9be40e352cbd13efebb94c5b86d4cd047a37cb05e1470b3799da491`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 7.7 MB (7654565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77c2f410b4ff91dda61e7492f539cf3280b1e296b0f87b974582537e952a860`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 348.9 KB (348949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f245645ed55f34a29dc8f3628a26a2df51feae716273e621d28255c5cd0366fc`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 76.3 KB (76313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5710c3924976aed640fb8f738d4e47e35ecd4a5fcf0b2511f68afe7d1146528`  
		Last Modified: Tue, 06 May 2025 17:58:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0454c720549b1dcd1cdef601206f434cdd971e17c9a772d65ba3975f97b969`  
		Last Modified: Tue, 06 May 2025 17:58:05 GMT  
		Size: 102.9 MB (102890031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a994b43877b24b8e8eb646784ca98c6cc75ae1c83f06754649a2bd484c7b1831`  
		Last Modified: Tue, 06 May 2025 17:58:02 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c16e2d34057757eb1428efb7c184e238c3794dd98268e3bd294f2f244475f`  
		Last Modified: Tue, 06 May 2025 17:58:02 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc5813c77ab5a6b2305995bddd3c3e4d7a17f36fc53dbf8de965c6d9d85f0a`  
		Last Modified: Tue, 06 May 2025 17:58:03 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc85c73a0cbd10b91c9982c83b79f58e9b9deab4cf54e563375a8a928c2dffa`  
		Last Modified: Tue, 06 May 2025 17:58:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:fe60acaabade72ceee44fb2665c04f57bc8c5b0c47358f52c9b5043925401920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b478e56c588977ce65a82fb0d0c0f20cc1f87c7ea3af87f9bbd3fdaeae84d40c`

```dockerfile
```

-	Layers:
	-	`sha256:89d3e99d85d7bb933bd62e346a0a1620c97bdf09d7c859d291d8a37233ee45df`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 4.0 MB (3977764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:112e82b651057c0dc11627c3143fd48ca8640c788a42c40bdf853c248d46e608`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:aa073d5b2899110636aa11b4ccab6e222f76ee8d6066a8d595b6932a31f35352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136508976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5d7eb1088b9aeadc82c9d60d973705ecad3e5cfbe2233370486d9318bce329`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae941489b0da77e1ee8a58c546530f92eb369117b11a80bba562437bc949405`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215e6a02cfb983cdf525705ca0c858e32481b6d88effe8dd5638e254428c9bc1`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 7.4 MB (7390952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea51146f220497d66074837aed4d4957b378c092326bae49eb2d25956a7124ed`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 355.6 KB (355621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8ebfd7a69c538a6ea4a568bbcbd2d09dbe7dc0cb1c8ad80b5013567bf9c77`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 76.3 KB (76309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f6d65faf14a43908fc64a3f7c5b8a0093df475ab99ccd1d0fbb4cb1856eabf`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8bc5ef397d902964b72e93ad3785ed5674999751e96c4039ef937aecb8127d`  
		Last Modified: Thu, 22 May 2025 01:04:40 GMT  
		Size: 101.8 MB (101797850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa33ac6d9246fc0b0be7672444d9e70ff24dae5519016facb02368cdf4db1d1a`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62df8f16139eddb5120f8765468175dd99b130d830b7d9f1d53f4935dc7ed44`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c74ac65654aa3b3e84aaa87876e05096485f3682d04333e26366ac6161fe75`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a4f71afa5a484da6c2c13331d63e07dfe4c47964b692716adf42caeab50c9`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:636b405f48663602370accde8d8bdac3d47d86051471d1734ec16114c16d8098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4036180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a640caec505c17fdd7c1ef70a9b01903be51d0432e21c40889962ba68ea7094a`

```dockerfile
```

-	Layers:
	-	`sha256:c8cb70efa326f50969856150cf5c10d1b1700062b0465df1ef7c61d992759afc`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 4.0 MB (4004399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa0b8b821b8a67c0bf0425f63deb4111df467de46101259a3c149b787203648`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:69f0862d6fce32301cecfb5b1c3c1e4f9b3b762d725766e83dcc731a79ea94ce
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
$ docker pull couchdb@sha256:0e9d627a82619751cc0d6f42f899aa11e8b0fd01afa5f06cbc2de5dbc0151e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156377003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f486850fee961991297613cd422a46f6df9bf60911d27619b99ab996d1a18ef`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9499470c9acbc00bcc886054c1cda3f5c8c36fbf550a642960f2726c99f7cccd`  
		Last Modified: Wed, 21 May 2025 23:21:31 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0590250af4762255b25cff955958f055fdfcafdeb9007c8e4b4f571432bc98cc`  
		Last Modified: Wed, 21 May 2025 23:21:32 GMT  
		Size: 7.9 MB (7876617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffa6110867a1df8c941ceb29416c301977da6dcc8a82ce3dbf7d4931009ac58`  
		Last Modified: Wed, 21 May 2025 23:21:34 GMT  
		Size: 77.3 MB (77324631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5f96efa9cf3073c2562091ffd7f4ef6b7934631bc159dee2cda56169bb3c37`  
		Last Modified: Wed, 21 May 2025 23:21:31 GMT  
		Size: 415.0 KB (414987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98d8ddcf13047ccfd1fc7c4747bc785c5cb1a0459ff93c5263a96defebe4d42`  
		Last Modified: Wed, 21 May 2025 23:21:32 GMT  
		Size: 99.3 KB (99323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733d973b08d70309f6af91291d0d69983e350cf6377bd9a4649c156c22827d6`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749f6475cadf4afd508e15603543c680150a2dcf6641c3d8a64a766c1bc71bc`  
		Last Modified: Wed, 21 May 2025 23:21:35 GMT  
		Size: 42.4 MB (42434239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002a25bfa7ceaa38750737429b07cefd358da6cdc7699c3062c6602c8a5db5bc`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:e06b980a13665020a73a39fbad472958d45e6c263edc8c901c8c6782efd65326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3527788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e8f86012d808409684a3638c5fcf10b5cc3c3250ea82df6f6bc0c3cb24aaef`

```dockerfile
```

-	Layers:
	-	`sha256:6b81beb7bb8f78ee184908beda66bcd1024e3a72659520cb1cf1e11b7b3cc114`  
		Last Modified: Wed, 21 May 2025 23:21:32 GMT  
		Size: 3.5 MB (3503225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e797f8a70670a8c360e264c6b98942981c8680eb266df741b8e284dd2db0f5a`  
		Last Modified: Wed, 21 May 2025 23:21:31 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7fdb1df7e89b35ae184e2975f8ed5d5c72acd6e651588d7854923639ea383648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155180531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90792137fb7d00afa09943655aa32c8b56afb2ed23f9ca819aef6c02127e89b0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104637e2eb67ec32ff000f153eebca995c5a32bdca49fe1b16015251fd887842`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc58e96c4d79f04a31e09066efeea0f21f93f87a60cd80b537546b799ebbff9`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 7.7 MB (7654542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f58f87545a1ea3e85e36bc4f13c6528480a4d096cabe6e23b6919d84a3a21fa`  
		Last Modified: Tue, 06 May 2025 17:58:59 GMT  
		Size: 76.7 MB (76653670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886a375283a50138292c4ab34c2a2cd473c86f479a0657d206917439b9293ef4`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 371.7 KB (371732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccf50ebfde2d6eb28578d23558bec7ad3fcf33ed5edbbda390b0c02b37636ab`  
		Last Modified: Tue, 06 May 2025 17:58:56 GMT  
		Size: 99.3 KB (99262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a67aafe8a97aa0a8dd806d49d1da627072a88c7e466a6957064c3b1ac9f579`  
		Last Modified: Tue, 06 May 2025 17:58:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd40dddaef0fcda5c486a0d107b1aeac5eae87d112d92a7f8babc07a9c2bc5b`  
		Last Modified: Tue, 06 May 2025 17:58:59 GMT  
		Size: 42.3 MB (42332820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ead4ac28d2805b9ad7d4bc386937a7df61b55d7493ee5c9fa48d6eab8baa75c`  
		Last Modified: Tue, 06 May 2025 17:58:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc0f7d743c3b12042d2363c435ba9a3136bffb0e8741d2777c0e9501b34fb0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b851a388ca66506c60d98b25da2535df558b509b5464f97e568dcd7055452f`

```dockerfile
```

-	Layers:
	-	`sha256:926a4dc0d56e3c9be08d364b9e30b94d534c9a7d479ce49b32d9a7fac0b85348`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 3.5 MB (3467148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22075a440bd6b34723136a723584525e19f147bda33189d33a6d6199161fb556`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:c144920a1f33f2407cb3611ea12b4e80ceebd4fa134fe745503729ed901bbe2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149990045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e2d1ccfff6600840e8ab5f7799ad12211edb132dddf6c0f6f05b11f2e47fd8`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26396a1c92d005f1f73ce8a5a786829b16fd7bfeea83b11aab47577c79125a6`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474be071a26fc29b13f67d8e56c399b46d3b8233fba772eddf197a41e47b3ce`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 7.4 MB (7391039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7557a7943629e9a5e09974b851cd3f71af7ae009a3c979a57c2005e05a04ae`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 73.1 MB (73075902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364ab5de64b0f27b98361254033eb8e64dab17927d0d5ed36673abde5d5a1116`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 378.1 KB (378082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9582aebb38d001676e191f1d1739f9651fb01da8c1d4099e8e0eb6e86e453`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 99.4 KB (99441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15939d7d9273f1580bd4614a899539324dde9b46bb9c958cb5ecd8b6e118b3b7`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9ca0b94e18b2399600f2856dafbb9e4ad3d61ca982c486d68ee6f2f8e2f845`  
		Last Modified: Thu, 22 May 2025 01:05:47 GMT  
		Size: 42.2 MB (42160892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afc856a01f3eda18d2caeeef10985ba6f113d6e40fa30d36627cffd35c50895`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:9026af3d06aa014b566e394abb7e54e49cf289dcb09ad6c4bc2363b87545ace7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbed73861a10a7185fb0f4d338c33bb2b7b13941e243ef568f46cd7853f1b44`

```dockerfile
```

-	Layers:
	-	`sha256:50da05748a9be431439b8d33cd60430c479b3050bc095b88e787d64e1bfbbbbc`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 3.5 MB (3496646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b67689b0e1b9ff33b91e6f02f0d07c8551e1671ab573b630d590e1607976d665`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0`

```console
$ docker pull couchdb@sha256:6ec7bea4222980f4630b91614ef668e75042c0fdf1a2c6dd153c34f5c2522d2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.0` - linux; amd64

```console
$ docker pull couchdb@sha256:48461e712eb19a62999037cecd2592b579cd2a099aff546bffd354d4a4981503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139819073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457042a730fbb82c61566ed8e79d453f3a2b8b3b4f1caacf640675f0b7d967cf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db76d6e1c7998fb7ae0ccb603376f72d1b2018fc3301cdf33f421573621423`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796832cf42a2afc1527f14d3835cb90abc5d314cbb4eb381fef0e2953985377c`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 7.9 MB (7876592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c546028bb904f5fd511313dc39d6843111f3a6e0f8466d9d6d021b2a23e9a6d`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 392.1 KB (392129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb8ea8809565d82d409be15bb0a487592feb0f0f45a1a9f85ff4eaf4de21225`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 76.3 KB (76283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587baf2d1aec5aecdd448d026ad54ff5c007d7060b808956f70d6f7a9bd14340`  
		Last Modified: Wed, 21 May 2025 23:21:19 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496680db7db212dcc94ccbce6034c0f0791a93a26474a3fee2fa192a624cc7dd`  
		Last Modified: Wed, 21 May 2025 23:21:21 GMT  
		Size: 103.2 MB (103243310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588b33ca1e68b6ff6bf8acb7508583394d58125f6223688c34370302ecc14411`  
		Last Modified: Wed, 21 May 2025 23:21:19 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b863b579a751a6b5cbe57b4c53895d5078b68b027d26e71de5b951d9bcc23b04`  
		Last Modified: Wed, 21 May 2025 23:21:20 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711bcfe1ad83602d399128ff2639b813736951b0469a95ba7e5d4bc87cc7bdbe`  
		Last Modified: Wed, 21 May 2025 23:21:20 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66f91f3e055f54abdbf7b7c953477bd00bc4af34ec3fcfe884b8622aee2c30f`  
		Last Modified: Wed, 21 May 2025 23:21:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:984ceb992e4fae3bfe805ef41aae42ff8c56bdd05b11f97b3f91aeb74287d2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4037092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cadb37b6ecf8b6b8916ca50c9b249a8dac3cdca7772600f52d1498fc1993da`

```dockerfile
```

-	Layers:
	-	`sha256:fe5b854cbd1b60d14e82a3922af523976763eecef3b1e94d773d249cbd8c5136`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 4.0 MB (4005311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f2d4dd498de68b34125f3c8cf7cf8b06b23533a94545eb9f97858fc055533de`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2e5d6e31ba5b9b92989e29faa365e2bffb92af2c68d74ece6a2ca43016ba6648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139041917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11de94aa647367ba5fe5a4ea744897e9a6e24f0ab3c0db12740c8cafca9ee4d4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fda7edaf9e5fa4bff22f8647fc45ace1dec9a2413c557a56f3d209571bb03d3`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f44d3c9be40e352cbd13efebb94c5b86d4cd047a37cb05e1470b3799da491`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 7.7 MB (7654565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77c2f410b4ff91dda61e7492f539cf3280b1e296b0f87b974582537e952a860`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 348.9 KB (348949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f245645ed55f34a29dc8f3628a26a2df51feae716273e621d28255c5cd0366fc`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 76.3 KB (76313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5710c3924976aed640fb8f738d4e47e35ecd4a5fcf0b2511f68afe7d1146528`  
		Last Modified: Tue, 06 May 2025 17:58:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0454c720549b1dcd1cdef601206f434cdd971e17c9a772d65ba3975f97b969`  
		Last Modified: Tue, 06 May 2025 17:58:05 GMT  
		Size: 102.9 MB (102890031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a994b43877b24b8e8eb646784ca98c6cc75ae1c83f06754649a2bd484c7b1831`  
		Last Modified: Tue, 06 May 2025 17:58:02 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c16e2d34057757eb1428efb7c184e238c3794dd98268e3bd294f2f244475f`  
		Last Modified: Tue, 06 May 2025 17:58:02 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc5813c77ab5a6b2305995bddd3c3e4d7a17f36fc53dbf8de965c6d9d85f0a`  
		Last Modified: Tue, 06 May 2025 17:58:03 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc85c73a0cbd10b91c9982c83b79f58e9b9deab4cf54e563375a8a928c2dffa`  
		Last Modified: Tue, 06 May 2025 17:58:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:fe60acaabade72ceee44fb2665c04f57bc8c5b0c47358f52c9b5043925401920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b478e56c588977ce65a82fb0d0c0f20cc1f87c7ea3af87f9bbd3fdaeae84d40c`

```dockerfile
```

-	Layers:
	-	`sha256:89d3e99d85d7bb933bd62e346a0a1620c97bdf09d7c859d291d8a37233ee45df`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 4.0 MB (3977764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:112e82b651057c0dc11627c3143fd48ca8640c788a42c40bdf853c248d46e608`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; s390x

```console
$ docker pull couchdb@sha256:aa073d5b2899110636aa11b4ccab6e222f76ee8d6066a8d595b6932a31f35352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136508976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5d7eb1088b9aeadc82c9d60d973705ecad3e5cfbe2233370486d9318bce329`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae941489b0da77e1ee8a58c546530f92eb369117b11a80bba562437bc949405`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215e6a02cfb983cdf525705ca0c858e32481b6d88effe8dd5638e254428c9bc1`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 7.4 MB (7390952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea51146f220497d66074837aed4d4957b378c092326bae49eb2d25956a7124ed`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 355.6 KB (355621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8ebfd7a69c538a6ea4a568bbcbd2d09dbe7dc0cb1c8ad80b5013567bf9c77`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 76.3 KB (76309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f6d65faf14a43908fc64a3f7c5b8a0093df475ab99ccd1d0fbb4cb1856eabf`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8bc5ef397d902964b72e93ad3785ed5674999751e96c4039ef937aecb8127d`  
		Last Modified: Thu, 22 May 2025 01:04:40 GMT  
		Size: 101.8 MB (101797850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa33ac6d9246fc0b0be7672444d9e70ff24dae5519016facb02368cdf4db1d1a`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62df8f16139eddb5120f8765468175dd99b130d830b7d9f1d53f4935dc7ed44`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c74ac65654aa3b3e84aaa87876e05096485f3682d04333e26366ac6161fe75`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a4f71afa5a484da6c2c13331d63e07dfe4c47964b692716adf42caeab50c9`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:636b405f48663602370accde8d8bdac3d47d86051471d1734ec16114c16d8098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4036180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a640caec505c17fdd7c1ef70a9b01903be51d0432e21c40889962ba68ea7094a`

```dockerfile
```

-	Layers:
	-	`sha256:c8cb70efa326f50969856150cf5c10d1b1700062b0465df1ef7c61d992759afc`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 4.0 MB (4004399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa0b8b821b8a67c0bf0425f63deb4111df467de46101259a3c149b787203648`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0-nouveau`

```console
$ docker pull couchdb@sha256:69f0862d6fce32301cecfb5b1c3c1e4f9b3b762d725766e83dcc731a79ea94ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.0-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:0e9d627a82619751cc0d6f42f899aa11e8b0fd01afa5f06cbc2de5dbc0151e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156377003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f486850fee961991297613cd422a46f6df9bf60911d27619b99ab996d1a18ef`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9499470c9acbc00bcc886054c1cda3f5c8c36fbf550a642960f2726c99f7cccd`  
		Last Modified: Wed, 21 May 2025 23:21:31 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0590250af4762255b25cff955958f055fdfcafdeb9007c8e4b4f571432bc98cc`  
		Last Modified: Wed, 21 May 2025 23:21:32 GMT  
		Size: 7.9 MB (7876617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffa6110867a1df8c941ceb29416c301977da6dcc8a82ce3dbf7d4931009ac58`  
		Last Modified: Wed, 21 May 2025 23:21:34 GMT  
		Size: 77.3 MB (77324631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5f96efa9cf3073c2562091ffd7f4ef6b7934631bc159dee2cda56169bb3c37`  
		Last Modified: Wed, 21 May 2025 23:21:31 GMT  
		Size: 415.0 KB (414987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98d8ddcf13047ccfd1fc7c4747bc785c5cb1a0459ff93c5263a96defebe4d42`  
		Last Modified: Wed, 21 May 2025 23:21:32 GMT  
		Size: 99.3 KB (99323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733d973b08d70309f6af91291d0d69983e350cf6377bd9a4649c156c22827d6`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749f6475cadf4afd508e15603543c680150a2dcf6641c3d8a64a766c1bc71bc`  
		Last Modified: Wed, 21 May 2025 23:21:35 GMT  
		Size: 42.4 MB (42434239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002a25bfa7ceaa38750737429b07cefd358da6cdc7699c3062c6602c8a5db5bc`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:e06b980a13665020a73a39fbad472958d45e6c263edc8c901c8c6782efd65326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3527788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e8f86012d808409684a3638c5fcf10b5cc3c3250ea82df6f6bc0c3cb24aaef`

```dockerfile
```

-	Layers:
	-	`sha256:6b81beb7bb8f78ee184908beda66bcd1024e3a72659520cb1cf1e11b7b3cc114`  
		Last Modified: Wed, 21 May 2025 23:21:32 GMT  
		Size: 3.5 MB (3503225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e797f8a70670a8c360e264c6b98942981c8680eb266df741b8e284dd2db0f5a`  
		Last Modified: Wed, 21 May 2025 23:21:31 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7fdb1df7e89b35ae184e2975f8ed5d5c72acd6e651588d7854923639ea383648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155180531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90792137fb7d00afa09943655aa32c8b56afb2ed23f9ca819aef6c02127e89b0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104637e2eb67ec32ff000f153eebca995c5a32bdca49fe1b16015251fd887842`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc58e96c4d79f04a31e09066efeea0f21f93f87a60cd80b537546b799ebbff9`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 7.7 MB (7654542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f58f87545a1ea3e85e36bc4f13c6528480a4d096cabe6e23b6919d84a3a21fa`  
		Last Modified: Tue, 06 May 2025 17:58:59 GMT  
		Size: 76.7 MB (76653670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886a375283a50138292c4ab34c2a2cd473c86f479a0657d206917439b9293ef4`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 371.7 KB (371732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccf50ebfde2d6eb28578d23558bec7ad3fcf33ed5edbbda390b0c02b37636ab`  
		Last Modified: Tue, 06 May 2025 17:58:56 GMT  
		Size: 99.3 KB (99262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a67aafe8a97aa0a8dd806d49d1da627072a88c7e466a6957064c3b1ac9f579`  
		Last Modified: Tue, 06 May 2025 17:58:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd40dddaef0fcda5c486a0d107b1aeac5eae87d112d92a7f8babc07a9c2bc5b`  
		Last Modified: Tue, 06 May 2025 17:58:59 GMT  
		Size: 42.3 MB (42332820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ead4ac28d2805b9ad7d4bc386937a7df61b55d7493ee5c9fa48d6eab8baa75c`  
		Last Modified: Tue, 06 May 2025 17:58:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc0f7d743c3b12042d2363c435ba9a3136bffb0e8741d2777c0e9501b34fb0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b851a388ca66506c60d98b25da2535df558b509b5464f97e568dcd7055452f`

```dockerfile
```

-	Layers:
	-	`sha256:926a4dc0d56e3c9be08d364b9e30b94d534c9a7d479ce49b32d9a7fac0b85348`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 3.5 MB (3467148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22075a440bd6b34723136a723584525e19f147bda33189d33a6d6199161fb556`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:c144920a1f33f2407cb3611ea12b4e80ceebd4fa134fe745503729ed901bbe2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149990045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e2d1ccfff6600840e8ab5f7799ad12211edb132dddf6c0f6f05b11f2e47fd8`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26396a1c92d005f1f73ce8a5a786829b16fd7bfeea83b11aab47577c79125a6`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474be071a26fc29b13f67d8e56c399b46d3b8233fba772eddf197a41e47b3ce`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 7.4 MB (7391039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7557a7943629e9a5e09974b851cd3f71af7ae009a3c979a57c2005e05a04ae`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 73.1 MB (73075902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364ab5de64b0f27b98361254033eb8e64dab17927d0d5ed36673abde5d5a1116`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 378.1 KB (378082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9582aebb38d001676e191f1d1739f9651fb01da8c1d4099e8e0eb6e86e453`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 99.4 KB (99441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15939d7d9273f1580bd4614a899539324dde9b46bb9c958cb5ecd8b6e118b3b7`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9ca0b94e18b2399600f2856dafbb9e4ad3d61ca982c486d68ee6f2f8e2f845`  
		Last Modified: Thu, 22 May 2025 01:05:47 GMT  
		Size: 42.2 MB (42160892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afc856a01f3eda18d2caeeef10985ba6f113d6e40fa30d36627cffd35c50895`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:9026af3d06aa014b566e394abb7e54e49cf289dcb09ad6c4bc2363b87545ace7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbed73861a10a7185fb0f4d338c33bb2b7b13941e243ef568f46cd7853f1b44`

```dockerfile
```

-	Layers:
	-	`sha256:50da05748a9be431439b8d33cd60430c479b3050bc095b88e787d64e1bfbbbbc`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 3.5 MB (3496646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b67689b0e1b9ff33b91e6f02f0d07c8551e1671ab573b630d590e1607976d665`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:6ec7bea4222980f4630b91614ef668e75042c0fdf1a2c6dd153c34f5c2522d2f
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
$ docker pull couchdb@sha256:48461e712eb19a62999037cecd2592b579cd2a099aff546bffd354d4a4981503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139819073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457042a730fbb82c61566ed8e79d453f3a2b8b3b4f1caacf640675f0b7d967cf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db76d6e1c7998fb7ae0ccb603376f72d1b2018fc3301cdf33f421573621423`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796832cf42a2afc1527f14d3835cb90abc5d314cbb4eb381fef0e2953985377c`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 7.9 MB (7876592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c546028bb904f5fd511313dc39d6843111f3a6e0f8466d9d6d021b2a23e9a6d`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 392.1 KB (392129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb8ea8809565d82d409be15bb0a487592feb0f0f45a1a9f85ff4eaf4de21225`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 76.3 KB (76283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587baf2d1aec5aecdd448d026ad54ff5c007d7060b808956f70d6f7a9bd14340`  
		Last Modified: Wed, 21 May 2025 23:21:19 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496680db7db212dcc94ccbce6034c0f0791a93a26474a3fee2fa192a624cc7dd`  
		Last Modified: Wed, 21 May 2025 23:21:21 GMT  
		Size: 103.2 MB (103243310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588b33ca1e68b6ff6bf8acb7508583394d58125f6223688c34370302ecc14411`  
		Last Modified: Wed, 21 May 2025 23:21:19 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b863b579a751a6b5cbe57b4c53895d5078b68b027d26e71de5b951d9bcc23b04`  
		Last Modified: Wed, 21 May 2025 23:21:20 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711bcfe1ad83602d399128ff2639b813736951b0469a95ba7e5d4bc87cc7bdbe`  
		Last Modified: Wed, 21 May 2025 23:21:20 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66f91f3e055f54abdbf7b7c953477bd00bc4af34ec3fcfe884b8622aee2c30f`  
		Last Modified: Wed, 21 May 2025 23:21:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:984ceb992e4fae3bfe805ef41aae42ff8c56bdd05b11f97b3f91aeb74287d2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4037092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cadb37b6ecf8b6b8916ca50c9b249a8dac3cdca7772600f52d1498fc1993da`

```dockerfile
```

-	Layers:
	-	`sha256:fe5b854cbd1b60d14e82a3922af523976763eecef3b1e94d773d249cbd8c5136`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 4.0 MB (4005311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f2d4dd498de68b34125f3c8cf7cf8b06b23533a94545eb9f97858fc055533de`  
		Last Modified: Wed, 21 May 2025 23:21:18 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2e5d6e31ba5b9b92989e29faa365e2bffb92af2c68d74ece6a2ca43016ba6648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139041917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11de94aa647367ba5fe5a4ea744897e9a6e24f0ab3c0db12740c8cafca9ee4d4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fda7edaf9e5fa4bff22f8647fc45ace1dec9a2413c557a56f3d209571bb03d3`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f44d3c9be40e352cbd13efebb94c5b86d4cd047a37cb05e1470b3799da491`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 7.7 MB (7654565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77c2f410b4ff91dda61e7492f539cf3280b1e296b0f87b974582537e952a860`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 348.9 KB (348949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f245645ed55f34a29dc8f3628a26a2df51feae716273e621d28255c5cd0366fc`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 76.3 KB (76313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5710c3924976aed640fb8f738d4e47e35ecd4a5fcf0b2511f68afe7d1146528`  
		Last Modified: Tue, 06 May 2025 17:58:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0454c720549b1dcd1cdef601206f434cdd971e17c9a772d65ba3975f97b969`  
		Last Modified: Tue, 06 May 2025 17:58:05 GMT  
		Size: 102.9 MB (102890031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a994b43877b24b8e8eb646784ca98c6cc75ae1c83f06754649a2bd484c7b1831`  
		Last Modified: Tue, 06 May 2025 17:58:02 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c16e2d34057757eb1428efb7c184e238c3794dd98268e3bd294f2f244475f`  
		Last Modified: Tue, 06 May 2025 17:58:02 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc5813c77ab5a6b2305995bddd3c3e4d7a17f36fc53dbf8de965c6d9d85f0a`  
		Last Modified: Tue, 06 May 2025 17:58:03 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc85c73a0cbd10b91c9982c83b79f58e9b9deab4cf54e563375a8a928c2dffa`  
		Last Modified: Tue, 06 May 2025 17:58:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:fe60acaabade72ceee44fb2665c04f57bc8c5b0c47358f52c9b5043925401920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b478e56c588977ce65a82fb0d0c0f20cc1f87c7ea3af87f9bbd3fdaeae84d40c`

```dockerfile
```

-	Layers:
	-	`sha256:89d3e99d85d7bb933bd62e346a0a1620c97bdf09d7c859d291d8a37233ee45df`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 4.0 MB (3977764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:112e82b651057c0dc11627c3143fd48ca8640c788a42c40bdf853c248d46e608`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:aa073d5b2899110636aa11b4ccab6e222f76ee8d6066a8d595b6932a31f35352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136508976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5d7eb1088b9aeadc82c9d60d973705ecad3e5cfbe2233370486d9318bce329`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae941489b0da77e1ee8a58c546530f92eb369117b11a80bba562437bc949405`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215e6a02cfb983cdf525705ca0c858e32481b6d88effe8dd5638e254428c9bc1`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 7.4 MB (7390952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea51146f220497d66074837aed4d4957b378c092326bae49eb2d25956a7124ed`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 355.6 KB (355621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8ebfd7a69c538a6ea4a568bbcbd2d09dbe7dc0cb1c8ad80b5013567bf9c77`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 76.3 KB (76309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f6d65faf14a43908fc64a3f7c5b8a0093df475ab99ccd1d0fbb4cb1856eabf`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8bc5ef397d902964b72e93ad3785ed5674999751e96c4039ef937aecb8127d`  
		Last Modified: Thu, 22 May 2025 01:04:40 GMT  
		Size: 101.8 MB (101797850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa33ac6d9246fc0b0be7672444d9e70ff24dae5519016facb02368cdf4db1d1a`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62df8f16139eddb5120f8765468175dd99b130d830b7d9f1d53f4935dc7ed44`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c74ac65654aa3b3e84aaa87876e05096485f3682d04333e26366ac6161fe75`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a4f71afa5a484da6c2c13331d63e07dfe4c47964b692716adf42caeab50c9`  
		Last Modified: Thu, 22 May 2025 01:04:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:636b405f48663602370accde8d8bdac3d47d86051471d1734ec16114c16d8098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4036180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a640caec505c17fdd7c1ef70a9b01903be51d0432e21c40889962ba68ea7094a`

```dockerfile
```

-	Layers:
	-	`sha256:c8cb70efa326f50969856150cf5c10d1b1700062b0465df1ef7c61d992759afc`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 4.0 MB (4004399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa0b8b821b8a67c0bf0425f63deb4111df467de46101259a3c149b787203648`  
		Last Modified: Thu, 22 May 2025 01:04:37 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json
