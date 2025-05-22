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
