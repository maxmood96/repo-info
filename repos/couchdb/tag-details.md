<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3-nouveau`](#couchdb3-nouveau)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.3`](#couchdb333)
-	[`couchdb:3.4`](#couchdb34)
-	[`couchdb:3.4-nouveau`](#couchdb34-nouveau)
-	[`couchdb:3.4.3`](#couchdb343)
-	[`couchdb:3.4.3-nouveau`](#couchdb343-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:eaccac1af6288e7c81f62ccb093a5ec4a03d7762ea85347fb00a1793571a57f6
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
$ docker pull couchdb@sha256:29bda1ef06e431703b2b2ae415afbd8e39cc0bfd5e618aec2ef4afd9b6e8c708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138996025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577f5a2bf8281f310410466f9ff2dbcabfe1473b4e50a8384be08b36ecf99607`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8bb06f1e12481f1734930caaf5aec605aaa24e1a4a714390080ff8d49a9bae`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c643e44c289be880b7e1077b20be39cc8aa46c96dc275d3c274d9f4285b16e89`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 7.9 MB (7874898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139f130bffc490d838a88a0d05accd783a68e9f617fd52025ac774f55bfe8b96`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 392.2 KB (392157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482d9e178fbe5fbe5cfad58aa00c10b65769efe8fb24ae45ec9a43b2389fb87b`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 76.3 KB (76322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662901ec9a4cb6ba009d3607b9ad113b7bdd517130e2eec9112df2d01a05d6cb`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e060d223a8335af42564a119d05c7671db6bf1f629900166eac7b8c0e939a`  
		Last Modified: Mon, 28 Apr 2025 21:56:05 GMT  
		Size: 102.4 MB (102419585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a1370ccd45c896adc8fd7170cfbeb3eeac84209a0219dd34aec6210e1ab02`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1e127bb37e749c471a816e789f4ded13248cb110d7e3f9e4e17c8f7191e9d6`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87be8d54aedb6022da943334261c18e1eed1d602beb1ea3baf8af2a328b975`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133652bc69003427ae7004295dfcdea96aa5a003479ceaa3742c9e0e88528555`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:42c546356d24d3788c955b5d00eb4bcd393a46bc59e6fd076597281b2fe6b7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e2799689e298289b95db4b12008b49d684dc9a4297f34dd80dbfa169f6da0a`

```dockerfile
```

-	Layers:
	-	`sha256:a3f7e3b29115dda76e014b52b775a8dc0168d756776e2e5f0c6569ab4e764c88`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 4.0 MB (3962194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f550c2045c0da081acd88fb3e06f2f1cfe56c8b3010ee2d89946189a639dff5`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

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

### `couchdb:3` - unknown; unknown

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

### `couchdb:3` - linux; s390x

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

### `couchdb:3` - unknown; unknown

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

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:21ade5564867292f2d134e3ac5d61c3a530fafe26df5409f4b184e47959923b0
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
$ docker pull couchdb@sha256:77ffe59ff29af9d3c5219482f72482fbcb2a0ff2483c083e2d49fb115673bb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156349834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a27220813b744db3146ca8ced46f5cabde9a8fb7793a6c920793d220354a0f6`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a837b37dbc4aaf872f53093cddc1be6d7ef890b0711392143a9af72cef98aa9`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75c714820d9f6c5cbd4bf86389324df57d7541f49cf758a529ba5491022d8f`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 7.9 MB (7874927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe12777043dbe4709756fe502296dc6f6c3bbd613e3ef916bf1734214b192ba7`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 77.3 MB (77297600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78ba57999ae720b3c4071011a08e9999098f55ed42ff9b6ed3f3803132698e6`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 415.0 KB (414976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29364f5cdb32bc05cdd929c02986311ed94c76e959a4e263ba9cf30cd49229ce`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 99.3 KB (99309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bc17ee849dc1a4faaa61126db10e65016ed2a4c2710bd1d2ad98c07f3660bf`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9cc3233d493f6ccb82dbb845f9bf89aedb7a809588f957dff97a8a417b20bd`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 42.4 MB (42433507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fa03def47bdb76fe273a3779236c9b64f6cbba548c826afab19c88bef4e4d`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a6081534b52d88c51815ba521ecff693dea686881b9966a95ee75abfab2e5fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ce8df7d14f7982fb816dce683b26a15fde337ce687af08ea53c0ade53063f9`

```dockerfile
```

-	Layers:
	-	`sha256:a76c0ac78c05527f8220cc9ae241667389856abc3b537b0574c27f99d4400106`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 3.5 MB (3468472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a08d555edab0c60d4bcb148bd4978664d1b20f9aae43f6e9a2097f7d4c7bdf4`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

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

### `couchdb:3-nouveau` - unknown; unknown

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

### `couchdb:3-nouveau` - linux; s390x

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

### `couchdb:3-nouveau` - unknown; unknown

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

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:307a3f5276f64c0db28f226b7b5c180b8f2c851afa681cfb4fbb1b1fe7fd5587
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
$ docker pull couchdb@sha256:e99f02d9e4742707e405b21443cd0a356c00d04a1bf8cf77577eebd1dc3868b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96727790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca5e1fbe30fdbccb0459c3f10a79d739e0f31c530be14b0557c819d19ab393f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407f5eb39ed8742e057e33cd1b896b81f5b6929d23bce88cb5c17a81840cfcfa`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d7e18ff8a4005a7f5ea9ca6b86b9cf9ab15aad74f4bbddcd638b81960bc3e`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 7.9 MB (7874918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf731d868a24446da372fcb6f05404a7ce5545902bca70f90b2c6c4fe01adaa`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 392.1 KB (392142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55312866b224adebbae017ad55435170d1149844fe1671127cd88aede44274e3`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 76.3 KB (76292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a576df24c6c7e8b0a5e1aac2dfd8597604c94ddf4e52a7d33f34ab766e67cc9b`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce368c5697d630b4246a24b2b7ff45afd37f3cd045c4b44c02b52e25663ce4f6`  
		Last Modified: Mon, 28 Apr 2025 21:56:06 GMT  
		Size: 60.2 MB (60151368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452d939ad465209dfd377643a24569f7b5d7f4b3bea489ac55f68d9fa4b0ff5a`  
		Last Modified: Mon, 28 Apr 2025 21:56:04 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115bf3cdefa316d34f53af2c4589620247c1144983b22cb680d5bf94ce0e05f0`  
		Last Modified: Mon, 28 Apr 2025 21:56:04 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bed53beb22392f56a73cb344cb68487e3da83f60dec8adf055a709d28a5aea`  
		Last Modified: Mon, 28 Apr 2025 21:56:04 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4106aeb26392af5bd9eaa662f9464b7adea8a2fda8399cea3bef5301cb7efc`  
		Last Modified: Mon, 28 Apr 2025 21:56:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:b4e4c2d3260ab92828d8996365e50c56d88d0d43c1a1fb760ae7ea34b92d4e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3767400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5125fcae8f23f87e03de19bd622915ac4dea9351a5ec5bd8defd9ca1572f2aaa`

```dockerfile
```

-	Layers:
	-	`sha256:c8c489da1cc8ad4704d7635333a5193730c24f0b25b995f1bc2437419ff0c802`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 3.7 MB (3736208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f5b842c6900d66e2d973d0a39c6a8fe8d8833659c0e3ab471b23965e9049cbb`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:939b4086d52e5a787945bed1caf85ee3411ebd26f3d26121942529aa6c3c0ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96086213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efff69c8f8e024fcbf404d877ac943df90d7f30e4524aeeec94aa4a3050f160`
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:e7c373fdbfe317a860467686a1c033fc439386ed4ac09cfc640abfe53068101b`  
		Last Modified: Tue, 29 Apr 2025 01:52:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f584142958f90c4044a93df2a9ee87cf5e76ccdc59763f558c2a96bcc4f4a64f`  
		Last Modified: Tue, 29 Apr 2025 01:52:19 GMT  
		Size: 59.9 MB (59934335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ce26b4de543db0be50e9a6a8f4cb28a4fe3720d5422f54894d6403b1193b87`  
		Last Modified: Tue, 29 Apr 2025 01:52:17 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edce2e0a8b64a874d1bf15d1a0a369c8f8607864b9be0697f8fe7b1167666f19`  
		Last Modified: Tue, 29 Apr 2025 01:52:17 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c5126744b1e4b7a801c29ece7761f527249b3654f149f90eec435bad828768`  
		Last Modified: Tue, 29 Apr 2025 01:52:18 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbbe95f930a021582f71ba0d78f7eebd957b0202bbab1939f78fb296c26d72a`  
		Last Modified: Tue, 29 Apr 2025 01:52:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:654a7fd2ad004631468975e1f89476ba51dfdd98cbf6e766df096ec3dde25774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3767839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecab0d851d19cb215b48d1bf63bcb31d7ddf7976f06d5975165701f94e9368f1`

```dockerfile
```

-	Layers:
	-	`sha256:700023bb6b815902a666e9c5e328428f3b8cb1bc9a8c524c58e47f42e8f8ba56`  
		Last Modified: Tue, 29 Apr 2025 01:52:17 GMT  
		Size: 3.7 MB (3736477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29afba81d6cbb7789fb3dcc716f39632aa3027d65eaaf88e640c678403b08ee8`  
		Last Modified: Tue, 29 Apr 2025 01:52:17 GMT  
		Size: 31.4 KB (31362 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f45396da7cc26743f8e72c872006515047df8d81359252a87e1207c16199e4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102861906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddbcfc4d7be5608ef2fd4acccf6eb20002393936967c187719f4dbdb37851d2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8731030796c12ce9b5d62a2a419d1f71171ca01a4f77173d3b2ba7e8bd33362`  
		Last Modified: Tue, 29 Apr 2025 00:40:26 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15208278f2164f047a2789391c076f61302a28318a44cb9584ed8042b115cb9e`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 8.9 MB (8890023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef32d7d78ee5ac90dfb01f5ffea9e564790ab1fce565caac1107a258b5c3a405`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 444.7 KB (444703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2784d482238c88cb632a8dfc389afdea294c256834519a7748ac07cc2d06f605`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 76.4 KB (76362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd88b39de501bc5bc7b95537db178bb105328de4757f651a3c52b5c52b6defe4`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c053eb35ca156613e1c1e7d5d17c124768083ef0df7752005e19436882fc5262`  
		Last Modified: Tue, 29 Apr 2025 00:40:30 GMT  
		Size: 61.4 MB (61376946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1199e9c940aa8c4136c5f981a8123a0a5e6e56c10c81dd16b6bdd20afff59cb6`  
		Last Modified: Tue, 29 Apr 2025 00:40:28 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3bc3511c87e7b79ae803b28d433431d260ef1ef26cc90f52630cab82892fff`  
		Last Modified: Tue, 29 Apr 2025 00:40:28 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a723ce6d2cecaf0bbe4ff843d6f14a1de1cc278ac4c0e2b7e6ffa8fc9a2c8f46`  
		Last Modified: Tue, 29 Apr 2025 00:40:29 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9490a38aa65df97b8809cb8cf036bc7b6fc393257dcd58c90f3c10a41e4be957`  
		Last Modified: Tue, 29 Apr 2025 00:40:29 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e5af63559e8bbffc038fb0bee9cb097174710b494567524359313fe63d791cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3771948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569f456fdee9d1e1f3c0d862d04a31b91f6a53999e36c450710b0f072d501f8f`

```dockerfile
```

-	Layers:
	-	`sha256:a40ed823df7c76efce63ebc8dd981e6dc3926470fb2e0b146673b6a1aa9d7ea4`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 3.7 MB (3740712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4853a45ed87121c7bafba000562fd2c2f854b5ce3ed4024d99804dad2e327a7b`  
		Last Modified: Tue, 29 Apr 2025 00:40:26 GMT  
		Size: 31.2 KB (31236 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:8da535f283bf6fe9b3c2baa9252a4a13e4794f6f8a779a1180e6f68084cabffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93450974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4819b1906862b3cdf1650526984d06ad927ec281a53c901e0744ce6905c68ce`
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:626eda8b887690797597b86d47fbf9bd887a653d72a8694aae4fad8825b8f4e9`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309ae0ff12be0ccf11ecb17b85e5f7e2d2044a66e84113a33c7d970dc59f9c95`  
		Last Modified: Tue, 29 Apr 2025 00:05:33 GMT  
		Size: 58.7 MB (58740760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d86c95fee04803ae944fbf26c47f3da6214b06c42a1742ea41f22667df8a426`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec1814a99eaa0cf1a6f08a05bfacc74dc65180f4b46838a62e041b4f2db600b`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891160d2d5c6cda656e3a61e2aa974fd98a2ed9a696a1204bda32857619c2e69`  
		Last Modified: Tue, 29 Apr 2025 00:05:33 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97eb0bb15e1241d2f0c8e094baa13bd0b8b6e36eb787478469a9f1f9e7726a4`  
		Last Modified: Tue, 29 Apr 2025 00:05:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:3509830c86e729659945ff2e7eeb172dbd6cc475aaafd1b127300045f690f969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16330a21bc29dfe1d0dfd270b5407b313f177cc1c5fb1b5b644fda5a18cd2719`

```dockerfile
```

-	Layers:
	-	`sha256:80394274165a2b65e8450f5373b03ab197b73b71d3ab927ee89f379f3ff30bfa`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 3.7 MB (3735296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1103b97f0c1b9b9be544d5817b02013cb2a74420389995f13dca8ad7c70f9a2f`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 31.2 KB (31190 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:307a3f5276f64c0db28f226b7b5c180b8f2c851afa681cfb4fbb1b1fe7fd5587
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
$ docker pull couchdb@sha256:e99f02d9e4742707e405b21443cd0a356c00d04a1bf8cf77577eebd1dc3868b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96727790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca5e1fbe30fdbccb0459c3f10a79d739e0f31c530be14b0557c819d19ab393f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407f5eb39ed8742e057e33cd1b896b81f5b6929d23bce88cb5c17a81840cfcfa`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d7e18ff8a4005a7f5ea9ca6b86b9cf9ab15aad74f4bbddcd638b81960bc3e`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 7.9 MB (7874918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf731d868a24446da372fcb6f05404a7ce5545902bca70f90b2c6c4fe01adaa`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 392.1 KB (392142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55312866b224adebbae017ad55435170d1149844fe1671127cd88aede44274e3`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 76.3 KB (76292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a576df24c6c7e8b0a5e1aac2dfd8597604c94ddf4e52a7d33f34ab766e67cc9b`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce368c5697d630b4246a24b2b7ff45afd37f3cd045c4b44c02b52e25663ce4f6`  
		Last Modified: Mon, 28 Apr 2025 21:56:06 GMT  
		Size: 60.2 MB (60151368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452d939ad465209dfd377643a24569f7b5d7f4b3bea489ac55f68d9fa4b0ff5a`  
		Last Modified: Mon, 28 Apr 2025 21:56:04 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115bf3cdefa316d34f53af2c4589620247c1144983b22cb680d5bf94ce0e05f0`  
		Last Modified: Mon, 28 Apr 2025 21:56:04 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bed53beb22392f56a73cb344cb68487e3da83f60dec8adf055a709d28a5aea`  
		Last Modified: Mon, 28 Apr 2025 21:56:04 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4106aeb26392af5bd9eaa662f9464b7adea8a2fda8399cea3bef5301cb7efc`  
		Last Modified: Mon, 28 Apr 2025 21:56:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:b4e4c2d3260ab92828d8996365e50c56d88d0d43c1a1fb760ae7ea34b92d4e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3767400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5125fcae8f23f87e03de19bd622915ac4dea9351a5ec5bd8defd9ca1572f2aaa`

```dockerfile
```

-	Layers:
	-	`sha256:c8c489da1cc8ad4704d7635333a5193730c24f0b25b995f1bc2437419ff0c802`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 3.7 MB (3736208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f5b842c6900d66e2d973d0a39c6a8fe8d8833659c0e3ab471b23965e9049cbb`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:939b4086d52e5a787945bed1caf85ee3411ebd26f3d26121942529aa6c3c0ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96086213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efff69c8f8e024fcbf404d877ac943df90d7f30e4524aeeec94aa4a3050f160`
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:e7c373fdbfe317a860467686a1c033fc439386ed4ac09cfc640abfe53068101b`  
		Last Modified: Tue, 29 Apr 2025 01:52:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f584142958f90c4044a93df2a9ee87cf5e76ccdc59763f558c2a96bcc4f4a64f`  
		Last Modified: Tue, 29 Apr 2025 01:52:19 GMT  
		Size: 59.9 MB (59934335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ce26b4de543db0be50e9a6a8f4cb28a4fe3720d5422f54894d6403b1193b87`  
		Last Modified: Tue, 29 Apr 2025 01:52:17 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edce2e0a8b64a874d1bf15d1a0a369c8f8607864b9be0697f8fe7b1167666f19`  
		Last Modified: Tue, 29 Apr 2025 01:52:17 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c5126744b1e4b7a801c29ece7761f527249b3654f149f90eec435bad828768`  
		Last Modified: Tue, 29 Apr 2025 01:52:18 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbbe95f930a021582f71ba0d78f7eebd957b0202bbab1939f78fb296c26d72a`  
		Last Modified: Tue, 29 Apr 2025 01:52:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:654a7fd2ad004631468975e1f89476ba51dfdd98cbf6e766df096ec3dde25774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3767839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecab0d851d19cb215b48d1bf63bcb31d7ddf7976f06d5975165701f94e9368f1`

```dockerfile
```

-	Layers:
	-	`sha256:700023bb6b815902a666e9c5e328428f3b8cb1bc9a8c524c58e47f42e8f8ba56`  
		Last Modified: Tue, 29 Apr 2025 01:52:17 GMT  
		Size: 3.7 MB (3736477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29afba81d6cbb7789fb3dcc716f39632aa3027d65eaaf88e640c678403b08ee8`  
		Last Modified: Tue, 29 Apr 2025 01:52:17 GMT  
		Size: 31.4 KB (31362 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f45396da7cc26743f8e72c872006515047df8d81359252a87e1207c16199e4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102861906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddbcfc4d7be5608ef2fd4acccf6eb20002393936967c187719f4dbdb37851d2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8731030796c12ce9b5d62a2a419d1f71171ca01a4f77173d3b2ba7e8bd33362`  
		Last Modified: Tue, 29 Apr 2025 00:40:26 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15208278f2164f047a2789391c076f61302a28318a44cb9584ed8042b115cb9e`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 8.9 MB (8890023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef32d7d78ee5ac90dfb01f5ffea9e564790ab1fce565caac1107a258b5c3a405`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 444.7 KB (444703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2784d482238c88cb632a8dfc389afdea294c256834519a7748ac07cc2d06f605`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 76.4 KB (76362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd88b39de501bc5bc7b95537db178bb105328de4757f651a3c52b5c52b6defe4`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c053eb35ca156613e1c1e7d5d17c124768083ef0df7752005e19436882fc5262`  
		Last Modified: Tue, 29 Apr 2025 00:40:30 GMT  
		Size: 61.4 MB (61376946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1199e9c940aa8c4136c5f981a8123a0a5e6e56c10c81dd16b6bdd20afff59cb6`  
		Last Modified: Tue, 29 Apr 2025 00:40:28 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3bc3511c87e7b79ae803b28d433431d260ef1ef26cc90f52630cab82892fff`  
		Last Modified: Tue, 29 Apr 2025 00:40:28 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a723ce6d2cecaf0bbe4ff843d6f14a1de1cc278ac4c0e2b7e6ffa8fc9a2c8f46`  
		Last Modified: Tue, 29 Apr 2025 00:40:29 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9490a38aa65df97b8809cb8cf036bc7b6fc393257dcd58c90f3c10a41e4be957`  
		Last Modified: Tue, 29 Apr 2025 00:40:29 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e5af63559e8bbffc038fb0bee9cb097174710b494567524359313fe63d791cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3771948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569f456fdee9d1e1f3c0d862d04a31b91f6a53999e36c450710b0f072d501f8f`

```dockerfile
```

-	Layers:
	-	`sha256:a40ed823df7c76efce63ebc8dd981e6dc3926470fb2e0b146673b6a1aa9d7ea4`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 3.7 MB (3740712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4853a45ed87121c7bafba000562fd2c2f854b5ce3ed4024d99804dad2e327a7b`  
		Last Modified: Tue, 29 Apr 2025 00:40:26 GMT  
		Size: 31.2 KB (31236 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:8da535f283bf6fe9b3c2baa9252a4a13e4794f6f8a779a1180e6f68084cabffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93450974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4819b1906862b3cdf1650526984d06ad927ec281a53c901e0744ce6905c68ce`
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:626eda8b887690797597b86d47fbf9bd887a653d72a8694aae4fad8825b8f4e9`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309ae0ff12be0ccf11ecb17b85e5f7e2d2044a66e84113a33c7d970dc59f9c95`  
		Last Modified: Tue, 29 Apr 2025 00:05:33 GMT  
		Size: 58.7 MB (58740760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d86c95fee04803ae944fbf26c47f3da6214b06c42a1742ea41f22667df8a426`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec1814a99eaa0cf1a6f08a05bfacc74dc65180f4b46838a62e041b4f2db600b`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891160d2d5c6cda656e3a61e2aa974fd98a2ed9a696a1204bda32857619c2e69`  
		Last Modified: Tue, 29 Apr 2025 00:05:33 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97eb0bb15e1241d2f0c8e094baa13bd0b8b6e36eb787478469a9f1f9e7726a4`  
		Last Modified: Tue, 29 Apr 2025 00:05:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:3509830c86e729659945ff2e7eeb172dbd6cc475aaafd1b127300045f690f969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16330a21bc29dfe1d0dfd270b5407b313f177cc1c5fb1b5b644fda5a18cd2719`

```dockerfile
```

-	Layers:
	-	`sha256:80394274165a2b65e8450f5373b03ab197b73b71d3ab927ee89f379f3ff30bfa`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 3.7 MB (3735296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1103b97f0c1b9b9be544d5817b02013cb2a74420389995f13dca8ad7c70f9a2f`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 31.2 KB (31190 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:eaccac1af6288e7c81f62ccb093a5ec4a03d7762ea85347fb00a1793571a57f6
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
$ docker pull couchdb@sha256:29bda1ef06e431703b2b2ae415afbd8e39cc0bfd5e618aec2ef4afd9b6e8c708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138996025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577f5a2bf8281f310410466f9ff2dbcabfe1473b4e50a8384be08b36ecf99607`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8bb06f1e12481f1734930caaf5aec605aaa24e1a4a714390080ff8d49a9bae`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c643e44c289be880b7e1077b20be39cc8aa46c96dc275d3c274d9f4285b16e89`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 7.9 MB (7874898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139f130bffc490d838a88a0d05accd783a68e9f617fd52025ac774f55bfe8b96`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 392.2 KB (392157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482d9e178fbe5fbe5cfad58aa00c10b65769efe8fb24ae45ec9a43b2389fb87b`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 76.3 KB (76322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662901ec9a4cb6ba009d3607b9ad113b7bdd517130e2eec9112df2d01a05d6cb`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e060d223a8335af42564a119d05c7671db6bf1f629900166eac7b8c0e939a`  
		Last Modified: Mon, 28 Apr 2025 21:56:05 GMT  
		Size: 102.4 MB (102419585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a1370ccd45c896adc8fd7170cfbeb3eeac84209a0219dd34aec6210e1ab02`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1e127bb37e749c471a816e789f4ded13248cb110d7e3f9e4e17c8f7191e9d6`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87be8d54aedb6022da943334261c18e1eed1d602beb1ea3baf8af2a328b975`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133652bc69003427ae7004295dfcdea96aa5a003479ceaa3742c9e0e88528555`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:42c546356d24d3788c955b5d00eb4bcd393a46bc59e6fd076597281b2fe6b7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e2799689e298289b95db4b12008b49d684dc9a4297f34dd80dbfa169f6da0a`

```dockerfile
```

-	Layers:
	-	`sha256:a3f7e3b29115dda76e014b52b775a8dc0168d756776e2e5f0c6569ab4e764c88`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 4.0 MB (3962194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f550c2045c0da081acd88fb3e06f2f1cfe56c8b3010ee2d89946189a639dff5`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 31.8 KB (31781 bytes)  
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
$ docker pull couchdb@sha256:21ade5564867292f2d134e3ac5d61c3a530fafe26df5409f4b184e47959923b0
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
$ docker pull couchdb@sha256:77ffe59ff29af9d3c5219482f72482fbcb2a0ff2483c083e2d49fb115673bb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156349834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a27220813b744db3146ca8ced46f5cabde9a8fb7793a6c920793d220354a0f6`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a837b37dbc4aaf872f53093cddc1be6d7ef890b0711392143a9af72cef98aa9`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75c714820d9f6c5cbd4bf86389324df57d7541f49cf758a529ba5491022d8f`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 7.9 MB (7874927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe12777043dbe4709756fe502296dc6f6c3bbd613e3ef916bf1734214b192ba7`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 77.3 MB (77297600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78ba57999ae720b3c4071011a08e9999098f55ed42ff9b6ed3f3803132698e6`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 415.0 KB (414976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29364f5cdb32bc05cdd929c02986311ed94c76e959a4e263ba9cf30cd49229ce`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 99.3 KB (99309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bc17ee849dc1a4faaa61126db10e65016ed2a4c2710bd1d2ad98c07f3660bf`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9cc3233d493f6ccb82dbb845f9bf89aedb7a809588f957dff97a8a417b20bd`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 42.4 MB (42433507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fa03def47bdb76fe273a3779236c9b64f6cbba548c826afab19c88bef4e4d`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a6081534b52d88c51815ba521ecff693dea686881b9966a95ee75abfab2e5fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ce8df7d14f7982fb816dce683b26a15fde337ce687af08ea53c0ade53063f9`

```dockerfile
```

-	Layers:
	-	`sha256:a76c0ac78c05527f8220cc9ae241667389856abc3b537b0574c27f99d4400106`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 3.5 MB (3468472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a08d555edab0c60d4bcb148bd4978664d1b20f9aae43f6e9a2097f7d4c7bdf4`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 24.6 KB (24563 bytes)  
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
$ docker pull couchdb@sha256:eaccac1af6288e7c81f62ccb093a5ec4a03d7762ea85347fb00a1793571a57f6
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
$ docker pull couchdb@sha256:29bda1ef06e431703b2b2ae415afbd8e39cc0bfd5e618aec2ef4afd9b6e8c708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138996025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577f5a2bf8281f310410466f9ff2dbcabfe1473b4e50a8384be08b36ecf99607`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8bb06f1e12481f1734930caaf5aec605aaa24e1a4a714390080ff8d49a9bae`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c643e44c289be880b7e1077b20be39cc8aa46c96dc275d3c274d9f4285b16e89`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 7.9 MB (7874898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139f130bffc490d838a88a0d05accd783a68e9f617fd52025ac774f55bfe8b96`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 392.2 KB (392157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482d9e178fbe5fbe5cfad58aa00c10b65769efe8fb24ae45ec9a43b2389fb87b`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 76.3 KB (76322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662901ec9a4cb6ba009d3607b9ad113b7bdd517130e2eec9112df2d01a05d6cb`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e060d223a8335af42564a119d05c7671db6bf1f629900166eac7b8c0e939a`  
		Last Modified: Mon, 28 Apr 2025 21:56:05 GMT  
		Size: 102.4 MB (102419585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a1370ccd45c896adc8fd7170cfbeb3eeac84209a0219dd34aec6210e1ab02`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1e127bb37e749c471a816e789f4ded13248cb110d7e3f9e4e17c8f7191e9d6`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87be8d54aedb6022da943334261c18e1eed1d602beb1ea3baf8af2a328b975`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133652bc69003427ae7004295dfcdea96aa5a003479ceaa3742c9e0e88528555`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:42c546356d24d3788c955b5d00eb4bcd393a46bc59e6fd076597281b2fe6b7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e2799689e298289b95db4b12008b49d684dc9a4297f34dd80dbfa169f6da0a`

```dockerfile
```

-	Layers:
	-	`sha256:a3f7e3b29115dda76e014b52b775a8dc0168d756776e2e5f0c6569ab4e764c88`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 4.0 MB (3962194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f550c2045c0da081acd88fb3e06f2f1cfe56c8b3010ee2d89946189a639dff5`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 31.8 KB (31781 bytes)  
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
$ docker pull couchdb@sha256:21ade5564867292f2d134e3ac5d61c3a530fafe26df5409f4b184e47959923b0
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
$ docker pull couchdb@sha256:77ffe59ff29af9d3c5219482f72482fbcb2a0ff2483c083e2d49fb115673bb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156349834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a27220813b744db3146ca8ced46f5cabde9a8fb7793a6c920793d220354a0f6`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a837b37dbc4aaf872f53093cddc1be6d7ef890b0711392143a9af72cef98aa9`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75c714820d9f6c5cbd4bf86389324df57d7541f49cf758a529ba5491022d8f`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 7.9 MB (7874927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe12777043dbe4709756fe502296dc6f6c3bbd613e3ef916bf1734214b192ba7`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 77.3 MB (77297600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78ba57999ae720b3c4071011a08e9999098f55ed42ff9b6ed3f3803132698e6`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 415.0 KB (414976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29364f5cdb32bc05cdd929c02986311ed94c76e959a4e263ba9cf30cd49229ce`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 99.3 KB (99309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bc17ee849dc1a4faaa61126db10e65016ed2a4c2710bd1d2ad98c07f3660bf`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9cc3233d493f6ccb82dbb845f9bf89aedb7a809588f957dff97a8a417b20bd`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 42.4 MB (42433507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fa03def47bdb76fe273a3779236c9b64f6cbba548c826afab19c88bef4e4d`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a6081534b52d88c51815ba521ecff693dea686881b9966a95ee75abfab2e5fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ce8df7d14f7982fb816dce683b26a15fde337ce687af08ea53c0ade53063f9`

```dockerfile
```

-	Layers:
	-	`sha256:a76c0ac78c05527f8220cc9ae241667389856abc3b537b0574c27f99d4400106`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 3.5 MB (3468472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a08d555edab0c60d4bcb148bd4978664d1b20f9aae43f6e9a2097f7d4c7bdf4`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 24.6 KB (24563 bytes)  
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

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:eaccac1af6288e7c81f62ccb093a5ec4a03d7762ea85347fb00a1793571a57f6
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
$ docker pull couchdb@sha256:29bda1ef06e431703b2b2ae415afbd8e39cc0bfd5e618aec2ef4afd9b6e8c708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138996025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577f5a2bf8281f310410466f9ff2dbcabfe1473b4e50a8384be08b36ecf99607`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8bb06f1e12481f1734930caaf5aec605aaa24e1a4a714390080ff8d49a9bae`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c643e44c289be880b7e1077b20be39cc8aa46c96dc275d3c274d9f4285b16e89`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 7.9 MB (7874898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139f130bffc490d838a88a0d05accd783a68e9f617fd52025ac774f55bfe8b96`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 392.2 KB (392157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482d9e178fbe5fbe5cfad58aa00c10b65769efe8fb24ae45ec9a43b2389fb87b`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 76.3 KB (76322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662901ec9a4cb6ba009d3607b9ad113b7bdd517130e2eec9112df2d01a05d6cb`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e060d223a8335af42564a119d05c7671db6bf1f629900166eac7b8c0e939a`  
		Last Modified: Mon, 28 Apr 2025 21:56:05 GMT  
		Size: 102.4 MB (102419585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a1370ccd45c896adc8fd7170cfbeb3eeac84209a0219dd34aec6210e1ab02`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1e127bb37e749c471a816e789f4ded13248cb110d7e3f9e4e17c8f7191e9d6`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87be8d54aedb6022da943334261c18e1eed1d602beb1ea3baf8af2a328b975`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133652bc69003427ae7004295dfcdea96aa5a003479ceaa3742c9e0e88528555`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:42c546356d24d3788c955b5d00eb4bcd393a46bc59e6fd076597281b2fe6b7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e2799689e298289b95db4b12008b49d684dc9a4297f34dd80dbfa169f6da0a`

```dockerfile
```

-	Layers:
	-	`sha256:a3f7e3b29115dda76e014b52b775a8dc0168d756776e2e5f0c6569ab4e764c88`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 4.0 MB (3962194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f550c2045c0da081acd88fb3e06f2f1cfe56c8b3010ee2d89946189a639dff5`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

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

### `couchdb:latest` - unknown; unknown

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

### `couchdb:latest` - linux; s390x

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

### `couchdb:latest` - unknown; unknown

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
