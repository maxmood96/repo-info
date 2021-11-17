## `couchdb:latest`

```console
$ docker pull couchdb@sha256:b5a62a68fbe6e37401736f5da9c9bdb47975b20c3b04816f8410bcdfd711959b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:d44ca1317fa02802757690c4006115ce59183c87c019da95c9823cecef20902a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80555231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b72edd8b1ad67c4847fa458541026d4d4960f98c26e4665faf16f241f18346`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:36:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:36:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:36:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:36:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:36:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:36:49 GMT
ENV COUCHDB_VERSION=3.2.0
# Wed, 17 Nov 2021 03:36:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:37:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:37:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:37:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:37:09 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:37:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:37:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:37:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:37:11 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:37:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa9620155d936e98f43252dadc4e586951619a4986135c8f8b2088f0c651867`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31474bb5de7990ab6e7451ab4ebe08ab585ed87effb09bf982e13e41133da5f3`  
		Last Modified: Wed, 17 Nov 2021 03:38:37 GMT  
		Size: 6.7 MB (6691326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5918906c341559cdc91df9aaccee014f9677ee7af9918df48c0f65880a6e4fbf`  
		Last Modified: Wed, 17 Nov 2021 03:38:36 GMT  
		Size: 1.3 MB (1258351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b07f325620694878eeead65f0dde169fbe2dbc20b052636e40b2345bfc0ce29`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 293.0 KB (292981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fced536466abc950895abafa11cb0321801b50d0b88972774d621dcfeebd5048`  
		Last Modified: Wed, 17 Nov 2021 03:38:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7372d4c41a2b14f6c1f5a562ceaa27cf9df18aad065b51a7f924eb88b0639c4`  
		Last Modified: Wed, 17 Nov 2021 03:38:39 GMT  
		Size: 45.2 MB (45151883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbcf15db1a866454cfee77ce904e73f33156d24384d99aba1fcd8fe91736381`  
		Last Modified: Wed, 17 Nov 2021 03:38:33 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37394932887976e4d6098fffa582e2312d7a6066d8d27e2179d0611e37663cb0`  
		Last Modified: Wed, 17 Nov 2021 03:38:32 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3a1135068494686c93ce341d735e8d498ec132b550f0b709dbb1abb9f4bde5`  
		Last Modified: Wed, 17 Nov 2021 03:38:32 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cd74753ae8a80e23a9433a800a678704eca6d66c3939bd6d0f98c9a1547e75`  
		Last Modified: Wed, 17 Nov 2021 03:38:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f2030d9ddbcb3ed7120aeeebdc4b089b0d969ad833a1a792297c0797c08bf33d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75231135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f19af1927bdddc0bceb963c64ece13b6daa206f047105a8a225966ffa901bcb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:58 GMT
ENV COUCHDB_VERSION=3.2.0
# Wed, 17 Nov 2021 03:12:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:13:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:13:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:13:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:13:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:13:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:13:23 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:13:24 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:13:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f10d6d3037836c6c8aa5c296f0f70e385564599dbbafe34639ded032c0e9c6`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95555d888dc786cead48d13eadcb9e9fc7e69b2ad36a9b2bd3ee118469e0dd7c`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 41.7 MB (41720155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922085445cffcaed101abaf1c2aed29901463589f4ca49f7be8dac5d197e12f`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0e02dae87f84ebee883fd339617c2324b116a2439ae1a225d22ce5dce53b11`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78060cecbefc0e301d5732233088293e426decdfb208b0e80307ba8c2ad95355`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9c11ef87ada6fcbf0f410909cc4aa6f1d28ed15ac59d1787f5624afdfb073e`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
