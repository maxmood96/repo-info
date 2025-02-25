<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3-nouveau`](#couchdb3-nouveau)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.3`](#couchdb333)
-	[`couchdb:3.4`](#couchdb34)
-	[`couchdb:3.4-nouveau`](#couchdb34-nouveau)
-	[`couchdb:3.4.2`](#couchdb342)
-	[`couchdb:3.4.2-nouveau`](#couchdb342-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:2bd5ec8b06df8a8420621ef2484108ac6529232d797437a0d46f4b85afd38784
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
$ docker pull couchdb@sha256:3d0e2be171ba9b66ab67a4907f188bb8eb83d8bb62da408cc509a61f3533f595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133231420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb4dcfdc18daadfecb197e9907e13418b9b66aa32fa737efef518db9a6c97b4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85591b9d52519ed0d072864357ab208c084989a9b71ec5ab7e4ac6bba4b3019c`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea8859ad3a7a6ad82b48a315171d96f45e40081f730ba0d89e9528b1fbe2d20`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 7.9 MB (7874885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c029b9046aaabc968fd53bcde850eb37af8224260eeab6c2b42e6e0e7e7be8`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 392.1 KB (392139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0cec16a910ed374ddc6e4f24b5bc1a81a1fabe0daf4e736a4027c5719ccac3`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 76.3 KB (76276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4847a061e7ef4ed08f872989838927ab956577e5d77505cff5210c61f7da8fa5`  
		Last Modified: Tue, 25 Feb 2025 02:13:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02523efe4f2bd0155cbd345b526911a8f4cdd9da14e8796ce038c7f901587b6`  
		Last Modified: Tue, 25 Feb 2025 02:13:38 GMT  
		Size: 96.7 MB (96663381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99d1e11ae938be5b8467f909feefadfba977832e2ed49ad54360397a57932db`  
		Last Modified: Tue, 25 Feb 2025 02:13:36 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7814e5128594e0ab39778919cc13848b884d9f61c070b6bfa4ecb0ed7979f8`  
		Last Modified: Tue, 25 Feb 2025 02:13:36 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce68bac6f4b571ddd97d5d83bd913a1ef66ff22b71783b7cb4b103419d89c46a`  
		Last Modified: Tue, 25 Feb 2025 02:13:37 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da84ea640acfe702897d9b081ecaf422133a08fb14884ed86162bd15404dc96`  
		Last Modified: Tue, 25 Feb 2025 02:13:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:3e80272c00dd206b2cea96d0a9dad78f2abbb442ddbdc22a57d1fe2e5121c4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c9f77ff71f65f98d9b9dece72b8615ec40f39bbdfeeb60fdd13200e639cb89`

```dockerfile
```

-	Layers:
	-	`sha256:e93ef5fdfe01284e0307e41d028297e66dafee115e5b64a22e52dd60b91ad558`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 3.9 MB (3896301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7577cb3aa464fc05709b6a37146f1427bb4b6cc07f70d6122c4196f04dfdc20d`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c1dad4d4a114f03206d7eb5fc813f786346a0effcfb51b214ed93253ca8c82f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132525123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b14bbacab0fcd2a682c985938363179f73f7392647e363db6e752439bb54530`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ed3ceb16c56b2588db16dee450d74aa1ef8289827ee553847b0478fdc53e63`  
		Last Modified: Tue, 04 Feb 2025 09:12:38 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3ea78740b6a3b3304eb626727a0ae344f42ca9947ff85a854bde8a5930bcc3`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 7.7 MB (7654497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d001ea6b43aeb929967462ce8b54b3f4db186bb90d348c00b96178594ab055d`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 348.9 KB (348923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76a9f0a91f7d533775b93c2500056380726ad8167d0836f55ee02d8a81ab037`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 76.3 KB (76272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b95425edf70a3faa302ed8ec9e1cfe5ab7117bea1e1a3626b9b93483b55e028`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebdfb636b7919dd927935a09015b93e30d256183e8a5dfa65c7b82d85aed010`  
		Last Modified: Tue, 04 Feb 2025 09:12:43 GMT  
		Size: 96.4 MB (96399124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d82a7e857cb78d0315c4e70a9e82c6e3b13a461d6108dd3d66ff880bf6725a`  
		Last Modified: Tue, 04 Feb 2025 09:12:40 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c4a8b83835238ab8d7370d152167316b9fef300077911ecb41a5f3f4995bb2`  
		Last Modified: Tue, 04 Feb 2025 09:12:40 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7189225d83a03d9c53c644f36dec592e383ba34133ef6453861ada635cf95bd1`  
		Last Modified: Tue, 04 Feb 2025 09:12:40 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccceb8c30650fde66f5614e35cc70b42add1e8217bf12fdb7bfeefa5d78a581c`  
		Last Modified: Tue, 04 Feb 2025 09:12:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c14cc657c8e65d0b20ea8955bcee471b922835a3f356ef7b61935b8827bcfa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e24b077874b1f8e90bfd4c86a355af3448ed3d17c8359c3498f3c8b218554e1`

```dockerfile
```

-	Layers:
	-	`sha256:856756d494cdbd53a304eb2b595bf3fa41e2b8395308b002038f46b0672a11b8`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 3.9 MB (3933852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:684e6ff21b2ce119827823c16ca83655357632cdd89f785ecad73c183db06ad0`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:bbb98875c2e60d55251caf3ec546a6f399d0344b517aff3d9419956ecc5ca8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129973243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af20b8448a5fc255e2ca6ec2e4b21aa035fe206f22cc74cd6b4e5667d18eaf94`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669ae66225b713189254b710db60d969b0da76c3a6fbfb597d3800dd2869e819`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43419d0575fa54de01c352b29709b0d5ccf15c49d3d1bcc25378930552dfbb`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 7.4 MB (7387928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705dcc6c28fd9ac1b53e0c99842c5e89260eaab760fc90e0989d4a5882121d7e`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 355.6 KB (355637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6008ecd238bf91fc60b5f372ddfdaf51cdc8a9afc258c4548be4d79f12ca23f9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 76.3 KB (76344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfff5ef737373de6ea03d251c1b50454071af66acdb81e7b7c7e04dfdf59fc9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970c2190b221a43960164c74df60732029a7aa45d4eccacc86cf8ed02e90a486`  
		Last Modified: Tue, 04 Feb 2025 07:35:44 GMT  
		Size: 95.3 MB (95289278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbca118bd3ee0264e7ab445907d9c994fcbe1ed9648b8eda4ffe96039cb9a0e`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6160c94cff5d390694fc67808062b79858db1a3398572487e90b4dc650545e6`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e20f342f24eeb86e2afa69eadfe2557a8a501105122c12940a5cc51347802ab`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaf3ddd7aa622b677ecfa8bac5af11f43f3f7d9217667acddd3d79c7c6ea220`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:fdc5ff418ce8940a48676ecb4f18464d922e1b3d7497b403ed26212bee936858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e961e74e238ac3326e88c598f3bd0ca37edca382b81867b8408e055b2a6ec8f`

```dockerfile
```

-	Layers:
	-	`sha256:eb4ee4c1d3c17de162d0cbf896506cb6a51b80c7095de98122fc04b08426ba87`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 3.9 MB (3932647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08d8adad896f090fbd3dc0dfc0edeebf4ed61abaacf54431482a74e0343885f`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:8c9ef39b851d0e2184613e26c67333b5258799eb6efafe2a1f75d8029deab706
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
$ docker pull couchdb@sha256:bf9d15a52b4a4159de6f776059a1fc43fe6f0db3fdfdbdfd21f288ec2be77b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155539446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c77c33bbbb0871a28c6df842259e0a2350a2c45d8b4ca305783b06ca1fce57e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bf3493e51923e21aca2e6b0ed8bdd6c7397432e6a9216e30f2b60a2a7a74b1`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c154d442b26e68a8569c856e9c65fc07ad78e6e22587a621336df375c0c37a`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 7.9 MB (7874871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45c389dd0343a2e240f3dc400e9a571a5dd89785d86095d6d9c017b92dcf94f`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 77.3 MB (77297471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618a4159279c674042f1505eb309bb61ad6e735ddf7fea3786d1ab4ef547b1fb`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 415.0 KB (414956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50377d11c2cfc8d00bfb06284f9d90303501c7e8591acc20594dd3e7a1cd5d0`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 99.3 KB (99279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5306fe2cf1e4820646b4c399391cc240a8572242d28718420e89286b264528b3`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f219b56b995df8101c472c812043e14b1e66a089de47c712964fc9520948cba`  
		Last Modified: Tue, 25 Feb 2025 02:26:35 GMT  
		Size: 41.6 MB (41631688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2f811beb79d2150fe05b012e87da5ee1ef9e84e8daa89b1cf1f268cc4de1d3`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d47b2188df79dcf9dca0d53660a2bdd44f613a9b2bb59b20d387f08a669292e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc925911c466003c1dcb05333360af3fe74198da7ac0e26c85aedbe617d9d1c5`

```dockerfile
```

-	Layers:
	-	`sha256:acb1dc572371d0464b91b652afac79b1800022d27bf82bc6ae8b3ec439d41868`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 3.5 MB (3462070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:635c35ed0a747f6dd5e0cc352dda4f32f8ba8df49ca711a277477ae6e7d45ed9`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:12190121e4afe37f7f4713d179302f43d07c45ba7458eb18994e684f1fa8f6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154320094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0afe6ac983956c792c4a72b95ec23405090ec067d9a1a2d62c60be2f4ededf`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8c4f2c46624f06564e77aac2a810773d1c6d589878c7e5c90453b64f7c3018`  
		Last Modified: Tue, 04 Feb 2025 09:13:34 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43f7d1aebdb65950c261b7b4e5edac88a6d4100d99de298df46d5d39cb4df7c`  
		Last Modified: Tue, 04 Feb 2025 09:13:35 GMT  
		Size: 7.7 MB (7654487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f99af1c739cc1c34fb1fc80f3b014f096c230bd797afe8a0d91c1415ecc178`  
		Last Modified: Tue, 04 Feb 2025 09:13:36 GMT  
		Size: 76.6 MB (76624201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db711157f27ad25a771ab518926d43a113ae58f26a3d472150fd5e9dbf3bc820`  
		Last Modified: Tue, 04 Feb 2025 09:13:34 GMT  
		Size: 371.7 KB (371707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb52220e78c407ec854f7d3057ca6392c5082e6728b5db1827d9a4c335ab192c`  
		Last Modified: Tue, 04 Feb 2025 09:13:35 GMT  
		Size: 99.2 KB (99230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abdc7e54221c13fda65ac4e3aadc8fa27908145c7a377227a17ec61303cdafa`  
		Last Modified: Tue, 04 Feb 2025 09:13:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435fcd2d3b443598407d59b50a5b5e077382cac33315ca321d0d6c2a3beb392a`  
		Last Modified: Tue, 04 Feb 2025 09:13:37 GMT  
		Size: 41.5 MB (41527712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeed426238edc4331b5af9f26701522b45e5c9443681ee17e6af5558e591b48`  
		Last Modified: Tue, 04 Feb 2025 09:13:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:813dc647967c6a9a8e23dc218e9f0e510531ecf418b7bf43e3d40acbf98eb9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b24f4a19ebe838401dee10e251d66883e2e2f0c1a07534783400093761f487`

```dockerfile
```

-	Layers:
	-	`sha256:4cc776e6b8d353323db2e118c9fb5852e20f9f51b9c4df75a54fc4542554248a`  
		Last Modified: Tue, 04 Feb 2025 09:13:35 GMT  
		Size: 3.5 MB (3460728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69393721467e2e4b92ea902efbf775ab22451e94ac4db41ae21e93866936cffa`  
		Last Modified: Tue, 04 Feb 2025 09:13:34 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:c7ef31bf2d0cf9cadfe093f47d3336284a052b7c09043f3baa84a0e3fa393386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149142669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4aeeab96a922d7a1ab78f8460fac69a2a816ca3b6e125fed1cb4a6eed7411b5`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a23a693d0435d9096a59c377a713b723450b592d3b5f06316fef9eeb38f17`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc051593c4a07ef7ad5fd762b44283836710587d01abf2ebeb0a56303ab6172`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 7.4 MB (7387901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f817f6fdb7f13d39c4df0f552ef9ca2bfa6e668a454e1da6ca2517a8efc439d9`  
		Last Modified: Tue, 04 Feb 2025 07:37:09 GMT  
		Size: 73.1 MB (73065167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0494d93c365c028f5059417ba8bf7f9b24d431a31b87fa6377d4e1d180e457af`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 378.0 KB (378017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7ebdc392d75cc71bd7cc7de5e4d9eea830b1b497cc592e1fec293906ad84a9`  
		Last Modified: Tue, 04 Feb 2025 07:37:07 GMT  
		Size: 99.4 KB (99372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4bcabe0e2faf2b52aaaa7bd8b12785b477e128f41870e5861a2fb57f266265`  
		Last Modified: Tue, 04 Feb 2025 07:37:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5594b52dc2ed41f07ca8731f1d3a1508f5f12286f3634272fb8051567df6b2`  
		Last Modified: Tue, 04 Feb 2025 07:37:08 GMT  
		Size: 41.4 MB (41351710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c8d679dc3d3d2968163532ab43de3cb43616f56858284de5bf2568d257228`  
		Last Modified: Tue, 04 Feb 2025 07:37:08 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:147ab9a2677c357e1185b231e231327efff5ee9bd4cb79ccd3cd7fee80e76849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e49dab81e90811dc3c065f49d460570083ed955142335d69205c40bcdf8370`

```dockerfile
```

-	Layers:
	-	`sha256:37f16ce50caae56e4424d9c7450676605d4306866eae78748dc06d4a5f21d5ac`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 3.5 MB (3455473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ef3b0df1d1e6be3ac92374cbf00a63eb24792839bf9e5fbd9a50931ab50a58`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:b20a471c2b009968f35e52e519887bac02a8955deecbfcbbda02e75477ef8c70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:b4614424e5a1e9e56988c197c001c0e34bbaab251e9775609553757071cc7188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96718829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65340ff2a4196e31ff9a03f9217cf7071736a3506ecf263bef935700a9721c49`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78029f177b31a8c6e4a70c55f68d59e00a0515fe3fe2c5c790e7a35e26223021`  
		Last Modified: Tue, 25 Feb 2025 02:13:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9d3bb414f1b2cff9dfab74a8fb20fc7109ff573587fe5c6cc36aa4af10beb8`  
		Last Modified: Tue, 25 Feb 2025 02:13:41 GMT  
		Size: 7.9 MB (7874896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac088bcdff62c62bea2f74a872809c7adb53eaa03ba0122c448b12c13c97a11`  
		Last Modified: Tue, 25 Feb 2025 02:13:41 GMT  
		Size: 392.1 KB (392131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7bebf1ca51f814094635df2868706dea131d30161c4c0d22cde152f2d740fa`  
		Last Modified: Tue, 25 Feb 2025 02:13:41 GMT  
		Size: 76.3 KB (76260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e8a9c7e5333d570e1185451ae024fad009debbefc08c37adb9552358f88437`  
		Last Modified: Tue, 25 Feb 2025 02:13:42 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d775e853e1623b95c79490132ee18908d3ee557078c8e3c94ebb5456a95718`  
		Last Modified: Tue, 25 Feb 2025 02:13:43 GMT  
		Size: 60.2 MB (60150811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786713f10583af94d2778180cb687315da648df474c1f3a16be5556e560c33f`  
		Last Modified: Tue, 25 Feb 2025 02:13:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b467576c0c17743fb5aeebdcdfc1831a260c1e3f2c52973805c6de91e20d709`  
		Last Modified: Tue, 25 Feb 2025 02:13:42 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7767cc3aa85ae215c8ba81ed8f7f66d88268615bcc53a6ff44ea730c153a28d8`  
		Last Modified: Tue, 25 Feb 2025 02:13:43 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7d491c6587767545794e56eeb4e943fc8b9513dc7dce017466b27053895fd0`  
		Last Modified: Tue, 25 Feb 2025 02:13:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d2c735f61c2a268d2388f490066d9d0396c30ff4d79acf181877e7a129eb037c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9380b9638e1ab6ec72fc6d1b667c7de38884108260e58bb324f5784db4cb7004`

```dockerfile
```

-	Layers:
	-	`sha256:ee73202b5f0196db9271683d87d0af611d3f4807cdb0d1c8091d9277ca1d401c`  
		Last Modified: Tue, 25 Feb 2025 02:13:41 GMT  
		Size: 3.7 MB (3698390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d3b594cd3d5141b8fa86378952d7e0fa1a18e1445bed3738ed9ce102b6076ad`  
		Last Modified: Tue, 25 Feb 2025 02:13:41 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:39968900cca3723be4d634b8f97ec58a308e49a3b629dcd94d636fd06e1d5d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96060064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbf9fb31ea50e7078e77a1b5ffac63e15a675cd0046c3168fa74c87f5dad47d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ed3ceb16c56b2588db16dee450d74aa1ef8289827ee553847b0478fdc53e63`  
		Last Modified: Tue, 04 Feb 2025 09:12:38 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3ea78740b6a3b3304eb626727a0ae344f42ca9947ff85a854bde8a5930bcc3`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 7.7 MB (7654497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d001ea6b43aeb929967462ce8b54b3f4db186bb90d348c00b96178594ab055d`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 348.9 KB (348923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76a9f0a91f7d533775b93c2500056380726ad8167d0836f55ee02d8a81ab037`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 76.3 KB (76272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e0f675876d677c8e36c67c7199db7e06481ecf8051655b2e6fac9cd340c15f`  
		Last Modified: Tue, 04 Feb 2025 09:14:08 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a13699a07a153ede32521adda003aacb2d682959617585739481cf2c351224`  
		Last Modified: Tue, 04 Feb 2025 09:14:10 GMT  
		Size: 59.9 MB (59934060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8086d7dcef6b90bd9c3d4c3f42d72748b282f5ba7f8daa5e5250d1ba534f653d`  
		Last Modified: Tue, 04 Feb 2025 09:14:08 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9e2361972e658a36c2a70e7781b9b05f5b273b797f6d5449cefeff78f1f4e2`  
		Last Modified: Tue, 04 Feb 2025 09:14:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc31c1b3fc50311637111254189a7feb132b4d85ed7b10b87e82e80d6446f6f8`  
		Last Modified: Tue, 04 Feb 2025 09:14:09 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36c822f21fbe4f7dc9fd3e0c7aadef6a35188847d4af3876ebd4a24db910c94`  
		Last Modified: Tue, 04 Feb 2025 09:14:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:6d36a2717ade7dff8252998092c0a7660da9cf888365df2b33c76a64145468c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e755c91993467cfc053362b042e65e2674a4e97739c507b7674c3508076674c`

```dockerfile
```

-	Layers:
	-	`sha256:4fb249ff34491a380f3ab546c5557cb170e8622ccebeff90a112b979ade31a47`  
		Last Modified: Tue, 04 Feb 2025 09:14:08 GMT  
		Size: 3.7 MB (3735107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee8f4cfd5e301c3cabee7089e96640ec88d73a54f16ed2dea0ebe4b887e9576`  
		Last Modified: Tue, 04 Feb 2025 09:14:08 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:01c8dfd74f8de7886bffe9d1a881023e8914c4032a7bce5ee76fcc173a4b7378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102845172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830dc6d3501997bddc06c97e00c5f82580a8e390fb6d2112d8574a43a1c23781`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c1c0d1c53faa85a05bda883073e3c29055edf2a25e6e2d4663f88b73aebe99`  
		Last Modified: Tue, 25 Feb 2025 04:36:05 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2a9855f152cda9c228c545076b24fba8bd3ada1953ec5ec0d91fdd6f1827e0`  
		Last Modified: Tue, 25 Feb 2025 04:36:06 GMT  
		Size: 8.9 MB (8890122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51b42499084bf015bb8da262d1c027292a3d4a3bfa675b705219e46e9ffedc6`  
		Last Modified: Tue, 25 Feb 2025 04:36:06 GMT  
		Size: 444.7 KB (444685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f6442915b09f3f08a99b9d16164eb19c633e416a8363c861ae6edf45db917a`  
		Last Modified: Tue, 25 Feb 2025 04:36:06 GMT  
		Size: 76.3 KB (76350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dfaff5e87740637752c328d73f737b6e591edda3f4f9d57b35bd56fa7d8d60`  
		Last Modified: Tue, 25 Feb 2025 04:36:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975cc3034c5955ca44c3581a1ac840744b46945a68d44836dbc94f6b0e678182`  
		Last Modified: Tue, 25 Feb 2025 04:36:09 GMT  
		Size: 61.4 MB (61376267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5984ae6dc20cc1cf1964c4e30c16b61a2b2f05607861d373014f6bd12c39ef76`  
		Last Modified: Tue, 25 Feb 2025 04:36:07 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfb150fffec35d3e24d7c18de9d0499319f3a9e60de6330dafcac2a8053e83`  
		Last Modified: Tue, 25 Feb 2025 04:36:07 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442cd60f15cb453c25a19c75a77d231eae6da5a7ea92955709c7e6920ff2f64c`  
		Last Modified: Tue, 25 Feb 2025 04:36:07 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5f4d48f2328d549e05acd355f4d1dee4d1e13f36f163497275ad2236546057`  
		Last Modified: Tue, 25 Feb 2025 04:36:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a24945e565b8ffe63d20c55fc3cfeeb21b5175dee54d931d31b933b2cc786ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3770596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7645a7fbc176a1e6391b85d118601b2e2b4b7b90639f9582d37d54618730f2`

```dockerfile
```

-	Layers:
	-	`sha256:e4455845e29f93fc5762d6fca0020a5db2d460d0f18ea0c06fa5bc34e20444a5`  
		Last Modified: Tue, 25 Feb 2025 04:36:06 GMT  
		Size: 3.7 MB (3739360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c907b913f39a45d0de3dc5131b3ac7539e02db1e3fa7168ff6e80242bb7c05`  
		Last Modified: Tue, 25 Feb 2025 04:36:05 GMT  
		Size: 31.2 KB (31236 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:f806d0e8d48d723abd226bfe56f1ee66f0c105b023165fed8b0603088d35879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93424352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3120857c7cd5358be78df5d0a64f0ebdf454ae26e0ca620f6fba80bfd8cdb1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669ae66225b713189254b710db60d969b0da76c3a6fbfb597d3800dd2869e819`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43419d0575fa54de01c352b29709b0d5ccf15c49d3d1bcc25378930552dfbb`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 7.4 MB (7387928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705dcc6c28fd9ac1b53e0c99842c5e89260eaab760fc90e0989d4a5882121d7e`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 355.6 KB (355637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6008ecd238bf91fc60b5f372ddfdaf51cdc8a9afc258c4548be4d79f12ca23f9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 76.3 KB (76344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d368db74aca8069e746f41ea3262a15295a440bc0581103284d5f6a945bf8a3`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd1272845325e4cc432438bb9d5a803eb4077929c98b0caa67cddd2d5bc5204`  
		Last Modified: Tue, 04 Feb 2025 07:38:33 GMT  
		Size: 58.7 MB (58740382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5f89192dfb5c79e22c6858e946d89981fa419030667e29a8a2ade095453bc8`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ded5cd457c8f978623355726031c8b4bda96e9adc258fd3565df2bf02f7b6a1`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43362fd9147e5da284972e9d11a1386096074aec9e0e42612c3aa9edab0a0890`  
		Last Modified: Tue, 04 Feb 2025 07:38:32 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f555ef45dcf68ec7fdd9280dd9ac90cbaed985d644417539d7802a26f69b4ce7`  
		Last Modified: Tue, 04 Feb 2025 07:38:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:5d1912c62dc995a38321d928950f0e50585737b8de9f3e07185da9dff0bbb3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3765118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbba2b8fefee56480374411558cd98ed349cb446953d41abb2695bfe5dc7178`

```dockerfile
```

-	Layers:
	-	`sha256:46498bf7cc20271924d83a4520a85aa1ea05177e5ae9561e1b98874f42d65bcb`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 3.7 MB (3733926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f505cf7b3bcaeebd2cad48b853850d61e42f252a718718fa7cbb02ad4cf89a`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:b20a471c2b009968f35e52e519887bac02a8955deecbfcbbda02e75477ef8c70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:b4614424e5a1e9e56988c197c001c0e34bbaab251e9775609553757071cc7188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96718829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65340ff2a4196e31ff9a03f9217cf7071736a3506ecf263bef935700a9721c49`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78029f177b31a8c6e4a70c55f68d59e00a0515fe3fe2c5c790e7a35e26223021`  
		Last Modified: Tue, 25 Feb 2025 02:13:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9d3bb414f1b2cff9dfab74a8fb20fc7109ff573587fe5c6cc36aa4af10beb8`  
		Last Modified: Tue, 25 Feb 2025 02:13:41 GMT  
		Size: 7.9 MB (7874896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac088bcdff62c62bea2f74a872809c7adb53eaa03ba0122c448b12c13c97a11`  
		Last Modified: Tue, 25 Feb 2025 02:13:41 GMT  
		Size: 392.1 KB (392131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7bebf1ca51f814094635df2868706dea131d30161c4c0d22cde152f2d740fa`  
		Last Modified: Tue, 25 Feb 2025 02:13:41 GMT  
		Size: 76.3 KB (76260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e8a9c7e5333d570e1185451ae024fad009debbefc08c37adb9552358f88437`  
		Last Modified: Tue, 25 Feb 2025 02:13:42 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d775e853e1623b95c79490132ee18908d3ee557078c8e3c94ebb5456a95718`  
		Last Modified: Tue, 25 Feb 2025 02:13:43 GMT  
		Size: 60.2 MB (60150811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786713f10583af94d2778180cb687315da648df474c1f3a16be5556e560c33f`  
		Last Modified: Tue, 25 Feb 2025 02:13:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b467576c0c17743fb5aeebdcdfc1831a260c1e3f2c52973805c6de91e20d709`  
		Last Modified: Tue, 25 Feb 2025 02:13:42 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7767cc3aa85ae215c8ba81ed8f7f66d88268615bcc53a6ff44ea730c153a28d8`  
		Last Modified: Tue, 25 Feb 2025 02:13:43 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7d491c6587767545794e56eeb4e943fc8b9513dc7dce017466b27053895fd0`  
		Last Modified: Tue, 25 Feb 2025 02:13:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d2c735f61c2a268d2388f490066d9d0396c30ff4d79acf181877e7a129eb037c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9380b9638e1ab6ec72fc6d1b667c7de38884108260e58bb324f5784db4cb7004`

```dockerfile
```

-	Layers:
	-	`sha256:ee73202b5f0196db9271683d87d0af611d3f4807cdb0d1c8091d9277ca1d401c`  
		Last Modified: Tue, 25 Feb 2025 02:13:41 GMT  
		Size: 3.7 MB (3698390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d3b594cd3d5141b8fa86378952d7e0fa1a18e1445bed3738ed9ce102b6076ad`  
		Last Modified: Tue, 25 Feb 2025 02:13:41 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:39968900cca3723be4d634b8f97ec58a308e49a3b629dcd94d636fd06e1d5d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96060064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbf9fb31ea50e7078e77a1b5ffac63e15a675cd0046c3168fa74c87f5dad47d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ed3ceb16c56b2588db16dee450d74aa1ef8289827ee553847b0478fdc53e63`  
		Last Modified: Tue, 04 Feb 2025 09:12:38 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3ea78740b6a3b3304eb626727a0ae344f42ca9947ff85a854bde8a5930bcc3`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 7.7 MB (7654497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d001ea6b43aeb929967462ce8b54b3f4db186bb90d348c00b96178594ab055d`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 348.9 KB (348923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76a9f0a91f7d533775b93c2500056380726ad8167d0836f55ee02d8a81ab037`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 76.3 KB (76272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e0f675876d677c8e36c67c7199db7e06481ecf8051655b2e6fac9cd340c15f`  
		Last Modified: Tue, 04 Feb 2025 09:14:08 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a13699a07a153ede32521adda003aacb2d682959617585739481cf2c351224`  
		Last Modified: Tue, 04 Feb 2025 09:14:10 GMT  
		Size: 59.9 MB (59934060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8086d7dcef6b90bd9c3d4c3f42d72748b282f5ba7f8daa5e5250d1ba534f653d`  
		Last Modified: Tue, 04 Feb 2025 09:14:08 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9e2361972e658a36c2a70e7781b9b05f5b273b797f6d5449cefeff78f1f4e2`  
		Last Modified: Tue, 04 Feb 2025 09:14:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc31c1b3fc50311637111254189a7feb132b4d85ed7b10b87e82e80d6446f6f8`  
		Last Modified: Tue, 04 Feb 2025 09:14:09 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36c822f21fbe4f7dc9fd3e0c7aadef6a35188847d4af3876ebd4a24db910c94`  
		Last Modified: Tue, 04 Feb 2025 09:14:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:6d36a2717ade7dff8252998092c0a7660da9cf888365df2b33c76a64145468c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e755c91993467cfc053362b042e65e2674a4e97739c507b7674c3508076674c`

```dockerfile
```

-	Layers:
	-	`sha256:4fb249ff34491a380f3ab546c5557cb170e8622ccebeff90a112b979ade31a47`  
		Last Modified: Tue, 04 Feb 2025 09:14:08 GMT  
		Size: 3.7 MB (3735107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee8f4cfd5e301c3cabee7089e96640ec88d73a54f16ed2dea0ebe4b887e9576`  
		Last Modified: Tue, 04 Feb 2025 09:14:08 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:01c8dfd74f8de7886bffe9d1a881023e8914c4032a7bce5ee76fcc173a4b7378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102845172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830dc6d3501997bddc06c97e00c5f82580a8e390fb6d2112d8574a43a1c23781`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c1c0d1c53faa85a05bda883073e3c29055edf2a25e6e2d4663f88b73aebe99`  
		Last Modified: Tue, 25 Feb 2025 04:36:05 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2a9855f152cda9c228c545076b24fba8bd3ada1953ec5ec0d91fdd6f1827e0`  
		Last Modified: Tue, 25 Feb 2025 04:36:06 GMT  
		Size: 8.9 MB (8890122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51b42499084bf015bb8da262d1c027292a3d4a3bfa675b705219e46e9ffedc6`  
		Last Modified: Tue, 25 Feb 2025 04:36:06 GMT  
		Size: 444.7 KB (444685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f6442915b09f3f08a99b9d16164eb19c633e416a8363c861ae6edf45db917a`  
		Last Modified: Tue, 25 Feb 2025 04:36:06 GMT  
		Size: 76.3 KB (76350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dfaff5e87740637752c328d73f737b6e591edda3f4f9d57b35bd56fa7d8d60`  
		Last Modified: Tue, 25 Feb 2025 04:36:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975cc3034c5955ca44c3581a1ac840744b46945a68d44836dbc94f6b0e678182`  
		Last Modified: Tue, 25 Feb 2025 04:36:09 GMT  
		Size: 61.4 MB (61376267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5984ae6dc20cc1cf1964c4e30c16b61a2b2f05607861d373014f6bd12c39ef76`  
		Last Modified: Tue, 25 Feb 2025 04:36:07 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfb150fffec35d3e24d7c18de9d0499319f3a9e60de6330dafcac2a8053e83`  
		Last Modified: Tue, 25 Feb 2025 04:36:07 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442cd60f15cb453c25a19c75a77d231eae6da5a7ea92955709c7e6920ff2f64c`  
		Last Modified: Tue, 25 Feb 2025 04:36:07 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5f4d48f2328d549e05acd355f4d1dee4d1e13f36f163497275ad2236546057`  
		Last Modified: Tue, 25 Feb 2025 04:36:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a24945e565b8ffe63d20c55fc3cfeeb21b5175dee54d931d31b933b2cc786ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3770596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7645a7fbc176a1e6391b85d118601b2e2b4b7b90639f9582d37d54618730f2`

```dockerfile
```

-	Layers:
	-	`sha256:e4455845e29f93fc5762d6fca0020a5db2d460d0f18ea0c06fa5bc34e20444a5`  
		Last Modified: Tue, 25 Feb 2025 04:36:06 GMT  
		Size: 3.7 MB (3739360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c907b913f39a45d0de3dc5131b3ac7539e02db1e3fa7168ff6e80242bb7c05`  
		Last Modified: Tue, 25 Feb 2025 04:36:05 GMT  
		Size: 31.2 KB (31236 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:f806d0e8d48d723abd226bfe56f1ee66f0c105b023165fed8b0603088d35879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93424352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3120857c7cd5358be78df5d0a64f0ebdf454ae26e0ca620f6fba80bfd8cdb1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669ae66225b713189254b710db60d969b0da76c3a6fbfb597d3800dd2869e819`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43419d0575fa54de01c352b29709b0d5ccf15c49d3d1bcc25378930552dfbb`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 7.4 MB (7387928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705dcc6c28fd9ac1b53e0c99842c5e89260eaab760fc90e0989d4a5882121d7e`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 355.6 KB (355637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6008ecd238bf91fc60b5f372ddfdaf51cdc8a9afc258c4548be4d79f12ca23f9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 76.3 KB (76344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d368db74aca8069e746f41ea3262a15295a440bc0581103284d5f6a945bf8a3`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd1272845325e4cc432438bb9d5a803eb4077929c98b0caa67cddd2d5bc5204`  
		Last Modified: Tue, 04 Feb 2025 07:38:33 GMT  
		Size: 58.7 MB (58740382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5f89192dfb5c79e22c6858e946d89981fa419030667e29a8a2ade095453bc8`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ded5cd457c8f978623355726031c8b4bda96e9adc258fd3565df2bf02f7b6a1`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43362fd9147e5da284972e9d11a1386096074aec9e0e42612c3aa9edab0a0890`  
		Last Modified: Tue, 04 Feb 2025 07:38:32 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f555ef45dcf68ec7fdd9280dd9ac90cbaed985d644417539d7802a26f69b4ce7`  
		Last Modified: Tue, 04 Feb 2025 07:38:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:5d1912c62dc995a38321d928950f0e50585737b8de9f3e07185da9dff0bbb3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3765118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbba2b8fefee56480374411558cd98ed349cb446953d41abb2695bfe5dc7178`

```dockerfile
```

-	Layers:
	-	`sha256:46498bf7cc20271924d83a4520a85aa1ea05177e5ae9561e1b98874f42d65bcb`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 3.7 MB (3733926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f505cf7b3bcaeebd2cad48b853850d61e42f252a718718fa7cbb02ad4cf89a`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:2bd5ec8b06df8a8420621ef2484108ac6529232d797437a0d46f4b85afd38784
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
$ docker pull couchdb@sha256:3d0e2be171ba9b66ab67a4907f188bb8eb83d8bb62da408cc509a61f3533f595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133231420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb4dcfdc18daadfecb197e9907e13418b9b66aa32fa737efef518db9a6c97b4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85591b9d52519ed0d072864357ab208c084989a9b71ec5ab7e4ac6bba4b3019c`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea8859ad3a7a6ad82b48a315171d96f45e40081f730ba0d89e9528b1fbe2d20`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 7.9 MB (7874885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c029b9046aaabc968fd53bcde850eb37af8224260eeab6c2b42e6e0e7e7be8`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 392.1 KB (392139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0cec16a910ed374ddc6e4f24b5bc1a81a1fabe0daf4e736a4027c5719ccac3`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 76.3 KB (76276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4847a061e7ef4ed08f872989838927ab956577e5d77505cff5210c61f7da8fa5`  
		Last Modified: Tue, 25 Feb 2025 02:13:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02523efe4f2bd0155cbd345b526911a8f4cdd9da14e8796ce038c7f901587b6`  
		Last Modified: Tue, 25 Feb 2025 02:13:38 GMT  
		Size: 96.7 MB (96663381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99d1e11ae938be5b8467f909feefadfba977832e2ed49ad54360397a57932db`  
		Last Modified: Tue, 25 Feb 2025 02:13:36 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7814e5128594e0ab39778919cc13848b884d9f61c070b6bfa4ecb0ed7979f8`  
		Last Modified: Tue, 25 Feb 2025 02:13:36 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce68bac6f4b571ddd97d5d83bd913a1ef66ff22b71783b7cb4b103419d89c46a`  
		Last Modified: Tue, 25 Feb 2025 02:13:37 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da84ea640acfe702897d9b081ecaf422133a08fb14884ed86162bd15404dc96`  
		Last Modified: Tue, 25 Feb 2025 02:13:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:3e80272c00dd206b2cea96d0a9dad78f2abbb442ddbdc22a57d1fe2e5121c4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c9f77ff71f65f98d9b9dece72b8615ec40f39bbdfeeb60fdd13200e639cb89`

```dockerfile
```

-	Layers:
	-	`sha256:e93ef5fdfe01284e0307e41d028297e66dafee115e5b64a22e52dd60b91ad558`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 3.9 MB (3896301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7577cb3aa464fc05709b6a37146f1427bb4b6cc07f70d6122c4196f04dfdc20d`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c1dad4d4a114f03206d7eb5fc813f786346a0effcfb51b214ed93253ca8c82f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132525123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b14bbacab0fcd2a682c985938363179f73f7392647e363db6e752439bb54530`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ed3ceb16c56b2588db16dee450d74aa1ef8289827ee553847b0478fdc53e63`  
		Last Modified: Tue, 04 Feb 2025 09:12:38 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3ea78740b6a3b3304eb626727a0ae344f42ca9947ff85a854bde8a5930bcc3`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 7.7 MB (7654497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d001ea6b43aeb929967462ce8b54b3f4db186bb90d348c00b96178594ab055d`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 348.9 KB (348923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76a9f0a91f7d533775b93c2500056380726ad8167d0836f55ee02d8a81ab037`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 76.3 KB (76272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b95425edf70a3faa302ed8ec9e1cfe5ab7117bea1e1a3626b9b93483b55e028`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebdfb636b7919dd927935a09015b93e30d256183e8a5dfa65c7b82d85aed010`  
		Last Modified: Tue, 04 Feb 2025 09:12:43 GMT  
		Size: 96.4 MB (96399124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d82a7e857cb78d0315c4e70a9e82c6e3b13a461d6108dd3d66ff880bf6725a`  
		Last Modified: Tue, 04 Feb 2025 09:12:40 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c4a8b83835238ab8d7370d152167316b9fef300077911ecb41a5f3f4995bb2`  
		Last Modified: Tue, 04 Feb 2025 09:12:40 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7189225d83a03d9c53c644f36dec592e383ba34133ef6453861ada635cf95bd1`  
		Last Modified: Tue, 04 Feb 2025 09:12:40 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccceb8c30650fde66f5614e35cc70b42add1e8217bf12fdb7bfeefa5d78a581c`  
		Last Modified: Tue, 04 Feb 2025 09:12:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:c14cc657c8e65d0b20ea8955bcee471b922835a3f356ef7b61935b8827bcfa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e24b077874b1f8e90bfd4c86a355af3448ed3d17c8359c3498f3c8b218554e1`

```dockerfile
```

-	Layers:
	-	`sha256:856756d494cdbd53a304eb2b595bf3fa41e2b8395308b002038f46b0672a11b8`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 3.9 MB (3933852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:684e6ff21b2ce119827823c16ca83655357632cdd89f785ecad73c183db06ad0`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:bbb98875c2e60d55251caf3ec546a6f399d0344b517aff3d9419956ecc5ca8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129973243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af20b8448a5fc255e2ca6ec2e4b21aa035fe206f22cc74cd6b4e5667d18eaf94`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669ae66225b713189254b710db60d969b0da76c3a6fbfb597d3800dd2869e819`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43419d0575fa54de01c352b29709b0d5ccf15c49d3d1bcc25378930552dfbb`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 7.4 MB (7387928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705dcc6c28fd9ac1b53e0c99842c5e89260eaab760fc90e0989d4a5882121d7e`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 355.6 KB (355637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6008ecd238bf91fc60b5f372ddfdaf51cdc8a9afc258c4548be4d79f12ca23f9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 76.3 KB (76344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfff5ef737373de6ea03d251c1b50454071af66acdb81e7b7c7e04dfdf59fc9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970c2190b221a43960164c74df60732029a7aa45d4eccacc86cf8ed02e90a486`  
		Last Modified: Tue, 04 Feb 2025 07:35:44 GMT  
		Size: 95.3 MB (95289278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbca118bd3ee0264e7ab445907d9c994fcbe1ed9648b8eda4ffe96039cb9a0e`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6160c94cff5d390694fc67808062b79858db1a3398572487e90b4dc650545e6`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e20f342f24eeb86e2afa69eadfe2557a8a501105122c12940a5cc51347802ab`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaf3ddd7aa622b677ecfa8bac5af11f43f3f7d9217667acddd3d79c7c6ea220`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:fdc5ff418ce8940a48676ecb4f18464d922e1b3d7497b403ed26212bee936858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e961e74e238ac3326e88c598f3bd0ca37edca382b81867b8408e055b2a6ec8f`

```dockerfile
```

-	Layers:
	-	`sha256:eb4ee4c1d3c17de162d0cbf896506cb6a51b80c7095de98122fc04b08426ba87`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 3.9 MB (3932647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08d8adad896f090fbd3dc0dfc0edeebf4ed61abaacf54431482a74e0343885f`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:8c9ef39b851d0e2184613e26c67333b5258799eb6efafe2a1f75d8029deab706
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
$ docker pull couchdb@sha256:bf9d15a52b4a4159de6f776059a1fc43fe6f0db3fdfdbdfd21f288ec2be77b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155539446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c77c33bbbb0871a28c6df842259e0a2350a2c45d8b4ca305783b06ca1fce57e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bf3493e51923e21aca2e6b0ed8bdd6c7397432e6a9216e30f2b60a2a7a74b1`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c154d442b26e68a8569c856e9c65fc07ad78e6e22587a621336df375c0c37a`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 7.9 MB (7874871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45c389dd0343a2e240f3dc400e9a571a5dd89785d86095d6d9c017b92dcf94f`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 77.3 MB (77297471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618a4159279c674042f1505eb309bb61ad6e735ddf7fea3786d1ab4ef547b1fb`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 415.0 KB (414956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50377d11c2cfc8d00bfb06284f9d90303501c7e8591acc20594dd3e7a1cd5d0`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 99.3 KB (99279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5306fe2cf1e4820646b4c399391cc240a8572242d28718420e89286b264528b3`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f219b56b995df8101c472c812043e14b1e66a089de47c712964fc9520948cba`  
		Last Modified: Tue, 25 Feb 2025 02:26:35 GMT  
		Size: 41.6 MB (41631688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2f811beb79d2150fe05b012e87da5ee1ef9e84e8daa89b1cf1f268cc4de1d3`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d47b2188df79dcf9dca0d53660a2bdd44f613a9b2bb59b20d387f08a669292e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc925911c466003c1dcb05333360af3fe74198da7ac0e26c85aedbe617d9d1c5`

```dockerfile
```

-	Layers:
	-	`sha256:acb1dc572371d0464b91b652afac79b1800022d27bf82bc6ae8b3ec439d41868`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 3.5 MB (3462070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:635c35ed0a747f6dd5e0cc352dda4f32f8ba8df49ca711a277477ae6e7d45ed9`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:12190121e4afe37f7f4713d179302f43d07c45ba7458eb18994e684f1fa8f6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154320094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0afe6ac983956c792c4a72b95ec23405090ec067d9a1a2d62c60be2f4ededf`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8c4f2c46624f06564e77aac2a810773d1c6d589878c7e5c90453b64f7c3018`  
		Last Modified: Tue, 04 Feb 2025 09:13:34 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43f7d1aebdb65950c261b7b4e5edac88a6d4100d99de298df46d5d39cb4df7c`  
		Last Modified: Tue, 04 Feb 2025 09:13:35 GMT  
		Size: 7.7 MB (7654487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f99af1c739cc1c34fb1fc80f3b014f096c230bd797afe8a0d91c1415ecc178`  
		Last Modified: Tue, 04 Feb 2025 09:13:36 GMT  
		Size: 76.6 MB (76624201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db711157f27ad25a771ab518926d43a113ae58f26a3d472150fd5e9dbf3bc820`  
		Last Modified: Tue, 04 Feb 2025 09:13:34 GMT  
		Size: 371.7 KB (371707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb52220e78c407ec854f7d3057ca6392c5082e6728b5db1827d9a4c335ab192c`  
		Last Modified: Tue, 04 Feb 2025 09:13:35 GMT  
		Size: 99.2 KB (99230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abdc7e54221c13fda65ac4e3aadc8fa27908145c7a377227a17ec61303cdafa`  
		Last Modified: Tue, 04 Feb 2025 09:13:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435fcd2d3b443598407d59b50a5b5e077382cac33315ca321d0d6c2a3beb392a`  
		Last Modified: Tue, 04 Feb 2025 09:13:37 GMT  
		Size: 41.5 MB (41527712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeed426238edc4331b5af9f26701522b45e5c9443681ee17e6af5558e591b48`  
		Last Modified: Tue, 04 Feb 2025 09:13:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:813dc647967c6a9a8e23dc218e9f0e510531ecf418b7bf43e3d40acbf98eb9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b24f4a19ebe838401dee10e251d66883e2e2f0c1a07534783400093761f487`

```dockerfile
```

-	Layers:
	-	`sha256:4cc776e6b8d353323db2e118c9fb5852e20f9f51b9c4df75a54fc4542554248a`  
		Last Modified: Tue, 04 Feb 2025 09:13:35 GMT  
		Size: 3.5 MB (3460728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69393721467e2e4b92ea902efbf775ab22451e94ac4db41ae21e93866936cffa`  
		Last Modified: Tue, 04 Feb 2025 09:13:34 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:c7ef31bf2d0cf9cadfe093f47d3336284a052b7c09043f3baa84a0e3fa393386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149142669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4aeeab96a922d7a1ab78f8460fac69a2a816ca3b6e125fed1cb4a6eed7411b5`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a23a693d0435d9096a59c377a713b723450b592d3b5f06316fef9eeb38f17`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc051593c4a07ef7ad5fd762b44283836710587d01abf2ebeb0a56303ab6172`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 7.4 MB (7387901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f817f6fdb7f13d39c4df0f552ef9ca2bfa6e668a454e1da6ca2517a8efc439d9`  
		Last Modified: Tue, 04 Feb 2025 07:37:09 GMT  
		Size: 73.1 MB (73065167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0494d93c365c028f5059417ba8bf7f9b24d431a31b87fa6377d4e1d180e457af`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 378.0 KB (378017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7ebdc392d75cc71bd7cc7de5e4d9eea830b1b497cc592e1fec293906ad84a9`  
		Last Modified: Tue, 04 Feb 2025 07:37:07 GMT  
		Size: 99.4 KB (99372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4bcabe0e2faf2b52aaaa7bd8b12785b477e128f41870e5861a2fb57f266265`  
		Last Modified: Tue, 04 Feb 2025 07:37:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5594b52dc2ed41f07ca8731f1d3a1508f5f12286f3634272fb8051567df6b2`  
		Last Modified: Tue, 04 Feb 2025 07:37:08 GMT  
		Size: 41.4 MB (41351710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c8d679dc3d3d2968163532ab43de3cb43616f56858284de5bf2568d257228`  
		Last Modified: Tue, 04 Feb 2025 07:37:08 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:147ab9a2677c357e1185b231e231327efff5ee9bd4cb79ccd3cd7fee80e76849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e49dab81e90811dc3c065f49d460570083ed955142335d69205c40bcdf8370`

```dockerfile
```

-	Layers:
	-	`sha256:37f16ce50caae56e4424d9c7450676605d4306866eae78748dc06d4a5f21d5ac`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 3.5 MB (3455473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ef3b0df1d1e6be3ac92374cbf00a63eb24792839bf9e5fbd9a50931ab50a58`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.2`

```console
$ docker pull couchdb@sha256:2bd5ec8b06df8a8420621ef2484108ac6529232d797437a0d46f4b85afd38784
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.2` - linux; amd64

```console
$ docker pull couchdb@sha256:3d0e2be171ba9b66ab67a4907f188bb8eb83d8bb62da408cc509a61f3533f595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133231420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb4dcfdc18daadfecb197e9907e13418b9b66aa32fa737efef518db9a6c97b4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85591b9d52519ed0d072864357ab208c084989a9b71ec5ab7e4ac6bba4b3019c`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea8859ad3a7a6ad82b48a315171d96f45e40081f730ba0d89e9528b1fbe2d20`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 7.9 MB (7874885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c029b9046aaabc968fd53bcde850eb37af8224260eeab6c2b42e6e0e7e7be8`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 392.1 KB (392139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0cec16a910ed374ddc6e4f24b5bc1a81a1fabe0daf4e736a4027c5719ccac3`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 76.3 KB (76276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4847a061e7ef4ed08f872989838927ab956577e5d77505cff5210c61f7da8fa5`  
		Last Modified: Tue, 25 Feb 2025 02:13:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02523efe4f2bd0155cbd345b526911a8f4cdd9da14e8796ce038c7f901587b6`  
		Last Modified: Tue, 25 Feb 2025 02:13:38 GMT  
		Size: 96.7 MB (96663381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99d1e11ae938be5b8467f909feefadfba977832e2ed49ad54360397a57932db`  
		Last Modified: Tue, 25 Feb 2025 02:13:36 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7814e5128594e0ab39778919cc13848b884d9f61c070b6bfa4ecb0ed7979f8`  
		Last Modified: Tue, 25 Feb 2025 02:13:36 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce68bac6f4b571ddd97d5d83bd913a1ef66ff22b71783b7cb4b103419d89c46a`  
		Last Modified: Tue, 25 Feb 2025 02:13:37 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da84ea640acfe702897d9b081ecaf422133a08fb14884ed86162bd15404dc96`  
		Last Modified: Tue, 25 Feb 2025 02:13:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:3e80272c00dd206b2cea96d0a9dad78f2abbb442ddbdc22a57d1fe2e5121c4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c9f77ff71f65f98d9b9dece72b8615ec40f39bbdfeeb60fdd13200e639cb89`

```dockerfile
```

-	Layers:
	-	`sha256:e93ef5fdfe01284e0307e41d028297e66dafee115e5b64a22e52dd60b91ad558`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 3.9 MB (3896301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7577cb3aa464fc05709b6a37146f1427bb4b6cc07f70d6122c4196f04dfdc20d`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c1dad4d4a114f03206d7eb5fc813f786346a0effcfb51b214ed93253ca8c82f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132525123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b14bbacab0fcd2a682c985938363179f73f7392647e363db6e752439bb54530`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ed3ceb16c56b2588db16dee450d74aa1ef8289827ee553847b0478fdc53e63`  
		Last Modified: Tue, 04 Feb 2025 09:12:38 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3ea78740b6a3b3304eb626727a0ae344f42ca9947ff85a854bde8a5930bcc3`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 7.7 MB (7654497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d001ea6b43aeb929967462ce8b54b3f4db186bb90d348c00b96178594ab055d`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 348.9 KB (348923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76a9f0a91f7d533775b93c2500056380726ad8167d0836f55ee02d8a81ab037`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 76.3 KB (76272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b95425edf70a3faa302ed8ec9e1cfe5ab7117bea1e1a3626b9b93483b55e028`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebdfb636b7919dd927935a09015b93e30d256183e8a5dfa65c7b82d85aed010`  
		Last Modified: Tue, 04 Feb 2025 09:12:43 GMT  
		Size: 96.4 MB (96399124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d82a7e857cb78d0315c4e70a9e82c6e3b13a461d6108dd3d66ff880bf6725a`  
		Last Modified: Tue, 04 Feb 2025 09:12:40 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c4a8b83835238ab8d7370d152167316b9fef300077911ecb41a5f3f4995bb2`  
		Last Modified: Tue, 04 Feb 2025 09:12:40 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7189225d83a03d9c53c644f36dec592e383ba34133ef6453861ada635cf95bd1`  
		Last Modified: Tue, 04 Feb 2025 09:12:40 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccceb8c30650fde66f5614e35cc70b42add1e8217bf12fdb7bfeefa5d78a581c`  
		Last Modified: Tue, 04 Feb 2025 09:12:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:c14cc657c8e65d0b20ea8955bcee471b922835a3f356ef7b61935b8827bcfa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e24b077874b1f8e90bfd4c86a355af3448ed3d17c8359c3498f3c8b218554e1`

```dockerfile
```

-	Layers:
	-	`sha256:856756d494cdbd53a304eb2b595bf3fa41e2b8395308b002038f46b0672a11b8`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 3.9 MB (3933852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:684e6ff21b2ce119827823c16ca83655357632cdd89f785ecad73c183db06ad0`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2` - linux; s390x

```console
$ docker pull couchdb@sha256:bbb98875c2e60d55251caf3ec546a6f399d0344b517aff3d9419956ecc5ca8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129973243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af20b8448a5fc255e2ca6ec2e4b21aa035fe206f22cc74cd6b4e5667d18eaf94`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669ae66225b713189254b710db60d969b0da76c3a6fbfb597d3800dd2869e819`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43419d0575fa54de01c352b29709b0d5ccf15c49d3d1bcc25378930552dfbb`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 7.4 MB (7387928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705dcc6c28fd9ac1b53e0c99842c5e89260eaab760fc90e0989d4a5882121d7e`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 355.6 KB (355637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6008ecd238bf91fc60b5f372ddfdaf51cdc8a9afc258c4548be4d79f12ca23f9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 76.3 KB (76344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfff5ef737373de6ea03d251c1b50454071af66acdb81e7b7c7e04dfdf59fc9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970c2190b221a43960164c74df60732029a7aa45d4eccacc86cf8ed02e90a486`  
		Last Modified: Tue, 04 Feb 2025 07:35:44 GMT  
		Size: 95.3 MB (95289278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbca118bd3ee0264e7ab445907d9c994fcbe1ed9648b8eda4ffe96039cb9a0e`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6160c94cff5d390694fc67808062b79858db1a3398572487e90b4dc650545e6`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e20f342f24eeb86e2afa69eadfe2557a8a501105122c12940a5cc51347802ab`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaf3ddd7aa622b677ecfa8bac5af11f43f3f7d9217667acddd3d79c7c6ea220`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:fdc5ff418ce8940a48676ecb4f18464d922e1b3d7497b403ed26212bee936858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e961e74e238ac3326e88c598f3bd0ca37edca382b81867b8408e055b2a6ec8f`

```dockerfile
```

-	Layers:
	-	`sha256:eb4ee4c1d3c17de162d0cbf896506cb6a51b80c7095de98122fc04b08426ba87`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 3.9 MB (3932647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08d8adad896f090fbd3dc0dfc0edeebf4ed61abaacf54431482a74e0343885f`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.2-nouveau`

```console
$ docker pull couchdb@sha256:8c9ef39b851d0e2184613e26c67333b5258799eb6efafe2a1f75d8029deab706
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.2-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:bf9d15a52b4a4159de6f776059a1fc43fe6f0db3fdfdbdfd21f288ec2be77b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155539446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c77c33bbbb0871a28c6df842259e0a2350a2c45d8b4ca305783b06ca1fce57e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bf3493e51923e21aca2e6b0ed8bdd6c7397432e6a9216e30f2b60a2a7a74b1`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c154d442b26e68a8569c856e9c65fc07ad78e6e22587a621336df375c0c37a`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 7.9 MB (7874871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45c389dd0343a2e240f3dc400e9a571a5dd89785d86095d6d9c017b92dcf94f`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 77.3 MB (77297471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618a4159279c674042f1505eb309bb61ad6e735ddf7fea3786d1ab4ef547b1fb`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 415.0 KB (414956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50377d11c2cfc8d00bfb06284f9d90303501c7e8591acc20594dd3e7a1cd5d0`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 99.3 KB (99279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5306fe2cf1e4820646b4c399391cc240a8572242d28718420e89286b264528b3`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f219b56b995df8101c472c812043e14b1e66a089de47c712964fc9520948cba`  
		Last Modified: Tue, 25 Feb 2025 02:26:35 GMT  
		Size: 41.6 MB (41631688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2f811beb79d2150fe05b012e87da5ee1ef9e84e8daa89b1cf1f268cc4de1d3`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d47b2188df79dcf9dca0d53660a2bdd44f613a9b2bb59b20d387f08a669292e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc925911c466003c1dcb05333360af3fe74198da7ac0e26c85aedbe617d9d1c5`

```dockerfile
```

-	Layers:
	-	`sha256:acb1dc572371d0464b91b652afac79b1800022d27bf82bc6ae8b3ec439d41868`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 3.5 MB (3462070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:635c35ed0a747f6dd5e0cc352dda4f32f8ba8df49ca711a277477ae6e7d45ed9`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:12190121e4afe37f7f4713d179302f43d07c45ba7458eb18994e684f1fa8f6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154320094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0afe6ac983956c792c4a72b95ec23405090ec067d9a1a2d62c60be2f4ededf`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8c4f2c46624f06564e77aac2a810773d1c6d589878c7e5c90453b64f7c3018`  
		Last Modified: Tue, 04 Feb 2025 09:13:34 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43f7d1aebdb65950c261b7b4e5edac88a6d4100d99de298df46d5d39cb4df7c`  
		Last Modified: Tue, 04 Feb 2025 09:13:35 GMT  
		Size: 7.7 MB (7654487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f99af1c739cc1c34fb1fc80f3b014f096c230bd797afe8a0d91c1415ecc178`  
		Last Modified: Tue, 04 Feb 2025 09:13:36 GMT  
		Size: 76.6 MB (76624201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db711157f27ad25a771ab518926d43a113ae58f26a3d472150fd5e9dbf3bc820`  
		Last Modified: Tue, 04 Feb 2025 09:13:34 GMT  
		Size: 371.7 KB (371707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb52220e78c407ec854f7d3057ca6392c5082e6728b5db1827d9a4c335ab192c`  
		Last Modified: Tue, 04 Feb 2025 09:13:35 GMT  
		Size: 99.2 KB (99230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abdc7e54221c13fda65ac4e3aadc8fa27908145c7a377227a17ec61303cdafa`  
		Last Modified: Tue, 04 Feb 2025 09:13:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435fcd2d3b443598407d59b50a5b5e077382cac33315ca321d0d6c2a3beb392a`  
		Last Modified: Tue, 04 Feb 2025 09:13:37 GMT  
		Size: 41.5 MB (41527712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeed426238edc4331b5af9f26701522b45e5c9443681ee17e6af5558e591b48`  
		Last Modified: Tue, 04 Feb 2025 09:13:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:813dc647967c6a9a8e23dc218e9f0e510531ecf418b7bf43e3d40acbf98eb9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b24f4a19ebe838401dee10e251d66883e2e2f0c1a07534783400093761f487`

```dockerfile
```

-	Layers:
	-	`sha256:4cc776e6b8d353323db2e118c9fb5852e20f9f51b9c4df75a54fc4542554248a`  
		Last Modified: Tue, 04 Feb 2025 09:13:35 GMT  
		Size: 3.5 MB (3460728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69393721467e2e4b92ea902efbf775ab22451e94ac4db41ae21e93866936cffa`  
		Last Modified: Tue, 04 Feb 2025 09:13:34 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:c7ef31bf2d0cf9cadfe093f47d3336284a052b7c09043f3baa84a0e3fa393386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149142669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4aeeab96a922d7a1ab78f8460fac69a2a816ca3b6e125fed1cb4a6eed7411b5`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a23a693d0435d9096a59c377a713b723450b592d3b5f06316fef9eeb38f17`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc051593c4a07ef7ad5fd762b44283836710587d01abf2ebeb0a56303ab6172`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 7.4 MB (7387901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f817f6fdb7f13d39c4df0f552ef9ca2bfa6e668a454e1da6ca2517a8efc439d9`  
		Last Modified: Tue, 04 Feb 2025 07:37:09 GMT  
		Size: 73.1 MB (73065167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0494d93c365c028f5059417ba8bf7f9b24d431a31b87fa6377d4e1d180e457af`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 378.0 KB (378017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7ebdc392d75cc71bd7cc7de5e4d9eea830b1b497cc592e1fec293906ad84a9`  
		Last Modified: Tue, 04 Feb 2025 07:37:07 GMT  
		Size: 99.4 KB (99372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4bcabe0e2faf2b52aaaa7bd8b12785b477e128f41870e5861a2fb57f266265`  
		Last Modified: Tue, 04 Feb 2025 07:37:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5594b52dc2ed41f07ca8731f1d3a1508f5f12286f3634272fb8051567df6b2`  
		Last Modified: Tue, 04 Feb 2025 07:37:08 GMT  
		Size: 41.4 MB (41351710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c8d679dc3d3d2968163532ab43de3cb43616f56858284de5bf2568d257228`  
		Last Modified: Tue, 04 Feb 2025 07:37:08 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:147ab9a2677c357e1185b231e231327efff5ee9bd4cb79ccd3cd7fee80e76849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e49dab81e90811dc3c065f49d460570083ed955142335d69205c40bcdf8370`

```dockerfile
```

-	Layers:
	-	`sha256:37f16ce50caae56e4424d9c7450676605d4306866eae78748dc06d4a5f21d5ac`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 3.5 MB (3455473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ef3b0df1d1e6be3ac92374cbf00a63eb24792839bf9e5fbd9a50931ab50a58`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:2bd5ec8b06df8a8420621ef2484108ac6529232d797437a0d46f4b85afd38784
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
$ docker pull couchdb@sha256:3d0e2be171ba9b66ab67a4907f188bb8eb83d8bb62da408cc509a61f3533f595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133231420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb4dcfdc18daadfecb197e9907e13418b9b66aa32fa737efef518db9a6c97b4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85591b9d52519ed0d072864357ab208c084989a9b71ec5ab7e4ac6bba4b3019c`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea8859ad3a7a6ad82b48a315171d96f45e40081f730ba0d89e9528b1fbe2d20`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 7.9 MB (7874885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c029b9046aaabc968fd53bcde850eb37af8224260eeab6c2b42e6e0e7e7be8`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 392.1 KB (392139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0cec16a910ed374ddc6e4f24b5bc1a81a1fabe0daf4e736a4027c5719ccac3`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 76.3 KB (76276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4847a061e7ef4ed08f872989838927ab956577e5d77505cff5210c61f7da8fa5`  
		Last Modified: Tue, 25 Feb 2025 02:13:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02523efe4f2bd0155cbd345b526911a8f4cdd9da14e8796ce038c7f901587b6`  
		Last Modified: Tue, 25 Feb 2025 02:13:38 GMT  
		Size: 96.7 MB (96663381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99d1e11ae938be5b8467f909feefadfba977832e2ed49ad54360397a57932db`  
		Last Modified: Tue, 25 Feb 2025 02:13:36 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7814e5128594e0ab39778919cc13848b884d9f61c070b6bfa4ecb0ed7979f8`  
		Last Modified: Tue, 25 Feb 2025 02:13:36 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce68bac6f4b571ddd97d5d83bd913a1ef66ff22b71783b7cb4b103419d89c46a`  
		Last Modified: Tue, 25 Feb 2025 02:13:37 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da84ea640acfe702897d9b081ecaf422133a08fb14884ed86162bd15404dc96`  
		Last Modified: Tue, 25 Feb 2025 02:13:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:3e80272c00dd206b2cea96d0a9dad78f2abbb442ddbdc22a57d1fe2e5121c4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c9f77ff71f65f98d9b9dece72b8615ec40f39bbdfeeb60fdd13200e639cb89`

```dockerfile
```

-	Layers:
	-	`sha256:e93ef5fdfe01284e0307e41d028297e66dafee115e5b64a22e52dd60b91ad558`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 3.9 MB (3896301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7577cb3aa464fc05709b6a37146f1427bb4b6cc07f70d6122c4196f04dfdc20d`  
		Last Modified: Tue, 25 Feb 2025 02:13:35 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c1dad4d4a114f03206d7eb5fc813f786346a0effcfb51b214ed93253ca8c82f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132525123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b14bbacab0fcd2a682c985938363179f73f7392647e363db6e752439bb54530`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ed3ceb16c56b2588db16dee450d74aa1ef8289827ee553847b0478fdc53e63`  
		Last Modified: Tue, 04 Feb 2025 09:12:38 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3ea78740b6a3b3304eb626727a0ae344f42ca9947ff85a854bde8a5930bcc3`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 7.7 MB (7654497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d001ea6b43aeb929967462ce8b54b3f4db186bb90d348c00b96178594ab055d`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 348.9 KB (348923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76a9f0a91f7d533775b93c2500056380726ad8167d0836f55ee02d8a81ab037`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 76.3 KB (76272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b95425edf70a3faa302ed8ec9e1cfe5ab7117bea1e1a3626b9b93483b55e028`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebdfb636b7919dd927935a09015b93e30d256183e8a5dfa65c7b82d85aed010`  
		Last Modified: Tue, 04 Feb 2025 09:12:43 GMT  
		Size: 96.4 MB (96399124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d82a7e857cb78d0315c4e70a9e82c6e3b13a461d6108dd3d66ff880bf6725a`  
		Last Modified: Tue, 04 Feb 2025 09:12:40 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c4a8b83835238ab8d7370d152167316b9fef300077911ecb41a5f3f4995bb2`  
		Last Modified: Tue, 04 Feb 2025 09:12:40 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7189225d83a03d9c53c644f36dec592e383ba34133ef6453861ada635cf95bd1`  
		Last Modified: Tue, 04 Feb 2025 09:12:40 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccceb8c30650fde66f5614e35cc70b42add1e8217bf12fdb7bfeefa5d78a581c`  
		Last Modified: Tue, 04 Feb 2025 09:12:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:c14cc657c8e65d0b20ea8955bcee471b922835a3f356ef7b61935b8827bcfa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e24b077874b1f8e90bfd4c86a355af3448ed3d17c8359c3498f3c8b218554e1`

```dockerfile
```

-	Layers:
	-	`sha256:856756d494cdbd53a304eb2b595bf3fa41e2b8395308b002038f46b0672a11b8`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 3.9 MB (3933852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:684e6ff21b2ce119827823c16ca83655357632cdd89f785ecad73c183db06ad0`  
		Last Modified: Tue, 04 Feb 2025 09:12:39 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:bbb98875c2e60d55251caf3ec546a6f399d0344b517aff3d9419956ecc5ca8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129973243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af20b8448a5fc255e2ca6ec2e4b21aa035fe206f22cc74cd6b4e5667d18eaf94`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669ae66225b713189254b710db60d969b0da76c3a6fbfb597d3800dd2869e819`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43419d0575fa54de01c352b29709b0d5ccf15c49d3d1bcc25378930552dfbb`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 7.4 MB (7387928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705dcc6c28fd9ac1b53e0c99842c5e89260eaab760fc90e0989d4a5882121d7e`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 355.6 KB (355637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6008ecd238bf91fc60b5f372ddfdaf51cdc8a9afc258c4548be4d79f12ca23f9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 76.3 KB (76344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfff5ef737373de6ea03d251c1b50454071af66acdb81e7b7c7e04dfdf59fc9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970c2190b221a43960164c74df60732029a7aa45d4eccacc86cf8ed02e90a486`  
		Last Modified: Tue, 04 Feb 2025 07:35:44 GMT  
		Size: 95.3 MB (95289278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbca118bd3ee0264e7ab445907d9c994fcbe1ed9648b8eda4ffe96039cb9a0e`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6160c94cff5d390694fc67808062b79858db1a3398572487e90b4dc650545e6`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e20f342f24eeb86e2afa69eadfe2557a8a501105122c12940a5cc51347802ab`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaf3ddd7aa622b677ecfa8bac5af11f43f3f7d9217667acddd3d79c7c6ea220`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:fdc5ff418ce8940a48676ecb4f18464d922e1b3d7497b403ed26212bee936858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e961e74e238ac3326e88c598f3bd0ca37edca382b81867b8408e055b2a6ec8f`

```dockerfile
```

-	Layers:
	-	`sha256:eb4ee4c1d3c17de162d0cbf896506cb6a51b80c7095de98122fc04b08426ba87`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 3.9 MB (3932647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08d8adad896f090fbd3dc0dfc0edeebf4ed61abaacf54431482a74e0343885f`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json
