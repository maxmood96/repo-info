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
-	[`couchdb:3.5.2`](#couchdb352)
-	[`couchdb:3.5.2-nouveau`](#couchdb352-nouveau)
-	[`couchdb:3.5.2.1`](#couchdb3521)
-	[`couchdb:3.5.2.1-nouveau`](#couchdb3521-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:e2f17b38f2f83bb3d0d1d68e0902477b21c697c062e97e7aabeff5f247b4c77a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:cc3732411c64ced82a0b60aa8aa3de3d506085745bc70a74ecb3b3be6116502d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44232e2936d17afb2b1798bf2c507aec7faf0cafbd28fe901513e041cdbd91b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:45 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:02 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:42:02 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:14 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:42:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:42:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf4e623ec506cc4a3dac913d3b56b90e4fef2a77a9c36fdcf173f8d3b5278c5`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41389ef1d3c08b13549c1b4348192c604ad3a284329e5871b954354eea29701a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 7.5 MB (7492182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc441dd0740be802ff13f9f1b47daf5a3bc15af218d5781f017c26802a8a59`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 417.6 KB (417586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff6e59fcf95b99c098ff3c8880d2452b7aba9d13bf6c0f19ad0b5fe06b97e30`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 338.6 KB (338589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502ff7fc683f79f37d7c73b6e619ed701d657f0ceb516a15a687ca25a370a2d2`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729ef1d7ef490d9df9a9bef35e40236961c036f4e42e61b4bba68825d9f4200`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 110.8 MB (110804902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fcad644c61c6a3b04844a48f337699db4d160e2c4236738941c1396e297ed7`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30231fb7931d1261052bec6b2a3aea93155252de5867b2d3056530b0b784d3af`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3153c610da961afa19f846e0e599bf564690dbfb87a41ac22e613f5ec4e042b7`  
		Last Modified: Wed, 24 Jun 2026 01:42:30 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe1d9b4ca3855ee21d8ca2d057b734e762a2749caf05b395eb4314e6d18e99c`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c0a6265cdedc5f932c8432b70206466e94fa714fbd92ba1a364ba1e2d977b915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb9afdcbd7a9e6a733e0fb6934737903fae00152b13a1d44bfe1701f63b0eaf`

```dockerfile
```

-	Layers:
	-	`sha256:a2a421c48dedd1c7d59b486174d617e7b94ad5a4ad3b1dbd53f3d3643e38722e`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5350a5f3c13beedaf06d881b2ad3a3232267c800b3458b46c120994b684bd98a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:944dfe008f706100d9b057834e3b40c5458a8c6067128f0ad663d273150c3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad95c003b35e7fe7956ebdfa924318bce0a6e1b5963594b06515e77c62742870`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:51 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:33:23 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:33:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:33:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97325a7b140fe651aff8154d858a5a021c7b18c0b6aa682a107ba073a5ab4879`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f167452d2cba1aff408cd8774a342c06c7f6a04cc37baa0babef0c91a3f5625c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 7.3 MB (7261105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce20fd804da016a251954138074418b094a0dc4bcfc6ee19b8cd22088e4129`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 382.6 KB (382557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ad336cd92502642e2f46731304ff5129e7e079b418a0d2f9f8076af161f1a1`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 338.7 KB (338710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c13331aba23eb23da2064499c081c6c3a520fd7f7ffb5ddb550936bff241a9`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa8af252651ec950c2e762b7b6be36b2607e24b082a1ea8eda27e848e4bf461`  
		Last Modified: Tue, 23 Jun 2026 23:33:41 GMT  
		Size: 110.5 MB (110474604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3ca67ecc05254da1956d0294bae75089e9baeaae4b55a4040cf2104523569e`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc2ad2ae49d30c206b47a550edbfdb8f272d4655f1df57ff2a325879200801c`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba0691351b5030d43fcf1ba78d55b5379ab91823c2196eabf6e913e9730452`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ceb85a9d500a56bae2f07da226dcfe1b0205fa0376ee99bab8cc3d7dfa6da`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:415c6f64ce0b44c20e9a1df07f92ca185b56638dacb503c74820fadf51f1fab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420cd8298ed3cfb7b0358d7b5d372573c7432bb6ddc7e9e996a25dfd75e3df71`

```dockerfile
```

-	Layers:
	-	`sha256:772fe5e4c62244afd01871715e0219380812c7045c0eebdf7c9f304cd4cacc10`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870cc7123fb12633ccff3283c814b3d934e261eb18435e57a2948acf80e2829c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:8da84c776c43a47c41d97cec331c096d279774db11cf5f6d62c57aea6d22b981
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:a4f81ea823e89814fd49342b7afaa10ec5484a088bd7b04431364d3decdfec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066f2bd675e9f8eefe75ed8101f03c04593468ae1ba9fd0dab60ee09a3f28a61`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:46 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:06 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:06 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:42:11 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:42:11 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b4f3a550bbab7a60d55fe4084cdfb1461ec280fc6ebb368c7f7ff552d75b4f`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501acc060a5c6b292aae2516f814a1327c0172c7248a72eaefa6c94ca45b3ea4`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 7.5 MB (7492088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38a0a807b1c3e2ef8ac7093fe8ba8fbde384bc101830ec3a5f7bc06a80812cb`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 70.0 MB (70032502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fb09798c8df22a655cd0d6e428703b97158dadbb5522427bff65bfe767b6ae`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 426.0 KB (425954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8732e1e77f7f125f10e74108815945d28d1ef4c0214620b3871fd3440be62`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 347.4 KB (347406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115e152bad6a028a7a5ba2099e6e2a2bbaeb01176aa328e5ab39a72496ba6af8`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc568814ebcaf941d047d29b0ce94404c65a9c12eeea4474390818a991a1f329`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 42.8 MB (42815670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871728428bcca3734b8e1fe6b9df1e0be4cded4f20c40b5fb5f27216c0bf984d`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc251961f9e3fac2cd1ac06330d76fc2fe8157f19ee13bb6da811597e27843d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3389170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5d71ae57d78ac9697623eddbe290111da65587ddbc7671cb8db1dc17332e2a`

```dockerfile
```

-	Layers:
	-	`sha256:9d4ad28e48e6b7218fbcf6f5f24c87bea7f88a8f0615675a064a7fb5e1be71cf`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 3.4 MB (3364655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d2bf3efdfcf1edb20b2925aa4fd8ec8bb10f6be633c4c1bd26e32329caf959`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 24.5 KB (24515 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b58614245c5f6861f59c37c7370a9be54fc61087a96a9ffb9f2b712a273da2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410645668157d46958b1415602b102a7ab2a5128ec41b8b426df94922d5dcb93`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 23 Jun 2026 23:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:33:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:33:02 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
VOLUME [/opt/nouveau/data]
# Tue, 23 Jun 2026 23:33:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 23 Jun 2026 23:33:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5313ce6db74f98627afe0c7e4d43f8b57a0ad77d4d3184ea9e0d01253abd33c8`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40836ca234bd40b8c4295cd5a94a7f4a82f682c8f33844bae255d7a478d7dc4a`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 7.3 MB (7261179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a9848ec6c2ee307d8714baeec49e7bf5425762816245c9b0fb5f279c422a3f`  
		Last Modified: Tue, 23 Jun 2026 23:33:32 GMT  
		Size: 69.2 MB (69179730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7010cf1c1c6d1a1900757033c5552425409fc6a2ca148b95da9821808d0c7b`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 390.2 KB (390249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce482bfa8391c85475e9b9f5c31fc168fc5ed90ad518340b7f4d25f8d6fec8b2`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 347.4 KB (347418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dc170d66d6619a3baeb573638bde792eb024ff90158a35042dfe10130708ef`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcb5ef627136ba3bcfdfeb04eaf3befa8df1179de18c09851623e49eb1ee6ca`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 42.7 MB (42731780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19d0ccfba4ad18823eb374f84b7eda28d7d3febcf012f3d0a055e344190e2e`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:1a3070bb6674fbd4130b503a1ea4f1b33ef83e3c1f047f52e375976113bd771b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85de82f4abfe2b8fb1830a1dff75fcf62b7badf54c28672ddef151f1f9922ea`

```dockerfile
```

-	Layers:
	-	`sha256:7b7e3cf0d0456eb003b663814fc3d531897a1574d956b425fa5151d48d39b3aa`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 3.4 MB (3363308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b577a1dc55bd252562e26292b066fa2b53cfbb445788988c8f0fdba069317ce`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 24.7 KB (24709 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:f415b2fd260921a6f997b4e97ccafa65431e06124a375a7a51d19e2801d7abb3
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
$ docker pull couchdb@sha256:6c5046c5e71559d43247120c8d2cb88e40ffa5155820e52b58238acdf9466f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139025765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0f3695187d24d1c4884f1b570ff032ecc37a1872fe78df3289571b02934cd0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:41:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:07 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 24 Jun 2026 01:42:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:20 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:42:20 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:42:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a7e9dddcaceb4ae46ab993ad4dde748a920aee3f2c65009f2846c2856f9c6e`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d850789af8f7bf837bdc26e3183c08cf4bbb04d8aef88481a85388b1ba607`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 7.9 MB (7884360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e2dd308906c78bcbaf32250f34c3a878a859a0770a9d8aaf79c0ca9e4ed4e9`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 401.8 KB (401780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f364d64a056ed9ae609a36b63604ff2adb1cb4a52bee407ee7d4a6fab5a823`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 76.5 KB (76477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502a29388f3637bfb5a66dcd70786551e66372cc96fe5557fe6964ffc7e9cf03`  
		Last Modified: Wed, 24 Jun 2026 01:42:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3315bf91ee656ef13cb64342c6cb8a8f1e169c28d5a1dff4dbf222737d1773bb`  
		Last Modified: Wed, 24 Jun 2026 01:42:37 GMT  
		Size: 102.4 MB (102420072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae451b4e5e7897443e48a95d0f8c01e158f562928a1ecf6c6e82f757267d7e4`  
		Last Modified: Wed, 24 Jun 2026 01:42:34 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf69c505fa71b86bf6dda2dbb714ee276a7a7b8d38e8fcdd2aa8368f09357c3e`  
		Last Modified: Wed, 24 Jun 2026 01:42:34 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac33719b5de063d014d61d41eb8f7715970f3a0aa989332bafc8f4b58906fb8`  
		Last Modified: Wed, 24 Jun 2026 01:42:35 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45bbba1e489a6af08c5fa86ad2f9f14fe2e94e0d24420fafc1b202a092c2690`  
		Last Modified: Wed, 24 Jun 2026 01:42:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:11fcf65d96cbc7b98be04221d78f53163817a408f9512d9f37ad81002690f172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b661c8c6e786e985007005388f98df0b8c1a7dc6ca917c9e1ab90ac551eb9017`

```dockerfile
```

-	Layers:
	-	`sha256:24892a59691d3dca135a945bb9ef1a05981c542ab8196dbde25a0d4ced1d3ffe`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 4.1 MB (4125431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50e0984901f8f8bc511de0f1a23678d63f272e15c6af91f4bc089f263b87bc3e`  
		Last Modified: Wed, 24 Jun 2026 01:42:32 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:049514162c51d11865cdc310c1769749a2275331bd02a0a0138c40bf3464af1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138439846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69255e01667ccabe19378b986197d6dc9d240fb231608608f1b38cd0cdcc9a73`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:46 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 00:44:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:44:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:44:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:59 GMT
ENV COUCHDB_VERSION=3.4.3
# Thu, 11 Jun 2026 00:45:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:12 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jun 2026 00:45:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Thu, 11 Jun 2026 00:45:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aee71e24adb5275604b9f50abc13d3f67677bc222d3395a0c0076e081d0e5a`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9832854a56a6d76b1da37f382b69d09edad10c4539bdb32ba1f61e5259190d3`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 7.7 MB (7695522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a66c66cfafaa1a452b9c6a9c9b4e8eb3a4dfcef9fb0ecbb19fb9a4206098c23`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 370.5 KB (370546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd35905aad39aac2dcbf4da522f1846f833ee3af602e3b2bb585cbab1403494b`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 76.5 KB (76507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782207841376aee6faa094eb6d431b354b3a3b44150c609ccc2a85e606745be`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc146342ab1f431d43e62af84fbb85b14c31929d61e0e4b50f7fcc425fe53c32`  
		Last Modified: Thu, 11 Jun 2026 00:45:29 GMT  
		Size: 102.2 MB (102169527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4b23147c3ec7f86e6ba9007751db3411c36cfdf3154c36e653e01e79f98d5a`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ccb8a8e416945485ebb66919e88f61d697b750c824d9c860accadffb860e32`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efead0bbb4af60da230f69031439e25fe81305c4e370cfad8e2052964d2dd3f`  
		Last Modified: Thu, 11 Jun 2026 00:45:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e44c90c7482adff76124a2a002a12cda9e73d17e0ab2c074e140e2b8a9c783`  
		Last Modified: Thu, 11 Jun 2026 00:45:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:2f801e4f0f7ff763e2259f5faed3ef8c965467194047b3be1317646b09472510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bb7b0366e3c8eb790d70be9320cdfd0ec30f6e3bb1ce8742fd0baff8e66201`

```dockerfile
```

-	Layers:
	-	`sha256:efc6e4277213e5a7af3497f65f3f5c1ee886776e2e0b6a0bc45a6edcaf3ff605`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 4.1 MB (4125700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7040609ff024b230a9cbe93499304aca43746c882934eb0094c4517dc58b1c9`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 31.3 KB (31317 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:944ffe7706b9190f28ea763cb14210f7995f0ef9e94a39375b8e44e2c12da149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135804777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31901e766b8cfcb28ae354d0a8531dbb6cc7d6007d21e22ac5462ebdc7b17b3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:46:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 02:46:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 02:46:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 02:46:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 02:46:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:38 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 24 Jun 2026 02:46:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 02:46:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:46:56 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 02:46:56 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 02:46:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c74692a8c1f4356abe88429f627fd6b302f6f73952b95d71b04569b79dc6c6`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a44e034a2e5b15aeb96ce5473cdf2d322c1c3da7424bfa8a501a5a829b686b1`  
		Last Modified: Wed, 24 Jun 2026 02:47:17 GMT  
		Size: 7.4 MB (7400241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a512d7ee7f021226d1a5f24e929b0f155040e189302657566cca875db2956ba`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 372.2 KB (372163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed82bc36abb2bd092c5c734e96c3302b9454f639465572e632ebd3a84d0115c`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 76.6 KB (76561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd9d835f4fab2a7b392bf2531caea1b576fe8f461bce2784bcc35599124cbf2`  
		Last Modified: Wed, 24 Jun 2026 02:47:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426265479a0f717d0e9bf0518216548ebbc6e250a12f07f84b634f0eb5752aee`  
		Last Modified: Wed, 24 Jun 2026 02:47:20 GMT  
		Size: 101.1 MB (101056797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d444136e52d33b379d93d2cc02b4e14a558181d3b9bcd843f9e6fe84dfab55`  
		Last Modified: Wed, 24 Jun 2026 02:47:18 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af920742abefb95b12c6fbb530efe765248948f0e620e08fbd59690e9f25a0d2`  
		Last Modified: Wed, 24 Jun 2026 02:47:18 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d86e99b1478db4f20a19804afb135333f7ab7bc313a4cd224e8de4d39e267ed`  
		Last Modified: Wed, 24 Jun 2026 02:47:19 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663ff4ede45caf34f6004d8566ba4abfbea9253226272723ae64888bdafb7abe`  
		Last Modified: Wed, 24 Jun 2026 02:47:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:2fc360f7ad0f86472acf7286b2b4e54e45f730dfc9c9062c1094e191aad9e253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a69249aa1ff2a90be0fc30a76bfd2ed3ffcdcae0b05a91f55bc89be9adae8b`

```dockerfile
```

-	Layers:
	-	`sha256:075451d8e58ce370d95c940192f581b11e58f0ac036932a6921d2bf4ac912455`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 4.1 MB (4121627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c35576e828da9763b750c1a355f0428ae7eb253bc7c242491801f9203c0f2b4`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:3bcc8bf8609d6703cc8cd1e87085566114a71b78a2f3ebb9bcafa39c82eaab77
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
$ docker pull couchdb@sha256:cc9b3be27ab36ddb3b29e5747ef2bc2dd320b2d819e02d372232a765632771cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156561204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299345f2f4e404d10d894b00f4ec5912eb8f712eb2c92be52da8b74ac12a5be1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:42:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:42:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:42:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:29 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:29 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:33 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:42:34 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:42:34 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:42:34 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:42:34 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4e082a827213656d819e35a25d5e435bb7935cc2652958e1fc78a50f8a1208`  
		Last Modified: Wed, 24 Jun 2026 01:42:49 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7f581f923ae5bc7db932a63377062178c8cb8bf01cbddbc55c4a20f5db385e`  
		Last Modified: Wed, 24 Jun 2026 01:42:50 GMT  
		Size: 7.9 MB (7884338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1855dcbd232eb8f3abff21fa8f607de64bb3925091e8c0f2007287e14ef0aa2f`  
		Last Modified: Wed, 24 Jun 2026 01:42:52 GMT  
		Size: 77.5 MB (77477845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a66ec35499463ebbc4dd500a66e4351553ac59bec84998b1c2779fceace47f6`  
		Last Modified: Wed, 24 Jun 2026 01:42:50 GMT  
		Size: 424.1 KB (424140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b7c01d8c31ceb84a2f9759f4b15d7d8bfbacd23884bc8682a262bb5b01bc66`  
		Last Modified: Wed, 24 Jun 2026 01:42:51 GMT  
		Size: 99.6 KB (99592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bfc78b7a7af23034d4c2cff48545faf054087a21d51936822d339eded093f0`  
		Last Modified: Wed, 24 Jun 2026 01:42:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92cd722f7f3474b05eaa3170813628e30a9f7d4852d1564ea129eee87998cbf`  
		Last Modified: Wed, 24 Jun 2026 01:42:53 GMT  
		Size: 42.4 MB (42435771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38e460ad23878163f8f38587cced6d70081b37e0d6dfdc7a7f58412dc4a4ce1`  
		Last Modified: Wed, 24 Jun 2026 01:42:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b228fa9269fd3b9a929356c90a82b04572db4fc8208f084b9a9d770a28e7aab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b38f210d53a9f63d9e85cbbdf424221ce2981b982eda86677418501414a72d`

```dockerfile
```

-	Layers:
	-	`sha256:7489782a4f9c466ed9c86dbb3d0dc731b0ac9058d8b03043c2aaf6e438d11287`  
		Last Modified: Wed, 24 Jun 2026 01:42:50 GMT  
		Size: 3.7 MB (3658671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8acc8b7f976d3ec1c9d3f62e3f154792332212a46e7c7ecb76fcfafbb8392c7`  
		Last Modified: Wed, 24 Jun 2026 01:42:49 GMT  
		Size: 24.2 KB (24214 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0a5996ce00cdec6425d2b154a0b3363a9aa54d9967c62aed814ec263ea4548d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155443294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ff954b6eb81e7184f39bf7b459ec6109e450b138ef955c997c0508f0f11656`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:53 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Thu, 11 Jun 2026 00:44:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:45:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:45:12 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Thu, 11 Jun 2026 00:45:17 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Thu, 11 Jun 2026 00:45:17 GMT
VOLUME [/opt/nouveau/data]
# Thu, 11 Jun 2026 00:45:17 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Thu, 11 Jun 2026 00:45:17 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad224af02a5321b3eb29482ae705ae0f1e6544a563c86c09116caa3e8de361b5`  
		Last Modified: Thu, 11 Jun 2026 00:45:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6841905915492705f7458eb369dfce8ab834bf46a1423f78939762c62141d594`  
		Last Modified: Thu, 11 Jun 2026 00:45:33 GMT  
		Size: 7.7 MB (7695462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d263ded6b9aebd1331abaf55b3c7fe3f4f129ebcdc161ffd0566ce20b41c3b26`  
		Last Modified: Thu, 11 Jun 2026 00:45:35 GMT  
		Size: 76.8 MB (76793345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13bd7bb1465de6505ba9a4f4352aebec9172629dd2281cc3a8ee824808364665`  
		Last Modified: Thu, 11 Jun 2026 00:45:32 GMT  
		Size: 392.8 KB (392802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635bdeee11d0d90063c9252f316bc0d4b33c5b9c2c3693d696ff99341751d501`  
		Last Modified: Thu, 11 Jun 2026 00:45:34 GMT  
		Size: 99.5 KB (99545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86cafb0efd9657ed3a9a81947f88bbeb6f1d21c62a247b3407f08c1a40b4e66`  
		Last Modified: Thu, 11 Jun 2026 00:45:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0407a0241520f6ad2cc044f1f1c3336e3afcb74cd1d18eae6e93e6bc21e5ac19`  
		Last Modified: Thu, 11 Jun 2026 00:45:35 GMT  
		Size: 42.3 MB (42337953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cbf3cb3452afa3a7f5e686c07bc4eca25aeeec96425337ff7e80bffbb976e3`  
		Last Modified: Thu, 11 Jun 2026 00:45:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:ce501070e9e01b977a9af7464dbc4cfc820556d36a7ea1b745a5a504748fd4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c263201881589b1be3f9766ab240d76bf68f4f466caacb01ec9b6f31624420b`

```dockerfile
```

-	Layers:
	-	`sha256:9f0ff81bd1d2e8b87d77163b3cb04e4df47839789155190b480f8c03dffceb8a`  
		Last Modified: Thu, 11 Jun 2026 00:45:33 GMT  
		Size: 3.7 MB (3657339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95da38822ce4f7bd93a39d0a00d7e28af1c721db9a7bdcf0c3f06c46709d32e9`  
		Last Modified: Thu, 11 Jun 2026 00:45:32 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:5da3f6a6a5db3f9bd7d1cfea6f5c66773f8d777aa4b480743794afc00c2c921b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150178075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bf166913572b785e904d38e406ef9d27585473fb6a7d757a3f4b4927a47f15`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:46:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 02:46:31 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 02:46:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 02:46:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 02:46:52 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:52 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 02:47:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 02:47:00 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 02:47:00 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 02:47:00 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 02:47:00 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c4c35f9774ecad1c3bad431f618287d5d25f795c2abdf32ebcab26128efef`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059ff1c6e29c8344a8a59c5641838b7636b539ede46fa83ae2c13dfcb1e4958e`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 7.4 MB (7400193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd709311124fab46ec7c9282d0c30a5d6a479ca082c744135d182ee9d81b1748`  
		Last Modified: Wed, 24 Jun 2026 02:47:24 GMT  
		Size: 73.2 MB (73225361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87813195098071fe74d5d1ac69a2dcca169b13019de131fa6260734e740d5068`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 394.5 KB (394518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdcf0dde2ac53ff144117390f118341c362a4a599d223d8f3f361d7bf6e4969`  
		Last Modified: Wed, 24 Jun 2026 02:47:24 GMT  
		Size: 99.7 KB (99687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98f10795ec0711c6fb1c1c2d9aaf02a8135b77ce56fb1448fda05b4d13a7717`  
		Last Modified: Wed, 24 Jun 2026 02:47:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaabca7f1103b56ac333a0be1240140af54cd0ed33fc57c0ad749c6b3adc633`  
		Last Modified: Wed, 24 Jun 2026 02:47:25 GMT  
		Size: 42.2 MB (42162856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b27e6fcecf7b713c53863d2b5bd48f86d03d5b195fa8e6051741d0bce49c3d2`  
		Last Modified: Wed, 24 Jun 2026 02:47:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:6ff4682ef484e2f8e1ebb2ce54f44b3cebd2895336a188c5b714fc0d61c440cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de6284d11fb18093a35538214885a90f057e29e3ca45e48caca07259686fb31`

```dockerfile
```

-	Layers:
	-	`sha256:be79239d219b209b9d2f18f33d324866a220b298b9ccbea8d10047d5f8923441`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 3.6 MB (3649204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d63773d4b69bde66025c54ba37e5906bed3b59835ac891ec8f2c451730179eb`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:f415b2fd260921a6f997b4e97ccafa65431e06124a375a7a51d19e2801d7abb3
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
$ docker pull couchdb@sha256:6c5046c5e71559d43247120c8d2cb88e40ffa5155820e52b58238acdf9466f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139025765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0f3695187d24d1c4884f1b570ff032ecc37a1872fe78df3289571b02934cd0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:41:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:07 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 24 Jun 2026 01:42:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:20 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:42:20 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:42:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a7e9dddcaceb4ae46ab993ad4dde748a920aee3f2c65009f2846c2856f9c6e`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d850789af8f7bf837bdc26e3183c08cf4bbb04d8aef88481a85388b1ba607`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 7.9 MB (7884360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e2dd308906c78bcbaf32250f34c3a878a859a0770a9d8aaf79c0ca9e4ed4e9`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 401.8 KB (401780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f364d64a056ed9ae609a36b63604ff2adb1cb4a52bee407ee7d4a6fab5a823`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 76.5 KB (76477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502a29388f3637bfb5a66dcd70786551e66372cc96fe5557fe6964ffc7e9cf03`  
		Last Modified: Wed, 24 Jun 2026 01:42:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3315bf91ee656ef13cb64342c6cb8a8f1e169c28d5a1dff4dbf222737d1773bb`  
		Last Modified: Wed, 24 Jun 2026 01:42:37 GMT  
		Size: 102.4 MB (102420072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae451b4e5e7897443e48a95d0f8c01e158f562928a1ecf6c6e82f757267d7e4`  
		Last Modified: Wed, 24 Jun 2026 01:42:34 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf69c505fa71b86bf6dda2dbb714ee276a7a7b8d38e8fcdd2aa8368f09357c3e`  
		Last Modified: Wed, 24 Jun 2026 01:42:34 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac33719b5de063d014d61d41eb8f7715970f3a0aa989332bafc8f4b58906fb8`  
		Last Modified: Wed, 24 Jun 2026 01:42:35 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45bbba1e489a6af08c5fa86ad2f9f14fe2e94e0d24420fafc1b202a092c2690`  
		Last Modified: Wed, 24 Jun 2026 01:42:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:11fcf65d96cbc7b98be04221d78f53163817a408f9512d9f37ad81002690f172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b661c8c6e786e985007005388f98df0b8c1a7dc6ca917c9e1ab90ac551eb9017`

```dockerfile
```

-	Layers:
	-	`sha256:24892a59691d3dca135a945bb9ef1a05981c542ab8196dbde25a0d4ced1d3ffe`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 4.1 MB (4125431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50e0984901f8f8bc511de0f1a23678d63f272e15c6af91f4bc089f263b87bc3e`  
		Last Modified: Wed, 24 Jun 2026 01:42:32 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:049514162c51d11865cdc310c1769749a2275331bd02a0a0138c40bf3464af1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138439846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69255e01667ccabe19378b986197d6dc9d240fb231608608f1b38cd0cdcc9a73`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:46 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 00:44:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:44:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:44:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:59 GMT
ENV COUCHDB_VERSION=3.4.3
# Thu, 11 Jun 2026 00:45:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:12 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jun 2026 00:45:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Thu, 11 Jun 2026 00:45:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aee71e24adb5275604b9f50abc13d3f67677bc222d3395a0c0076e081d0e5a`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9832854a56a6d76b1da37f382b69d09edad10c4539bdb32ba1f61e5259190d3`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 7.7 MB (7695522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a66c66cfafaa1a452b9c6a9c9b4e8eb3a4dfcef9fb0ecbb19fb9a4206098c23`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 370.5 KB (370546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd35905aad39aac2dcbf4da522f1846f833ee3af602e3b2bb585cbab1403494b`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 76.5 KB (76507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782207841376aee6faa094eb6d431b354b3a3b44150c609ccc2a85e606745be`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc146342ab1f431d43e62af84fbb85b14c31929d61e0e4b50f7fcc425fe53c32`  
		Last Modified: Thu, 11 Jun 2026 00:45:29 GMT  
		Size: 102.2 MB (102169527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4b23147c3ec7f86e6ba9007751db3411c36cfdf3154c36e653e01e79f98d5a`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ccb8a8e416945485ebb66919e88f61d697b750c824d9c860accadffb860e32`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efead0bbb4af60da230f69031439e25fe81305c4e370cfad8e2052964d2dd3f`  
		Last Modified: Thu, 11 Jun 2026 00:45:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e44c90c7482adff76124a2a002a12cda9e73d17e0ab2c074e140e2b8a9c783`  
		Last Modified: Thu, 11 Jun 2026 00:45:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:2f801e4f0f7ff763e2259f5faed3ef8c965467194047b3be1317646b09472510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bb7b0366e3c8eb790d70be9320cdfd0ec30f6e3bb1ce8742fd0baff8e66201`

```dockerfile
```

-	Layers:
	-	`sha256:efc6e4277213e5a7af3497f65f3f5c1ee886776e2e0b6a0bc45a6edcaf3ff605`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 4.1 MB (4125700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7040609ff024b230a9cbe93499304aca43746c882934eb0094c4517dc58b1c9`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 31.3 KB (31317 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:944ffe7706b9190f28ea763cb14210f7995f0ef9e94a39375b8e44e2c12da149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135804777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31901e766b8cfcb28ae354d0a8531dbb6cc7d6007d21e22ac5462ebdc7b17b3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:46:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 02:46:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 02:46:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 02:46:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 02:46:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:38 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 24 Jun 2026 02:46:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 02:46:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:46:56 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 02:46:56 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 02:46:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c74692a8c1f4356abe88429f627fd6b302f6f73952b95d71b04569b79dc6c6`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a44e034a2e5b15aeb96ce5473cdf2d322c1c3da7424bfa8a501a5a829b686b1`  
		Last Modified: Wed, 24 Jun 2026 02:47:17 GMT  
		Size: 7.4 MB (7400241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a512d7ee7f021226d1a5f24e929b0f155040e189302657566cca875db2956ba`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 372.2 KB (372163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed82bc36abb2bd092c5c734e96c3302b9454f639465572e632ebd3a84d0115c`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 76.6 KB (76561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd9d835f4fab2a7b392bf2531caea1b576fe8f461bce2784bcc35599124cbf2`  
		Last Modified: Wed, 24 Jun 2026 02:47:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426265479a0f717d0e9bf0518216548ebbc6e250a12f07f84b634f0eb5752aee`  
		Last Modified: Wed, 24 Jun 2026 02:47:20 GMT  
		Size: 101.1 MB (101056797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d444136e52d33b379d93d2cc02b4e14a558181d3b9bcd843f9e6fe84dfab55`  
		Last Modified: Wed, 24 Jun 2026 02:47:18 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af920742abefb95b12c6fbb530efe765248948f0e620e08fbd59690e9f25a0d2`  
		Last Modified: Wed, 24 Jun 2026 02:47:18 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d86e99b1478db4f20a19804afb135333f7ab7bc313a4cd224e8de4d39e267ed`  
		Last Modified: Wed, 24 Jun 2026 02:47:19 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663ff4ede45caf34f6004d8566ba4abfbea9253226272723ae64888bdafb7abe`  
		Last Modified: Wed, 24 Jun 2026 02:47:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:2fc360f7ad0f86472acf7286b2b4e54e45f730dfc9c9062c1094e191aad9e253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a69249aa1ff2a90be0fc30a76bfd2ed3ffcdcae0b05a91f55bc89be9adae8b`

```dockerfile
```

-	Layers:
	-	`sha256:075451d8e58ce370d95c940192f581b11e58f0ac036932a6921d2bf4ac912455`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 4.1 MB (4121627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c35576e828da9763b750c1a355f0428ae7eb253bc7c242491801f9203c0f2b4`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:3bcc8bf8609d6703cc8cd1e87085566114a71b78a2f3ebb9bcafa39c82eaab77
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
$ docker pull couchdb@sha256:cc9b3be27ab36ddb3b29e5747ef2bc2dd320b2d819e02d372232a765632771cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156561204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299345f2f4e404d10d894b00f4ec5912eb8f712eb2c92be52da8b74ac12a5be1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:42:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:42:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:42:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:29 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:29 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:33 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:42:34 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:42:34 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:42:34 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:42:34 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4e082a827213656d819e35a25d5e435bb7935cc2652958e1fc78a50f8a1208`  
		Last Modified: Wed, 24 Jun 2026 01:42:49 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7f581f923ae5bc7db932a63377062178c8cb8bf01cbddbc55c4a20f5db385e`  
		Last Modified: Wed, 24 Jun 2026 01:42:50 GMT  
		Size: 7.9 MB (7884338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1855dcbd232eb8f3abff21fa8f607de64bb3925091e8c0f2007287e14ef0aa2f`  
		Last Modified: Wed, 24 Jun 2026 01:42:52 GMT  
		Size: 77.5 MB (77477845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a66ec35499463ebbc4dd500a66e4351553ac59bec84998b1c2779fceace47f6`  
		Last Modified: Wed, 24 Jun 2026 01:42:50 GMT  
		Size: 424.1 KB (424140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b7c01d8c31ceb84a2f9759f4b15d7d8bfbacd23884bc8682a262bb5b01bc66`  
		Last Modified: Wed, 24 Jun 2026 01:42:51 GMT  
		Size: 99.6 KB (99592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bfc78b7a7af23034d4c2cff48545faf054087a21d51936822d339eded093f0`  
		Last Modified: Wed, 24 Jun 2026 01:42:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92cd722f7f3474b05eaa3170813628e30a9f7d4852d1564ea129eee87998cbf`  
		Last Modified: Wed, 24 Jun 2026 01:42:53 GMT  
		Size: 42.4 MB (42435771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38e460ad23878163f8f38587cced6d70081b37e0d6dfdc7a7f58412dc4a4ce1`  
		Last Modified: Wed, 24 Jun 2026 01:42:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b228fa9269fd3b9a929356c90a82b04572db4fc8208f084b9a9d770a28e7aab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b38f210d53a9f63d9e85cbbdf424221ce2981b982eda86677418501414a72d`

```dockerfile
```

-	Layers:
	-	`sha256:7489782a4f9c466ed9c86dbb3d0dc731b0ac9058d8b03043c2aaf6e438d11287`  
		Last Modified: Wed, 24 Jun 2026 01:42:50 GMT  
		Size: 3.7 MB (3658671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8acc8b7f976d3ec1c9d3f62e3f154792332212a46e7c7ecb76fcfafbb8392c7`  
		Last Modified: Wed, 24 Jun 2026 01:42:49 GMT  
		Size: 24.2 KB (24214 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0a5996ce00cdec6425d2b154a0b3363a9aa54d9967c62aed814ec263ea4548d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155443294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ff954b6eb81e7184f39bf7b459ec6109e450b138ef955c997c0508f0f11656`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:53 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Thu, 11 Jun 2026 00:44:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:45:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:45:12 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Thu, 11 Jun 2026 00:45:17 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Thu, 11 Jun 2026 00:45:17 GMT
VOLUME [/opt/nouveau/data]
# Thu, 11 Jun 2026 00:45:17 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Thu, 11 Jun 2026 00:45:17 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad224af02a5321b3eb29482ae705ae0f1e6544a563c86c09116caa3e8de361b5`  
		Last Modified: Thu, 11 Jun 2026 00:45:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6841905915492705f7458eb369dfce8ab834bf46a1423f78939762c62141d594`  
		Last Modified: Thu, 11 Jun 2026 00:45:33 GMT  
		Size: 7.7 MB (7695462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d263ded6b9aebd1331abaf55b3c7fe3f4f129ebcdc161ffd0566ce20b41c3b26`  
		Last Modified: Thu, 11 Jun 2026 00:45:35 GMT  
		Size: 76.8 MB (76793345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13bd7bb1465de6505ba9a4f4352aebec9172629dd2281cc3a8ee824808364665`  
		Last Modified: Thu, 11 Jun 2026 00:45:32 GMT  
		Size: 392.8 KB (392802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635bdeee11d0d90063c9252f316bc0d4b33c5b9c2c3693d696ff99341751d501`  
		Last Modified: Thu, 11 Jun 2026 00:45:34 GMT  
		Size: 99.5 KB (99545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86cafb0efd9657ed3a9a81947f88bbeb6f1d21c62a247b3407f08c1a40b4e66`  
		Last Modified: Thu, 11 Jun 2026 00:45:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0407a0241520f6ad2cc044f1f1c3336e3afcb74cd1d18eae6e93e6bc21e5ac19`  
		Last Modified: Thu, 11 Jun 2026 00:45:35 GMT  
		Size: 42.3 MB (42337953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cbf3cb3452afa3a7f5e686c07bc4eca25aeeec96425337ff7e80bffbb976e3`  
		Last Modified: Thu, 11 Jun 2026 00:45:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:ce501070e9e01b977a9af7464dbc4cfc820556d36a7ea1b745a5a504748fd4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c263201881589b1be3f9766ab240d76bf68f4f466caacb01ec9b6f31624420b`

```dockerfile
```

-	Layers:
	-	`sha256:9f0ff81bd1d2e8b87d77163b3cb04e4df47839789155190b480f8c03dffceb8a`  
		Last Modified: Thu, 11 Jun 2026 00:45:33 GMT  
		Size: 3.7 MB (3657339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95da38822ce4f7bd93a39d0a00d7e28af1c721db9a7bdcf0c3f06c46709d32e9`  
		Last Modified: Thu, 11 Jun 2026 00:45:32 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:5da3f6a6a5db3f9bd7d1cfea6f5c66773f8d777aa4b480743794afc00c2c921b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150178075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bf166913572b785e904d38e406ef9d27585473fb6a7d757a3f4b4927a47f15`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:46:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 02:46:31 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 02:46:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 02:46:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 02:46:52 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:52 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 02:47:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 02:47:00 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 02:47:00 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 02:47:00 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 02:47:00 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c4c35f9774ecad1c3bad431f618287d5d25f795c2abdf32ebcab26128efef`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059ff1c6e29c8344a8a59c5641838b7636b539ede46fa83ae2c13dfcb1e4958e`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 7.4 MB (7400193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd709311124fab46ec7c9282d0c30a5d6a479ca082c744135d182ee9d81b1748`  
		Last Modified: Wed, 24 Jun 2026 02:47:24 GMT  
		Size: 73.2 MB (73225361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87813195098071fe74d5d1ac69a2dcca169b13019de131fa6260734e740d5068`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 394.5 KB (394518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdcf0dde2ac53ff144117390f118341c362a4a599d223d8f3f361d7bf6e4969`  
		Last Modified: Wed, 24 Jun 2026 02:47:24 GMT  
		Size: 99.7 KB (99687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98f10795ec0711c6fb1c1c2d9aaf02a8135b77ce56fb1448fda05b4d13a7717`  
		Last Modified: Wed, 24 Jun 2026 02:47:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaabca7f1103b56ac333a0be1240140af54cd0ed33fc57c0ad749c6b3adc633`  
		Last Modified: Wed, 24 Jun 2026 02:47:25 GMT  
		Size: 42.2 MB (42162856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b27e6fcecf7b713c53863d2b5bd48f86d03d5b195fa8e6051741d0bce49c3d2`  
		Last Modified: Wed, 24 Jun 2026 02:47:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:6ff4682ef484e2f8e1ebb2ce54f44b3cebd2895336a188c5b714fc0d61c440cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de6284d11fb18093a35538214885a90f057e29e3ca45e48caca07259686fb31`

```dockerfile
```

-	Layers:
	-	`sha256:be79239d219b209b9d2f18f33d324866a220b298b9ccbea8d10047d5f8923441`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 3.6 MB (3649204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d63773d4b69bde66025c54ba37e5906bed3b59835ac891ec8f2c451730179eb`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:e2f17b38f2f83bb3d0d1d68e0902477b21c697c062e97e7aabeff5f247b4c77a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5` - linux; amd64

```console
$ docker pull couchdb@sha256:cc3732411c64ced82a0b60aa8aa3de3d506085745bc70a74ecb3b3be6116502d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44232e2936d17afb2b1798bf2c507aec7faf0cafbd28fe901513e041cdbd91b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:45 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:02 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:42:02 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:14 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:42:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:42:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf4e623ec506cc4a3dac913d3b56b90e4fef2a77a9c36fdcf173f8d3b5278c5`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41389ef1d3c08b13549c1b4348192c604ad3a284329e5871b954354eea29701a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 7.5 MB (7492182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc441dd0740be802ff13f9f1b47daf5a3bc15af218d5781f017c26802a8a59`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 417.6 KB (417586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff6e59fcf95b99c098ff3c8880d2452b7aba9d13bf6c0f19ad0b5fe06b97e30`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 338.6 KB (338589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502ff7fc683f79f37d7c73b6e619ed701d657f0ceb516a15a687ca25a370a2d2`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729ef1d7ef490d9df9a9bef35e40236961c036f4e42e61b4bba68825d9f4200`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 110.8 MB (110804902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fcad644c61c6a3b04844a48f337699db4d160e2c4236738941c1396e297ed7`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30231fb7931d1261052bec6b2a3aea93155252de5867b2d3056530b0b784d3af`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3153c610da961afa19f846e0e599bf564690dbfb87a41ac22e613f5ec4e042b7`  
		Last Modified: Wed, 24 Jun 2026 01:42:30 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe1d9b4ca3855ee21d8ca2d057b734e762a2749caf05b395eb4314e6d18e99c`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:c0a6265cdedc5f932c8432b70206466e94fa714fbd92ba1a364ba1e2d977b915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb9afdcbd7a9e6a733e0fb6934737903fae00152b13a1d44bfe1701f63b0eaf`

```dockerfile
```

-	Layers:
	-	`sha256:a2a421c48dedd1c7d59b486174d617e7b94ad5a4ad3b1dbd53f3d3643e38722e`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5350a5f3c13beedaf06d881b2ad3a3232267c800b3458b46c120994b684bd98a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:944dfe008f706100d9b057834e3b40c5458a8c6067128f0ad663d273150c3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad95c003b35e7fe7956ebdfa924318bce0a6e1b5963594b06515e77c62742870`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:51 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:33:23 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:33:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:33:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97325a7b140fe651aff8154d858a5a021c7b18c0b6aa682a107ba073a5ab4879`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f167452d2cba1aff408cd8774a342c06c7f6a04cc37baa0babef0c91a3f5625c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 7.3 MB (7261105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce20fd804da016a251954138074418b094a0dc4bcfc6ee19b8cd22088e4129`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 382.6 KB (382557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ad336cd92502642e2f46731304ff5129e7e079b418a0d2f9f8076af161f1a1`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 338.7 KB (338710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c13331aba23eb23da2064499c081c6c3a520fd7f7ffb5ddb550936bff241a9`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa8af252651ec950c2e762b7b6be36b2607e24b082a1ea8eda27e848e4bf461`  
		Last Modified: Tue, 23 Jun 2026 23:33:41 GMT  
		Size: 110.5 MB (110474604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3ca67ecc05254da1956d0294bae75089e9baeaae4b55a4040cf2104523569e`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc2ad2ae49d30c206b47a550edbfdb8f272d4655f1df57ff2a325879200801c`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba0691351b5030d43fcf1ba78d55b5379ab91823c2196eabf6e913e9730452`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ceb85a9d500a56bae2f07da226dcfe1b0205fa0376ee99bab8cc3d7dfa6da`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:415c6f64ce0b44c20e9a1df07f92ca185b56638dacb503c74820fadf51f1fab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420cd8298ed3cfb7b0358d7b5d372573c7432bb6ddc7e9e996a25dfd75e3df71`

```dockerfile
```

-	Layers:
	-	`sha256:772fe5e4c62244afd01871715e0219380812c7045c0eebdf7c9f304cd4cacc10`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870cc7123fb12633ccff3283c814b3d934e261eb18435e57a2948acf80e2829c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:8da84c776c43a47c41d97cec331c096d279774db11cf5f6d62c57aea6d22b981
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:a4f81ea823e89814fd49342b7afaa10ec5484a088bd7b04431364d3decdfec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066f2bd675e9f8eefe75ed8101f03c04593468ae1ba9fd0dab60ee09a3f28a61`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:46 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:06 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:06 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:42:11 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:42:11 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b4f3a550bbab7a60d55fe4084cdfb1461ec280fc6ebb368c7f7ff552d75b4f`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501acc060a5c6b292aae2516f814a1327c0172c7248a72eaefa6c94ca45b3ea4`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 7.5 MB (7492088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38a0a807b1c3e2ef8ac7093fe8ba8fbde384bc101830ec3a5f7bc06a80812cb`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 70.0 MB (70032502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fb09798c8df22a655cd0d6e428703b97158dadbb5522427bff65bfe767b6ae`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 426.0 KB (425954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8732e1e77f7f125f10e74108815945d28d1ef4c0214620b3871fd3440be62`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 347.4 KB (347406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115e152bad6a028a7a5ba2099e6e2a2bbaeb01176aa328e5ab39a72496ba6af8`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc568814ebcaf941d047d29b0ce94404c65a9c12eeea4474390818a991a1f329`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 42.8 MB (42815670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871728428bcca3734b8e1fe6b9df1e0be4cded4f20c40b5fb5f27216c0bf984d`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc251961f9e3fac2cd1ac06330d76fc2fe8157f19ee13bb6da811597e27843d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3389170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5d71ae57d78ac9697623eddbe290111da65587ddbc7671cb8db1dc17332e2a`

```dockerfile
```

-	Layers:
	-	`sha256:9d4ad28e48e6b7218fbcf6f5f24c87bea7f88a8f0615675a064a7fb5e1be71cf`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 3.4 MB (3364655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d2bf3efdfcf1edb20b2925aa4fd8ec8bb10f6be633c4c1bd26e32329caf959`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 24.5 KB (24515 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b58614245c5f6861f59c37c7370a9be54fc61087a96a9ffb9f2b712a273da2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410645668157d46958b1415602b102a7ab2a5128ec41b8b426df94922d5dcb93`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 23 Jun 2026 23:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:33:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:33:02 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
VOLUME [/opt/nouveau/data]
# Tue, 23 Jun 2026 23:33:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 23 Jun 2026 23:33:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5313ce6db74f98627afe0c7e4d43f8b57a0ad77d4d3184ea9e0d01253abd33c8`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40836ca234bd40b8c4295cd5a94a7f4a82f682c8f33844bae255d7a478d7dc4a`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 7.3 MB (7261179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a9848ec6c2ee307d8714baeec49e7bf5425762816245c9b0fb5f279c422a3f`  
		Last Modified: Tue, 23 Jun 2026 23:33:32 GMT  
		Size: 69.2 MB (69179730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7010cf1c1c6d1a1900757033c5552425409fc6a2ca148b95da9821808d0c7b`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 390.2 KB (390249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce482bfa8391c85475e9b9f5c31fc168fc5ed90ad518340b7f4d25f8d6fec8b2`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 347.4 KB (347418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dc170d66d6619a3baeb573638bde792eb024ff90158a35042dfe10130708ef`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcb5ef627136ba3bcfdfeb04eaf3befa8df1179de18c09851623e49eb1ee6ca`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 42.7 MB (42731780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19d0ccfba4ad18823eb374f84b7eda28d7d3febcf012f3d0a055e344190e2e`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:1a3070bb6674fbd4130b503a1ea4f1b33ef83e3c1f047f52e375976113bd771b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85de82f4abfe2b8fb1830a1dff75fcf62b7badf54c28672ddef151f1f9922ea`

```dockerfile
```

-	Layers:
	-	`sha256:7b7e3cf0d0456eb003b663814fc3d531897a1574d956b425fa5151d48d39b3aa`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 3.4 MB (3363308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b577a1dc55bd252562e26292b066fa2b53cfbb445788988c8f0fdba069317ce`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 24.7 KB (24709 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2`

```console
$ docker pull couchdb@sha256:e2f17b38f2f83bb3d0d1d68e0902477b21c697c062e97e7aabeff5f247b4c77a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2` - linux; amd64

```console
$ docker pull couchdb@sha256:cc3732411c64ced82a0b60aa8aa3de3d506085745bc70a74ecb3b3be6116502d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44232e2936d17afb2b1798bf2c507aec7faf0cafbd28fe901513e041cdbd91b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:45 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:02 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:42:02 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:14 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:42:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:42:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf4e623ec506cc4a3dac913d3b56b90e4fef2a77a9c36fdcf173f8d3b5278c5`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41389ef1d3c08b13549c1b4348192c604ad3a284329e5871b954354eea29701a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 7.5 MB (7492182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc441dd0740be802ff13f9f1b47daf5a3bc15af218d5781f017c26802a8a59`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 417.6 KB (417586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff6e59fcf95b99c098ff3c8880d2452b7aba9d13bf6c0f19ad0b5fe06b97e30`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 338.6 KB (338589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502ff7fc683f79f37d7c73b6e619ed701d657f0ceb516a15a687ca25a370a2d2`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729ef1d7ef490d9df9a9bef35e40236961c036f4e42e61b4bba68825d9f4200`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 110.8 MB (110804902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fcad644c61c6a3b04844a48f337699db4d160e2c4236738941c1396e297ed7`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30231fb7931d1261052bec6b2a3aea93155252de5867b2d3056530b0b784d3af`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3153c610da961afa19f846e0e599bf564690dbfb87a41ac22e613f5ec4e042b7`  
		Last Modified: Wed, 24 Jun 2026 01:42:30 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe1d9b4ca3855ee21d8ca2d057b734e762a2749caf05b395eb4314e6d18e99c`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:c0a6265cdedc5f932c8432b70206466e94fa714fbd92ba1a364ba1e2d977b915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb9afdcbd7a9e6a733e0fb6934737903fae00152b13a1d44bfe1701f63b0eaf`

```dockerfile
```

-	Layers:
	-	`sha256:a2a421c48dedd1c7d59b486174d617e7b94ad5a4ad3b1dbd53f3d3643e38722e`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5350a5f3c13beedaf06d881b2ad3a3232267c800b3458b46c120994b684bd98a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:944dfe008f706100d9b057834e3b40c5458a8c6067128f0ad663d273150c3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad95c003b35e7fe7956ebdfa924318bce0a6e1b5963594b06515e77c62742870`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:51 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:33:23 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:33:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:33:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97325a7b140fe651aff8154d858a5a021c7b18c0b6aa682a107ba073a5ab4879`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f167452d2cba1aff408cd8774a342c06c7f6a04cc37baa0babef0c91a3f5625c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 7.3 MB (7261105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce20fd804da016a251954138074418b094a0dc4bcfc6ee19b8cd22088e4129`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 382.6 KB (382557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ad336cd92502642e2f46731304ff5129e7e079b418a0d2f9f8076af161f1a1`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 338.7 KB (338710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c13331aba23eb23da2064499c081c6c3a520fd7f7ffb5ddb550936bff241a9`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa8af252651ec950c2e762b7b6be36b2607e24b082a1ea8eda27e848e4bf461`  
		Last Modified: Tue, 23 Jun 2026 23:33:41 GMT  
		Size: 110.5 MB (110474604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3ca67ecc05254da1956d0294bae75089e9baeaae4b55a4040cf2104523569e`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc2ad2ae49d30c206b47a550edbfdb8f272d4655f1df57ff2a325879200801c`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba0691351b5030d43fcf1ba78d55b5379ab91823c2196eabf6e913e9730452`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ceb85a9d500a56bae2f07da226dcfe1b0205fa0376ee99bab8cc3d7dfa6da`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:415c6f64ce0b44c20e9a1df07f92ca185b56638dacb503c74820fadf51f1fab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420cd8298ed3cfb7b0358d7b5d372573c7432bb6ddc7e9e996a25dfd75e3df71`

```dockerfile
```

-	Layers:
	-	`sha256:772fe5e4c62244afd01871715e0219380812c7045c0eebdf7c9f304cd4cacc10`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870cc7123fb12633ccff3283c814b3d934e261eb18435e57a2948acf80e2829c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2-nouveau`

```console
$ docker pull couchdb@sha256:8da84c776c43a47c41d97cec331c096d279774db11cf5f6d62c57aea6d22b981
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:a4f81ea823e89814fd49342b7afaa10ec5484a088bd7b04431364d3decdfec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066f2bd675e9f8eefe75ed8101f03c04593468ae1ba9fd0dab60ee09a3f28a61`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:46 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:06 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:06 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:42:11 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:42:11 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b4f3a550bbab7a60d55fe4084cdfb1461ec280fc6ebb368c7f7ff552d75b4f`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501acc060a5c6b292aae2516f814a1327c0172c7248a72eaefa6c94ca45b3ea4`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 7.5 MB (7492088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38a0a807b1c3e2ef8ac7093fe8ba8fbde384bc101830ec3a5f7bc06a80812cb`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 70.0 MB (70032502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fb09798c8df22a655cd0d6e428703b97158dadbb5522427bff65bfe767b6ae`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 426.0 KB (425954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8732e1e77f7f125f10e74108815945d28d1ef4c0214620b3871fd3440be62`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 347.4 KB (347406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115e152bad6a028a7a5ba2099e6e2a2bbaeb01176aa328e5ab39a72496ba6af8`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc568814ebcaf941d047d29b0ce94404c65a9c12eeea4474390818a991a1f329`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 42.8 MB (42815670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871728428bcca3734b8e1fe6b9df1e0be4cded4f20c40b5fb5f27216c0bf984d`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc251961f9e3fac2cd1ac06330d76fc2fe8157f19ee13bb6da811597e27843d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3389170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5d71ae57d78ac9697623eddbe290111da65587ddbc7671cb8db1dc17332e2a`

```dockerfile
```

-	Layers:
	-	`sha256:9d4ad28e48e6b7218fbcf6f5f24c87bea7f88a8f0615675a064a7fb5e1be71cf`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 3.4 MB (3364655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d2bf3efdfcf1edb20b2925aa4fd8ec8bb10f6be633c4c1bd26e32329caf959`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 24.5 KB (24515 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b58614245c5f6861f59c37c7370a9be54fc61087a96a9ffb9f2b712a273da2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410645668157d46958b1415602b102a7ab2a5128ec41b8b426df94922d5dcb93`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 23 Jun 2026 23:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:33:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:33:02 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
VOLUME [/opt/nouveau/data]
# Tue, 23 Jun 2026 23:33:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 23 Jun 2026 23:33:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5313ce6db74f98627afe0c7e4d43f8b57a0ad77d4d3184ea9e0d01253abd33c8`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40836ca234bd40b8c4295cd5a94a7f4a82f682c8f33844bae255d7a478d7dc4a`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 7.3 MB (7261179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a9848ec6c2ee307d8714baeec49e7bf5425762816245c9b0fb5f279c422a3f`  
		Last Modified: Tue, 23 Jun 2026 23:33:32 GMT  
		Size: 69.2 MB (69179730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7010cf1c1c6d1a1900757033c5552425409fc6a2ca148b95da9821808d0c7b`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 390.2 KB (390249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce482bfa8391c85475e9b9f5c31fc168fc5ed90ad518340b7f4d25f8d6fec8b2`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 347.4 KB (347418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dc170d66d6619a3baeb573638bde792eb024ff90158a35042dfe10130708ef`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcb5ef627136ba3bcfdfeb04eaf3befa8df1179de18c09851623e49eb1ee6ca`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 42.7 MB (42731780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19d0ccfba4ad18823eb374f84b7eda28d7d3febcf012f3d0a055e344190e2e`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:1a3070bb6674fbd4130b503a1ea4f1b33ef83e3c1f047f52e375976113bd771b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85de82f4abfe2b8fb1830a1dff75fcf62b7badf54c28672ddef151f1f9922ea`

```dockerfile
```

-	Layers:
	-	`sha256:7b7e3cf0d0456eb003b663814fc3d531897a1574d956b425fa5151d48d39b3aa`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 3.4 MB (3363308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b577a1dc55bd252562e26292b066fa2b53cfbb445788988c8f0fdba069317ce`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 24.7 KB (24709 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2.1`

```console
$ docker pull couchdb@sha256:e2f17b38f2f83bb3d0d1d68e0902477b21c697c062e97e7aabeff5f247b4c77a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2.1` - linux; amd64

```console
$ docker pull couchdb@sha256:cc3732411c64ced82a0b60aa8aa3de3d506085745bc70a74ecb3b3be6116502d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44232e2936d17afb2b1798bf2c507aec7faf0cafbd28fe901513e041cdbd91b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:45 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:02 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:42:02 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:14 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:42:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:42:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf4e623ec506cc4a3dac913d3b56b90e4fef2a77a9c36fdcf173f8d3b5278c5`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41389ef1d3c08b13549c1b4348192c604ad3a284329e5871b954354eea29701a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 7.5 MB (7492182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc441dd0740be802ff13f9f1b47daf5a3bc15af218d5781f017c26802a8a59`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 417.6 KB (417586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff6e59fcf95b99c098ff3c8880d2452b7aba9d13bf6c0f19ad0b5fe06b97e30`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 338.6 KB (338589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502ff7fc683f79f37d7c73b6e619ed701d657f0ceb516a15a687ca25a370a2d2`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729ef1d7ef490d9df9a9bef35e40236961c036f4e42e61b4bba68825d9f4200`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 110.8 MB (110804902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fcad644c61c6a3b04844a48f337699db4d160e2c4236738941c1396e297ed7`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30231fb7931d1261052bec6b2a3aea93155252de5867b2d3056530b0b784d3af`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3153c610da961afa19f846e0e599bf564690dbfb87a41ac22e613f5ec4e042b7`  
		Last Modified: Wed, 24 Jun 2026 01:42:30 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe1d9b4ca3855ee21d8ca2d057b734e762a2749caf05b395eb4314e6d18e99c`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:c0a6265cdedc5f932c8432b70206466e94fa714fbd92ba1a364ba1e2d977b915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb9afdcbd7a9e6a733e0fb6934737903fae00152b13a1d44bfe1701f63b0eaf`

```dockerfile
```

-	Layers:
	-	`sha256:a2a421c48dedd1c7d59b486174d617e7b94ad5a4ad3b1dbd53f3d3643e38722e`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5350a5f3c13beedaf06d881b2ad3a3232267c800b3458b46c120994b684bd98a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:944dfe008f706100d9b057834e3b40c5458a8c6067128f0ad663d273150c3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad95c003b35e7fe7956ebdfa924318bce0a6e1b5963594b06515e77c62742870`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:51 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:33:23 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:33:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:33:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97325a7b140fe651aff8154d858a5a021c7b18c0b6aa682a107ba073a5ab4879`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f167452d2cba1aff408cd8774a342c06c7f6a04cc37baa0babef0c91a3f5625c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 7.3 MB (7261105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce20fd804da016a251954138074418b094a0dc4bcfc6ee19b8cd22088e4129`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 382.6 KB (382557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ad336cd92502642e2f46731304ff5129e7e079b418a0d2f9f8076af161f1a1`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 338.7 KB (338710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c13331aba23eb23da2064499c081c6c3a520fd7f7ffb5ddb550936bff241a9`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa8af252651ec950c2e762b7b6be36b2607e24b082a1ea8eda27e848e4bf461`  
		Last Modified: Tue, 23 Jun 2026 23:33:41 GMT  
		Size: 110.5 MB (110474604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3ca67ecc05254da1956d0294bae75089e9baeaae4b55a4040cf2104523569e`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc2ad2ae49d30c206b47a550edbfdb8f272d4655f1df57ff2a325879200801c`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba0691351b5030d43fcf1ba78d55b5379ab91823c2196eabf6e913e9730452`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ceb85a9d500a56bae2f07da226dcfe1b0205fa0376ee99bab8cc3d7dfa6da`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:415c6f64ce0b44c20e9a1df07f92ca185b56638dacb503c74820fadf51f1fab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420cd8298ed3cfb7b0358d7b5d372573c7432bb6ddc7e9e996a25dfd75e3df71`

```dockerfile
```

-	Layers:
	-	`sha256:772fe5e4c62244afd01871715e0219380812c7045c0eebdf7c9f304cd4cacc10`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870cc7123fb12633ccff3283c814b3d934e261eb18435e57a2948acf80e2829c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2.1-nouveau`

```console
$ docker pull couchdb@sha256:8da84c776c43a47c41d97cec331c096d279774db11cf5f6d62c57aea6d22b981
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2.1-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:a4f81ea823e89814fd49342b7afaa10ec5484a088bd7b04431364d3decdfec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066f2bd675e9f8eefe75ed8101f03c04593468ae1ba9fd0dab60ee09a3f28a61`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:46 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:06 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:06 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:42:11 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:42:11 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b4f3a550bbab7a60d55fe4084cdfb1461ec280fc6ebb368c7f7ff552d75b4f`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501acc060a5c6b292aae2516f814a1327c0172c7248a72eaefa6c94ca45b3ea4`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 7.5 MB (7492088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38a0a807b1c3e2ef8ac7093fe8ba8fbde384bc101830ec3a5f7bc06a80812cb`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 70.0 MB (70032502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fb09798c8df22a655cd0d6e428703b97158dadbb5522427bff65bfe767b6ae`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 426.0 KB (425954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8732e1e77f7f125f10e74108815945d28d1ef4c0214620b3871fd3440be62`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 347.4 KB (347406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115e152bad6a028a7a5ba2099e6e2a2bbaeb01176aa328e5ab39a72496ba6af8`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc568814ebcaf941d047d29b0ce94404c65a9c12eeea4474390818a991a1f329`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 42.8 MB (42815670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871728428bcca3734b8e1fe6b9df1e0be4cded4f20c40b5fb5f27216c0bf984d`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc251961f9e3fac2cd1ac06330d76fc2fe8157f19ee13bb6da811597e27843d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3389170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5d71ae57d78ac9697623eddbe290111da65587ddbc7671cb8db1dc17332e2a`

```dockerfile
```

-	Layers:
	-	`sha256:9d4ad28e48e6b7218fbcf6f5f24c87bea7f88a8f0615675a064a7fb5e1be71cf`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 3.4 MB (3364655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d2bf3efdfcf1edb20b2925aa4fd8ec8bb10f6be633c4c1bd26e32329caf959`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 24.5 KB (24515 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2.1-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b58614245c5f6861f59c37c7370a9be54fc61087a96a9ffb9f2b712a273da2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410645668157d46958b1415602b102a7ab2a5128ec41b8b426df94922d5dcb93`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 23 Jun 2026 23:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:33:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:33:02 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
VOLUME [/opt/nouveau/data]
# Tue, 23 Jun 2026 23:33:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 23 Jun 2026 23:33:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5313ce6db74f98627afe0c7e4d43f8b57a0ad77d4d3184ea9e0d01253abd33c8`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40836ca234bd40b8c4295cd5a94a7f4a82f682c8f33844bae255d7a478d7dc4a`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 7.3 MB (7261179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a9848ec6c2ee307d8714baeec49e7bf5425762816245c9b0fb5f279c422a3f`  
		Last Modified: Tue, 23 Jun 2026 23:33:32 GMT  
		Size: 69.2 MB (69179730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7010cf1c1c6d1a1900757033c5552425409fc6a2ca148b95da9821808d0c7b`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 390.2 KB (390249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce482bfa8391c85475e9b9f5c31fc168fc5ed90ad518340b7f4d25f8d6fec8b2`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 347.4 KB (347418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dc170d66d6619a3baeb573638bde792eb024ff90158a35042dfe10130708ef`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcb5ef627136ba3bcfdfeb04eaf3befa8df1179de18c09851623e49eb1ee6ca`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 42.7 MB (42731780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19d0ccfba4ad18823eb374f84b7eda28d7d3febcf012f3d0a055e344190e2e`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:1a3070bb6674fbd4130b503a1ea4f1b33ef83e3c1f047f52e375976113bd771b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85de82f4abfe2b8fb1830a1dff75fcf62b7badf54c28672ddef151f1f9922ea`

```dockerfile
```

-	Layers:
	-	`sha256:7b7e3cf0d0456eb003b663814fc3d531897a1574d956b425fa5151d48d39b3aa`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 3.4 MB (3363308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b577a1dc55bd252562e26292b066fa2b53cfbb445788988c8f0fdba069317ce`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 24.7 KB (24709 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:e2f17b38f2f83bb3d0d1d68e0902477b21c697c062e97e7aabeff5f247b4c77a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:cc3732411c64ced82a0b60aa8aa3de3d506085745bc70a74ecb3b3be6116502d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44232e2936d17afb2b1798bf2c507aec7faf0cafbd28fe901513e041cdbd91b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:45 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:02 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:42:02 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:14 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:42:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:42:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf4e623ec506cc4a3dac913d3b56b90e4fef2a77a9c36fdcf173f8d3b5278c5`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41389ef1d3c08b13549c1b4348192c604ad3a284329e5871b954354eea29701a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 7.5 MB (7492182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc441dd0740be802ff13f9f1b47daf5a3bc15af218d5781f017c26802a8a59`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 417.6 KB (417586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff6e59fcf95b99c098ff3c8880d2452b7aba9d13bf6c0f19ad0b5fe06b97e30`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 338.6 KB (338589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502ff7fc683f79f37d7c73b6e619ed701d657f0ceb516a15a687ca25a370a2d2`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729ef1d7ef490d9df9a9bef35e40236961c036f4e42e61b4bba68825d9f4200`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 110.8 MB (110804902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fcad644c61c6a3b04844a48f337699db4d160e2c4236738941c1396e297ed7`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30231fb7931d1261052bec6b2a3aea93155252de5867b2d3056530b0b784d3af`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3153c610da961afa19f846e0e599bf564690dbfb87a41ac22e613f5ec4e042b7`  
		Last Modified: Wed, 24 Jun 2026 01:42:30 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe1d9b4ca3855ee21d8ca2d057b734e762a2749caf05b395eb4314e6d18e99c`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:c0a6265cdedc5f932c8432b70206466e94fa714fbd92ba1a364ba1e2d977b915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb9afdcbd7a9e6a733e0fb6934737903fae00152b13a1d44bfe1701f63b0eaf`

```dockerfile
```

-	Layers:
	-	`sha256:a2a421c48dedd1c7d59b486174d617e7b94ad5a4ad3b1dbd53f3d3643e38722e`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5350a5f3c13beedaf06d881b2ad3a3232267c800b3458b46c120994b684bd98a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:944dfe008f706100d9b057834e3b40c5458a8c6067128f0ad663d273150c3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad95c003b35e7fe7956ebdfa924318bce0a6e1b5963594b06515e77c62742870`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:51 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:33:23 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:33:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:33:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97325a7b140fe651aff8154d858a5a021c7b18c0b6aa682a107ba073a5ab4879`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f167452d2cba1aff408cd8774a342c06c7f6a04cc37baa0babef0c91a3f5625c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 7.3 MB (7261105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce20fd804da016a251954138074418b094a0dc4bcfc6ee19b8cd22088e4129`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 382.6 KB (382557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ad336cd92502642e2f46731304ff5129e7e079b418a0d2f9f8076af161f1a1`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 338.7 KB (338710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c13331aba23eb23da2064499c081c6c3a520fd7f7ffb5ddb550936bff241a9`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa8af252651ec950c2e762b7b6be36b2607e24b082a1ea8eda27e848e4bf461`  
		Last Modified: Tue, 23 Jun 2026 23:33:41 GMT  
		Size: 110.5 MB (110474604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3ca67ecc05254da1956d0294bae75089e9baeaae4b55a4040cf2104523569e`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc2ad2ae49d30c206b47a550edbfdb8f272d4655f1df57ff2a325879200801c`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba0691351b5030d43fcf1ba78d55b5379ab91823c2196eabf6e913e9730452`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ceb85a9d500a56bae2f07da226dcfe1b0205fa0376ee99bab8cc3d7dfa6da`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:415c6f64ce0b44c20e9a1df07f92ca185b56638dacb503c74820fadf51f1fab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420cd8298ed3cfb7b0358d7b5d372573c7432bb6ddc7e9e996a25dfd75e3df71`

```dockerfile
```

-	Layers:
	-	`sha256:772fe5e4c62244afd01871715e0219380812c7045c0eebdf7c9f304cd4cacc10`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870cc7123fb12633ccff3283c814b3d934e261eb18435e57a2948acf80e2829c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json
