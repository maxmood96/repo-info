## `couchdb:latest`

```console
$ docker pull couchdb@sha256:fce5d02e200e3a96030084a057b4430f9f946cefb7df9abca3a1120153b5e265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:227198eb13b4d8e48ab02a69862ac03b68e44b2e879441399c96c3e130ed8cac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90240323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d827434098752cb94ff077a95fef98532ff66a71643aa133e760eeeda419ecb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:53:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 00:53:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 00:54:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 00:54:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 00:54:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:54:08 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 00:54:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 00:54:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 00:54:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 00:54:22 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 00:54:22 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 00:54:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 00:54:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 00:54:23 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 00:54:23 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 00:54:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c404450a25c52aaf36ad6cf2df7bf83eb65d98bca7cb78649b4a22fbe62aba`  
		Last Modified: Fri, 28 Jul 2023 00:56:02 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e16992934da47a606ee48c95eebfce4c426068c7b046352ca614ce1161a10`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 5.2 MB (5224480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4e80f87d5f0ac56fd4616490a14b6299e1b71054316e29e79922dabfe4cc77`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 610.3 KB (610275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcb668df53bd84b62cfbd8b5ca4fa69e26041fdd9a7e919993f81fa1de5dfaf`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 294.4 KB (294410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519c2591a1a074436d27db4d303d302c79f5317fa1873cbdbf6a711863c6ef2c`  
		Last Modified: Fri, 28 Jul 2023 00:56:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc7cbd8bea6ee19dbafe441e0b78a2a7fe1c01a4e83f2d8518c09fcb2a4b57a`  
		Last Modified: Fri, 28 Jul 2023 00:56:03 GMT  
		Size: 52.7 MB (52686137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fe90e4dff94e302b5f98efe1337955d9a56d04f64eaa8cd4642552a30dbeca`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0572f1b6b33e5a9a305c54b7ac1ba36188faa7a53e3461c213bfa0f17eb9b4`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520ff0c4c1c630b2c9838ee8eb05a11d541dfe16c5ac442c1db62fd8cb592fd2`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c53a8228db1b37a14d63d5945d500959e69ab4832bfbe9d335a1bd314cb69`  
		Last Modified: Fri, 28 Jul 2023 00:55:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2e70f5d37f5cc7cf4b3650aa83698c05e29e4328b28742c4d62d23f3fb1b6f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88684803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56332a507d98c5fa88cbd5c18427e6a0800e1a7abf254ed11626b02b9fa166d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:54:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 01:54:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 01:54:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 01:54:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 01:54:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:50 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 01:54:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 01:55:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 01:55:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 01:55:02 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 01:55:02 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 01:55:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 01:55:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:55:03 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 01:55:03 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 01:55:03 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7f9b366f53bc414354cc8f76b4a69b8a893a5ec10d1eb92df285ea58245e46`  
		Last Modified: Fri, 28 Jul 2023 01:56:25 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219ecbff31414f0f2ad54c2cd4518b665c19f0e00070963eae158f618fd8939d`  
		Last Modified: Fri, 28 Jul 2023 01:56:24 GMT  
		Size: 5.2 MB (5209548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4404fb20af6a73b94f81a1c25c6830a3e0e0c11d7e67eee7c83959875945ecd`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 566.3 KB (566291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40659943f33c45b039960055ee53cff41e91c4d354ea2dcf5b0b9577e4a40450`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 294.3 KB (294296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6da584c0e08eb2f1723a97553ba41ebafabd4cc802967fb1ffec13223613dd`  
		Last Modified: Fri, 28 Jul 2023 01:56:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905bdb07374a015ef787de5082afc33403aa603166b94703f7230771d5291fa2`  
		Last Modified: Fri, 28 Jul 2023 01:56:26 GMT  
		Size: 52.5 MB (52544396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b47c179c832b7798be1c9b78f682f0796fc80c9c1fe3d1fd0bd4e133f3d0584`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae080c493858f5df5a92c38f7672c9a8e1043e8d36e871e541df543232646818`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98abec4e2dd5439587c3a84207dd9b94e400f9c2a210935144cfa25de112a60`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448423c6a5375ebc98e39645b49903543b6de8d6c1df8146f7129c837b2125a5`  
		Last Modified: Fri, 28 Jul 2023 01:56:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:195e387b9e77db7faf72f3138d8e494d67869deb38acb0d1dc5deae048f10c22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b1b56534f75b9f1bbfbf2b5af66f6aed83154e252a6a25a6b6178032fa36f5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:23:41 GMT
ADD file:bc63550bad6e6b1e46c01c4911ac409a0a01e632b56a9a846fa2d7c86d8bb292 in / 
# Thu, 27 Jul 2023 23:23:43 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:44:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 03:44:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 03:44:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:44:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 03:44:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 03:45:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:45:08 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 03:45:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 03:45:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 03:45:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 03:45:45 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 03:45:45 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 03:45:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 03:45:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 03:45:47 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 03:45:48 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 03:45:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:90fff1cd317dd6511bdf25cbc4f6797ea09a5bc0657b6e1d88772d885bed1da0`  
		Last Modified: Thu, 27 Jul 2023 23:30:33 GMT  
		Size: 35.3 MB (35291031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89881e295647078d9c302e443081459979a2cd3b1161a78a449001074720911`  
		Last Modified: Fri, 28 Jul 2023 03:46:39 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44e1763c279db8dfa52f1640c68fa14adfa41f5a055addc6f0a7b9959585354`  
		Last Modified: Fri, 28 Jul 2023 03:46:38 GMT  
		Size: 6.0 MB (6044154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b95b80c92cb8cda5a88e018d853eff3eb94b9df3651a91fe4238fb4cf0dc0ef`  
		Last Modified: Fri, 28 Jul 2023 03:46:37 GMT  
		Size: 662.2 KB (662169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a478ddd7fcbd6eff286a6cc7dfe93f5ee5d3de16ccfc19e827e0b4fd82249e0b`  
		Last Modified: Fri, 28 Jul 2023 03:46:36 GMT  
		Size: 294.4 KB (294375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93724178719de15b26283a933ff2f41443ff52b2b11b6191b5b484501ad51c9b`  
		Last Modified: Fri, 28 Jul 2023 03:46:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eeb8574d1906c43163ebcd0459cf5a3d8298a7a9fec7d2a16f9e6cc052b121`  
		Last Modified: Fri, 28 Jul 2023 03:46:44 GMT  
		Size: 53.7 MB (53663059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b1aa1f11ad7febca6e0e6a1d29121fbba6dd3a4abbe795f1d7184015e0caae`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3094563d60c9c847de9ae3119c4afc8edd6877d73a4308b4dc314eed18e4e`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76163dedbf2715457e9f61f4d785a3ad85110c6911e164bea2196d513e05835`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b593398a60565eddef5653aa64a341cc80bcd14d839d4ae79cb54818f3c6ae6`  
		Last Modified: Fri, 28 Jul 2023 03:46:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:b4436cfee6fb1f617f62f435cf8f8928ef5ff65a17f8d250d113fcad60db722b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86992654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0462abac2949145f42dbd36149a362a2799a53b4ce92e5bcd092207ead848744`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:42 GMT
ADD file:af0651fb20da5a08d22c074a04a2d96d68d66b5be86a11d348364e151de46196 in / 
# Thu, 27 Jul 2023 23:47:44 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:05:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 28 Jul 2023 02:05:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 28 Jul 2023 02:05:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:05:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Fri, 28 Jul 2023 02:05:19 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 28 Jul 2023 02:05:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:05:24 GMT
ENV COUCHDB_VERSION=3.3.2
# Fri, 28 Jul 2023 02:05:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 28 Jul 2023 02:05:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 28 Jul 2023 02:05:40 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 28 Jul 2023 02:05:40 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Fri, 28 Jul 2023 02:05:40 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Fri, 28 Jul 2023 02:05:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 02:05:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:05:41 GMT
VOLUME [/opt/couchdb/data]
# Fri, 28 Jul 2023 02:05:41 GMT
EXPOSE 4369 5984 9100
# Fri, 28 Jul 2023 02:05:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:010ebc9d3534dabb784b6e93117170f0f20f698913991111a4ea549e5d951b7b`  
		Last Modified: Thu, 27 Jul 2023 23:52:47 GMT  
		Size: 29.7 MB (29652882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebe9433e686daf506ce0412a2e870f9375f2b4a9adebc1124bdac2c94e40b84`  
		Last Modified: Fri, 28 Jul 2023 02:06:00 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b1f4c5fb7051b121d29432853340993dacd3820b783719cec985e575a5b097`  
		Last Modified: Fri, 28 Jul 2023 02:06:00 GMT  
		Size: 5.1 MB (5110361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09ff47afedc1f64df9b0457edfb716da23b39d1d0635ed9b9c2827c8fcc80fb`  
		Last Modified: Fri, 28 Jul 2023 02:05:59 GMT  
		Size: 573.0 KB (573002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882364bf72cf29abbd9eea99f4deab7dc5d006774b680cd8cf7c873004c5c7f1`  
		Last Modified: Fri, 28 Jul 2023 02:05:59 GMT  
		Size: 294.3 KB (294349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0c556952b0caa59dbb74cd9caaee7c9b2a41bc40e89d6ac7711314b0b6c7ed`  
		Last Modified: Fri, 28 Jul 2023 02:05:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5478d623f0f5fdf2104ed41f8b821dbcb1faa8d511b9aca76081d7794ad5b2a`  
		Last Modified: Fri, 28 Jul 2023 02:06:03 GMT  
		Size: 51.4 MB (51354617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cefca2110efbbc66b98c4c51fad325440374d2c837d943c357e6e668bb4ddfb`  
		Last Modified: Fri, 28 Jul 2023 02:05:58 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad59591fc8983f5880fe5317ee964acbdf74c5b5aedf0c28e796eec6644265fd`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 997.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb0d9378e1540623419ca5aa93a86c26104ca658ae6b5ceb3c40977e448a174`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44cb5db485ad317f73a25062fc2d6509149caeb60585c2cd08daf9af133bf5f`  
		Last Modified: Fri, 28 Jul 2023 02:05:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
