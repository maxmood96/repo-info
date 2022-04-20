## `couchdb:latest`

```console
$ docker pull couchdb@sha256:ed6f005a05230539aa3300f178b7ac10bbc120c6bd50edfba438249aa2a6860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:2c96232290fe0414177909bdb8c30224af32c2f8f7031d868fb832ffaac6cc4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87451684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53c5467cf3ac9c9d94c8922a210bc132fa625e0059a48054a22a992881b1a8f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 07:10:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Apr 2022 07:10:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Apr 2022 07:10:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:10:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 20 Apr 2022 07:10:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Apr 2022 07:10:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:10:47 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 20 Apr 2022 07:10:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Apr 2022 07:11:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Apr 2022 07:11:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Apr 2022 07:11:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 20 Apr 2022 07:11:01 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 20 Apr 2022 07:11:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 07:11:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Apr 2022 07:11:01 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Apr 2022 07:11:02 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Apr 2022 07:11:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e4fb628d536f433a0a908e8e65812c407b41d7039fa72adc77277f091a8924`  
		Last Modified: Wed, 20 Apr 2022 07:12:30 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5ada74819f3e5a933ad7776886fd3b202f99653d68b746f8e1ca6bf158db5a`  
		Last Modified: Wed, 20 Apr 2022 07:12:29 GMT  
		Size: 5.2 MB (5223690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7d8f1aed9465ca9c4007a6277de02a53c60b7f77c8a0a6dca2a0fe064afa93`  
		Last Modified: Wed, 20 Apr 2022 07:12:29 GMT  
		Size: 1.6 MB (1553283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464d6b8b4bbbc83281231e89eac3d0d5d2142d261de2db10cc7f65167b545c77`  
		Last Modified: Wed, 20 Apr 2022 07:12:28 GMT  
		Size: 295.6 KB (295569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b71906ef4252c8d9093a53eaeae741462aed454881113137d2c5539a5b39cca`  
		Last Modified: Wed, 20 Apr 2022 07:12:28 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43f2ebb365be093fc6c10de52167a7915582ca0d80a1594fe31f74d652ec583`  
		Last Modified: Wed, 20 Apr 2022 07:12:32 GMT  
		Size: 49.0 MB (48993027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09b9610f19e31700a17b805c579fed67585d29389cd706ac975e38fe16967c3`  
		Last Modified: Wed, 20 Apr 2022 07:12:26 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad96a982041d41e0a94650bcac88201e50a18622c16b84db337c84799cbaadf2`  
		Last Modified: Wed, 20 Apr 2022 07:12:26 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9590c0cb12e900d1d82e53daf2bb099c6230b830cc3f3b72fd4455e2ff598306`  
		Last Modified: Wed, 20 Apr 2022 07:12:26 GMT  
		Size: 2.2 KB (2179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a01aac1048bee36c25c3b24ae92a24faf3c8418d592dbd209938398b439036`  
		Last Modified: Wed, 20 Apr 2022 07:12:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b1ce2bd46ec5ea9656d89ee31fb5ddb80f5bbb18c24b38536eab91423bd75654
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85383029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dd9a06ea5af54ebc9afe1b239f350e954ae38e39e75097dcbfba5ce977eb21`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:10 GMT
ADD file:84523b5820128293b713ef35d8db618921162250da1e4c72bf9923f34ad7d87d in / 
# Wed, 20 Apr 2022 04:29:11 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 07:02:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Apr 2022 07:02:48 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Apr 2022 07:02:55 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:02:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 20 Apr 2022 07:03:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Apr 2022 07:03:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:03:07 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 20 Apr 2022 07:03:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Apr 2022 07:03:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Apr 2022 07:03:27 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Apr 2022 07:03:28 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 20 Apr 2022 07:03:29 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 20 Apr 2022 07:03:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 07:03:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Apr 2022 07:03:31 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Apr 2022 07:03:32 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Apr 2022 07:03:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d4a449ac69c579312443ded09f57c4894e7adb42f7406abd364f95982fafc59`  
		Last Modified: Wed, 20 Apr 2022 04:35:49 GMT  
		Size: 30.1 MB (30065801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51cefb89564694ca915e167c405ee5881088311379fb87639609d213f6bb420`  
		Last Modified: Wed, 20 Apr 2022 07:05:36 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ec39efab772ade8e91f1021e60940ff0365826df140afe1f51e150ceb0303b`  
		Last Modified: Wed, 20 Apr 2022 07:05:35 GMT  
		Size: 5.0 MB (5002920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b4d5c3bee5b8e99b3e70d3a88123a53caf0860986a9eb6e68d6c4ed7022533`  
		Last Modified: Wed, 20 Apr 2022 07:05:34 GMT  
		Size: 1.2 MB (1221077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6fb8160cb2a1f0d19dd386151a86a62c1e568354e1aac1a650c0d9fde62de7`  
		Last Modified: Wed, 20 Apr 2022 07:05:34 GMT  
		Size: 79.2 KB (79168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b99c7181f5a3992355deabe6e521d071029050e68f777a730b24dba5cf3a949`  
		Last Modified: Wed, 20 Apr 2022 07:05:34 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd1b9b51ff525d46c102aafe33ec2631c99218677d1fb9505db73af88f22380`  
		Last Modified: Wed, 20 Apr 2022 07:05:37 GMT  
		Size: 49.0 MB (49007026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf44f240a74efe39263490f22dbad69cb71869ee20eeeca196dc544cadaa1e26`  
		Last Modified: Wed, 20 Apr 2022 07:05:31 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfe021f0efc89117bdd8aaf84ff80a530d7366daf172e2ce3aabb5b7d4c9ea7`  
		Last Modified: Wed, 20 Apr 2022 07:05:32 GMT  
		Size: 761.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03dfc4e590017fbe73692daf143f06beda0a5c608db21e54a1f335fe8a112c4`  
		Last Modified: Wed, 20 Apr 2022 07:05:31 GMT  
		Size: 2.2 KB (2182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726df3f6f358317ff48ad598cd6294cc97db9360f05674ad2b3251d7ec7c9cd4`  
		Last Modified: Wed, 20 Apr 2022 07:05:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:a0ec772898e7b98ab726da9bbf9e2a8067686b33407d545eb345b3cce3afc553
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93167466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958978428a8edc826010f4eb4f833438a7e7c7417d4228fa95f577ed5102c636`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:08 GMT
ADD file:e7ae113c10f322a9cffc46b62ba12820e270caaadaee3c5b907c801a37e1632c in / 
# Tue, 29 Mar 2022 00:22:11 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 10:49:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 30 Mar 2022 10:49:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 30 Mar 2022 10:50:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 10:50:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 30 Mar 2022 10:50:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 30 Mar 2022 10:51:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 10:51:11 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 30 Mar 2022 10:51:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 30 Mar 2022 10:51:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 30 Mar 2022 10:51:57 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 30 Mar 2022 10:51:58 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 30 Mar 2022 10:52:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 30 Mar 2022 10:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 30 Mar 2022 10:52:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 10:52:13 GMT
VOLUME [/opt/couchdb/data]
# Wed, 30 Mar 2022 10:52:17 GMT
EXPOSE 4369 5984 9100
# Wed, 30 Mar 2022 10:52:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ecc74bb8af5a048e1123af0e17d88ef3da1d10951ada79e8e1cc9c0a694245d3`  
		Last Modified: Tue, 29 Mar 2022 00:32:57 GMT  
		Size: 35.3 MB (35282506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e95f94117dc731d116e8d312bc23f0c7c790e38bd6ab7f727ec457b553c993`  
		Last Modified: Wed, 30 Mar 2022 10:52:49 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f5e8f5cbad19275da76f517a0a7ef0ec7f0e54ad76035a18c00fd4a37134c`  
		Last Modified: Wed, 30 Mar 2022 10:52:47 GMT  
		Size: 6.0 MB (6043641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a0779c52e66bf4a49e1fe70a0882b6f3d14d1416145a03b89332f18baabc8e`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 1.5 MB (1509286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05bee7e95e7677193b00f56a750d6362cc0f2076daac532b0f932b19bf1518e`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 295.6 KB (295648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54285c6aef4afa86d38a12cd2da3259c66f04a426ce7565f44407391e624a12a`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb57879a9c4ffc05dabe1871b51ede9836db31b04ede125d89443e49e5cda0c9`  
		Last Modified: Wed, 30 Mar 2022 10:52:48 GMT  
		Size: 50.0 MB (50029239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6cd7b2f21c43f6964cca89efbc25e47a664495439380cfa6893fa22f55de93`  
		Last Modified: Wed, 30 Mar 2022 10:52:40 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5d472bb6e5961d60b48ba0d00a55475445b0ac511e884daa55db57a536e99a`  
		Last Modified: Wed, 30 Mar 2022 10:52:40 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a27af1791dc6b357b1d5c107f38d595649b0820b031f8771c16e48d54382a3`  
		Last Modified: Wed, 30 Mar 2022 10:52:41 GMT  
		Size: 2.2 KB (2189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e2c1d4e6f6c55894d6e3ce5ff51e6555cd0b856ade14a766c4b7bb7e4f8277`  
		Last Modified: Wed, 30 Mar 2022 10:52:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
