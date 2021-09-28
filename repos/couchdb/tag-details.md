<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.1`](#couchdb311)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:59603b138140739a86ab2a45bea1e9958b709baf0e0f000906b18b753291bbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:20afaa26929c6fdf5509380b64cba3a6a030fc29c2e1f9694de1f7da5140595c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84509525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcd2be3330041b630b943aa363c5c0989233d5d69b1b822ece6d94612c3bee6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:07:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:07:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:07:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:07:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:07:47 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:07:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:08:17 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 28 Sep 2021 02:08:18 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:08:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:08:38 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:08:38 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:08:38 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 28 Sep 2021 02:08:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:08:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:08:39 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:08:39 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:08:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf6d2572e5cb46cd161abd1cad4bfe814861bb79af678e8c8878bfceea39800`  
		Last Modified: Tue, 28 Sep 2021 02:08:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c07788136736f89aa055ecaf94d8a84930476f22f9743523ea520a89676871`  
		Last Modified: Tue, 28 Sep 2021 02:08:57 GMT  
		Size: 6.7 MB (6691239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f38611f22a1bf97d622c97f121883635774e7c90a58b732ea6ac173481ed5f`  
		Last Modified: Tue, 28 Sep 2021 02:08:56 GMT  
		Size: 1.3 MB (1258340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7085d2ce04f2475efd91088b35d5999a9d08265c4b69ff48f3756f569dfc0`  
		Last Modified: Tue, 28 Sep 2021 02:08:56 GMT  
		Size: 293.0 KB (292984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cc649cd37b33d7f88267ea570d4ad24fb391def7dfa7953b5bd0fa250c270`  
		Last Modified: Tue, 28 Sep 2021 02:09:19 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64852f62a00eab073f23b3ae7d3cd18437e01410f7f9b62789193af7b14500fc`  
		Last Modified: Tue, 28 Sep 2021 02:09:22 GMT  
		Size: 49.1 MB (49113955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca02031105a2b78eec9e6333a8829db9480c9c54512ae3f2cec01b878401fd95`  
		Last Modified: Tue, 28 Sep 2021 02:09:15 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea605e13122135a2130e78baf3b4143e079c2c939e2a624a0e54ad590ab32c2`  
		Last Modified: Tue, 28 Sep 2021 02:09:15 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a644d96aa8f47918c7efe71c17e1a1883f2d008353e8b99b69e0d02ceeb54d5`  
		Last Modified: Tue, 28 Sep 2021 02:09:15 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe5cc1d9bb2c971a6309e7e4957e73e122bb638d5764c4299907320a0fab580`  
		Last Modified: Tue, 28 Sep 2021 02:09:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9dd9ffe56508bd6f0789584e3eefb1b06119a07b47908cb290419df8fd3ebbc3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72941767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b087a7767afc8a39e4e3196e4074b4795563e2b29fd05915d53057b68b649725`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:14:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 28 Sep 2021 02:14:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:14:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:14:17 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:14:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:14:18 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 28 Sep 2021 02:14:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:14:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:14:19 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:14:19 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:14:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e28e896b4ae04dbf8ef8ce85c5ca01b73a5da373c5ee4f330a3cc82752bd72`  
		Last Modified: Tue, 28 Sep 2021 02:15:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5f60f5bc43bec3cc68bb513b4fd76f28f8ed5a701bcea76de1e786331fab6d`  
		Last Modified: Tue, 28 Sep 2021 02:15:14 GMT  
		Size: 39.0 MB (39012565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5ecee5454b78e9edd7e565df2f104c1955ceae4ceab9b1a5725b3ae0bd80e`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c950fa2453ec470f652eec7abd5358f5ed9c06fa300dcb51fcdf945d29eac7a`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d10b6a90ff4a25500f82ffec4a5930bb8e14fdc6950c717b11b4f18e2ec66`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adcf5258254be8c5a9897cbeb5e02b334ac4751faa9d033ef2d522c3b45e6e4`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:59603b138140739a86ab2a45bea1e9958b709baf0e0f000906b18b753291bbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:20afaa26929c6fdf5509380b64cba3a6a030fc29c2e1f9694de1f7da5140595c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84509525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcd2be3330041b630b943aa363c5c0989233d5d69b1b822ece6d94612c3bee6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:07:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:07:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:07:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:07:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:07:47 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:07:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:08:17 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 28 Sep 2021 02:08:18 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:08:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:08:38 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:08:38 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:08:38 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 28 Sep 2021 02:08:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:08:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:08:39 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:08:39 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:08:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf6d2572e5cb46cd161abd1cad4bfe814861bb79af678e8c8878bfceea39800`  
		Last Modified: Tue, 28 Sep 2021 02:08:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c07788136736f89aa055ecaf94d8a84930476f22f9743523ea520a89676871`  
		Last Modified: Tue, 28 Sep 2021 02:08:57 GMT  
		Size: 6.7 MB (6691239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f38611f22a1bf97d622c97f121883635774e7c90a58b732ea6ac173481ed5f`  
		Last Modified: Tue, 28 Sep 2021 02:08:56 GMT  
		Size: 1.3 MB (1258340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7085d2ce04f2475efd91088b35d5999a9d08265c4b69ff48f3756f569dfc0`  
		Last Modified: Tue, 28 Sep 2021 02:08:56 GMT  
		Size: 293.0 KB (292984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cc649cd37b33d7f88267ea570d4ad24fb391def7dfa7953b5bd0fa250c270`  
		Last Modified: Tue, 28 Sep 2021 02:09:19 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64852f62a00eab073f23b3ae7d3cd18437e01410f7f9b62789193af7b14500fc`  
		Last Modified: Tue, 28 Sep 2021 02:09:22 GMT  
		Size: 49.1 MB (49113955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca02031105a2b78eec9e6333a8829db9480c9c54512ae3f2cec01b878401fd95`  
		Last Modified: Tue, 28 Sep 2021 02:09:15 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea605e13122135a2130e78baf3b4143e079c2c939e2a624a0e54ad590ab32c2`  
		Last Modified: Tue, 28 Sep 2021 02:09:15 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a644d96aa8f47918c7efe71c17e1a1883f2d008353e8b99b69e0d02ceeb54d5`  
		Last Modified: Tue, 28 Sep 2021 02:09:15 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe5cc1d9bb2c971a6309e7e4957e73e122bb638d5764c4299907320a0fab580`  
		Last Modified: Tue, 28 Sep 2021 02:09:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9dd9ffe56508bd6f0789584e3eefb1b06119a07b47908cb290419df8fd3ebbc3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72941767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b087a7767afc8a39e4e3196e4074b4795563e2b29fd05915d53057b68b649725`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:14:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 28 Sep 2021 02:14:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:14:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:14:17 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:14:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:14:18 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 28 Sep 2021 02:14:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:14:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:14:19 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:14:19 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:14:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e28e896b4ae04dbf8ef8ce85c5ca01b73a5da373c5ee4f330a3cc82752bd72`  
		Last Modified: Tue, 28 Sep 2021 02:15:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5f60f5bc43bec3cc68bb513b4fd76f28f8ed5a701bcea76de1e786331fab6d`  
		Last Modified: Tue, 28 Sep 2021 02:15:14 GMT  
		Size: 39.0 MB (39012565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5ecee5454b78e9edd7e565df2f104c1955ceae4ceab9b1a5725b3ae0bd80e`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c950fa2453ec470f652eec7abd5358f5ed9c06fa300dcb51fcdf945d29eac7a`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d10b6a90ff4a25500f82ffec4a5930bb8e14fdc6950c717b11b4f18e2ec66`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adcf5258254be8c5a9897cbeb5e02b334ac4751faa9d033ef2d522c3b45e6e4`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:59603b138140739a86ab2a45bea1e9958b709baf0e0f000906b18b753291bbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:20afaa26929c6fdf5509380b64cba3a6a030fc29c2e1f9694de1f7da5140595c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84509525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcd2be3330041b630b943aa363c5c0989233d5d69b1b822ece6d94612c3bee6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:07:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:07:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:07:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:07:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:07:47 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:07:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:08:17 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 28 Sep 2021 02:08:18 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:08:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:08:38 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:08:38 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:08:38 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 28 Sep 2021 02:08:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:08:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:08:39 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:08:39 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:08:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf6d2572e5cb46cd161abd1cad4bfe814861bb79af678e8c8878bfceea39800`  
		Last Modified: Tue, 28 Sep 2021 02:08:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c07788136736f89aa055ecaf94d8a84930476f22f9743523ea520a89676871`  
		Last Modified: Tue, 28 Sep 2021 02:08:57 GMT  
		Size: 6.7 MB (6691239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f38611f22a1bf97d622c97f121883635774e7c90a58b732ea6ac173481ed5f`  
		Last Modified: Tue, 28 Sep 2021 02:08:56 GMT  
		Size: 1.3 MB (1258340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7085d2ce04f2475efd91088b35d5999a9d08265c4b69ff48f3756f569dfc0`  
		Last Modified: Tue, 28 Sep 2021 02:08:56 GMT  
		Size: 293.0 KB (292984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cc649cd37b33d7f88267ea570d4ad24fb391def7dfa7953b5bd0fa250c270`  
		Last Modified: Tue, 28 Sep 2021 02:09:19 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64852f62a00eab073f23b3ae7d3cd18437e01410f7f9b62789193af7b14500fc`  
		Last Modified: Tue, 28 Sep 2021 02:09:22 GMT  
		Size: 49.1 MB (49113955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca02031105a2b78eec9e6333a8829db9480c9c54512ae3f2cec01b878401fd95`  
		Last Modified: Tue, 28 Sep 2021 02:09:15 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea605e13122135a2130e78baf3b4143e079c2c939e2a624a0e54ad590ab32c2`  
		Last Modified: Tue, 28 Sep 2021 02:09:15 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a644d96aa8f47918c7efe71c17e1a1883f2d008353e8b99b69e0d02ceeb54d5`  
		Last Modified: Tue, 28 Sep 2021 02:09:15 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe5cc1d9bb2c971a6309e7e4957e73e122bb638d5764c4299907320a0fab580`  
		Last Modified: Tue, 28 Sep 2021 02:09:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9dd9ffe56508bd6f0789584e3eefb1b06119a07b47908cb290419df8fd3ebbc3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72941767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b087a7767afc8a39e4e3196e4074b4795563e2b29fd05915d53057b68b649725`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:14:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 28 Sep 2021 02:14:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:14:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:14:17 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:14:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:14:18 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 28 Sep 2021 02:14:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:14:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:14:19 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:14:19 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:14:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e28e896b4ae04dbf8ef8ce85c5ca01b73a5da373c5ee4f330a3cc82752bd72`  
		Last Modified: Tue, 28 Sep 2021 02:15:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5f60f5bc43bec3cc68bb513b4fd76f28f8ed5a701bcea76de1e786331fab6d`  
		Last Modified: Tue, 28 Sep 2021 02:15:14 GMT  
		Size: 39.0 MB (39012565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5ecee5454b78e9edd7e565df2f104c1955ceae4ceab9b1a5725b3ae0bd80e`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c950fa2453ec470f652eec7abd5358f5ed9c06fa300dcb51fcdf945d29eac7a`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d10b6a90ff4a25500f82ffec4a5930bb8e14fdc6950c717b11b4f18e2ec66`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adcf5258254be8c5a9897cbeb5e02b334ac4751faa9d033ef2d522c3b45e6e4`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:b422509b1648306dee1038f41756a982aefa17f986fa8ba18f6cd80e433dafdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:ca88e0f690f425cdd99b368073320f197317bed549d5560e0bdcf7877ff2918c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83772106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81efb6c8280c889d695b176c5f6597fec9b540fdb2974f9be5c3d654602d9ab`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:07:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:07:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:07:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:07:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:07:47 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:07:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:07:54 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 28 Sep 2021 02:07:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:08:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:08:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:08:11 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:08:11 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 28 Sep 2021 02:08:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:08:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:08:13 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:08:13 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:08:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf6d2572e5cb46cd161abd1cad4bfe814861bb79af678e8c8878bfceea39800`  
		Last Modified: Tue, 28 Sep 2021 02:08:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c07788136736f89aa055ecaf94d8a84930476f22f9743523ea520a89676871`  
		Last Modified: Tue, 28 Sep 2021 02:08:57 GMT  
		Size: 6.7 MB (6691239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f38611f22a1bf97d622c97f121883635774e7c90a58b732ea6ac173481ed5f`  
		Last Modified: Tue, 28 Sep 2021 02:08:56 GMT  
		Size: 1.3 MB (1258340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7085d2ce04f2475efd91088b35d5999a9d08265c4b69ff48f3756f569dfc0`  
		Last Modified: Tue, 28 Sep 2021 02:08:56 GMT  
		Size: 293.0 KB (292984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8884e223396a1ed82ed7286b9c3df03ac5b9869aa724a925872ef5d7096000b9`  
		Last Modified: Tue, 28 Sep 2021 02:08:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2be17aa7a1974f8ec1d74c76d8e5c7d56b50bdbf6f797a3da0a6020ce7e81cd`  
		Last Modified: Tue, 28 Sep 2021 02:08:59 GMT  
		Size: 48.4 MB (48376535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356eb1ff43b1918f0002995eef23ceb57e972579cbd8cc01fefda2e6a2260380`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6960ebdd0a7eba7433b2074bb47df88c68ebd6c9d542e4eaa1c72b0733ddc8ab`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92df28681e5b2d10bdc5b17b014ad2f3d54dde0b5ba5886ee1487995f2b6e8e`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130bc089b183384af5d0d23577af6520bff51727aee476f02354710dee1b7b64`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c8203604e2555cdaa201d2f33fddc1b684533ab522103424169d7667af043dc8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78787285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f398aff04cfa1c345800a93c3ae01142d9a0cb1793b4e9a1cb39d776982ba4c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:39 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 28 Sep 2021 02:13:39 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:13:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:13:53 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:13:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:13:53 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 28 Sep 2021 02:13:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:13:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:13:54 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:13:54 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:13:55 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a567769b3d8168bb1b7fac501b3e15fb35e1e1a40b34a9258451876bf3b6ab9`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3b66a31e4294cd1da1d2a4a2d5914ca6ca6a7cef5ede944bddf8c85384041`  
		Last Modified: Tue, 28 Sep 2021 02:14:50 GMT  
		Size: 44.9 MB (44858084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095af1ccc0a9a0ae3e3a3f231f0f10bb20156e466b86a896ee7ef7ce823c362`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc66bb6b6f96d475e20cd3f5757b00e0391b8011b7a1cab27d9b083c3908514`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124f915d2307e6140d7fb5a5ea7d8be8903a6f27e1e33d1206638b3c04e8ad0e`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918f15c61365133b7c84bcd91e0b4232407a200db0010a427afbe5684d259ad7`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:b422509b1648306dee1038f41756a982aefa17f986fa8ba18f6cd80e433dafdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:ca88e0f690f425cdd99b368073320f197317bed549d5560e0bdcf7877ff2918c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83772106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81efb6c8280c889d695b176c5f6597fec9b540fdb2974f9be5c3d654602d9ab`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:07:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:07:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:07:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:07:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:07:47 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:07:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:07:54 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 28 Sep 2021 02:07:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:08:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:08:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:08:11 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:08:11 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 28 Sep 2021 02:08:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:08:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:08:13 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:08:13 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:08:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf6d2572e5cb46cd161abd1cad4bfe814861bb79af678e8c8878bfceea39800`  
		Last Modified: Tue, 28 Sep 2021 02:08:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c07788136736f89aa055ecaf94d8a84930476f22f9743523ea520a89676871`  
		Last Modified: Tue, 28 Sep 2021 02:08:57 GMT  
		Size: 6.7 MB (6691239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f38611f22a1bf97d622c97f121883635774e7c90a58b732ea6ac173481ed5f`  
		Last Modified: Tue, 28 Sep 2021 02:08:56 GMT  
		Size: 1.3 MB (1258340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7085d2ce04f2475efd91088b35d5999a9d08265c4b69ff48f3756f569dfc0`  
		Last Modified: Tue, 28 Sep 2021 02:08:56 GMT  
		Size: 293.0 KB (292984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8884e223396a1ed82ed7286b9c3df03ac5b9869aa724a925872ef5d7096000b9`  
		Last Modified: Tue, 28 Sep 2021 02:08:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2be17aa7a1974f8ec1d74c76d8e5c7d56b50bdbf6f797a3da0a6020ce7e81cd`  
		Last Modified: Tue, 28 Sep 2021 02:08:59 GMT  
		Size: 48.4 MB (48376535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356eb1ff43b1918f0002995eef23ceb57e972579cbd8cc01fefda2e6a2260380`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6960ebdd0a7eba7433b2074bb47df88c68ebd6c9d542e4eaa1c72b0733ddc8ab`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92df28681e5b2d10bdc5b17b014ad2f3d54dde0b5ba5886ee1487995f2b6e8e`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130bc089b183384af5d0d23577af6520bff51727aee476f02354710dee1b7b64`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c8203604e2555cdaa201d2f33fddc1b684533ab522103424169d7667af043dc8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78787285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f398aff04cfa1c345800a93c3ae01142d9a0cb1793b4e9a1cb39d776982ba4c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:39 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 28 Sep 2021 02:13:39 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:13:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:13:53 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:13:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:13:53 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 28 Sep 2021 02:13:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:13:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:13:54 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:13:54 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:13:55 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a567769b3d8168bb1b7fac501b3e15fb35e1e1a40b34a9258451876bf3b6ab9`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3b66a31e4294cd1da1d2a4a2d5914ca6ca6a7cef5ede944bddf8c85384041`  
		Last Modified: Tue, 28 Sep 2021 02:14:50 GMT  
		Size: 44.9 MB (44858084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095af1ccc0a9a0ae3e3a3f231f0f10bb20156e466b86a896ee7ef7ce823c362`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc66bb6b6f96d475e20cd3f5757b00e0391b8011b7a1cab27d9b083c3908514`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124f915d2307e6140d7fb5a5ea7d8be8903a6f27e1e33d1206638b3c04e8ad0e`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918f15c61365133b7c84bcd91e0b4232407a200db0010a427afbe5684d259ad7`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.1`

```console
$ docker pull couchdb@sha256:b422509b1648306dee1038f41756a982aefa17f986fa8ba18f6cd80e433dafdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.1` - linux; amd64

```console
$ docker pull couchdb@sha256:ca88e0f690f425cdd99b368073320f197317bed549d5560e0bdcf7877ff2918c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83772106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81efb6c8280c889d695b176c5f6597fec9b540fdb2974f9be5c3d654602d9ab`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:07:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:07:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:07:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:07:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:07:47 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:07:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:07:54 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 28 Sep 2021 02:07:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:08:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:08:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:08:11 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:08:11 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 28 Sep 2021 02:08:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:08:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:08:13 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:08:13 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:08:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf6d2572e5cb46cd161abd1cad4bfe814861bb79af678e8c8878bfceea39800`  
		Last Modified: Tue, 28 Sep 2021 02:08:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c07788136736f89aa055ecaf94d8a84930476f22f9743523ea520a89676871`  
		Last Modified: Tue, 28 Sep 2021 02:08:57 GMT  
		Size: 6.7 MB (6691239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f38611f22a1bf97d622c97f121883635774e7c90a58b732ea6ac173481ed5f`  
		Last Modified: Tue, 28 Sep 2021 02:08:56 GMT  
		Size: 1.3 MB (1258340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7085d2ce04f2475efd91088b35d5999a9d08265c4b69ff48f3756f569dfc0`  
		Last Modified: Tue, 28 Sep 2021 02:08:56 GMT  
		Size: 293.0 KB (292984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8884e223396a1ed82ed7286b9c3df03ac5b9869aa724a925872ef5d7096000b9`  
		Last Modified: Tue, 28 Sep 2021 02:08:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2be17aa7a1974f8ec1d74c76d8e5c7d56b50bdbf6f797a3da0a6020ce7e81cd`  
		Last Modified: Tue, 28 Sep 2021 02:08:59 GMT  
		Size: 48.4 MB (48376535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356eb1ff43b1918f0002995eef23ceb57e972579cbd8cc01fefda2e6a2260380`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6960ebdd0a7eba7433b2074bb47df88c68ebd6c9d542e4eaa1c72b0733ddc8ab`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92df28681e5b2d10bdc5b17b014ad2f3d54dde0b5ba5886ee1487995f2b6e8e`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130bc089b183384af5d0d23577af6520bff51727aee476f02354710dee1b7b64`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c8203604e2555cdaa201d2f33fddc1b684533ab522103424169d7667af043dc8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78787285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f398aff04cfa1c345800a93c3ae01142d9a0cb1793b4e9a1cb39d776982ba4c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:39 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 28 Sep 2021 02:13:39 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:13:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:13:53 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:13:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:13:53 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 28 Sep 2021 02:13:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:13:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:13:54 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:13:54 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:13:55 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a567769b3d8168bb1b7fac501b3e15fb35e1e1a40b34a9258451876bf3b6ab9`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3b66a31e4294cd1da1d2a4a2d5914ca6ca6a7cef5ede944bddf8c85384041`  
		Last Modified: Tue, 28 Sep 2021 02:14:50 GMT  
		Size: 44.9 MB (44858084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095af1ccc0a9a0ae3e3a3f231f0f10bb20156e466b86a896ee7ef7ce823c362`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc66bb6b6f96d475e20cd3f5757b00e0391b8011b7a1cab27d9b083c3908514`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124f915d2307e6140d7fb5a5ea7d8be8903a6f27e1e33d1206638b3c04e8ad0e`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918f15c61365133b7c84bcd91e0b4232407a200db0010a427afbe5684d259ad7`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:b422509b1648306dee1038f41756a982aefa17f986fa8ba18f6cd80e433dafdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:ca88e0f690f425cdd99b368073320f197317bed549d5560e0bdcf7877ff2918c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83772106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81efb6c8280c889d695b176c5f6597fec9b540fdb2974f9be5c3d654602d9ab`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:07:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:07:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:07:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:07:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:07:47 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:07:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:07:54 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 28 Sep 2021 02:07:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:08:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:08:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:08:11 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:08:11 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 28 Sep 2021 02:08:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:08:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:08:13 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:08:13 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:08:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf6d2572e5cb46cd161abd1cad4bfe814861bb79af678e8c8878bfceea39800`  
		Last Modified: Tue, 28 Sep 2021 02:08:58 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c07788136736f89aa055ecaf94d8a84930476f22f9743523ea520a89676871`  
		Last Modified: Tue, 28 Sep 2021 02:08:57 GMT  
		Size: 6.7 MB (6691239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f38611f22a1bf97d622c97f121883635774e7c90a58b732ea6ac173481ed5f`  
		Last Modified: Tue, 28 Sep 2021 02:08:56 GMT  
		Size: 1.3 MB (1258340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7085d2ce04f2475efd91088b35d5999a9d08265c4b69ff48f3756f569dfc0`  
		Last Modified: Tue, 28 Sep 2021 02:08:56 GMT  
		Size: 293.0 KB (292984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8884e223396a1ed82ed7286b9c3df03ac5b9869aa724a925872ef5d7096000b9`  
		Last Modified: Tue, 28 Sep 2021 02:08:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2be17aa7a1974f8ec1d74c76d8e5c7d56b50bdbf6f797a3da0a6020ce7e81cd`  
		Last Modified: Tue, 28 Sep 2021 02:08:59 GMT  
		Size: 48.4 MB (48376535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356eb1ff43b1918f0002995eef23ceb57e972579cbd8cc01fefda2e6a2260380`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6960ebdd0a7eba7433b2074bb47df88c68ebd6c9d542e4eaa1c72b0733ddc8ab`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92df28681e5b2d10bdc5b17b014ad2f3d54dde0b5ba5886ee1487995f2b6e8e`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130bc089b183384af5d0d23577af6520bff51727aee476f02354710dee1b7b64`  
		Last Modified: Tue, 28 Sep 2021 02:08:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c8203604e2555cdaa201d2f33fddc1b684533ab522103424169d7667af043dc8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78787285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f398aff04cfa1c345800a93c3ae01142d9a0cb1793b4e9a1cb39d776982ba4c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:39 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 28 Sep 2021 02:13:39 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:13:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:13:53 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:13:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:13:53 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 28 Sep 2021 02:13:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:13:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:13:54 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:13:54 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:13:55 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a567769b3d8168bb1b7fac501b3e15fb35e1e1a40b34a9258451876bf3b6ab9`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3b66a31e4294cd1da1d2a4a2d5914ca6ca6a7cef5ede944bddf8c85384041`  
		Last Modified: Tue, 28 Sep 2021 02:14:50 GMT  
		Size: 44.9 MB (44858084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095af1ccc0a9a0ae3e3a3f231f0f10bb20156e466b86a896ee7ef7ce823c362`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc66bb6b6f96d475e20cd3f5757b00e0391b8011b7a1cab27d9b083c3908514`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124f915d2307e6140d7fb5a5ea7d8be8903a6f27e1e33d1206638b3c04e8ad0e`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918f15c61365133b7c84bcd91e0b4232407a200db0010a427afbe5684d259ad7`  
		Last Modified: Tue, 28 Sep 2021 02:14:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
