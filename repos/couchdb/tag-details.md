<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.2`](#couchdb312)
-	[`couchdb:3.2`](#couchdb32)
-	[`couchdb:3.2.2`](#couchdb322)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:2e830c71d2a87dabeb768d2829bbdcb3339ec16996e01290391afe8ab967d5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:89ec990c38a98c072461b37efc3fdd3e6af059d26bab0bc14ca0c03a75eb9a29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7730f520a9e0d91cc76a3b1213178dc8c039c5f847aba061618f531f13e9b598`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:33 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 23 Jun 2022 01:07:33 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:52 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:53 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:53 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02b79ba8f20a74d6043fa2f3eceab9cb4311187e228e822cedc254f3c158b7`  
		Last Modified: Thu, 23 Jun 2022 01:08:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b44dcfa4a8386763976c2fa29204037a9051563713501777f0b060e85e38bb1`  
		Last Modified: Thu, 23 Jun 2022 01:08:53 GMT  
		Size: 49.1 MB (49127735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb73a35366ebb8c0aa3c79869555b534dabcb30bc834f9457de16c3681034e4f`  
		Last Modified: Thu, 23 Jun 2022 01:08:48 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c0c6f989ed30ae055bd89195fdc6a7330b0ec131d12fd1b3b277e8319d4f10`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f7fc0dd5f8432ce4345dadaeb1a417adf17681a5d1c27cbd407149d546d862`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ac49a371125c8caea5047c3e01280a947350ace78997afcd09bf91c05ab518`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:04da7034c2d938d1359d1d119fecd0585094fe541c830db2f981b68e760f50d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72532212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6beabb9121b8b32406b286c1228b74aeb48a9e5d1c8977f3497fdb3c106890c8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:10:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:10:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:10:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:10:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:10:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:11:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:11:38 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Sat, 28 May 2022 02:11:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:11:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:11:54 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:11:55 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:11:56 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Sat, 28 May 2022 02:11:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:11:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:11:58 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:11:59 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:12:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df87715dbbc0f7e9fa4464ebf57262fda4e050c820a30b343e73a1f4b5ddd809`  
		Last Modified: Sat, 28 May 2022 02:12:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5910279a024018bff17c24cc89641da2954a3729de66031786a65c1c6f3e48`  
		Last Modified: Sat, 28 May 2022 02:12:54 GMT  
		Size: 6.6 MB (6556694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f084ee6afeab9340278b262b3fa9696bc76445c96dd5894e9084040bdfda17`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 951.2 KB (951185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43024313a99504411fbb816f5b182c78bfc4ddefe215ead2b9e70dde7f212db1`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196c92a64d57c7ff3c2606f7b9944afa6a20f3075589a35b5b3abfa2a192c70e`  
		Last Modified: Sat, 28 May 2022 02:13:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87df0f0db5e9ffaf7f8c019cce783c94ab9e64dcd32eda09be56e7698b68e055`  
		Last Modified: Sat, 28 May 2022 02:13:12 GMT  
		Size: 39.0 MB (39023420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d0578cd28a91cb154e00cd03fd7217372e288d9cc0f86e8180f1b16a6980a`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1ec7cc039a84d291862bfa8bc4adb2debfbb048e828e73e5f441466ce3dd5d`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e1b514fa109f16f2af17c44ce0b0d0a08b60e4434789b992e857c21458a40`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180a2a0b44558153945d91cd4dcefc8cac563fd23e45a0ae4dbd9de8edc47de6`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:2e830c71d2a87dabeb768d2829bbdcb3339ec16996e01290391afe8ab967d5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:89ec990c38a98c072461b37efc3fdd3e6af059d26bab0bc14ca0c03a75eb9a29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7730f520a9e0d91cc76a3b1213178dc8c039c5f847aba061618f531f13e9b598`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:33 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 23 Jun 2022 01:07:33 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:52 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:53 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:53 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02b79ba8f20a74d6043fa2f3eceab9cb4311187e228e822cedc254f3c158b7`  
		Last Modified: Thu, 23 Jun 2022 01:08:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b44dcfa4a8386763976c2fa29204037a9051563713501777f0b060e85e38bb1`  
		Last Modified: Thu, 23 Jun 2022 01:08:53 GMT  
		Size: 49.1 MB (49127735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb73a35366ebb8c0aa3c79869555b534dabcb30bc834f9457de16c3681034e4f`  
		Last Modified: Thu, 23 Jun 2022 01:08:48 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c0c6f989ed30ae055bd89195fdc6a7330b0ec131d12fd1b3b277e8319d4f10`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f7fc0dd5f8432ce4345dadaeb1a417adf17681a5d1c27cbd407149d546d862`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ac49a371125c8caea5047c3e01280a947350ace78997afcd09bf91c05ab518`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:04da7034c2d938d1359d1d119fecd0585094fe541c830db2f981b68e760f50d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72532212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6beabb9121b8b32406b286c1228b74aeb48a9e5d1c8977f3497fdb3c106890c8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:10:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:10:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:10:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:10:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:10:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:11:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:11:38 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Sat, 28 May 2022 02:11:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:11:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:11:54 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:11:55 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:11:56 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Sat, 28 May 2022 02:11:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:11:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:11:58 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:11:59 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:12:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df87715dbbc0f7e9fa4464ebf57262fda4e050c820a30b343e73a1f4b5ddd809`  
		Last Modified: Sat, 28 May 2022 02:12:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5910279a024018bff17c24cc89641da2954a3729de66031786a65c1c6f3e48`  
		Last Modified: Sat, 28 May 2022 02:12:54 GMT  
		Size: 6.6 MB (6556694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f084ee6afeab9340278b262b3fa9696bc76445c96dd5894e9084040bdfda17`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 951.2 KB (951185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43024313a99504411fbb816f5b182c78bfc4ddefe215ead2b9e70dde7f212db1`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196c92a64d57c7ff3c2606f7b9944afa6a20f3075589a35b5b3abfa2a192c70e`  
		Last Modified: Sat, 28 May 2022 02:13:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87df0f0db5e9ffaf7f8c019cce783c94ab9e64dcd32eda09be56e7698b68e055`  
		Last Modified: Sat, 28 May 2022 02:13:12 GMT  
		Size: 39.0 MB (39023420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d0578cd28a91cb154e00cd03fd7217372e288d9cc0f86e8180f1b16a6980a`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1ec7cc039a84d291862bfa8bc4adb2debfbb048e828e73e5f441466ce3dd5d`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e1b514fa109f16f2af17c44ce0b0d0a08b60e4434789b992e857c21458a40`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180a2a0b44558153945d91cd4dcefc8cac563fd23e45a0ae4dbd9de8edc47de6`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:2e830c71d2a87dabeb768d2829bbdcb3339ec16996e01290391afe8ab967d5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:89ec990c38a98c072461b37efc3fdd3e6af059d26bab0bc14ca0c03a75eb9a29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7730f520a9e0d91cc76a3b1213178dc8c039c5f847aba061618f531f13e9b598`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:33 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 23 Jun 2022 01:07:33 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:52 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:53 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:53 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02b79ba8f20a74d6043fa2f3eceab9cb4311187e228e822cedc254f3c158b7`  
		Last Modified: Thu, 23 Jun 2022 01:08:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b44dcfa4a8386763976c2fa29204037a9051563713501777f0b060e85e38bb1`  
		Last Modified: Thu, 23 Jun 2022 01:08:53 GMT  
		Size: 49.1 MB (49127735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb73a35366ebb8c0aa3c79869555b534dabcb30bc834f9457de16c3681034e4f`  
		Last Modified: Thu, 23 Jun 2022 01:08:48 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c0c6f989ed30ae055bd89195fdc6a7330b0ec131d12fd1b3b277e8319d4f10`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f7fc0dd5f8432ce4345dadaeb1a417adf17681a5d1c27cbd407149d546d862`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ac49a371125c8caea5047c3e01280a947350ace78997afcd09bf91c05ab518`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:04da7034c2d938d1359d1d119fecd0585094fe541c830db2f981b68e760f50d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72532212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6beabb9121b8b32406b286c1228b74aeb48a9e5d1c8977f3497fdb3c106890c8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:10:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:10:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:10:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:10:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:10:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:11:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:11:38 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Sat, 28 May 2022 02:11:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:11:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:11:54 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:11:55 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:11:56 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Sat, 28 May 2022 02:11:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:11:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:11:58 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:11:59 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:12:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df87715dbbc0f7e9fa4464ebf57262fda4e050c820a30b343e73a1f4b5ddd809`  
		Last Modified: Sat, 28 May 2022 02:12:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5910279a024018bff17c24cc89641da2954a3729de66031786a65c1c6f3e48`  
		Last Modified: Sat, 28 May 2022 02:12:54 GMT  
		Size: 6.6 MB (6556694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f084ee6afeab9340278b262b3fa9696bc76445c96dd5894e9084040bdfda17`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 951.2 KB (951185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43024313a99504411fbb816f5b182c78bfc4ddefe215ead2b9e70dde7f212db1`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196c92a64d57c7ff3c2606f7b9944afa6a20f3075589a35b5b3abfa2a192c70e`  
		Last Modified: Sat, 28 May 2022 02:13:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87df0f0db5e9ffaf7f8c019cce783c94ab9e64dcd32eda09be56e7698b68e055`  
		Last Modified: Sat, 28 May 2022 02:13:12 GMT  
		Size: 39.0 MB (39023420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d0578cd28a91cb154e00cd03fd7217372e288d9cc0f86e8180f1b16a6980a`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1ec7cc039a84d291862bfa8bc4adb2debfbb048e828e73e5f441466ce3dd5d`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e1b514fa109f16f2af17c44ce0b0d0a08b60e4434789b992e857c21458a40`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180a2a0b44558153945d91cd4dcefc8cac563fd23e45a0ae4dbd9de8edc47de6`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:fd47475b0c6980bfc926bbc5fee35ac867b54ae0d7ea5f9ed64bd0621efc568c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:3ea7f178b119a1bbd2adbec78486241a087ba35d1d3ec9128a3ada704d55ec97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87498751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9d2dcf03aa6b53788baca7b138c9069926ce70119f77c999d0e2d0858e21d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:06:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:06:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:35 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:06:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:06:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:06:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:06:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:06:50 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:06:50 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:06:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b67ef10ab3031244bf995ed483d30c4423feb9f42f12d55c8511d7497c931`  
		Last Modified: Thu, 23 Jun 2022 01:08:14 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd945ed68b3fecb83857780d70642d81019952136407b87a9f4b6b94711e7dda`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 5.2 MB (5224047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1d67ad9668554764252390c4e5b06fb0f33517e33a831601a00c10a05cfbe7`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 1.6 MB (1553288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b56aaaffae17f3010ab5ba52d88e22126a8b18f5f8fd49ea4a01655c55e20b`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 295.6 KB (295555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e601de752a6ea7ddb9a0b7201437219d647dd0a6555b1d9f48ae8d94004f40`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd769730295be73a2aae5a0882ad80bb9284ad34c68bff96c93ccd15f3cc73`  
		Last Modified: Thu, 23 Jun 2022 01:08:15 GMT  
		Size: 49.0 MB (49039317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0fe21a89a509108c6d599b399458e374353649854cc07814e901deb7030198`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9700366d2b2b831d620b0ee23a1b1ed39c86a91aa69aaad560465e5dd33889`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd356f58092365eb5086db70cc449f1fce114ea73ac0ee9bc18298ac6c579120`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f797d1e3134f5eda53222acba18a0644f920f20c2431b5b3604ab90b7d882c09`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2ae0ffc4c377ee938da9a432c88899028b8daaded48a9b8709aabfbe549c6806
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85427246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137eb0cb0d3d6b84966c58c7b4f1e89b60281aac5617846a7f304eec5c713117`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:40:39 GMT
ADD file:55b4fe3115c684f545e4e4148c93745f12192976a08c37d090fcac708fb709a7 in / 
# Sat, 28 May 2022 00:40:39 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:09:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:09:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:09:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:09:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:09:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:09:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:09:59 GMT
ENV COUCHDB_VERSION=3.2.2
# Sat, 28 May 2022 02:10:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:10:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:10:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:10:22 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:10:23 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 28 May 2022 02:10:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:10:24 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:10:25 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:10:26 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:10:27 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:dc1f00a5d701e86e2cd2568b860c61b393d66be1341e7267d07e6e57448ceeba`  
		Last Modified: Sat, 28 May 2022 00:47:35 GMT  
		Size: 30.1 MB (30065728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019212e3841694cf915d2b4e3a102c24a48dc2d9b1209f9dfa7fa5543a16a11`  
		Last Modified: Sat, 28 May 2022 02:12:30 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4521f7861665e16dfd49c07f787e547874576d4059000fc11030b17e0764f34b`  
		Last Modified: Sat, 28 May 2022 02:12:29 GMT  
		Size: 5.0 MB (5003022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff02a9a55d396ff6ab401ff8ac0cb819932c2978d35472b245bb1ec9478c76b`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 1.2 MB (1221097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3658fbe5e3be4dbdd901239e554c80fae1f781fa21942f3b60aa3fe97713d6`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 79.2 KB (79191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9437832abdd28bcf179cd3b59f44729f00647bebcbd751d4de97c5c672416b6`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc4682e178e1470eed9a7df80cf8bc0351edcdd374e553a1a6af823f80919d7`  
		Last Modified: Sat, 28 May 2022 02:12:31 GMT  
		Size: 49.1 MB (49051159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6a360daac77bf8e38418a4c0736676d5261a47c342f274fe3f3a4bb60afef1`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da968eb8433ffe2a36ef9c4d86873b79f94e7f0a1969101ed4fff7b3cbad84b5`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0dedcc40dd9866f51ac6d9620fe64dd7e2e13c25da0403571fd6ba8c4776f8`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098da8954095caac906291f3740c25905e4b6634cfc8ce2f576ee0dd2a36c655`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f95e2cea87b96ad9d1f58b2f7a1cc297fafa4a0ba2ac8264ac49d1638308fc9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93222784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b27bcbda415fb7a19f938be7247b5b8374059229cdc9cd529fb5307a210896`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 01:22:54 GMT
ADD file:64e264b12eed99d87380e38f36bfecd62b9bb1e5460f0242cfbc5dc76c212ead in / 
# Sat, 28 May 2022 01:22:59 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:40:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 03:40:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 03:41:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:41:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 03:41:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 03:42:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:42:07 GMT
ENV COUCHDB_VERSION=3.2.2
# Sat, 28 May 2022 03:42:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 03:42:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 03:42:58 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 03:42:59 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 03:43:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 28 May 2022 03:43:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 03:43:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 03:43:12 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 03:43:14 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 03:43:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:893e245a8f6219935016f2dd4422ec4b7fdab43d98ba29c024ec0d9ce57794ba`  
		Last Modified: Sat, 28 May 2022 01:32:28 GMT  
		Size: 35.3 MB (35286698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875b56da848a25def16ef02568eeffc6bbc68f8a2468a40da18f7804d2dd4dc9`  
		Last Modified: Sat, 28 May 2022 03:43:47 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308e008e7e9f9a18c5718a2d3de1662a1db954494a646fdf8ba6d823e164163`  
		Last Modified: Sat, 28 May 2022 03:43:46 GMT  
		Size: 6.0 MB (6043917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5459503824efb70b765dc12230fae1a2e7f1d57ba12e7e9167fb178b49e2d7eb`  
		Last Modified: Sat, 28 May 2022 03:43:45 GMT  
		Size: 1.5 MB (1509317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc78eafedf794548c6bb2337ef3e6c836e38b32b8614595cba142a46bf2e9dd7`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 295.7 KB (295711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a0c9e549e3260acc9bf35d347a6d917255de993dd25ed0b87d3e42a07e7db8`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a195ecb14f19305eece3c42f9ca34a34d6b56c3068466d8bb2bbd3e718b6946e`  
		Last Modified: Sat, 28 May 2022 03:43:52 GMT  
		Size: 50.1 MB (50080003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dfd3f63efba486fe137f4f549db8e61c85af415f596ed332b7c0c8b59ee455`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986d6fa4c295a869df86de585d8914fe5b1a862f8bd8b6e7eb7b271f8095833`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa73f76a3e72dfaf15f902a8ab24390ed60ac0c9ee076c28ea9e6b81e55ce9a`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e53af1ea2a6650916769ea2f4ba0611b52a7bc36e0e0c1d740aeb583a7add7`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:2f7350c2981bc0f2fbac1009d71e04d14a65b90efab8e36a804ef584af9de0d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:f5e1d26a55dca17d784c1f2b9f669b81abac7ef6338e7eea1521a44df2fa2f21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80009555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d833bfc7acc1bf6fb4701f88ab1edd3d6175e9fae0d5e5c87a0f63be9ea39785`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:10 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 23 Jun 2022 01:07:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:24 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:25 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:25 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:26 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab9ba22220b6188d53d6fc816b63e62996f696e875a21ba2861e839ec5a6861`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdda34c0972965fdcda16044c6018c724818515b86c4c58acf9c1b051b20858`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 44.6 MB (44612451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a85c10523399f67c5c6eefeda3cdd2db8d6ba9dae6f6ef9733ed4d1754e9553`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea223f715c88770fbcef6e32b8cb5f10171bdbe81362aec840af62e8fe3b03d`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35c25494b5c7fa8293dd4ada6b829e1802920894aaad64c7feb17e29b0057e0`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed9f94e6c2271887064031d91d640c36b409089a60fa5db5f7ef0734c643e48`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:847e2c962236313df65996d351b8e3931b4ae8719bcb96398079f15e3765e6c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74621355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35fc584cf6b2bf00f347d30a3ffec6b181f9a5faba80b39eb639df5eb1da2136`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:10:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:10:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:10:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:10:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:10:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:11:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:11:03 GMT
ENV COUCHDB_VERSION=3.1.2
# Sat, 28 May 2022 02:11:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:11:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:11:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:11:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:11:26 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Sat, 28 May 2022 02:11:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:11:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:11:28 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:11:29 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:11:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df87715dbbc0f7e9fa4464ebf57262fda4e050c820a30b343e73a1f4b5ddd809`  
		Last Modified: Sat, 28 May 2022 02:12:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5910279a024018bff17c24cc89641da2954a3729de66031786a65c1c6f3e48`  
		Last Modified: Sat, 28 May 2022 02:12:54 GMT  
		Size: 6.6 MB (6556694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f084ee6afeab9340278b262b3fa9696bc76445c96dd5894e9084040bdfda17`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 951.2 KB (951185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43024313a99504411fbb816f5b182c78bfc4ddefe215ead2b9e70dde7f212db1`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6539d7e341cbcd00982b2f11dc0397ecd3486187357afe47e566e43399a1673d`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2524916e993a60f307cc1b61f1da428e13143afdd839e96665727d8ace3d44`  
		Last Modified: Sat, 28 May 2022 02:12:55 GMT  
		Size: 41.1 MB (41112565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee69a3a77f17bda355f100fa3c2133c87760f680ae0b228cfbd6d0d2b50f3e5`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2cd60ccdcd13ab0550a20f9d1271e32a1f7a012ec851ae3efe7113693a8c73`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfea82c5bcc6c9add963ff1fef209ce5628576752fe80f9eacd7319ee56a140`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893a37410d58b1e6329af6294978dd6d13f946f8950e6cfcaee1127826a8b462`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:2f7350c2981bc0f2fbac1009d71e04d14a65b90efab8e36a804ef584af9de0d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:f5e1d26a55dca17d784c1f2b9f669b81abac7ef6338e7eea1521a44df2fa2f21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80009555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d833bfc7acc1bf6fb4701f88ab1edd3d6175e9fae0d5e5c87a0f63be9ea39785`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:10 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 23 Jun 2022 01:07:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:24 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:25 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:25 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:26 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab9ba22220b6188d53d6fc816b63e62996f696e875a21ba2861e839ec5a6861`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdda34c0972965fdcda16044c6018c724818515b86c4c58acf9c1b051b20858`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 44.6 MB (44612451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a85c10523399f67c5c6eefeda3cdd2db8d6ba9dae6f6ef9733ed4d1754e9553`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea223f715c88770fbcef6e32b8cb5f10171bdbe81362aec840af62e8fe3b03d`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35c25494b5c7fa8293dd4ada6b829e1802920894aaad64c7feb17e29b0057e0`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed9f94e6c2271887064031d91d640c36b409089a60fa5db5f7ef0734c643e48`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:847e2c962236313df65996d351b8e3931b4ae8719bcb96398079f15e3765e6c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74621355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35fc584cf6b2bf00f347d30a3ffec6b181f9a5faba80b39eb639df5eb1da2136`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:10:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:10:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:10:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:10:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:10:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:11:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:11:03 GMT
ENV COUCHDB_VERSION=3.1.2
# Sat, 28 May 2022 02:11:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:11:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:11:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:11:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:11:26 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Sat, 28 May 2022 02:11:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:11:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:11:28 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:11:29 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:11:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df87715dbbc0f7e9fa4464ebf57262fda4e050c820a30b343e73a1f4b5ddd809`  
		Last Modified: Sat, 28 May 2022 02:12:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5910279a024018bff17c24cc89641da2954a3729de66031786a65c1c6f3e48`  
		Last Modified: Sat, 28 May 2022 02:12:54 GMT  
		Size: 6.6 MB (6556694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f084ee6afeab9340278b262b3fa9696bc76445c96dd5894e9084040bdfda17`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 951.2 KB (951185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43024313a99504411fbb816f5b182c78bfc4ddefe215ead2b9e70dde7f212db1`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6539d7e341cbcd00982b2f11dc0397ecd3486187357afe47e566e43399a1673d`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2524916e993a60f307cc1b61f1da428e13143afdd839e96665727d8ace3d44`  
		Last Modified: Sat, 28 May 2022 02:12:55 GMT  
		Size: 41.1 MB (41112565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee69a3a77f17bda355f100fa3c2133c87760f680ae0b228cfbd6d0d2b50f3e5`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2cd60ccdcd13ab0550a20f9d1271e32a1f7a012ec851ae3efe7113693a8c73`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfea82c5bcc6c9add963ff1fef209ce5628576752fe80f9eacd7319ee56a140`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893a37410d58b1e6329af6294978dd6d13f946f8950e6cfcaee1127826a8b462`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:fd47475b0c6980bfc926bbc5fee35ac867b54ae0d7ea5f9ed64bd0621efc568c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:3ea7f178b119a1bbd2adbec78486241a087ba35d1d3ec9128a3ada704d55ec97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87498751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9d2dcf03aa6b53788baca7b138c9069926ce70119f77c999d0e2d0858e21d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:06:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:06:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:35 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:06:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:06:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:06:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:06:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:06:50 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:06:50 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:06:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b67ef10ab3031244bf995ed483d30c4423feb9f42f12d55c8511d7497c931`  
		Last Modified: Thu, 23 Jun 2022 01:08:14 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd945ed68b3fecb83857780d70642d81019952136407b87a9f4b6b94711e7dda`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 5.2 MB (5224047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1d67ad9668554764252390c4e5b06fb0f33517e33a831601a00c10a05cfbe7`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 1.6 MB (1553288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b56aaaffae17f3010ab5ba52d88e22126a8b18f5f8fd49ea4a01655c55e20b`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 295.6 KB (295555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e601de752a6ea7ddb9a0b7201437219d647dd0a6555b1d9f48ae8d94004f40`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd769730295be73a2aae5a0882ad80bb9284ad34c68bff96c93ccd15f3cc73`  
		Last Modified: Thu, 23 Jun 2022 01:08:15 GMT  
		Size: 49.0 MB (49039317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0fe21a89a509108c6d599b399458e374353649854cc07814e901deb7030198`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9700366d2b2b831d620b0ee23a1b1ed39c86a91aa69aaad560465e5dd33889`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd356f58092365eb5086db70cc449f1fce114ea73ac0ee9bc18298ac6c579120`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f797d1e3134f5eda53222acba18a0644f920f20c2431b5b3604ab90b7d882c09`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2ae0ffc4c377ee938da9a432c88899028b8daaded48a9b8709aabfbe549c6806
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85427246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137eb0cb0d3d6b84966c58c7b4f1e89b60281aac5617846a7f304eec5c713117`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:40:39 GMT
ADD file:55b4fe3115c684f545e4e4148c93745f12192976a08c37d090fcac708fb709a7 in / 
# Sat, 28 May 2022 00:40:39 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:09:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:09:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:09:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:09:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:09:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:09:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:09:59 GMT
ENV COUCHDB_VERSION=3.2.2
# Sat, 28 May 2022 02:10:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:10:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:10:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:10:22 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:10:23 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 28 May 2022 02:10:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:10:24 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:10:25 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:10:26 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:10:27 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:dc1f00a5d701e86e2cd2568b860c61b393d66be1341e7267d07e6e57448ceeba`  
		Last Modified: Sat, 28 May 2022 00:47:35 GMT  
		Size: 30.1 MB (30065728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019212e3841694cf915d2b4e3a102c24a48dc2d9b1209f9dfa7fa5543a16a11`  
		Last Modified: Sat, 28 May 2022 02:12:30 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4521f7861665e16dfd49c07f787e547874576d4059000fc11030b17e0764f34b`  
		Last Modified: Sat, 28 May 2022 02:12:29 GMT  
		Size: 5.0 MB (5003022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff02a9a55d396ff6ab401ff8ac0cb819932c2978d35472b245bb1ec9478c76b`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 1.2 MB (1221097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3658fbe5e3be4dbdd901239e554c80fae1f781fa21942f3b60aa3fe97713d6`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 79.2 KB (79191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9437832abdd28bcf179cd3b59f44729f00647bebcbd751d4de97c5c672416b6`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc4682e178e1470eed9a7df80cf8bc0351edcdd374e553a1a6af823f80919d7`  
		Last Modified: Sat, 28 May 2022 02:12:31 GMT  
		Size: 49.1 MB (49051159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6a360daac77bf8e38418a4c0736676d5261a47c342f274fe3f3a4bb60afef1`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da968eb8433ffe2a36ef9c4d86873b79f94e7f0a1969101ed4fff7b3cbad84b5`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0dedcc40dd9866f51ac6d9620fe64dd7e2e13c25da0403571fd6ba8c4776f8`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098da8954095caac906291f3740c25905e4b6634cfc8ce2f576ee0dd2a36c655`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f95e2cea87b96ad9d1f58b2f7a1cc297fafa4a0ba2ac8264ac49d1638308fc9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93222784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b27bcbda415fb7a19f938be7247b5b8374059229cdc9cd529fb5307a210896`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 01:22:54 GMT
ADD file:64e264b12eed99d87380e38f36bfecd62b9bb1e5460f0242cfbc5dc76c212ead in / 
# Sat, 28 May 2022 01:22:59 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:40:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 03:40:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 03:41:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:41:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 03:41:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 03:42:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:42:07 GMT
ENV COUCHDB_VERSION=3.2.2
# Sat, 28 May 2022 03:42:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 03:42:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 03:42:58 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 03:42:59 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 03:43:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 28 May 2022 03:43:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 03:43:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 03:43:12 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 03:43:14 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 03:43:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:893e245a8f6219935016f2dd4422ec4b7fdab43d98ba29c024ec0d9ce57794ba`  
		Last Modified: Sat, 28 May 2022 01:32:28 GMT  
		Size: 35.3 MB (35286698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875b56da848a25def16ef02568eeffc6bbc68f8a2468a40da18f7804d2dd4dc9`  
		Last Modified: Sat, 28 May 2022 03:43:47 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308e008e7e9f9a18c5718a2d3de1662a1db954494a646fdf8ba6d823e164163`  
		Last Modified: Sat, 28 May 2022 03:43:46 GMT  
		Size: 6.0 MB (6043917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5459503824efb70b765dc12230fae1a2e7f1d57ba12e7e9167fb178b49e2d7eb`  
		Last Modified: Sat, 28 May 2022 03:43:45 GMT  
		Size: 1.5 MB (1509317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc78eafedf794548c6bb2337ef3e6c836e38b32b8614595cba142a46bf2e9dd7`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 295.7 KB (295711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a0c9e549e3260acc9bf35d347a6d917255de993dd25ed0b87d3e42a07e7db8`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a195ecb14f19305eece3c42f9ca34a34d6b56c3068466d8bb2bbd3e718b6946e`  
		Last Modified: Sat, 28 May 2022 03:43:52 GMT  
		Size: 50.1 MB (50080003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dfd3f63efba486fe137f4f549db8e61c85af415f596ed332b7c0c8b59ee455`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986d6fa4c295a869df86de585d8914fe5b1a862f8bd8b6e7eb7b271f8095833`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa73f76a3e72dfaf15f902a8ab24390ed60ac0c9ee076c28ea9e6b81e55ce9a`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e53af1ea2a6650916769ea2f4ba0611b52a7bc36e0e0c1d740aeb583a7add7`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.2`

```console
$ docker pull couchdb@sha256:fd47475b0c6980bfc926bbc5fee35ac867b54ae0d7ea5f9ed64bd0621efc568c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.2` - linux; amd64

```console
$ docker pull couchdb@sha256:3ea7f178b119a1bbd2adbec78486241a087ba35d1d3ec9128a3ada704d55ec97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87498751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9d2dcf03aa6b53788baca7b138c9069926ce70119f77c999d0e2d0858e21d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:06:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:06:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:35 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:06:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:06:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:06:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:06:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:06:50 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:06:50 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:06:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b67ef10ab3031244bf995ed483d30c4423feb9f42f12d55c8511d7497c931`  
		Last Modified: Thu, 23 Jun 2022 01:08:14 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd945ed68b3fecb83857780d70642d81019952136407b87a9f4b6b94711e7dda`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 5.2 MB (5224047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1d67ad9668554764252390c4e5b06fb0f33517e33a831601a00c10a05cfbe7`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 1.6 MB (1553288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b56aaaffae17f3010ab5ba52d88e22126a8b18f5f8fd49ea4a01655c55e20b`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 295.6 KB (295555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e601de752a6ea7ddb9a0b7201437219d647dd0a6555b1d9f48ae8d94004f40`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd769730295be73a2aae5a0882ad80bb9284ad34c68bff96c93ccd15f3cc73`  
		Last Modified: Thu, 23 Jun 2022 01:08:15 GMT  
		Size: 49.0 MB (49039317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0fe21a89a509108c6d599b399458e374353649854cc07814e901deb7030198`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9700366d2b2b831d620b0ee23a1b1ed39c86a91aa69aaad560465e5dd33889`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd356f58092365eb5086db70cc449f1fce114ea73ac0ee9bc18298ac6c579120`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f797d1e3134f5eda53222acba18a0644f920f20c2431b5b3604ab90b7d882c09`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2ae0ffc4c377ee938da9a432c88899028b8daaded48a9b8709aabfbe549c6806
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85427246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137eb0cb0d3d6b84966c58c7b4f1e89b60281aac5617846a7f304eec5c713117`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:40:39 GMT
ADD file:55b4fe3115c684f545e4e4148c93745f12192976a08c37d090fcac708fb709a7 in / 
# Sat, 28 May 2022 00:40:39 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:09:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:09:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:09:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:09:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:09:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:09:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:09:59 GMT
ENV COUCHDB_VERSION=3.2.2
# Sat, 28 May 2022 02:10:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:10:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:10:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:10:22 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:10:23 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 28 May 2022 02:10:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:10:24 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:10:25 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:10:26 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:10:27 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:dc1f00a5d701e86e2cd2568b860c61b393d66be1341e7267d07e6e57448ceeba`  
		Last Modified: Sat, 28 May 2022 00:47:35 GMT  
		Size: 30.1 MB (30065728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019212e3841694cf915d2b4e3a102c24a48dc2d9b1209f9dfa7fa5543a16a11`  
		Last Modified: Sat, 28 May 2022 02:12:30 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4521f7861665e16dfd49c07f787e547874576d4059000fc11030b17e0764f34b`  
		Last Modified: Sat, 28 May 2022 02:12:29 GMT  
		Size: 5.0 MB (5003022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff02a9a55d396ff6ab401ff8ac0cb819932c2978d35472b245bb1ec9478c76b`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 1.2 MB (1221097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3658fbe5e3be4dbdd901239e554c80fae1f781fa21942f3b60aa3fe97713d6`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 79.2 KB (79191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9437832abdd28bcf179cd3b59f44729f00647bebcbd751d4de97c5c672416b6`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc4682e178e1470eed9a7df80cf8bc0351edcdd374e553a1a6af823f80919d7`  
		Last Modified: Sat, 28 May 2022 02:12:31 GMT  
		Size: 49.1 MB (49051159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6a360daac77bf8e38418a4c0736676d5261a47c342f274fe3f3a4bb60afef1`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da968eb8433ffe2a36ef9c4d86873b79f94e7f0a1969101ed4fff7b3cbad84b5`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0dedcc40dd9866f51ac6d9620fe64dd7e2e13c25da0403571fd6ba8c4776f8`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098da8954095caac906291f3740c25905e4b6634cfc8ce2f576ee0dd2a36c655`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f95e2cea87b96ad9d1f58b2f7a1cc297fafa4a0ba2ac8264ac49d1638308fc9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93222784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b27bcbda415fb7a19f938be7247b5b8374059229cdc9cd529fb5307a210896`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 01:22:54 GMT
ADD file:64e264b12eed99d87380e38f36bfecd62b9bb1e5460f0242cfbc5dc76c212ead in / 
# Sat, 28 May 2022 01:22:59 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:40:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 03:40:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 03:41:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:41:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 03:41:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 03:42:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:42:07 GMT
ENV COUCHDB_VERSION=3.2.2
# Sat, 28 May 2022 03:42:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 03:42:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 03:42:58 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 03:42:59 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 03:43:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 28 May 2022 03:43:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 03:43:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 03:43:12 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 03:43:14 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 03:43:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:893e245a8f6219935016f2dd4422ec4b7fdab43d98ba29c024ec0d9ce57794ba`  
		Last Modified: Sat, 28 May 2022 01:32:28 GMT  
		Size: 35.3 MB (35286698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875b56da848a25def16ef02568eeffc6bbc68f8a2468a40da18f7804d2dd4dc9`  
		Last Modified: Sat, 28 May 2022 03:43:47 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308e008e7e9f9a18c5718a2d3de1662a1db954494a646fdf8ba6d823e164163`  
		Last Modified: Sat, 28 May 2022 03:43:46 GMT  
		Size: 6.0 MB (6043917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5459503824efb70b765dc12230fae1a2e7f1d57ba12e7e9167fb178b49e2d7eb`  
		Last Modified: Sat, 28 May 2022 03:43:45 GMT  
		Size: 1.5 MB (1509317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc78eafedf794548c6bb2337ef3e6c836e38b32b8614595cba142a46bf2e9dd7`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 295.7 KB (295711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a0c9e549e3260acc9bf35d347a6d917255de993dd25ed0b87d3e42a07e7db8`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a195ecb14f19305eece3c42f9ca34a34d6b56c3068466d8bb2bbd3e718b6946e`  
		Last Modified: Sat, 28 May 2022 03:43:52 GMT  
		Size: 50.1 MB (50080003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dfd3f63efba486fe137f4f549db8e61c85af415f596ed332b7c0c8b59ee455`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986d6fa4c295a869df86de585d8914fe5b1a862f8bd8b6e7eb7b271f8095833`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa73f76a3e72dfaf15f902a8ab24390ed60ac0c9ee076c28ea9e6b81e55ce9a`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e53af1ea2a6650916769ea2f4ba0611b52a7bc36e0e0c1d740aeb583a7add7`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:fd47475b0c6980bfc926bbc5fee35ac867b54ae0d7ea5f9ed64bd0621efc568c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:3ea7f178b119a1bbd2adbec78486241a087ba35d1d3ec9128a3ada704d55ec97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87498751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9d2dcf03aa6b53788baca7b138c9069926ce70119f77c999d0e2d0858e21d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:06:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:06:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:35 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:06:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:06:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:06:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:06:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:06:50 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:06:50 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:06:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b67ef10ab3031244bf995ed483d30c4423feb9f42f12d55c8511d7497c931`  
		Last Modified: Thu, 23 Jun 2022 01:08:14 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd945ed68b3fecb83857780d70642d81019952136407b87a9f4b6b94711e7dda`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 5.2 MB (5224047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1d67ad9668554764252390c4e5b06fb0f33517e33a831601a00c10a05cfbe7`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 1.6 MB (1553288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b56aaaffae17f3010ab5ba52d88e22126a8b18f5f8fd49ea4a01655c55e20b`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 295.6 KB (295555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e601de752a6ea7ddb9a0b7201437219d647dd0a6555b1d9f48ae8d94004f40`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd769730295be73a2aae5a0882ad80bb9284ad34c68bff96c93ccd15f3cc73`  
		Last Modified: Thu, 23 Jun 2022 01:08:15 GMT  
		Size: 49.0 MB (49039317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0fe21a89a509108c6d599b399458e374353649854cc07814e901deb7030198`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9700366d2b2b831d620b0ee23a1b1ed39c86a91aa69aaad560465e5dd33889`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd356f58092365eb5086db70cc449f1fce114ea73ac0ee9bc18298ac6c579120`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f797d1e3134f5eda53222acba18a0644f920f20c2431b5b3604ab90b7d882c09`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2ae0ffc4c377ee938da9a432c88899028b8daaded48a9b8709aabfbe549c6806
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85427246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137eb0cb0d3d6b84966c58c7b4f1e89b60281aac5617846a7f304eec5c713117`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:40:39 GMT
ADD file:55b4fe3115c684f545e4e4148c93745f12192976a08c37d090fcac708fb709a7 in / 
# Sat, 28 May 2022 00:40:39 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:09:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:09:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:09:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:09:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:09:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:09:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:09:59 GMT
ENV COUCHDB_VERSION=3.2.2
# Sat, 28 May 2022 02:10:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:10:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:10:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:10:22 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:10:23 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 28 May 2022 02:10:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:10:24 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:10:25 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:10:26 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:10:27 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:dc1f00a5d701e86e2cd2568b860c61b393d66be1341e7267d07e6e57448ceeba`  
		Last Modified: Sat, 28 May 2022 00:47:35 GMT  
		Size: 30.1 MB (30065728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019212e3841694cf915d2b4e3a102c24a48dc2d9b1209f9dfa7fa5543a16a11`  
		Last Modified: Sat, 28 May 2022 02:12:30 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4521f7861665e16dfd49c07f787e547874576d4059000fc11030b17e0764f34b`  
		Last Modified: Sat, 28 May 2022 02:12:29 GMT  
		Size: 5.0 MB (5003022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff02a9a55d396ff6ab401ff8ac0cb819932c2978d35472b245bb1ec9478c76b`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 1.2 MB (1221097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3658fbe5e3be4dbdd901239e554c80fae1f781fa21942f3b60aa3fe97713d6`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 79.2 KB (79191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9437832abdd28bcf179cd3b59f44729f00647bebcbd751d4de97c5c672416b6`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc4682e178e1470eed9a7df80cf8bc0351edcdd374e553a1a6af823f80919d7`  
		Last Modified: Sat, 28 May 2022 02:12:31 GMT  
		Size: 49.1 MB (49051159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6a360daac77bf8e38418a4c0736676d5261a47c342f274fe3f3a4bb60afef1`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da968eb8433ffe2a36ef9c4d86873b79f94e7f0a1969101ed4fff7b3cbad84b5`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0dedcc40dd9866f51ac6d9620fe64dd7e2e13c25da0403571fd6ba8c4776f8`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098da8954095caac906291f3740c25905e4b6634cfc8ce2f576ee0dd2a36c655`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f95e2cea87b96ad9d1f58b2f7a1cc297fafa4a0ba2ac8264ac49d1638308fc9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93222784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b27bcbda415fb7a19f938be7247b5b8374059229cdc9cd529fb5307a210896`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 01:22:54 GMT
ADD file:64e264b12eed99d87380e38f36bfecd62b9bb1e5460f0242cfbc5dc76c212ead in / 
# Sat, 28 May 2022 01:22:59 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:40:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 03:40:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 03:41:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:41:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 03:41:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 03:42:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:42:07 GMT
ENV COUCHDB_VERSION=3.2.2
# Sat, 28 May 2022 03:42:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 03:42:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 03:42:58 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 03:42:59 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 03:43:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 28 May 2022 03:43:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 03:43:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 03:43:12 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 03:43:14 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 03:43:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:893e245a8f6219935016f2dd4422ec4b7fdab43d98ba29c024ec0d9ce57794ba`  
		Last Modified: Sat, 28 May 2022 01:32:28 GMT  
		Size: 35.3 MB (35286698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875b56da848a25def16ef02568eeffc6bbc68f8a2468a40da18f7804d2dd4dc9`  
		Last Modified: Sat, 28 May 2022 03:43:47 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308e008e7e9f9a18c5718a2d3de1662a1db954494a646fdf8ba6d823e164163`  
		Last Modified: Sat, 28 May 2022 03:43:46 GMT  
		Size: 6.0 MB (6043917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5459503824efb70b765dc12230fae1a2e7f1d57ba12e7e9167fb178b49e2d7eb`  
		Last Modified: Sat, 28 May 2022 03:43:45 GMT  
		Size: 1.5 MB (1509317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc78eafedf794548c6bb2337ef3e6c836e38b32b8614595cba142a46bf2e9dd7`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 295.7 KB (295711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a0c9e549e3260acc9bf35d347a6d917255de993dd25ed0b87d3e42a07e7db8`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a195ecb14f19305eece3c42f9ca34a34d6b56c3068466d8bb2bbd3e718b6946e`  
		Last Modified: Sat, 28 May 2022 03:43:52 GMT  
		Size: 50.1 MB (50080003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dfd3f63efba486fe137f4f549db8e61c85af415f596ed332b7c0c8b59ee455`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986d6fa4c295a869df86de585d8914fe5b1a862f8bd8b6e7eb7b271f8095833`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa73f76a3e72dfaf15f902a8ab24390ed60ac0c9ee076c28ea9e6b81e55ce9a`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e53af1ea2a6650916769ea2f4ba0611b52a7bc36e0e0c1d740aeb583a7add7`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
