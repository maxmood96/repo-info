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
$ docker pull couchdb@sha256:4ef104f0a97f4016f48dea1056742f19863df2184af6db88b83b39d5306a9608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:847e1795b0a0d237d9f94be94629e33d811e0104c8c508897958440e1bdcf06c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10596e5ba2cc278725271cb50463f181896f424dbf4b06da88ce36c6ac59fd18`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:44:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:44:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:44:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:31 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 01 Mar 2022 05:44:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:44:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:44:50 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:44:50 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:44:50 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 01 Mar 2022 05:44:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:44:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:44:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:44:51 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:44:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e132993eb143d25686acdeb919d14985e8a65255f56170cc91230c350b203efa`  
		Last Modified: Tue, 01 Mar 2022 05:45:35 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50404ca1e1b3d297bb3c53a42e386f090eaa10f2d4db26fa324c39a836a18ea2`  
		Last Modified: Tue, 01 Mar 2022 05:45:34 GMT  
		Size: 6.7 MB (6691238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185b4237a163f4ee3d4cbb14cccd38dbfff817f923da22f90651149905d5957f`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 1.3 MB (1258328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a7c7c6b65c07b5de14a76f367630dcdc1f47fb75f959826b67e019b0617ec2`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 293.0 KB (293032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10737976dd7f04dffd2c8080cb3ea3718e864fb550e1f8e3354886937546574`  
		Last Modified: Tue, 01 Mar 2022 05:45:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a11c8284534d8d62c430ef5edd0b754f191ed08eb41a89dd12c88cc42f8876e`  
		Last Modified: Tue, 01 Mar 2022 05:45:52 GMT  
		Size: 49.1 MB (49114456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54d99378c788f80c9ecc1d468356b808769ef6e72ba204e99075047a72d9401`  
		Last Modified: Tue, 01 Mar 2022 05:45:47 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8f2f19f0705503827a4fdc361a6f99896e1875fb4fddbf33721a673720aef6`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bef14bec9c81959285cc9e53e3d5699eabb9be169611e2c125bbfd9f261c52b`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd86d7a071c031c015596ab2ec6dcfe4cfdf70bd5082935f1016dc604a66c4f`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d5faeab69938596cc25f9c1b52105c67801c5187b3fa64fd5a40d539e40427d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49a6ea2840b6fad1f61ac250caadcda9144931bf249c8044548022a19566fad`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:57 GMT
ADD file:7d35162eea06441e7115c6fd9508802eafee00f64b11a7529a8f125bc67fa95e in / 
# Tue, 01 Mar 2022 02:11:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:55:17 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 10:55:18 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 10:55:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:55:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 10:55:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 10:55:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:56:18 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 01 Mar 2022 10:56:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 10:56:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 10:56:39 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 10:56:40 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 10:56:41 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 01 Mar 2022 10:56:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 10:56:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 10:56:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 10:56:44 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 10:56:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:69bf0018a85cc0775a59a4dbda1b2f2e71086a2d817473f72336bf4d0a83b9d0`  
		Last Modified: Tue, 01 Mar 2022 02:19:15 GMT  
		Size: 25.9 MB (25923140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f3b0034185f805a7eca8287a2a7e1c7083a4a3803aa2ff831381977e362fdd`  
		Last Modified: Tue, 01 Mar 2022 10:57:38 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b11afb5df4d7ceb32be036fdf972d3345cdb7577b89ee1e2f5718768554a3b3`  
		Last Modified: Tue, 01 Mar 2022 10:57:37 GMT  
		Size: 6.5 MB (6549945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01d9cba25fe10102232e70e1e262509477dcbda240c129c62ff2a79c6870918`  
		Last Modified: Tue, 01 Mar 2022 10:57:36 GMT  
		Size: 951.2 KB (951181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75a3508d3b60b5de298e4411ecdd1e54e257ebe20f94a95023c85b62a5c2ad3`  
		Last Modified: Tue, 01 Mar 2022 10:57:36 GMT  
		Size: 79.9 KB (79885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b102dd0eb55f11c90904fccef03a986e2109c1c15ab98820ba9c5821bfe7e07`  
		Last Modified: Tue, 01 Mar 2022 10:57:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84f7d5462854b7642f779f2acad5f45f22257a80b41ed8846f7416e79785332`  
		Last Modified: Tue, 01 Mar 2022 10:57:55 GMT  
		Size: 39.0 MB (39011744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f95c1a2438170f86f990ad088f83767ba8e419f1ac96cdb294ff40c617a7d3`  
		Last Modified: Tue, 01 Mar 2022 10:57:50 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7614832d184c7d5e6c6fb96776cbcd809045a5a10fce32f263ac293ff39195`  
		Last Modified: Tue, 01 Mar 2022 10:57:50 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e269a34ba04007a35b2fa7baec856b1c30f30c697671b8540c393e84a631d49`  
		Last Modified: Tue, 01 Mar 2022 10:57:50 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d4b074057a622e81c2cc34c78ffb522085c5f499dd352f356ccb5ab44f33f7`  
		Last Modified: Tue, 01 Mar 2022 10:57:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:4ef104f0a97f4016f48dea1056742f19863df2184af6db88b83b39d5306a9608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:847e1795b0a0d237d9f94be94629e33d811e0104c8c508897958440e1bdcf06c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10596e5ba2cc278725271cb50463f181896f424dbf4b06da88ce36c6ac59fd18`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:44:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:44:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:44:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:31 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 01 Mar 2022 05:44:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:44:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:44:50 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:44:50 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:44:50 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 01 Mar 2022 05:44:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:44:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:44:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:44:51 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:44:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e132993eb143d25686acdeb919d14985e8a65255f56170cc91230c350b203efa`  
		Last Modified: Tue, 01 Mar 2022 05:45:35 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50404ca1e1b3d297bb3c53a42e386f090eaa10f2d4db26fa324c39a836a18ea2`  
		Last Modified: Tue, 01 Mar 2022 05:45:34 GMT  
		Size: 6.7 MB (6691238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185b4237a163f4ee3d4cbb14cccd38dbfff817f923da22f90651149905d5957f`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 1.3 MB (1258328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a7c7c6b65c07b5de14a76f367630dcdc1f47fb75f959826b67e019b0617ec2`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 293.0 KB (293032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10737976dd7f04dffd2c8080cb3ea3718e864fb550e1f8e3354886937546574`  
		Last Modified: Tue, 01 Mar 2022 05:45:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a11c8284534d8d62c430ef5edd0b754f191ed08eb41a89dd12c88cc42f8876e`  
		Last Modified: Tue, 01 Mar 2022 05:45:52 GMT  
		Size: 49.1 MB (49114456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54d99378c788f80c9ecc1d468356b808769ef6e72ba204e99075047a72d9401`  
		Last Modified: Tue, 01 Mar 2022 05:45:47 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8f2f19f0705503827a4fdc361a6f99896e1875fb4fddbf33721a673720aef6`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bef14bec9c81959285cc9e53e3d5699eabb9be169611e2c125bbfd9f261c52b`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd86d7a071c031c015596ab2ec6dcfe4cfdf70bd5082935f1016dc604a66c4f`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d5faeab69938596cc25f9c1b52105c67801c5187b3fa64fd5a40d539e40427d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49a6ea2840b6fad1f61ac250caadcda9144931bf249c8044548022a19566fad`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:57 GMT
ADD file:7d35162eea06441e7115c6fd9508802eafee00f64b11a7529a8f125bc67fa95e in / 
# Tue, 01 Mar 2022 02:11:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:55:17 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 10:55:18 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 10:55:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:55:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 10:55:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 10:55:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:56:18 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 01 Mar 2022 10:56:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 10:56:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 10:56:39 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 10:56:40 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 10:56:41 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 01 Mar 2022 10:56:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 10:56:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 10:56:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 10:56:44 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 10:56:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:69bf0018a85cc0775a59a4dbda1b2f2e71086a2d817473f72336bf4d0a83b9d0`  
		Last Modified: Tue, 01 Mar 2022 02:19:15 GMT  
		Size: 25.9 MB (25923140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f3b0034185f805a7eca8287a2a7e1c7083a4a3803aa2ff831381977e362fdd`  
		Last Modified: Tue, 01 Mar 2022 10:57:38 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b11afb5df4d7ceb32be036fdf972d3345cdb7577b89ee1e2f5718768554a3b3`  
		Last Modified: Tue, 01 Mar 2022 10:57:37 GMT  
		Size: 6.5 MB (6549945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01d9cba25fe10102232e70e1e262509477dcbda240c129c62ff2a79c6870918`  
		Last Modified: Tue, 01 Mar 2022 10:57:36 GMT  
		Size: 951.2 KB (951181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75a3508d3b60b5de298e4411ecdd1e54e257ebe20f94a95023c85b62a5c2ad3`  
		Last Modified: Tue, 01 Mar 2022 10:57:36 GMT  
		Size: 79.9 KB (79885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b102dd0eb55f11c90904fccef03a986e2109c1c15ab98820ba9c5821bfe7e07`  
		Last Modified: Tue, 01 Mar 2022 10:57:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84f7d5462854b7642f779f2acad5f45f22257a80b41ed8846f7416e79785332`  
		Last Modified: Tue, 01 Mar 2022 10:57:55 GMT  
		Size: 39.0 MB (39011744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f95c1a2438170f86f990ad088f83767ba8e419f1ac96cdb294ff40c617a7d3`  
		Last Modified: Tue, 01 Mar 2022 10:57:50 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7614832d184c7d5e6c6fb96776cbcd809045a5a10fce32f263ac293ff39195`  
		Last Modified: Tue, 01 Mar 2022 10:57:50 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e269a34ba04007a35b2fa7baec856b1c30f30c697671b8540c393e84a631d49`  
		Last Modified: Tue, 01 Mar 2022 10:57:50 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d4b074057a622e81c2cc34c78ffb522085c5f499dd352f356ccb5ab44f33f7`  
		Last Modified: Tue, 01 Mar 2022 10:57:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:4ef104f0a97f4016f48dea1056742f19863df2184af6db88b83b39d5306a9608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:847e1795b0a0d237d9f94be94629e33d811e0104c8c508897958440e1bdcf06c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10596e5ba2cc278725271cb50463f181896f424dbf4b06da88ce36c6ac59fd18`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:44:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:44:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:44:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:31 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 01 Mar 2022 05:44:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:44:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:44:50 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:44:50 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:44:50 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 01 Mar 2022 05:44:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:44:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:44:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:44:51 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:44:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e132993eb143d25686acdeb919d14985e8a65255f56170cc91230c350b203efa`  
		Last Modified: Tue, 01 Mar 2022 05:45:35 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50404ca1e1b3d297bb3c53a42e386f090eaa10f2d4db26fa324c39a836a18ea2`  
		Last Modified: Tue, 01 Mar 2022 05:45:34 GMT  
		Size: 6.7 MB (6691238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185b4237a163f4ee3d4cbb14cccd38dbfff817f923da22f90651149905d5957f`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 1.3 MB (1258328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a7c7c6b65c07b5de14a76f367630dcdc1f47fb75f959826b67e019b0617ec2`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 293.0 KB (293032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10737976dd7f04dffd2c8080cb3ea3718e864fb550e1f8e3354886937546574`  
		Last Modified: Tue, 01 Mar 2022 05:45:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a11c8284534d8d62c430ef5edd0b754f191ed08eb41a89dd12c88cc42f8876e`  
		Last Modified: Tue, 01 Mar 2022 05:45:52 GMT  
		Size: 49.1 MB (49114456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54d99378c788f80c9ecc1d468356b808769ef6e72ba204e99075047a72d9401`  
		Last Modified: Tue, 01 Mar 2022 05:45:47 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8f2f19f0705503827a4fdc361a6f99896e1875fb4fddbf33721a673720aef6`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bef14bec9c81959285cc9e53e3d5699eabb9be169611e2c125bbfd9f261c52b`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd86d7a071c031c015596ab2ec6dcfe4cfdf70bd5082935f1016dc604a66c4f`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d5faeab69938596cc25f9c1b52105c67801c5187b3fa64fd5a40d539e40427d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49a6ea2840b6fad1f61ac250caadcda9144931bf249c8044548022a19566fad`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:57 GMT
ADD file:7d35162eea06441e7115c6fd9508802eafee00f64b11a7529a8f125bc67fa95e in / 
# Tue, 01 Mar 2022 02:11:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:55:17 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 10:55:18 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 10:55:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:55:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 10:55:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 10:55:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:56:18 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 01 Mar 2022 10:56:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 10:56:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 10:56:39 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 10:56:40 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 10:56:41 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 01 Mar 2022 10:56:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 10:56:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 10:56:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 10:56:44 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 10:56:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:69bf0018a85cc0775a59a4dbda1b2f2e71086a2d817473f72336bf4d0a83b9d0`  
		Last Modified: Tue, 01 Mar 2022 02:19:15 GMT  
		Size: 25.9 MB (25923140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f3b0034185f805a7eca8287a2a7e1c7083a4a3803aa2ff831381977e362fdd`  
		Last Modified: Tue, 01 Mar 2022 10:57:38 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b11afb5df4d7ceb32be036fdf972d3345cdb7577b89ee1e2f5718768554a3b3`  
		Last Modified: Tue, 01 Mar 2022 10:57:37 GMT  
		Size: 6.5 MB (6549945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01d9cba25fe10102232e70e1e262509477dcbda240c129c62ff2a79c6870918`  
		Last Modified: Tue, 01 Mar 2022 10:57:36 GMT  
		Size: 951.2 KB (951181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75a3508d3b60b5de298e4411ecdd1e54e257ebe20f94a95023c85b62a5c2ad3`  
		Last Modified: Tue, 01 Mar 2022 10:57:36 GMT  
		Size: 79.9 KB (79885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b102dd0eb55f11c90904fccef03a986e2109c1c15ab98820ba9c5821bfe7e07`  
		Last Modified: Tue, 01 Mar 2022 10:57:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84f7d5462854b7642f779f2acad5f45f22257a80b41ed8846f7416e79785332`  
		Last Modified: Tue, 01 Mar 2022 10:57:55 GMT  
		Size: 39.0 MB (39011744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f95c1a2438170f86f990ad088f83767ba8e419f1ac96cdb294ff40c617a7d3`  
		Last Modified: Tue, 01 Mar 2022 10:57:50 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7614832d184c7d5e6c6fb96776cbcd809045a5a10fce32f263ac293ff39195`  
		Last Modified: Tue, 01 Mar 2022 10:57:50 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e269a34ba04007a35b2fa7baec856b1c30f30c697671b8540c393e84a631d49`  
		Last Modified: Tue, 01 Mar 2022 10:57:50 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d4b074057a622e81c2cc34c78ffb522085c5f499dd352f356ccb5ab44f33f7`  
		Last Modified: Tue, 01 Mar 2022 10:57:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:2b5f3ecf259bf3bf9f0655aa565a51fa3b86fae4e936b169c37ad843bfd5fa52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:822d0f6a1fa1a4468bc77928901cd80cfb9b0679382255660da873c4570f0ea0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87438641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f265241b13e4aafb4f0fda52c6626eb1885d026244944902e2188c4765c30f0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:11 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:43:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:43:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:43:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:28 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 05:43:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:43:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:43:43 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 05:43:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:43:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:43:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:43:44 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:43:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f736067abe3ec6aa7995ab61efa1d9a2b46b4c6a43e237fb15d6ba10bccc8a0`  
		Last Modified: Tue, 01 Mar 2022 05:45:13 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cf0cd8366d641805527862400e1bce25dfe0e4d75301bfca351f6cb51adf42`  
		Last Modified: Tue, 01 Mar 2022 05:45:12 GMT  
		Size: 5.2 MB (5223244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6765d7966078499cee66919d4eae6c448903398520afd4a9af50e628602308dd`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 1.6 MB (1553184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aa553e191057af86f122b236ee318ab2840b814e55f6ed1f843dbf2734c3df`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 295.5 KB (295513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6836a13a921ed1c7d33495e61fbf8c4110efd124ba364aa65719668d915df6`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670b70ba1f6cf592b77e0fbb8feefaa5d19731d115a8f40e5d7ad276b7572c0`  
		Last Modified: Tue, 01 Mar 2022 05:45:15 GMT  
		Size: 49.0 MB (48993167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abf74c316c94beb45bf67044c6219f3205152bbc1a595080a4d646cad125055`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91336f088c386950fab72a2eff4fb6e543ea167051299e920860f25763ddad4c`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec02748684ecc64a7c390d3f95f2556ed75c995c0018dca6d3a5bcb4f10222e`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50b0fab1478c6789e174467f18aec4753c1a77109436988456425cef86c95aa`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3e6dc6d0db2d323fddb035a9432235b94c05601e90dede631eef8984dfbd59c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85578848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ed81158960a991bcb8edcedb33f3bb86af2b2248ff74cadb7932938493c341`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:54:16 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 10:54:17 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 10:54:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:54:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 10:54:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 10:54:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:54:37 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 10:54:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 10:54:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 10:55:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 10:55:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 10:55:02 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 10:55:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 10:55:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 10:55:04 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 10:55:05 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 10:55:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dfcff81d5bffc5f578ce75b1352bd0ec1fbc72e64741076e33fec78f31f8251`  
		Last Modified: Tue, 01 Mar 2022 10:57:14 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd324560c127ebd17fc2f7dadad8e82385cada679ffe92bba01f0ac0dc1147c`  
		Last Modified: Tue, 01 Mar 2022 10:57:13 GMT  
		Size: 5.2 MB (5208018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b903e5b6f9f94a6b822e164537f5fce3c6b17d856646c5ed96bb2ca39b5d4d3a`  
		Last Modified: Tue, 01 Mar 2022 10:57:12 GMT  
		Size: 1.2 MB (1221005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c16dea62989609f7bd2a55428c40adcb00d517c47c9c52e0ec5e76d3e1af6ee`  
		Last Modified: Tue, 01 Mar 2022 10:57:12 GMT  
		Size: 79.1 KB (79098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b3299f2b80a371f9445b89065781cb0070d916bc4cb9cfabc1d747159652cd`  
		Last Modified: Tue, 01 Mar 2022 10:57:12 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4ee9c5380651ad3aa998731b2c7cfceaff37464c95ab95dfb1880628869f77`  
		Last Modified: Tue, 01 Mar 2022 10:57:16 GMT  
		Size: 49.0 MB (49006666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce8d37b711b0d0f9efce1b36bb75dc4823a4d16b320d261e0b1f4aa51cee6c3`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4daebd54e61f91fc444be8b7157fd4bbc43c96e578f49ac98381094e38ffc7a2`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76d8dbd3035c9da1363c7be373af9100c55b68b887d37581e4ea815d31fcef7`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772c4d8177aba4266c7d6008fd9345bca757dc38dbdeeee5eda1b255e2a92b38`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:92fdcff2acc7fd2cd527494e222e1d706dc01024461fb474ccc1780073d6cce9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88524339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec66a11c353a0bd55a16bc9e3df7c1f8436b50846e164d74bbfc74a0e46883dd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 12 Mar 2021 02:32:43 GMT
ADD file:6a0c0cfa71979cf6fdd859dce1e32582f0e55ed382b9e17b77a2001defc2c9db in / 
# Fri, 12 Mar 2021 02:32:50 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 19:37:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 12 Mar 2021 19:37:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 12 Mar 2021 19:40:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 19:40:05 GMT
ENV GOSU_VERSION=1.11
# Fri, 12 Mar 2021 19:40:07 GMT
ENV TINI_VERSION=0.18.0
# Fri, 12 Mar 2021 19:42:25 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Fri, 12 Mar 2021 19:42:43 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Fri, 12 Mar 2021 19:43:05 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Fri, 12 Mar 2021 19:43:21 GMT
ENV COUCHDB_VERSION=3.1.1
# Fri, 12 Mar 2021 19:43:54 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Fri, 12 Mar 2021 19:45:52 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 12 Mar 2021 19:45:58 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 12 Mar 2021 19:46:00 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 12 Mar 2021 19:46:02 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 12 Mar 2021 19:46:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 12 Mar 2021 19:46:17 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 19:46:26 GMT
VOLUME [/opt/couchdb/data]
# Fri, 12 Mar 2021 19:46:33 GMT
EXPOSE 4369 5984 9100
# Fri, 12 Mar 2021 19:46:38 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1d686056fdac1848f4fd78ba2b335502055ffe98c79619e21d0c2fb7db95257e`  
		Last Modified: Fri, 12 Mar 2021 02:45:35 GMT  
		Size: 30.5 MB (30525728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5946aff0873110b0478f9227873604e78c676af18e0dfcd1792e829269a797`  
		Last Modified: Fri, 12 Mar 2021 19:50:07 GMT  
		Size: 3.4 KB (3418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459905054f02704e0526a50655150b20d4241a97be26f9464d997ec614782ce4`  
		Last Modified: Fri, 12 Mar 2021 19:50:07 GMT  
		Size: 7.6 MB (7597596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fddccd01ec6846d36516b8583c310ef4af1b4df7e5ff47e9a5433bb7b1a6f1`  
		Last Modified: Fri, 12 Mar 2021 19:50:06 GMT  
		Size: 1.1 MB (1116351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a9cab3ce9525a6a24f4c1b583168b57d95c20d76c59eeec12e2e975f5bd6a1`  
		Last Modified: Fri, 12 Mar 2021 19:50:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09139ee3a9e5b64209b42b240aa99578fbf71585ea905c2eefccbd7c73cf31f3`  
		Last Modified: Fri, 12 Mar 2021 19:50:04 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7604a9876a71e095a20526d121d304d331595fb5d6a437dad6550e85747fde6e`  
		Last Modified: Fri, 12 Mar 2021 19:50:08 GMT  
		Size: 49.3 MB (49275194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776c0c6539d199f069a602efa1cda1b72fb94ecd2bbc595b97f2df4e19ccb3e6`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc447f4db7d5f4bbcd08dc6219def27d69bad292d2775d1e9cf212ca4277a1be`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 769.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0524070537bcddee5cbfd0aef55fc47bd89ae91bd05bd1919fec7dc348e00d28`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc8c9fce47f6e73a0786f841a42845cb7d720417f296a19ce54fd978cb02f0e`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:59d2c2a05e2e5bc6bf773d686777e07870b63b229e9909281e1d7087b083f74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:ca79518cf7009d4d0f0469fddac30481acbbc5c04dd9e4f68698c9fb209b2379
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80003576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bd847d3676edaaf93238ec7616aeef0990d0d366c26034bf10cefa563907f7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:44:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:44:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:44:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:13 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 01 Mar 2022 05:44:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:44:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:44:28 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:44:28 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:44:28 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 01 Mar 2022 05:44:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:44:29 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:44:29 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:44:29 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:44:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e132993eb143d25686acdeb919d14985e8a65255f56170cc91230c350b203efa`  
		Last Modified: Tue, 01 Mar 2022 05:45:35 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50404ca1e1b3d297bb3c53a42e386f090eaa10f2d4db26fa324c39a836a18ea2`  
		Last Modified: Tue, 01 Mar 2022 05:45:34 GMT  
		Size: 6.7 MB (6691238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185b4237a163f4ee3d4cbb14cccd38dbfff817f923da22f90651149905d5957f`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 1.3 MB (1258328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a7c7c6b65c07b5de14a76f367630dcdc1f47fb75f959826b67e019b0617ec2`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 293.0 KB (293032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30360495bdc30a76fa2b700246ad48767cacf9d445a76c0a5794bb67ffe1ff8a`  
		Last Modified: Tue, 01 Mar 2022 05:45:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c66f25dd672892d6a4f8fe8ada5c2761d4e92d82b846c1b3c0c324f20736ea7`  
		Last Modified: Tue, 01 Mar 2022 05:45:36 GMT  
		Size: 44.6 MB (44600228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fa53bb7e951e99619bfc60a13fe5fdb4627934cd960bfa56b8d32e1f7f7ff4`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ec6b081df4af00c592f2a0bb9b8d16a2e164dbc88510fac16341ee519f518f`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bae1344cc973a946de72a34a50f850ee96245021b199d90b188174ded7f00e3`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc978b9768eef46e866245b0df9c77957340e1ec7cc6935b34d15c38ce7623f5`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5f8dac4539f06028cd3ebb23990a6ccc41654b62c7a7c9839d46d8b1064104f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74612104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96626e4e6b82ff4ca1ff8ca3d3eda6acd2c1edb16fc68c307509a39302d31b0b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:57 GMT
ADD file:7d35162eea06441e7115c6fd9508802eafee00f64b11a7529a8f125bc67fa95e in / 
# Tue, 01 Mar 2022 02:11:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:55:17 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 10:55:18 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 10:55:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:55:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 10:55:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 10:55:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:55:39 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 01 Mar 2022 10:55:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 10:56:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 10:56:01 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 10:56:02 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 10:56:03 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 01 Mar 2022 10:56:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 10:56:04 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 10:56:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 10:56:06 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 10:56:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:69bf0018a85cc0775a59a4dbda1b2f2e71086a2d817473f72336bf4d0a83b9d0`  
		Last Modified: Tue, 01 Mar 2022 02:19:15 GMT  
		Size: 25.9 MB (25923140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f3b0034185f805a7eca8287a2a7e1c7083a4a3803aa2ff831381977e362fdd`  
		Last Modified: Tue, 01 Mar 2022 10:57:38 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b11afb5df4d7ceb32be036fdf972d3345cdb7577b89ee1e2f5718768554a3b3`  
		Last Modified: Tue, 01 Mar 2022 10:57:37 GMT  
		Size: 6.5 MB (6549945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01d9cba25fe10102232e70e1e262509477dcbda240c129c62ff2a79c6870918`  
		Last Modified: Tue, 01 Mar 2022 10:57:36 GMT  
		Size: 951.2 KB (951181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75a3508d3b60b5de298e4411ecdd1e54e257ebe20f94a95023c85b62a5c2ad3`  
		Last Modified: Tue, 01 Mar 2022 10:57:36 GMT  
		Size: 79.9 KB (79885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd20e0726ac6872eb93ae32931222420923cddc35a82d1837bce297f9a1c688`  
		Last Modified: Tue, 01 Mar 2022 10:57:36 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8567e8d6ec7c59ba98a6eb76aebda0812faad30e413650fbef6e472d2df467`  
		Last Modified: Tue, 01 Mar 2022 10:57:39 GMT  
		Size: 41.1 MB (41101035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b812b68765debb885ecc8cfbf4d04e83765c46ce0aedc425b31aeb639b15e2`  
		Last Modified: Tue, 01 Mar 2022 10:57:34 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cd704848b3b3a7577ef01bdc35a296be3225c307b4a590cb45a492395bfaec`  
		Last Modified: Tue, 01 Mar 2022 10:57:34 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c866c2a179409d96705fafdac1defc3fd36da15d4134ddb7723ca83aa03797f3`  
		Last Modified: Tue, 01 Mar 2022 10:57:34 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e167116d1ad782a3daab07acadb106fb1dd956fbb7bf7698577c2fdef9c54f3`  
		Last Modified: Tue, 01 Mar 2022 10:57:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:59d2c2a05e2e5bc6bf773d686777e07870b63b229e9909281e1d7087b083f74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:ca79518cf7009d4d0f0469fddac30481acbbc5c04dd9e4f68698c9fb209b2379
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80003576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bd847d3676edaaf93238ec7616aeef0990d0d366c26034bf10cefa563907f7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:44:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:44:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:44:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:13 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 01 Mar 2022 05:44:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:44:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:44:28 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:44:28 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:44:28 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 01 Mar 2022 05:44:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:44:29 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:44:29 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:44:29 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:44:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e132993eb143d25686acdeb919d14985e8a65255f56170cc91230c350b203efa`  
		Last Modified: Tue, 01 Mar 2022 05:45:35 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50404ca1e1b3d297bb3c53a42e386f090eaa10f2d4db26fa324c39a836a18ea2`  
		Last Modified: Tue, 01 Mar 2022 05:45:34 GMT  
		Size: 6.7 MB (6691238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185b4237a163f4ee3d4cbb14cccd38dbfff817f923da22f90651149905d5957f`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 1.3 MB (1258328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a7c7c6b65c07b5de14a76f367630dcdc1f47fb75f959826b67e019b0617ec2`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 293.0 KB (293032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30360495bdc30a76fa2b700246ad48767cacf9d445a76c0a5794bb67ffe1ff8a`  
		Last Modified: Tue, 01 Mar 2022 05:45:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c66f25dd672892d6a4f8fe8ada5c2761d4e92d82b846c1b3c0c324f20736ea7`  
		Last Modified: Tue, 01 Mar 2022 05:45:36 GMT  
		Size: 44.6 MB (44600228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fa53bb7e951e99619bfc60a13fe5fdb4627934cd960bfa56b8d32e1f7f7ff4`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ec6b081df4af00c592f2a0bb9b8d16a2e164dbc88510fac16341ee519f518f`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bae1344cc973a946de72a34a50f850ee96245021b199d90b188174ded7f00e3`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc978b9768eef46e866245b0df9c77957340e1ec7cc6935b34d15c38ce7623f5`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5f8dac4539f06028cd3ebb23990a6ccc41654b62c7a7c9839d46d8b1064104f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74612104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96626e4e6b82ff4ca1ff8ca3d3eda6acd2c1edb16fc68c307509a39302d31b0b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:57 GMT
ADD file:7d35162eea06441e7115c6fd9508802eafee00f64b11a7529a8f125bc67fa95e in / 
# Tue, 01 Mar 2022 02:11:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:55:17 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 10:55:18 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 10:55:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:55:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 10:55:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 10:55:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:55:39 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 01 Mar 2022 10:55:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 10:56:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 10:56:01 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 10:56:02 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 10:56:03 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 01 Mar 2022 10:56:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 10:56:04 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 10:56:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 10:56:06 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 10:56:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:69bf0018a85cc0775a59a4dbda1b2f2e71086a2d817473f72336bf4d0a83b9d0`  
		Last Modified: Tue, 01 Mar 2022 02:19:15 GMT  
		Size: 25.9 MB (25923140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f3b0034185f805a7eca8287a2a7e1c7083a4a3803aa2ff831381977e362fdd`  
		Last Modified: Tue, 01 Mar 2022 10:57:38 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b11afb5df4d7ceb32be036fdf972d3345cdb7577b89ee1e2f5718768554a3b3`  
		Last Modified: Tue, 01 Mar 2022 10:57:37 GMT  
		Size: 6.5 MB (6549945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01d9cba25fe10102232e70e1e262509477dcbda240c129c62ff2a79c6870918`  
		Last Modified: Tue, 01 Mar 2022 10:57:36 GMT  
		Size: 951.2 KB (951181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75a3508d3b60b5de298e4411ecdd1e54e257ebe20f94a95023c85b62a5c2ad3`  
		Last Modified: Tue, 01 Mar 2022 10:57:36 GMT  
		Size: 79.9 KB (79885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd20e0726ac6872eb93ae32931222420923cddc35a82d1837bce297f9a1c688`  
		Last Modified: Tue, 01 Mar 2022 10:57:36 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8567e8d6ec7c59ba98a6eb76aebda0812faad30e413650fbef6e472d2df467`  
		Last Modified: Tue, 01 Mar 2022 10:57:39 GMT  
		Size: 41.1 MB (41101035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b812b68765debb885ecc8cfbf4d04e83765c46ce0aedc425b31aeb639b15e2`  
		Last Modified: Tue, 01 Mar 2022 10:57:34 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cd704848b3b3a7577ef01bdc35a296be3225c307b4a590cb45a492395bfaec`  
		Last Modified: Tue, 01 Mar 2022 10:57:34 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c866c2a179409d96705fafdac1defc3fd36da15d4134ddb7723ca83aa03797f3`  
		Last Modified: Tue, 01 Mar 2022 10:57:34 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e167116d1ad782a3daab07acadb106fb1dd956fbb7bf7698577c2fdef9c54f3`  
		Last Modified: Tue, 01 Mar 2022 10:57:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:b757f4a1217abc9a218d87777ab8717f875cf33d90ce7c39775a88da2b0adf13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:822d0f6a1fa1a4468bc77928901cd80cfb9b0679382255660da873c4570f0ea0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87438641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f265241b13e4aafb4f0fda52c6626eb1885d026244944902e2188c4765c30f0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:11 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:43:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:43:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:43:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:28 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 05:43:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:43:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:43:43 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 05:43:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:43:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:43:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:43:44 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:43:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f736067abe3ec6aa7995ab61efa1d9a2b46b4c6a43e237fb15d6ba10bccc8a0`  
		Last Modified: Tue, 01 Mar 2022 05:45:13 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cf0cd8366d641805527862400e1bce25dfe0e4d75301bfca351f6cb51adf42`  
		Last Modified: Tue, 01 Mar 2022 05:45:12 GMT  
		Size: 5.2 MB (5223244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6765d7966078499cee66919d4eae6c448903398520afd4a9af50e628602308dd`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 1.6 MB (1553184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aa553e191057af86f122b236ee318ab2840b814e55f6ed1f843dbf2734c3df`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 295.5 KB (295513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6836a13a921ed1c7d33495e61fbf8c4110efd124ba364aa65719668d915df6`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670b70ba1f6cf592b77e0fbb8feefaa5d19731d115a8f40e5d7ad276b7572c0`  
		Last Modified: Tue, 01 Mar 2022 05:45:15 GMT  
		Size: 49.0 MB (48993167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abf74c316c94beb45bf67044c6219f3205152bbc1a595080a4d646cad125055`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91336f088c386950fab72a2eff4fb6e543ea167051299e920860f25763ddad4c`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec02748684ecc64a7c390d3f95f2556ed75c995c0018dca6d3a5bcb4f10222e`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50b0fab1478c6789e174467f18aec4753c1a77109436988456425cef86c95aa`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3e6dc6d0db2d323fddb035a9432235b94c05601e90dede631eef8984dfbd59c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85578848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ed81158960a991bcb8edcedb33f3bb86af2b2248ff74cadb7932938493c341`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:54:16 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 10:54:17 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 10:54:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:54:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 10:54:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 10:54:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:54:37 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 10:54:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 10:54:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 10:55:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 10:55:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 10:55:02 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 10:55:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 10:55:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 10:55:04 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 10:55:05 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 10:55:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dfcff81d5bffc5f578ce75b1352bd0ec1fbc72e64741076e33fec78f31f8251`  
		Last Modified: Tue, 01 Mar 2022 10:57:14 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd324560c127ebd17fc2f7dadad8e82385cada679ffe92bba01f0ac0dc1147c`  
		Last Modified: Tue, 01 Mar 2022 10:57:13 GMT  
		Size: 5.2 MB (5208018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b903e5b6f9f94a6b822e164537f5fce3c6b17d856646c5ed96bb2ca39b5d4d3a`  
		Last Modified: Tue, 01 Mar 2022 10:57:12 GMT  
		Size: 1.2 MB (1221005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c16dea62989609f7bd2a55428c40adcb00d517c47c9c52e0ec5e76d3e1af6ee`  
		Last Modified: Tue, 01 Mar 2022 10:57:12 GMT  
		Size: 79.1 KB (79098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b3299f2b80a371f9445b89065781cb0070d916bc4cb9cfabc1d747159652cd`  
		Last Modified: Tue, 01 Mar 2022 10:57:12 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4ee9c5380651ad3aa998731b2c7cfceaff37464c95ab95dfb1880628869f77`  
		Last Modified: Tue, 01 Mar 2022 10:57:16 GMT  
		Size: 49.0 MB (49006666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce8d37b711b0d0f9efce1b36bb75dc4823a4d16b320d261e0b1f4aa51cee6c3`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4daebd54e61f91fc444be8b7157fd4bbc43c96e578f49ac98381094e38ffc7a2`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76d8dbd3035c9da1363c7be373af9100c55b68b887d37581e4ea815d31fcef7`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772c4d8177aba4266c7d6008fd9345bca757dc38dbdeeee5eda1b255e2a92b38`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.1`

```console
$ docker pull couchdb@sha256:b757f4a1217abc9a218d87777ab8717f875cf33d90ce7c39775a88da2b0adf13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.2.1` - linux; amd64

```console
$ docker pull couchdb@sha256:822d0f6a1fa1a4468bc77928901cd80cfb9b0679382255660da873c4570f0ea0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87438641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f265241b13e4aafb4f0fda52c6626eb1885d026244944902e2188c4765c30f0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:11 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:43:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:43:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:43:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:28 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 05:43:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:43:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:43:43 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 05:43:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:43:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:43:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:43:44 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:43:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f736067abe3ec6aa7995ab61efa1d9a2b46b4c6a43e237fb15d6ba10bccc8a0`  
		Last Modified: Tue, 01 Mar 2022 05:45:13 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cf0cd8366d641805527862400e1bce25dfe0e4d75301bfca351f6cb51adf42`  
		Last Modified: Tue, 01 Mar 2022 05:45:12 GMT  
		Size: 5.2 MB (5223244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6765d7966078499cee66919d4eae6c448903398520afd4a9af50e628602308dd`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 1.6 MB (1553184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aa553e191057af86f122b236ee318ab2840b814e55f6ed1f843dbf2734c3df`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 295.5 KB (295513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6836a13a921ed1c7d33495e61fbf8c4110efd124ba364aa65719668d915df6`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670b70ba1f6cf592b77e0fbb8feefaa5d19731d115a8f40e5d7ad276b7572c0`  
		Last Modified: Tue, 01 Mar 2022 05:45:15 GMT  
		Size: 49.0 MB (48993167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abf74c316c94beb45bf67044c6219f3205152bbc1a595080a4d646cad125055`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91336f088c386950fab72a2eff4fb6e543ea167051299e920860f25763ddad4c`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec02748684ecc64a7c390d3f95f2556ed75c995c0018dca6d3a5bcb4f10222e`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50b0fab1478c6789e174467f18aec4753c1a77109436988456425cef86c95aa`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3e6dc6d0db2d323fddb035a9432235b94c05601e90dede631eef8984dfbd59c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85578848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ed81158960a991bcb8edcedb33f3bb86af2b2248ff74cadb7932938493c341`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:54:16 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 10:54:17 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 10:54:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:54:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 10:54:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 10:54:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:54:37 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 10:54:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 10:54:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 10:55:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 10:55:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 10:55:02 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 10:55:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 10:55:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 10:55:04 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 10:55:05 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 10:55:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dfcff81d5bffc5f578ce75b1352bd0ec1fbc72e64741076e33fec78f31f8251`  
		Last Modified: Tue, 01 Mar 2022 10:57:14 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd324560c127ebd17fc2f7dadad8e82385cada679ffe92bba01f0ac0dc1147c`  
		Last Modified: Tue, 01 Mar 2022 10:57:13 GMT  
		Size: 5.2 MB (5208018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b903e5b6f9f94a6b822e164537f5fce3c6b17d856646c5ed96bb2ca39b5d4d3a`  
		Last Modified: Tue, 01 Mar 2022 10:57:12 GMT  
		Size: 1.2 MB (1221005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c16dea62989609f7bd2a55428c40adcb00d517c47c9c52e0ec5e76d3e1af6ee`  
		Last Modified: Tue, 01 Mar 2022 10:57:12 GMT  
		Size: 79.1 KB (79098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b3299f2b80a371f9445b89065781cb0070d916bc4cb9cfabc1d747159652cd`  
		Last Modified: Tue, 01 Mar 2022 10:57:12 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4ee9c5380651ad3aa998731b2c7cfceaff37464c95ab95dfb1880628869f77`  
		Last Modified: Tue, 01 Mar 2022 10:57:16 GMT  
		Size: 49.0 MB (49006666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce8d37b711b0d0f9efce1b36bb75dc4823a4d16b320d261e0b1f4aa51cee6c3`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4daebd54e61f91fc444be8b7157fd4bbc43c96e578f49ac98381094e38ffc7a2`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76d8dbd3035c9da1363c7be373af9100c55b68b887d37581e4ea815d31fcef7`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772c4d8177aba4266c7d6008fd9345bca757dc38dbdeeee5eda1b255e2a92b38`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:2b5f3ecf259bf3bf9f0655aa565a51fa3b86fae4e936b169c37ad843bfd5fa52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:822d0f6a1fa1a4468bc77928901cd80cfb9b0679382255660da873c4570f0ea0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87438641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f265241b13e4aafb4f0fda52c6626eb1885d026244944902e2188c4765c30f0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:11 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:43:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:43:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:43:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:28 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 05:43:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:43:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:43:43 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 05:43:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:43:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:43:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:43:44 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:43:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f736067abe3ec6aa7995ab61efa1d9a2b46b4c6a43e237fb15d6ba10bccc8a0`  
		Last Modified: Tue, 01 Mar 2022 05:45:13 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cf0cd8366d641805527862400e1bce25dfe0e4d75301bfca351f6cb51adf42`  
		Last Modified: Tue, 01 Mar 2022 05:45:12 GMT  
		Size: 5.2 MB (5223244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6765d7966078499cee66919d4eae6c448903398520afd4a9af50e628602308dd`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 1.6 MB (1553184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aa553e191057af86f122b236ee318ab2840b814e55f6ed1f843dbf2734c3df`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 295.5 KB (295513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6836a13a921ed1c7d33495e61fbf8c4110efd124ba364aa65719668d915df6`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670b70ba1f6cf592b77e0fbb8feefaa5d19731d115a8f40e5d7ad276b7572c0`  
		Last Modified: Tue, 01 Mar 2022 05:45:15 GMT  
		Size: 49.0 MB (48993167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abf74c316c94beb45bf67044c6219f3205152bbc1a595080a4d646cad125055`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91336f088c386950fab72a2eff4fb6e543ea167051299e920860f25763ddad4c`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec02748684ecc64a7c390d3f95f2556ed75c995c0018dca6d3a5bcb4f10222e`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50b0fab1478c6789e174467f18aec4753c1a77109436988456425cef86c95aa`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3e6dc6d0db2d323fddb035a9432235b94c05601e90dede631eef8984dfbd59c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85578848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ed81158960a991bcb8edcedb33f3bb86af2b2248ff74cadb7932938493c341`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:54:16 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 10:54:17 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 10:54:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:54:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 10:54:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 10:54:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:54:37 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 10:54:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 10:54:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 10:55:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 10:55:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 10:55:02 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 10:55:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 10:55:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 10:55:04 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 10:55:05 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 10:55:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dfcff81d5bffc5f578ce75b1352bd0ec1fbc72e64741076e33fec78f31f8251`  
		Last Modified: Tue, 01 Mar 2022 10:57:14 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd324560c127ebd17fc2f7dadad8e82385cada679ffe92bba01f0ac0dc1147c`  
		Last Modified: Tue, 01 Mar 2022 10:57:13 GMT  
		Size: 5.2 MB (5208018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b903e5b6f9f94a6b822e164537f5fce3c6b17d856646c5ed96bb2ca39b5d4d3a`  
		Last Modified: Tue, 01 Mar 2022 10:57:12 GMT  
		Size: 1.2 MB (1221005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c16dea62989609f7bd2a55428c40adcb00d517c47c9c52e0ec5e76d3e1af6ee`  
		Last Modified: Tue, 01 Mar 2022 10:57:12 GMT  
		Size: 79.1 KB (79098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b3299f2b80a371f9445b89065781cb0070d916bc4cb9cfabc1d747159652cd`  
		Last Modified: Tue, 01 Mar 2022 10:57:12 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4ee9c5380651ad3aa998731b2c7cfceaff37464c95ab95dfb1880628869f77`  
		Last Modified: Tue, 01 Mar 2022 10:57:16 GMT  
		Size: 49.0 MB (49006666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce8d37b711b0d0f9efce1b36bb75dc4823a4d16b320d261e0b1f4aa51cee6c3`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4daebd54e61f91fc444be8b7157fd4bbc43c96e578f49ac98381094e38ffc7a2`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76d8dbd3035c9da1363c7be373af9100c55b68b887d37581e4ea815d31fcef7`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772c4d8177aba4266c7d6008fd9345bca757dc38dbdeeee5eda1b255e2a92b38`  
		Last Modified: Tue, 01 Mar 2022 10:57:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:92fdcff2acc7fd2cd527494e222e1d706dc01024461fb474ccc1780073d6cce9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88524339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec66a11c353a0bd55a16bc9e3df7c1f8436b50846e164d74bbfc74a0e46883dd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 12 Mar 2021 02:32:43 GMT
ADD file:6a0c0cfa71979cf6fdd859dce1e32582f0e55ed382b9e17b77a2001defc2c9db in / 
# Fri, 12 Mar 2021 02:32:50 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 19:37:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 12 Mar 2021 19:37:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 12 Mar 2021 19:40:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 19:40:05 GMT
ENV GOSU_VERSION=1.11
# Fri, 12 Mar 2021 19:40:07 GMT
ENV TINI_VERSION=0.18.0
# Fri, 12 Mar 2021 19:42:25 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Fri, 12 Mar 2021 19:42:43 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Fri, 12 Mar 2021 19:43:05 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Fri, 12 Mar 2021 19:43:21 GMT
ENV COUCHDB_VERSION=3.1.1
# Fri, 12 Mar 2021 19:43:54 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Fri, 12 Mar 2021 19:45:52 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 12 Mar 2021 19:45:58 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 12 Mar 2021 19:46:00 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 12 Mar 2021 19:46:02 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 12 Mar 2021 19:46:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 12 Mar 2021 19:46:17 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 19:46:26 GMT
VOLUME [/opt/couchdb/data]
# Fri, 12 Mar 2021 19:46:33 GMT
EXPOSE 4369 5984 9100
# Fri, 12 Mar 2021 19:46:38 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1d686056fdac1848f4fd78ba2b335502055ffe98c79619e21d0c2fb7db95257e`  
		Last Modified: Fri, 12 Mar 2021 02:45:35 GMT  
		Size: 30.5 MB (30525728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5946aff0873110b0478f9227873604e78c676af18e0dfcd1792e829269a797`  
		Last Modified: Fri, 12 Mar 2021 19:50:07 GMT  
		Size: 3.4 KB (3418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459905054f02704e0526a50655150b20d4241a97be26f9464d997ec614782ce4`  
		Last Modified: Fri, 12 Mar 2021 19:50:07 GMT  
		Size: 7.6 MB (7597596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fddccd01ec6846d36516b8583c310ef4af1b4df7e5ff47e9a5433bb7b1a6f1`  
		Last Modified: Fri, 12 Mar 2021 19:50:06 GMT  
		Size: 1.1 MB (1116351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a9cab3ce9525a6a24f4c1b583168b57d95c20d76c59eeec12e2e975f5bd6a1`  
		Last Modified: Fri, 12 Mar 2021 19:50:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09139ee3a9e5b64209b42b240aa99578fbf71585ea905c2eefccbd7c73cf31f3`  
		Last Modified: Fri, 12 Mar 2021 19:50:04 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7604a9876a71e095a20526d121d304d331595fb5d6a437dad6550e85747fde6e`  
		Last Modified: Fri, 12 Mar 2021 19:50:08 GMT  
		Size: 49.3 MB (49275194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776c0c6539d199f069a602efa1cda1b72fb94ecd2bbc595b97f2df4e19ccb3e6`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc447f4db7d5f4bbcd08dc6219def27d69bad292d2775d1e9cf212ca4277a1be`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 769.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0524070537bcddee5cbfd0aef55fc47bd89ae91bd05bd1919fec7dc348e00d28`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc8c9fce47f6e73a0786f841a42845cb7d720417f296a19ce54fd978cb02f0e`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
