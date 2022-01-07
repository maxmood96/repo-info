<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.2`](#couchdb312)
-	[`couchdb:3.2`](#couchdb32)
-	[`couchdb:3.2.1`](#couchdb321)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:8046799d478ea8bcb70567b31797217e979c9dd061e9117255babc9414d9e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:03775cf875992a4d4c2ecc960a3ad993ce75d1e253052d6a97a1b5f35d703373
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4eeb2fa8b5b9ce75c02a424d5d37dd3f2a515c2d5a0360dd625644e0dd84b71`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:09:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 02:09:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 02:09:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:09:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 02:09:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 02:09:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:10:13 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 21 Dec 2021 02:10:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Dec 2021 02:10:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Dec 2021 02:10:33 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Dec 2021 02:10:33 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Dec 2021 02:10:33 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 21 Dec 2021 02:10:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Dec 2021 02:10:34 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Dec 2021 02:10:34 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Dec 2021 02:10:35 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Dec 2021 02:10:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430d6c754b31c32dd1a76de01ad3420033c05661c724b97d708362a8ec139d42`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227820103030b5232e32ba7e76de56823a61d47245d450403c0040933f6aebd`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 6.7 MB (6691223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454611cf9dafef09164a7f64cb967a12ab5d1549d70599c56b74a2c283ae8ef1`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 1.3 MB (1258346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993063a8d6d688f066b9d8208c98f7d0dd3d78e7076cbc7a132ab98a975dece`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 293.0 KB (293029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1637f5ce62470caf7b07bea4f8d9390cbc4b7d4d0327077ff7dc0a6945d1c7e1`  
		Last Modified: Tue, 21 Dec 2021 02:11:33 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94c9d9a9a8f2c85a319528cd13d772ff89bec2ee8a63c3f44f29146f33381ae`  
		Last Modified: Tue, 21 Dec 2021 02:11:38 GMT  
		Size: 49.1 MB (49113865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5c1ae4a87ec62883c2b6cdecdcbd87b2b45770266482f2affe0e987595c1fd`  
		Last Modified: Tue, 21 Dec 2021 02:11:31 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca940117ded324a7613aec69d0a872122475b20d28490cc85075417bc2e1c14b`  
		Last Modified: Tue, 21 Dec 2021 02:11:31 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8b1e22e3198e344c657e9b7e16d7a102e3f9be9c43e64e085f782600ca1627`  
		Last Modified: Tue, 21 Dec 2021 02:11:31 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f074cac28bde7e408bfeaf9dbc7076e5376ff6197806fc282ef88f12967f2230`  
		Last Modified: Tue, 21 Dec 2021 02:11:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a3d10d9247c7752e14634448ace11aa91234bda900dadd8fc2e3e4ba14692cb6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154bfb5a3405c061d262397e60860c9e021f37a6b315cb6364d78e2bec56190c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:44:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 10:44:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 10:44:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:44:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 10:44:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 10:45:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:46:18 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 21 Dec 2021 10:46:18 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Dec 2021 10:46:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Dec 2021 10:46:39 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Dec 2021 10:46:40 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Dec 2021 10:46:41 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 21 Dec 2021 10:46:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Dec 2021 10:46:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Dec 2021 10:46:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Dec 2021 10:46:44 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Dec 2021 10:46:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589f1cb358d3e3a123049341ce44cdc00d6c6484a66c1169425711e3d4e5ef61`  
		Last Modified: Tue, 21 Dec 2021 10:47:20 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ca2948856ed69aa492a4294b0510bcc03616eceac737dd2fe13ddbdad889d`  
		Last Modified: Tue, 21 Dec 2021 10:47:19 GMT  
		Size: 6.5 MB (6549891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41232c99e6d3b4632a28126c15a9405dac5ec12ef1c3e71b47f7e455ed8bef7`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 951.2 KB (951161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8413befe0746257456c09468b422890a186a8cf1a2868f008b8d56de24a7d815`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 79.9 KB (79896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a6d094941ef8631acb8e5ee45fec2ede42e4bd34bd72487780d761a035d1c1`  
		Last Modified: Tue, 21 Dec 2021 10:48:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078d27380f72f29462473356c0b6ff2dd60b35664262a9837de59e80206d3ae4`  
		Last Modified: Tue, 21 Dec 2021 10:48:10 GMT  
		Size: 39.0 MB (39011935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9872b9e69dc520883ed7cf3d38d40f9562fdc9f921724a31f44513c172574bd0`  
		Last Modified: Tue, 21 Dec 2021 10:48:05 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60556cedd8f948beaed3ce12465b77400d7837624f2fb1d442631e6762cb356a`  
		Last Modified: Tue, 21 Dec 2021 10:48:05 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddc0d47de849ca62541cfade6c36dce399d20b240dda62ac32e7cc9362226ca`  
		Last Modified: Tue, 21 Dec 2021 10:48:05 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341aab2940e95718a85811ebfa73c3fb3c39b91aecf6e2e1e42f34f657e27e7e`  
		Last Modified: Tue, 21 Dec 2021 10:48:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:8046799d478ea8bcb70567b31797217e979c9dd061e9117255babc9414d9e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:03775cf875992a4d4c2ecc960a3ad993ce75d1e253052d6a97a1b5f35d703373
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4eeb2fa8b5b9ce75c02a424d5d37dd3f2a515c2d5a0360dd625644e0dd84b71`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:09:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 02:09:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 02:09:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:09:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 02:09:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 02:09:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:10:13 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 21 Dec 2021 02:10:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Dec 2021 02:10:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Dec 2021 02:10:33 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Dec 2021 02:10:33 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Dec 2021 02:10:33 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 21 Dec 2021 02:10:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Dec 2021 02:10:34 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Dec 2021 02:10:34 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Dec 2021 02:10:35 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Dec 2021 02:10:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430d6c754b31c32dd1a76de01ad3420033c05661c724b97d708362a8ec139d42`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227820103030b5232e32ba7e76de56823a61d47245d450403c0040933f6aebd`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 6.7 MB (6691223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454611cf9dafef09164a7f64cb967a12ab5d1549d70599c56b74a2c283ae8ef1`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 1.3 MB (1258346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993063a8d6d688f066b9d8208c98f7d0dd3d78e7076cbc7a132ab98a975dece`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 293.0 KB (293029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1637f5ce62470caf7b07bea4f8d9390cbc4b7d4d0327077ff7dc0a6945d1c7e1`  
		Last Modified: Tue, 21 Dec 2021 02:11:33 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94c9d9a9a8f2c85a319528cd13d772ff89bec2ee8a63c3f44f29146f33381ae`  
		Last Modified: Tue, 21 Dec 2021 02:11:38 GMT  
		Size: 49.1 MB (49113865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5c1ae4a87ec62883c2b6cdecdcbd87b2b45770266482f2affe0e987595c1fd`  
		Last Modified: Tue, 21 Dec 2021 02:11:31 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca940117ded324a7613aec69d0a872122475b20d28490cc85075417bc2e1c14b`  
		Last Modified: Tue, 21 Dec 2021 02:11:31 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8b1e22e3198e344c657e9b7e16d7a102e3f9be9c43e64e085f782600ca1627`  
		Last Modified: Tue, 21 Dec 2021 02:11:31 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f074cac28bde7e408bfeaf9dbc7076e5376ff6197806fc282ef88f12967f2230`  
		Last Modified: Tue, 21 Dec 2021 02:11:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a3d10d9247c7752e14634448ace11aa91234bda900dadd8fc2e3e4ba14692cb6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154bfb5a3405c061d262397e60860c9e021f37a6b315cb6364d78e2bec56190c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:44:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 10:44:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 10:44:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:44:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 10:44:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 10:45:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:46:18 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 21 Dec 2021 10:46:18 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Dec 2021 10:46:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Dec 2021 10:46:39 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Dec 2021 10:46:40 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Dec 2021 10:46:41 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 21 Dec 2021 10:46:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Dec 2021 10:46:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Dec 2021 10:46:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Dec 2021 10:46:44 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Dec 2021 10:46:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589f1cb358d3e3a123049341ce44cdc00d6c6484a66c1169425711e3d4e5ef61`  
		Last Modified: Tue, 21 Dec 2021 10:47:20 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ca2948856ed69aa492a4294b0510bcc03616eceac737dd2fe13ddbdad889d`  
		Last Modified: Tue, 21 Dec 2021 10:47:19 GMT  
		Size: 6.5 MB (6549891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41232c99e6d3b4632a28126c15a9405dac5ec12ef1c3e71b47f7e455ed8bef7`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 951.2 KB (951161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8413befe0746257456c09468b422890a186a8cf1a2868f008b8d56de24a7d815`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 79.9 KB (79896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a6d094941ef8631acb8e5ee45fec2ede42e4bd34bd72487780d761a035d1c1`  
		Last Modified: Tue, 21 Dec 2021 10:48:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078d27380f72f29462473356c0b6ff2dd60b35664262a9837de59e80206d3ae4`  
		Last Modified: Tue, 21 Dec 2021 10:48:10 GMT  
		Size: 39.0 MB (39011935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9872b9e69dc520883ed7cf3d38d40f9562fdc9f921724a31f44513c172574bd0`  
		Last Modified: Tue, 21 Dec 2021 10:48:05 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60556cedd8f948beaed3ce12465b77400d7837624f2fb1d442631e6762cb356a`  
		Last Modified: Tue, 21 Dec 2021 10:48:05 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddc0d47de849ca62541cfade6c36dce399d20b240dda62ac32e7cc9362226ca`  
		Last Modified: Tue, 21 Dec 2021 10:48:05 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341aab2940e95718a85811ebfa73c3fb3c39b91aecf6e2e1e42f34f657e27e7e`  
		Last Modified: Tue, 21 Dec 2021 10:48:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:8046799d478ea8bcb70567b31797217e979c9dd061e9117255babc9414d9e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:03775cf875992a4d4c2ecc960a3ad993ce75d1e253052d6a97a1b5f35d703373
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4eeb2fa8b5b9ce75c02a424d5d37dd3f2a515c2d5a0360dd625644e0dd84b71`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:09:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 02:09:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 02:09:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:09:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 02:09:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 02:09:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:10:13 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 21 Dec 2021 02:10:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Dec 2021 02:10:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Dec 2021 02:10:33 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Dec 2021 02:10:33 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Dec 2021 02:10:33 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 21 Dec 2021 02:10:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Dec 2021 02:10:34 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Dec 2021 02:10:34 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Dec 2021 02:10:35 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Dec 2021 02:10:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430d6c754b31c32dd1a76de01ad3420033c05661c724b97d708362a8ec139d42`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227820103030b5232e32ba7e76de56823a61d47245d450403c0040933f6aebd`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 6.7 MB (6691223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454611cf9dafef09164a7f64cb967a12ab5d1549d70599c56b74a2c283ae8ef1`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 1.3 MB (1258346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993063a8d6d688f066b9d8208c98f7d0dd3d78e7076cbc7a132ab98a975dece`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 293.0 KB (293029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1637f5ce62470caf7b07bea4f8d9390cbc4b7d4d0327077ff7dc0a6945d1c7e1`  
		Last Modified: Tue, 21 Dec 2021 02:11:33 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94c9d9a9a8f2c85a319528cd13d772ff89bec2ee8a63c3f44f29146f33381ae`  
		Last Modified: Tue, 21 Dec 2021 02:11:38 GMT  
		Size: 49.1 MB (49113865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5c1ae4a87ec62883c2b6cdecdcbd87b2b45770266482f2affe0e987595c1fd`  
		Last Modified: Tue, 21 Dec 2021 02:11:31 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca940117ded324a7613aec69d0a872122475b20d28490cc85075417bc2e1c14b`  
		Last Modified: Tue, 21 Dec 2021 02:11:31 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8b1e22e3198e344c657e9b7e16d7a102e3f9be9c43e64e085f782600ca1627`  
		Last Modified: Tue, 21 Dec 2021 02:11:31 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f074cac28bde7e408bfeaf9dbc7076e5376ff6197806fc282ef88f12967f2230`  
		Last Modified: Tue, 21 Dec 2021 02:11:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a3d10d9247c7752e14634448ace11aa91234bda900dadd8fc2e3e4ba14692cb6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154bfb5a3405c061d262397e60860c9e021f37a6b315cb6364d78e2bec56190c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:44:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 10:44:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 10:44:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:44:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 10:44:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 10:45:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:46:18 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 21 Dec 2021 10:46:18 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Dec 2021 10:46:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Dec 2021 10:46:39 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Dec 2021 10:46:40 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Dec 2021 10:46:41 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 21 Dec 2021 10:46:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Dec 2021 10:46:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Dec 2021 10:46:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Dec 2021 10:46:44 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Dec 2021 10:46:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589f1cb358d3e3a123049341ce44cdc00d6c6484a66c1169425711e3d4e5ef61`  
		Last Modified: Tue, 21 Dec 2021 10:47:20 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ca2948856ed69aa492a4294b0510bcc03616eceac737dd2fe13ddbdad889d`  
		Last Modified: Tue, 21 Dec 2021 10:47:19 GMT  
		Size: 6.5 MB (6549891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41232c99e6d3b4632a28126c15a9405dac5ec12ef1c3e71b47f7e455ed8bef7`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 951.2 KB (951161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8413befe0746257456c09468b422890a186a8cf1a2868f008b8d56de24a7d815`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 79.9 KB (79896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a6d094941ef8631acb8e5ee45fec2ede42e4bd34bd72487780d761a035d1c1`  
		Last Modified: Tue, 21 Dec 2021 10:48:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078d27380f72f29462473356c0b6ff2dd60b35664262a9837de59e80206d3ae4`  
		Last Modified: Tue, 21 Dec 2021 10:48:10 GMT  
		Size: 39.0 MB (39011935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9872b9e69dc520883ed7cf3d38d40f9562fdc9f921724a31f44513c172574bd0`  
		Last Modified: Tue, 21 Dec 2021 10:48:05 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60556cedd8f948beaed3ce12465b77400d7837624f2fb1d442631e6762cb356a`  
		Last Modified: Tue, 21 Dec 2021 10:48:05 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddc0d47de849ca62541cfade6c36dce399d20b240dda62ac32e7cc9362226ca`  
		Last Modified: Tue, 21 Dec 2021 10:48:05 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341aab2940e95718a85811ebfa73c3fb3c39b91aecf6e2e1e42f34f657e27e7e`  
		Last Modified: Tue, 21 Dec 2021 10:48:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:23ed255c28c572aa36807ee921ded8cbc1e7d7f3208a8840704122b45eddcab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:70238fcfb1c45bc522fb1f938f943d067b3a0a6d853019e71d60f8e8a05fea9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80511344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eef6d738a43d45b22aa6ae64fc27db658ea22a925f10704ac9a60b7d833b48e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:09:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 02:09:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 02:09:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:09:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 02:09:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 02:09:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 20:36:30 GMT
ENV COUCHDB_VERSION=3.2.1
# Fri, 07 Jan 2022 20:36:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 07 Jan 2022 20:36:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 07 Jan 2022 20:36:46 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 07 Jan 2022 20:36:46 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 07 Jan 2022 20:36:46 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 07 Jan 2022 20:36:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 07 Jan 2022 20:36:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 07 Jan 2022 20:36:48 GMT
VOLUME [/opt/couchdb/data]
# Fri, 07 Jan 2022 20:36:48 GMT
EXPOSE 4369 5984 9100
# Fri, 07 Jan 2022 20:36:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430d6c754b31c32dd1a76de01ad3420033c05661c724b97d708362a8ec139d42`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227820103030b5232e32ba7e76de56823a61d47245d450403c0040933f6aebd`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 6.7 MB (6691223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454611cf9dafef09164a7f64cb967a12ab5d1549d70599c56b74a2c283ae8ef1`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 1.3 MB (1258346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993063a8d6d688f066b9d8208c98f7d0dd3d78e7076cbc7a132ab98a975dece`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 293.0 KB (293029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daab33e2a8e2b31988302eefebb4d3fb95b679e20f9cb91197d781a81491e4ef`  
		Last Modified: Fri, 07 Jan 2022 20:37:12 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6f52546ad69b1df110088c52a1840548890672ffb46a5968af7180078c9c64`  
		Last Modified: Fri, 07 Jan 2022 20:37:16 GMT  
		Size: 45.1 MB (45108011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0a0f43f3f898a1e37c16c0a848e585ccc4e4ea7fe6748550907c396fbaf28e`  
		Last Modified: Fri, 07 Jan 2022 20:37:10 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876550ef73929756b8e909730728ff16701b28f403e844bddeaf2b599958bd01`  
		Last Modified: Fri, 07 Jan 2022 20:37:10 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d422fb7671bc9b35975f370ca04370e11c4052db5242bc084dc338955a89a36`  
		Last Modified: Fri, 07 Jan 2022 20:37:09 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e62e4ddd9f34131e7208bb0c78edf3a3945da27916c1254e354c10ea3798c1`  
		Last Modified: Fri, 07 Jan 2022 20:37:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8012c438a9e3a65a8038a0487bd369245c50e69a0c4e293b2824ee0c776daf4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75204155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da31e65e3b379792dba0dd84f3eabb0fe351fd12114709eb7fff52ba545a9e8d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:44:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 10:44:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 10:44:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:44:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 10:44:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 10:45:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 21:02:23 GMT
ENV COUCHDB_VERSION=3.2.1
# Fri, 07 Jan 2022 21:02:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 07 Jan 2022 21:02:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 07 Jan 2022 21:02:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 07 Jan 2022 21:02:45 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 07 Jan 2022 21:02:46 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 07 Jan 2022 21:02:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 07 Jan 2022 21:02:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 07 Jan 2022 21:02:48 GMT
VOLUME [/opt/couchdb/data]
# Fri, 07 Jan 2022 21:02:49 GMT
EXPOSE 4369 5984 9100
# Fri, 07 Jan 2022 21:02:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589f1cb358d3e3a123049341ce44cdc00d6c6484a66c1169425711e3d4e5ef61`  
		Last Modified: Tue, 21 Dec 2021 10:47:20 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ca2948856ed69aa492a4294b0510bcc03616eceac737dd2fe13ddbdad889d`  
		Last Modified: Tue, 21 Dec 2021 10:47:19 GMT  
		Size: 6.5 MB (6549891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41232c99e6d3b4632a28126c15a9405dac5ec12ef1c3e71b47f7e455ed8bef7`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 951.2 KB (951161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8413befe0746257456c09468b422890a186a8cf1a2868f008b8d56de24a7d815`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 79.9 KB (79896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad07ad1fcfb75834d9740456a30e61a390b2ccbb809791477e8a7fbe0b0dc645`  
		Last Modified: Fri, 07 Jan 2022 21:03:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd813278096e945f32723d914d08d50e2e82b3fdbe2cdd245e23ee0a7ab5aed`  
		Last Modified: Fri, 07 Jan 2022 21:03:34 GMT  
		Size: 41.7 MB (41693137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9281e76054aeaa925b24494e88c9fe127e126f173fe0275f4ed81cd9bae7d10c`  
		Last Modified: Fri, 07 Jan 2022 21:03:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773617ade8b61955b3be425a9807142b00b27a1c857a26c02fdd7e6edd6f0d02`  
		Last Modified: Fri, 07 Jan 2022 21:03:28 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34361202a634b564b220a4b67ac8147daf0a95652df68112019db1a35f2a562`  
		Last Modified: Fri, 07 Jan 2022 21:03:29 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae18d4fa0d0ec7548b0205881a7d67bf88b20d7457a505c7f0c0ec23c459e3f8`  
		Last Modified: Fri, 07 Jan 2022 21:03:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:f394b5efef2c7847717f1b19e8dfad21e7ee8549cd3a1c80bb4754a3b0b0c8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:2e06818b7a3fa8ae48f4e3bf7ca82db67de0d1f6bfe3c70e8a68d0d8170cfa53
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80002622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87828b0a612a59cc70d4a823c78f2a891faeb5ed9ed02814966fc51ff27a45b9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:09:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 02:09:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 02:09:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:09:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 02:09:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 02:09:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:09:54 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 21 Dec 2021 02:09:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Dec 2021 02:10:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Dec 2021 02:10:09 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Dec 2021 02:10:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Dec 2021 02:10:09 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 21 Dec 2021 02:10:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Dec 2021 02:10:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Dec 2021 02:10:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Dec 2021 02:10:11 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Dec 2021 02:10:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430d6c754b31c32dd1a76de01ad3420033c05661c724b97d708362a8ec139d42`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227820103030b5232e32ba7e76de56823a61d47245d450403c0040933f6aebd`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 6.7 MB (6691223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454611cf9dafef09164a7f64cb967a12ab5d1549d70599c56b74a2c283ae8ef1`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 1.3 MB (1258346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993063a8d6d688f066b9d8208c98f7d0dd3d78e7076cbc7a132ab98a975dece`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 293.0 KB (293029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae5e24fa47c4d07d685f4da7933c29053e805916adbc1f25a32b18431a019ab`  
		Last Modified: Tue, 21 Dec 2021 02:11:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aed3be65c5381338c3823426cd0d147ee4e6645dda931266529c35bb7cc38e1`  
		Last Modified: Tue, 21 Dec 2021 02:11:21 GMT  
		Size: 44.6 MB (44599286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83197b74e0dd7dbea62a348f70081bcc753e1e46abaf13c5b2a2ed0db63df8dc`  
		Last Modified: Tue, 21 Dec 2021 02:11:16 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa83aca7b989869c6bb1bab2377fc32570122aaba095a35659beba6b38bf12d`  
		Last Modified: Tue, 21 Dec 2021 02:11:16 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49a58d05524c9278149f90a1238c117f9169d6db7ff90351e62dba516890192`  
		Last Modified: Tue, 21 Dec 2021 02:11:16 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953b11a446c19d551e48a794270efad862132626a6a1e382b3245cd202fbfe7e`  
		Last Modified: Tue, 21 Dec 2021 02:11:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f988ebabdab088013e6ed91095e50319a6fd01c2eb1b7700ef91b01b7c699808
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74612501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6219f3f786f9d20c8771d747f90937559c8dbfe4247d20f513ec8bff4aca885`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:44:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 10:44:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 10:44:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:44:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 10:44:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 10:45:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:45:41 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 21 Dec 2021 10:45:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Dec 2021 10:46:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Dec 2021 10:46:03 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Dec 2021 10:46:04 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Dec 2021 10:46:05 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 21 Dec 2021 10:46:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Dec 2021 10:46:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Dec 2021 10:46:07 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Dec 2021 10:46:08 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Dec 2021 10:46:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589f1cb358d3e3a123049341ce44cdc00d6c6484a66c1169425711e3d4e5ef61`  
		Last Modified: Tue, 21 Dec 2021 10:47:20 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ca2948856ed69aa492a4294b0510bcc03616eceac737dd2fe13ddbdad889d`  
		Last Modified: Tue, 21 Dec 2021 10:47:19 GMT  
		Size: 6.5 MB (6549891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41232c99e6d3b4632a28126c15a9405dac5ec12ef1c3e71b47f7e455ed8bef7`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 951.2 KB (951161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8413befe0746257456c09468b422890a186a8cf1a2868f008b8d56de24a7d815`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 79.9 KB (79896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e08a629b29d021aa7226c26fefa17d5eace42fdaa6b6d956df056bf48eaf77`  
		Last Modified: Tue, 21 Dec 2021 10:47:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c222a0edd71310ef39bdb1dc12359794f490d9a23be86329fddf10d79845daf`  
		Last Modified: Tue, 21 Dec 2021 10:47:54 GMT  
		Size: 41.1 MB (41101483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162b8bee104f638573a4cd9b8c16469ec14e1f09cf944d0b7d43ac4651a579ce`  
		Last Modified: Tue, 21 Dec 2021 10:47:49 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4987da0c177b4aa3945ef21699e453608ae10613a07ecb18f25c710857b61b`  
		Last Modified: Tue, 21 Dec 2021 10:47:49 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d9540ea59c3e148a1b9a953f5eb3f9258a504165f8704eaf6e70b3a0f0acb`  
		Last Modified: Tue, 21 Dec 2021 10:47:49 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f657d8e28bae029f16c56ff6924e32764aba83819311f13114c37ec665f63f`  
		Last Modified: Tue, 21 Dec 2021 10:47:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:f394b5efef2c7847717f1b19e8dfad21e7ee8549cd3a1c80bb4754a3b0b0c8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:2e06818b7a3fa8ae48f4e3bf7ca82db67de0d1f6bfe3c70e8a68d0d8170cfa53
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80002622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87828b0a612a59cc70d4a823c78f2a891faeb5ed9ed02814966fc51ff27a45b9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:09:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 02:09:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 02:09:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:09:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 02:09:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 02:09:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:09:54 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 21 Dec 2021 02:09:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Dec 2021 02:10:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Dec 2021 02:10:09 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Dec 2021 02:10:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Dec 2021 02:10:09 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 21 Dec 2021 02:10:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Dec 2021 02:10:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Dec 2021 02:10:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Dec 2021 02:10:11 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Dec 2021 02:10:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430d6c754b31c32dd1a76de01ad3420033c05661c724b97d708362a8ec139d42`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227820103030b5232e32ba7e76de56823a61d47245d450403c0040933f6aebd`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 6.7 MB (6691223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454611cf9dafef09164a7f64cb967a12ab5d1549d70599c56b74a2c283ae8ef1`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 1.3 MB (1258346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993063a8d6d688f066b9d8208c98f7d0dd3d78e7076cbc7a132ab98a975dece`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 293.0 KB (293029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae5e24fa47c4d07d685f4da7933c29053e805916adbc1f25a32b18431a019ab`  
		Last Modified: Tue, 21 Dec 2021 02:11:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aed3be65c5381338c3823426cd0d147ee4e6645dda931266529c35bb7cc38e1`  
		Last Modified: Tue, 21 Dec 2021 02:11:21 GMT  
		Size: 44.6 MB (44599286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83197b74e0dd7dbea62a348f70081bcc753e1e46abaf13c5b2a2ed0db63df8dc`  
		Last Modified: Tue, 21 Dec 2021 02:11:16 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa83aca7b989869c6bb1bab2377fc32570122aaba095a35659beba6b38bf12d`  
		Last Modified: Tue, 21 Dec 2021 02:11:16 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49a58d05524c9278149f90a1238c117f9169d6db7ff90351e62dba516890192`  
		Last Modified: Tue, 21 Dec 2021 02:11:16 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953b11a446c19d551e48a794270efad862132626a6a1e382b3245cd202fbfe7e`  
		Last Modified: Tue, 21 Dec 2021 02:11:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f988ebabdab088013e6ed91095e50319a6fd01c2eb1b7700ef91b01b7c699808
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74612501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6219f3f786f9d20c8771d747f90937559c8dbfe4247d20f513ec8bff4aca885`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:44:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 10:44:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 10:44:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:44:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 10:44:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 10:45:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:45:41 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 21 Dec 2021 10:45:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Dec 2021 10:46:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Dec 2021 10:46:03 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Dec 2021 10:46:04 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Dec 2021 10:46:05 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 21 Dec 2021 10:46:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Dec 2021 10:46:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Dec 2021 10:46:07 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Dec 2021 10:46:08 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Dec 2021 10:46:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589f1cb358d3e3a123049341ce44cdc00d6c6484a66c1169425711e3d4e5ef61`  
		Last Modified: Tue, 21 Dec 2021 10:47:20 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ca2948856ed69aa492a4294b0510bcc03616eceac737dd2fe13ddbdad889d`  
		Last Modified: Tue, 21 Dec 2021 10:47:19 GMT  
		Size: 6.5 MB (6549891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41232c99e6d3b4632a28126c15a9405dac5ec12ef1c3e71b47f7e455ed8bef7`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 951.2 KB (951161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8413befe0746257456c09468b422890a186a8cf1a2868f008b8d56de24a7d815`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 79.9 KB (79896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e08a629b29d021aa7226c26fefa17d5eace42fdaa6b6d956df056bf48eaf77`  
		Last Modified: Tue, 21 Dec 2021 10:47:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c222a0edd71310ef39bdb1dc12359794f490d9a23be86329fddf10d79845daf`  
		Last Modified: Tue, 21 Dec 2021 10:47:54 GMT  
		Size: 41.1 MB (41101483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162b8bee104f638573a4cd9b8c16469ec14e1f09cf944d0b7d43ac4651a579ce`  
		Last Modified: Tue, 21 Dec 2021 10:47:49 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4987da0c177b4aa3945ef21699e453608ae10613a07ecb18f25c710857b61b`  
		Last Modified: Tue, 21 Dec 2021 10:47:49 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d9540ea59c3e148a1b9a953f5eb3f9258a504165f8704eaf6e70b3a0f0acb`  
		Last Modified: Tue, 21 Dec 2021 10:47:49 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f657d8e28bae029f16c56ff6924e32764aba83819311f13114c37ec665f63f`  
		Last Modified: Tue, 21 Dec 2021 10:47:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:23ed255c28c572aa36807ee921ded8cbc1e7d7f3208a8840704122b45eddcab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:70238fcfb1c45bc522fb1f938f943d067b3a0a6d853019e71d60f8e8a05fea9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80511344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eef6d738a43d45b22aa6ae64fc27db658ea22a925f10704ac9a60b7d833b48e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:09:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 02:09:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 02:09:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:09:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 02:09:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 02:09:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 20:36:30 GMT
ENV COUCHDB_VERSION=3.2.1
# Fri, 07 Jan 2022 20:36:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 07 Jan 2022 20:36:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 07 Jan 2022 20:36:46 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 07 Jan 2022 20:36:46 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 07 Jan 2022 20:36:46 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 07 Jan 2022 20:36:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 07 Jan 2022 20:36:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 07 Jan 2022 20:36:48 GMT
VOLUME [/opt/couchdb/data]
# Fri, 07 Jan 2022 20:36:48 GMT
EXPOSE 4369 5984 9100
# Fri, 07 Jan 2022 20:36:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430d6c754b31c32dd1a76de01ad3420033c05661c724b97d708362a8ec139d42`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227820103030b5232e32ba7e76de56823a61d47245d450403c0040933f6aebd`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 6.7 MB (6691223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454611cf9dafef09164a7f64cb967a12ab5d1549d70599c56b74a2c283ae8ef1`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 1.3 MB (1258346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993063a8d6d688f066b9d8208c98f7d0dd3d78e7076cbc7a132ab98a975dece`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 293.0 KB (293029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daab33e2a8e2b31988302eefebb4d3fb95b679e20f9cb91197d781a81491e4ef`  
		Last Modified: Fri, 07 Jan 2022 20:37:12 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6f52546ad69b1df110088c52a1840548890672ffb46a5968af7180078c9c64`  
		Last Modified: Fri, 07 Jan 2022 20:37:16 GMT  
		Size: 45.1 MB (45108011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0a0f43f3f898a1e37c16c0a848e585ccc4e4ea7fe6748550907c396fbaf28e`  
		Last Modified: Fri, 07 Jan 2022 20:37:10 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876550ef73929756b8e909730728ff16701b28f403e844bddeaf2b599958bd01`  
		Last Modified: Fri, 07 Jan 2022 20:37:10 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d422fb7671bc9b35975f370ca04370e11c4052db5242bc084dc338955a89a36`  
		Last Modified: Fri, 07 Jan 2022 20:37:09 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e62e4ddd9f34131e7208bb0c78edf3a3945da27916c1254e354c10ea3798c1`  
		Last Modified: Fri, 07 Jan 2022 20:37:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8012c438a9e3a65a8038a0487bd369245c50e69a0c4e293b2824ee0c776daf4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75204155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da31e65e3b379792dba0dd84f3eabb0fe351fd12114709eb7fff52ba545a9e8d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:44:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 10:44:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 10:44:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:44:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 10:44:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 10:45:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 21:02:23 GMT
ENV COUCHDB_VERSION=3.2.1
# Fri, 07 Jan 2022 21:02:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 07 Jan 2022 21:02:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 07 Jan 2022 21:02:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 07 Jan 2022 21:02:45 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 07 Jan 2022 21:02:46 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 07 Jan 2022 21:02:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 07 Jan 2022 21:02:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 07 Jan 2022 21:02:48 GMT
VOLUME [/opt/couchdb/data]
# Fri, 07 Jan 2022 21:02:49 GMT
EXPOSE 4369 5984 9100
# Fri, 07 Jan 2022 21:02:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589f1cb358d3e3a123049341ce44cdc00d6c6484a66c1169425711e3d4e5ef61`  
		Last Modified: Tue, 21 Dec 2021 10:47:20 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ca2948856ed69aa492a4294b0510bcc03616eceac737dd2fe13ddbdad889d`  
		Last Modified: Tue, 21 Dec 2021 10:47:19 GMT  
		Size: 6.5 MB (6549891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41232c99e6d3b4632a28126c15a9405dac5ec12ef1c3e71b47f7e455ed8bef7`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 951.2 KB (951161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8413befe0746257456c09468b422890a186a8cf1a2868f008b8d56de24a7d815`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 79.9 KB (79896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad07ad1fcfb75834d9740456a30e61a390b2ccbb809791477e8a7fbe0b0dc645`  
		Last Modified: Fri, 07 Jan 2022 21:03:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd813278096e945f32723d914d08d50e2e82b3fdbe2cdd245e23ee0a7ab5aed`  
		Last Modified: Fri, 07 Jan 2022 21:03:34 GMT  
		Size: 41.7 MB (41693137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9281e76054aeaa925b24494e88c9fe127e126f173fe0275f4ed81cd9bae7d10c`  
		Last Modified: Fri, 07 Jan 2022 21:03:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773617ade8b61955b3be425a9807142b00b27a1c857a26c02fdd7e6edd6f0d02`  
		Last Modified: Fri, 07 Jan 2022 21:03:28 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34361202a634b564b220a4b67ac8147daf0a95652df68112019db1a35f2a562`  
		Last Modified: Fri, 07 Jan 2022 21:03:29 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae18d4fa0d0ec7548b0205881a7d67bf88b20d7457a505c7f0c0ec23c459e3f8`  
		Last Modified: Fri, 07 Jan 2022 21:03:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.1`

```console
$ docker pull couchdb@sha256:23ed255c28c572aa36807ee921ded8cbc1e7d7f3208a8840704122b45eddcab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.2.1` - linux; amd64

```console
$ docker pull couchdb@sha256:70238fcfb1c45bc522fb1f938f943d067b3a0a6d853019e71d60f8e8a05fea9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80511344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eef6d738a43d45b22aa6ae64fc27db658ea22a925f10704ac9a60b7d833b48e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:09:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 02:09:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 02:09:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:09:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 02:09:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 02:09:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 20:36:30 GMT
ENV COUCHDB_VERSION=3.2.1
# Fri, 07 Jan 2022 20:36:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 07 Jan 2022 20:36:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 07 Jan 2022 20:36:46 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 07 Jan 2022 20:36:46 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 07 Jan 2022 20:36:46 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 07 Jan 2022 20:36:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 07 Jan 2022 20:36:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 07 Jan 2022 20:36:48 GMT
VOLUME [/opt/couchdb/data]
# Fri, 07 Jan 2022 20:36:48 GMT
EXPOSE 4369 5984 9100
# Fri, 07 Jan 2022 20:36:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430d6c754b31c32dd1a76de01ad3420033c05661c724b97d708362a8ec139d42`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227820103030b5232e32ba7e76de56823a61d47245d450403c0040933f6aebd`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 6.7 MB (6691223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454611cf9dafef09164a7f64cb967a12ab5d1549d70599c56b74a2c283ae8ef1`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 1.3 MB (1258346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993063a8d6d688f066b9d8208c98f7d0dd3d78e7076cbc7a132ab98a975dece`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 293.0 KB (293029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daab33e2a8e2b31988302eefebb4d3fb95b679e20f9cb91197d781a81491e4ef`  
		Last Modified: Fri, 07 Jan 2022 20:37:12 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6f52546ad69b1df110088c52a1840548890672ffb46a5968af7180078c9c64`  
		Last Modified: Fri, 07 Jan 2022 20:37:16 GMT  
		Size: 45.1 MB (45108011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0a0f43f3f898a1e37c16c0a848e585ccc4e4ea7fe6748550907c396fbaf28e`  
		Last Modified: Fri, 07 Jan 2022 20:37:10 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876550ef73929756b8e909730728ff16701b28f403e844bddeaf2b599958bd01`  
		Last Modified: Fri, 07 Jan 2022 20:37:10 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d422fb7671bc9b35975f370ca04370e11c4052db5242bc084dc338955a89a36`  
		Last Modified: Fri, 07 Jan 2022 20:37:09 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e62e4ddd9f34131e7208bb0c78edf3a3945da27916c1254e354c10ea3798c1`  
		Last Modified: Fri, 07 Jan 2022 20:37:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8012c438a9e3a65a8038a0487bd369245c50e69a0c4e293b2824ee0c776daf4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75204155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da31e65e3b379792dba0dd84f3eabb0fe351fd12114709eb7fff52ba545a9e8d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:44:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 10:44:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 10:44:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:44:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 10:44:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 10:45:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 21:02:23 GMT
ENV COUCHDB_VERSION=3.2.1
# Fri, 07 Jan 2022 21:02:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 07 Jan 2022 21:02:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 07 Jan 2022 21:02:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 07 Jan 2022 21:02:45 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 07 Jan 2022 21:02:46 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 07 Jan 2022 21:02:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 07 Jan 2022 21:02:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 07 Jan 2022 21:02:48 GMT
VOLUME [/opt/couchdb/data]
# Fri, 07 Jan 2022 21:02:49 GMT
EXPOSE 4369 5984 9100
# Fri, 07 Jan 2022 21:02:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589f1cb358d3e3a123049341ce44cdc00d6c6484a66c1169425711e3d4e5ef61`  
		Last Modified: Tue, 21 Dec 2021 10:47:20 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ca2948856ed69aa492a4294b0510bcc03616eceac737dd2fe13ddbdad889d`  
		Last Modified: Tue, 21 Dec 2021 10:47:19 GMT  
		Size: 6.5 MB (6549891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41232c99e6d3b4632a28126c15a9405dac5ec12ef1c3e71b47f7e455ed8bef7`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 951.2 KB (951161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8413befe0746257456c09468b422890a186a8cf1a2868f008b8d56de24a7d815`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 79.9 KB (79896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad07ad1fcfb75834d9740456a30e61a390b2ccbb809791477e8a7fbe0b0dc645`  
		Last Modified: Fri, 07 Jan 2022 21:03:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd813278096e945f32723d914d08d50e2e82b3fdbe2cdd245e23ee0a7ab5aed`  
		Last Modified: Fri, 07 Jan 2022 21:03:34 GMT  
		Size: 41.7 MB (41693137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9281e76054aeaa925b24494e88c9fe127e126f173fe0275f4ed81cd9bae7d10c`  
		Last Modified: Fri, 07 Jan 2022 21:03:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773617ade8b61955b3be425a9807142b00b27a1c857a26c02fdd7e6edd6f0d02`  
		Last Modified: Fri, 07 Jan 2022 21:03:28 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34361202a634b564b220a4b67ac8147daf0a95652df68112019db1a35f2a562`  
		Last Modified: Fri, 07 Jan 2022 21:03:29 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae18d4fa0d0ec7548b0205881a7d67bf88b20d7457a505c7f0c0ec23c459e3f8`  
		Last Modified: Fri, 07 Jan 2022 21:03:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:23ed255c28c572aa36807ee921ded8cbc1e7d7f3208a8840704122b45eddcab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:70238fcfb1c45bc522fb1f938f943d067b3a0a6d853019e71d60f8e8a05fea9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80511344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eef6d738a43d45b22aa6ae64fc27db658ea22a925f10704ac9a60b7d833b48e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:09:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 02:09:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 02:09:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:09:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 02:09:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 02:09:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 20:36:30 GMT
ENV COUCHDB_VERSION=3.2.1
# Fri, 07 Jan 2022 20:36:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 07 Jan 2022 20:36:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 07 Jan 2022 20:36:46 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 07 Jan 2022 20:36:46 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 07 Jan 2022 20:36:46 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 07 Jan 2022 20:36:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 07 Jan 2022 20:36:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 07 Jan 2022 20:36:48 GMT
VOLUME [/opt/couchdb/data]
# Fri, 07 Jan 2022 20:36:48 GMT
EXPOSE 4369 5984 9100
# Fri, 07 Jan 2022 20:36:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430d6c754b31c32dd1a76de01ad3420033c05661c724b97d708362a8ec139d42`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227820103030b5232e32ba7e76de56823a61d47245d450403c0040933f6aebd`  
		Last Modified: Tue, 21 Dec 2021 02:10:58 GMT  
		Size: 6.7 MB (6691223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454611cf9dafef09164a7f64cb967a12ab5d1549d70599c56b74a2c283ae8ef1`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 1.3 MB (1258346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993063a8d6d688f066b9d8208c98f7d0dd3d78e7076cbc7a132ab98a975dece`  
		Last Modified: Tue, 21 Dec 2021 02:10:56 GMT  
		Size: 293.0 KB (293029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daab33e2a8e2b31988302eefebb4d3fb95b679e20f9cb91197d781a81491e4ef`  
		Last Modified: Fri, 07 Jan 2022 20:37:12 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6f52546ad69b1df110088c52a1840548890672ffb46a5968af7180078c9c64`  
		Last Modified: Fri, 07 Jan 2022 20:37:16 GMT  
		Size: 45.1 MB (45108011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0a0f43f3f898a1e37c16c0a848e585ccc4e4ea7fe6748550907c396fbaf28e`  
		Last Modified: Fri, 07 Jan 2022 20:37:10 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876550ef73929756b8e909730728ff16701b28f403e844bddeaf2b599958bd01`  
		Last Modified: Fri, 07 Jan 2022 20:37:10 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d422fb7671bc9b35975f370ca04370e11c4052db5242bc084dc338955a89a36`  
		Last Modified: Fri, 07 Jan 2022 20:37:09 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e62e4ddd9f34131e7208bb0c78edf3a3945da27916c1254e354c10ea3798c1`  
		Last Modified: Fri, 07 Jan 2022 20:37:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8012c438a9e3a65a8038a0487bd369245c50e69a0c4e293b2824ee0c776daf4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75204155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da31e65e3b379792dba0dd84f3eabb0fe351fd12114709eb7fff52ba545a9e8d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:44:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Dec 2021 10:44:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Dec 2021 10:44:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:44:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Dec 2021 10:44:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Dec 2021 10:45:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 21:02:23 GMT
ENV COUCHDB_VERSION=3.2.1
# Fri, 07 Jan 2022 21:02:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 07 Jan 2022 21:02:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 07 Jan 2022 21:02:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 07 Jan 2022 21:02:45 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 07 Jan 2022 21:02:46 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 07 Jan 2022 21:02:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 07 Jan 2022 21:02:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 07 Jan 2022 21:02:48 GMT
VOLUME [/opt/couchdb/data]
# Fri, 07 Jan 2022 21:02:49 GMT
EXPOSE 4369 5984 9100
# Fri, 07 Jan 2022 21:02:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589f1cb358d3e3a123049341ce44cdc00d6c6484a66c1169425711e3d4e5ef61`  
		Last Modified: Tue, 21 Dec 2021 10:47:20 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ca2948856ed69aa492a4294b0510bcc03616eceac737dd2fe13ddbdad889d`  
		Last Modified: Tue, 21 Dec 2021 10:47:19 GMT  
		Size: 6.5 MB (6549891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41232c99e6d3b4632a28126c15a9405dac5ec12ef1c3e71b47f7e455ed8bef7`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 951.2 KB (951161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8413befe0746257456c09468b422890a186a8cf1a2868f008b8d56de24a7d815`  
		Last Modified: Tue, 21 Dec 2021 10:47:18 GMT  
		Size: 79.9 KB (79896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad07ad1fcfb75834d9740456a30e61a390b2ccbb809791477e8a7fbe0b0dc645`  
		Last Modified: Fri, 07 Jan 2022 21:03:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd813278096e945f32723d914d08d50e2e82b3fdbe2cdd245e23ee0a7ab5aed`  
		Last Modified: Fri, 07 Jan 2022 21:03:34 GMT  
		Size: 41.7 MB (41693137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9281e76054aeaa925b24494e88c9fe127e126f173fe0275f4ed81cd9bae7d10c`  
		Last Modified: Fri, 07 Jan 2022 21:03:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773617ade8b61955b3be425a9807142b00b27a1c857a26c02fdd7e6edd6f0d02`  
		Last Modified: Fri, 07 Jan 2022 21:03:28 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34361202a634b564b220a4b67ac8147daf0a95652df68112019db1a35f2a562`  
		Last Modified: Fri, 07 Jan 2022 21:03:29 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae18d4fa0d0ec7548b0205881a7d67bf88b20d7457a505c7f0c0ec23c459e3f8`  
		Last Modified: Fri, 07 Jan 2022 21:03:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
