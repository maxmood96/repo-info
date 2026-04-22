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
-	[`couchdb:3.5.1`](#couchdb351)
-	[`couchdb:3.5.1-nouveau`](#couchdb351-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:61ab333a29552dc0f3ac33031ea1273b006c8b7b6684331195cb189a01d684a3
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
$ docker pull couchdb@sha256:8a1ba2a19a4c6981e0c903c2c3cd4d59602748cae0246666818090091a1645ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142061148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806bab74c1a4fb65ea85eca0df6cbfaf75e633a8fe12b041057efc047f8c1b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:39:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:39:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 01:40:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:08 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 01:40:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:21 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 01:40:21 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 01:40:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a53138b1d134d26fa4d53d9a2683c90141d93b6e7bd622b6f43e87123095de`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d90394d687f0d05c4649b956181d3345b324547ad48051ae0f177b448cbaaed`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 7.9 MB (7883631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de30193b9c2bab17ecfbda0bcf2a02b262bd8ceafd9a031e19a120fd8c8ac1`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 401.8 KB (401802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cdf8fec417a2a0f21a217bd1809c4ea2cc4f135d262f6b0dcc8078c9a7c044`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 76.5 KB (76502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34740f51296d6acfab2fa462e3b8b1803c8737e466de7bbf0fe68db4d70eae7`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9cb5cf3e1dbb2d8da0afe8b27d8c08d85851a5ced23b121452557a3d3c751`  
		Last Modified: Wed, 22 Apr 2026 01:40:55 GMT  
		Size: 105.5 MB (105457531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de039ed6bde8981bad1b825c982292ee098f74b12f1b17c1ba36cfe31305eb3`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a0c60ddabd96476377d89beffea94139f3abd519bfe2f9addbefde09deac10`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731d920f2d4fef22403d1c15d88dd6c5ea16f0ad88cf18a477d7d5b2f9149f63`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408fb10825775c8965247a872391b284439aa7ca55f219ee2b556cd7af7f8cb`  
		Last Modified: Wed, 22 Apr 2026 01:40:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:3401257267e59435bdfe64dbed14ef495900c94738868e5585c90a8b15a0bf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbd66bb44251165fea91e9881fd9bba6ac85de3eb92c8b0575a83327bd36503`

```dockerfile
```

-	Layers:
	-	`sha256:5885b7c7950112751264b2ad2b6bc61f53aa9cf3d431edef5ecfe318a9857788`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf6461ec6d2ed586ec7996683ff351ab2e0289226e87e971668647852e88b16`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:25741ebc7caf91ed9d3f77b731934efda60e3bc6dbe99f949c8b9c7c41ece647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141419343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe61aed3690aab99f0a235a4263a9f9c9a3785f0786ece5a7e5016bd8b3b9b79`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:53:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:53:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 01:53:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:53:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:53:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:54 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 07 Apr 2026 01:53:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:54:09 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 01:54:09 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 01:54:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25e6100f274d4fad4e9e9ba77343e40c40872e57af49b3ef94501927706423a`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51761292baba02e8cc6b325a8a92561dde7a133b58cf3c62a0c569cc6d64a54a`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 7.7 MB (7692587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2090762aaa6ab1f672c9d8d135fdea412d38773df771cc8db671307e3974e84`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 370.5 KB (370542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebb3ea62ed4b15e333d5a57f21c89fbf6c5b1a599faf3d618de8bbaa3a556e0`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 76.5 KB (76491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662a58e215e3d102141ab8599f618a79c7dfff9c679ac22f74c7ec8e919c40f`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7647cc4028672882df2c04dd03bc161774e5b6e5af8bb8ae5010084a14b0d8eb`  
		Last Modified: Tue, 07 Apr 2026 01:54:28 GMT  
		Size: 105.2 MB (105158122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce06203c4a2555180f96708d6f482320f2cdf9a7b3ffb75e5e4e74d4bfb9345`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcf9e5de529df7d3da223c65065087e3bc92f9fdbe998a9701f20407da98c3c`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40da19d60d2b59538a70925c616adb516c7617dffa57103ac83df030205ffa07`  
		Last Modified: Tue, 07 Apr 2026 01:54:26 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5c716b570fa44399cd2b2f84f0bf550c3c6bfb09147995e76e56ede1639fb5`  
		Last Modified: Tue, 07 Apr 2026 01:54:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:2f59213a4b9318ec690692056b54c0199d9521ab85957dc4a1d240649c7278d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa199a98dfdb472d01efbfc92c66f406f9507dc4580bd8d7575f411577ef3f48`

```dockerfile
```

-	Layers:
	-	`sha256:18388ec4f02d173bb0eae90a09140c1a68edd85cf6802cad4235d708c490cc8e`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6fc0ebcb5833f0098dc74a550a60001bc024f046776f5fcb86da346e048e2a0`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:877bc4f2e9cebde5f6dd5db0625e8c11c1d5fc1450749b8df1ca04eee385183f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225182040bb866da2edada7d68127d3de35b20144022da2ee5092b81a48ff243`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 02:32:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:32:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:54 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 02:32:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:33:12 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 02:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 02:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d77fe6e136fe8121f88c8e24891e2e3ce57d89ace081cd7917cd296bf2781`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c6fd13d86c4615402446553400ddbf811488b8652dfeaf1b30369df23a3d31`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 7.4 MB (7399499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977c5ff033346e1cf892081e6ed41c4dcce967c151c4974c113f4e0406b20fa`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 372.1 KB (372140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28cd61fdf1d3cba5a38ba01f0090a13b851c1b038b6006be4782108f438976`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0df2b1587eda8004175334929323a5430ee32ec7ca0ad93243315dcdfcb1c4d`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d01bd714bd29509eccc7ffd6d42cf54ecb8e91fdd75f00b3a997e6b6adbaf5`  
		Last Modified: Wed, 22 Apr 2026 02:33:35 GMT  
		Size: 104.0 MB (104028166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b90460439c32fbf3c5d889b6093560b179158059ea12b5c62a42ce21380a3fe`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d8c0832e7dbb36e1959f210cc39b9c2f06cded3a0918c38f62da8bb11fe9cc`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846e3f061b916fca388e65c142917fbb47748b12371a1cc92c23fb6caa3881ea`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2a413a15f2d3d0b12253a678fe2d6199c1424fe5ce4d2166204aefde16a81`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:9d0ddb4a733d4cb15d823ccf7fef246af5176b6fbaf3ea6aaef729aa2ddd8e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa74c39c384641d3f8ad817a1c998223d297e3d2453b62a75dbd87fc179ca1c5`

```dockerfile
```

-	Layers:
	-	`sha256:8ae251a1734f9ea12b57e27040fd43078355bb4d78477392c9868f468347d2e5`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cd4bab63ce540f1c9dc037237c27456a1710328cd50cf0b8b3606d11ee6480`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 31.7 KB (31737 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:2306286ff2049d2683cadf51be1d1b4e6f8ee813c1362118bfd5a94b900818ed
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
$ docker pull couchdb@sha256:92cd36a141af320a0e396b3f186e488441d8f5a67a56fac69caf54c5c3c46cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156463311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faeb20718102ff657dc6a855312eda1db690059113db9d85bd5187756618b39`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:40:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:40:01 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 01:40:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 01:40:26 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 01:40:26 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3699c0bcc1c342ae39ac0c5795ee860204401b568e49f81e18539e9709faebc4`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec4bcefbaa2ddc5c5f850b85ffbe49c949b93ad9489b61b3f89cfb34180ffc6`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 7.9 MB (7883583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1541a282306121df04d871433c17b3b800404c707fb599c5a8f234b41af81494`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 77.4 MB (77381418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43036a360cced63fdca47587355730eb6ca55258262dd6b52e46567c797fea4`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 424.1 KB (424148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4a9d479467f6e24a6463d19d8543a2e02c577c849349b0ce23166c5d6413c4`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 99.6 KB (99590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a155df5e2bd3365d2f8221fd2d8deb9cce87e5d7dfe08b67981f61b3a117b392`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc59fcc663abe8a36653dc41b9a13683b410959194a214a77c63a0dfa7bf085`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 42.4 MB (42436440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9545a463d46340f4dc2317a6418c34656c03807cb0c7525ff875b6398b6619c`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7b18530a9ce9367951a915771a5a9595b716fca410e17a0b0ca29f7d32793208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640763ee15e9616ab3dd38c5eeb265cad1434dcea1e1ff5b39533fe8a6382db7`

```dockerfile
```

-	Layers:
	-	`sha256:5e2c3d5c92887b2a975e673d20f4dd218d7c5ffd8478ca1fb73ed1d26c39d70b`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e211ede0fc11c56aa53817d66bfbfdc5b86629c700866acedf8bf91383dbabdd`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9140c1e90c4668c82d1fc0f86d364a7168e5e5430c639e06ced9574b727246e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155360208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b2dcd7bad8ce8fb8847acbd65fbe4a42b612bb57d0daf8e0c3008051ecd79d`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:53:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:53:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 01:53:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:55 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:53:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:54:03 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:03 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 01:54:09 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 01:54:09 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d258e5f7ae5f1971dde27a179beef494fcb76f51d3c104e3148119beda4d3700`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390980d72a7e9ce4615f77822c0074883a0bb99ec4777020c3aafec9cae9cdb6`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 7.7 MB (7692646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621c0229e2890e11b009bf1678ec6ec716eaaa2aaad57d765d09aa549a3bd5`  
		Last Modified: Tue, 07 Apr 2026 01:54:27 GMT  
		Size: 76.7 MB (76718101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c900127ad59ab99b4ccf5f64b211ba22e325179a8f7f82447f4b5aea25cf5186`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 392.8 KB (392774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89177beba55df8f23373c2d7995557c42d596f92129e72b2d67ffb1a1642e4f2`  
		Last Modified: Tue, 07 Apr 2026 01:54:26 GMT  
		Size: 99.5 KB (99532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3562ee2e2f5eab7217bb086ceed411aa4b38b90f8c335aa5ce50ea56160be600`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecf093d8d4a3f64848a09b030db5314c7024b3c3674fa8dbb65f40020cb95e8`  
		Last Modified: Tue, 07 Apr 2026 01:54:27 GMT  
		Size: 42.3 MB (42339106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760f8ee828d2c630dbf3060c62b4fb3341a9604af4956c1773d3f407553229ee`  
		Last Modified: Tue, 07 Apr 2026 01:54:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:2aec03b2f25a41dc9ab40d739ebb8f527e65a2409f667371f0187c69383c00d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022707360bbfa52df4bcd20af17e457c3977dc02aed182962d54b696eefaf59b`

```dockerfile
```

-	Layers:
	-	`sha256:51a4ef763fa18ec15d5e0c79406d11fa3b6e3b5dda8247f3c90d415a637e3799`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 3.7 MB (3656771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:179425382c09ce0abe9a47dfd77e03fe096ee6a77107b8de0934bbfae9cc2773`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:cf725f5fc333ce5583c3a1bdc5c493b3ff2f80035acfe396b5d72fd91f07d765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150105066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1ee5ed95bc2b90e3a3e93630af5058bed2be6512d46323fed497d83ca3e700`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:42 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:42 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 02:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:33:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:33:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:33:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:33:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 02:33:14 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 02:33:14 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c72ad32031623d24cb015f06ba762b3e2605190b489f63556f5c5c54c26a174`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431023707f5f79b1f184ccc237ab2f994f164119af3c3c206647fa1a55b73464`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 7.4 MB (7399462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2ad2d5f20f69c12b06d18d0949dc33bc5c537de9fb95aed5c4c65874835f3f`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 73.2 MB (73153273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5a19190ca30575a8918e6cdfed0b8b8c654e027d95ebe94ec24fe7ec5dda88`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 394.5 KB (394500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a7dee933c23aaf5e57248fcb5d87c1681d5a3a500d396b2f887a7ad0cac2c1`  
		Last Modified: Wed, 22 Apr 2026 02:33:37 GMT  
		Size: 99.7 KB (99663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48cd1f38f663b0e9a746ae67a2609d0a3ca9beab4247f6c3c7a23d7bdfdddd3`  
		Last Modified: Wed, 22 Apr 2026 02:33:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69bf6b994e3969bc5a4a0775754d5e7e81ac5cef4e04e5b8a6af9fa2c1b111`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 42.2 MB (42164727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84df84af6c868bcfbf2fb72ac4d14ad4512360969fabab4f072bda72b3f84fe`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f219414bd8b1573e72b97f12aafa8a21443e21307c127870d5bbe6ca5c90b09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf901c9bcaad01ea643fb50cb373264849c48824372fd6cba1d9291c92aed21`

```dockerfile
```

-	Layers:
	-	`sha256:1deb324532a176476ff3b667e706dcf1f8598d923bdfb9840aa5c45a076f4312`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6937c36d9e12093fba3ca6879d372458ad4f0a5f2e8f698c480182ab3c45c58`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:64beda0d79cc192150ea851a283cee700f9700c999c8b3fd952d970decdd1bfe
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
$ docker pull couchdb@sha256:5428814b65a4e51c61950aacb1eb9f0547e7aa6813e82b5d758c6d01259c6230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139023493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac80a991e305b8c9783e99fe1f055d345c7f4e6bd982f6679d8b3e4e2b31ac4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:40:04 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:40:04 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 01:40:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:17 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 22 Apr 2026 01:40:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 01:40:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:40:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:30 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 01:40:30 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 01:40:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85e89b64bb046d626a907734ef7a9b40ff6c4ef8a01deedcdfc36dd6782d464`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b9cc78d51139e05e4e4b210d2e65d57a180a134a39598cf1ae533d15928ed7`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 7.9 MB (7883540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316153b895f76daaab8076cf011b6c8e5a177f55e48562af0e7a05283d8503fd`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 401.8 KB (401794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e805a04eabbeedab61d24437ad992d1f1fcec69bb934507f7d5e504ff607197`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 76.5 KB (76512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b66b657a671ac4a21dbfc6ae4cdcd7dcb43c9b2da99f8e926cd64c3a10382e`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f68875914be9bcaff4d3c42cf902b182678731d00e048ad985576031262b0f`  
		Last Modified: Wed, 22 Apr 2026 01:40:45 GMT  
		Size: 102.4 MB (102419968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423a9813d2f3ec90378081d6ad677feb6bab0cc43f7e777eb0b996eb78c92634`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d00bc280812ffb50673789dd6057b5c98f5d6bfb7b45b3ec18f9f32ed69e600`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ecd9d2ecd1bbff49f937712a0b920aad8ff0b3999ccd9b353d7685810cf96`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e6be45ae454f7dcb0b9845c58bceee7bdbc6668b3e1a70821c2eb35e3d0bc`  
		Last Modified: Wed, 22 Apr 2026 01:40:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:048c65e3a362c69f9cb3f18fd552ac18243e9d2e061d5f2768860080a1a6c3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b491106a4e23d95588bfd3c1184cb6e02336be9456a5ce7231db016b58c32012`

```dockerfile
```

-	Layers:
	-	`sha256:9ce1ad516d4e59603081f39ace6f4d622459aa4e9c14613dc9741c903b8c1d13`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb217b54b7504de5ae3d779581e2bb214209e93e933552a6b6f84ea8d375037`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e8b83813b3299c340511256900d7b8070839b467c6bffdeea7feb666c8b35ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138430400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ad3b510e2df1fa690ccf4ee313ff352396ea3a155e4ca1b018bfc3435efda4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:53:49 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:53:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 01:53:56 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:53:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:54:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:04 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 07 Apr 2026 01:54:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:54:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 01:54:16 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 01:54:16 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 01:54:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 01:54:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:54:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:54:16 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 01:54:16 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 01:54:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333b0923256009c9b4f47b48460d2ebf94c266585dd44f8d8c7052e3b30695f7`  
		Last Modified: Tue, 07 Apr 2026 01:54:30 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98f4fdb732465ca12dc6f95af56a9eec7525a7fe0ed6652b9b1c8ab01bb9f07`  
		Last Modified: Tue, 07 Apr 2026 01:54:30 GMT  
		Size: 7.7 MB (7692711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e01ebf0501fc43acae56530e935f79d4f4fe1adf6450f33720b8a89508906ec`  
		Last Modified: Tue, 07 Apr 2026 01:54:30 GMT  
		Size: 370.5 KB (370531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a41e3238b3187b65614a23c123381f6d53bb69febc2c96abe0a42603d71eb8`  
		Last Modified: Tue, 07 Apr 2026 01:54:30 GMT  
		Size: 76.5 KB (76513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6e828cfc50229de0c5dda4388d3c1d4b13d1421eb1323d34810ab6749a752e`  
		Last Modified: Tue, 07 Apr 2026 01:54:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a983f08d7d77566ad648db6741aff7416f4b02a89500eb33bb53d7d7a7248d`  
		Last Modified: Tue, 07 Apr 2026 01:54:34 GMT  
		Size: 102.2 MB (102169041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e14919234f63d25138edcfec3c8540f61c0468902a138437d3a64f1f4949fa5`  
		Last Modified: Tue, 07 Apr 2026 01:54:31 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a133c9358f4b1b282ded2dcaae15ea468bdc05794f95e057fab0964d437abb2b`  
		Last Modified: Tue, 07 Apr 2026 01:54:32 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9c567242f160a4afbf745d2a3fdc26774ea7d393511d91bcc16e20d6d06a16`  
		Last Modified: Tue, 07 Apr 2026 01:54:32 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dd72c04008677544a74776aa2215933bdb8ffc329da17c2bc5549b405cabd6`  
		Last Modified: Tue, 07 Apr 2026 01:54:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:090634e7c6506f11606e5b1499477ba0670324455cb7f11a59f1a211adbce6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596e755ac61bb03ea0a77b8d6f544a76b0f289ce4bc32101c711ae9a07a81a83`

```dockerfile
```

-	Layers:
	-	`sha256:b5696a22a091f3aead722430e856f9187e9d281f6b6423642c44541be2da1af2`  
		Last Modified: Tue, 07 Apr 2026 01:54:30 GMT  
		Size: 4.1 MB (4125664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ac97767f324e135edff981444072d2936f05b5bc6e6edbad595604a6ed09fb`  
		Last Modified: Tue, 07 Apr 2026 01:54:30 GMT  
		Size: 31.3 KB (31317 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:fe69688f8a8a9fc7e558a72a4ac5cbead8abdc92ed794bdff5d2f857bad642ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135801559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0db4c4038cfbb749e099a7e7d629ac585ff220f732a490ed133003b519f36b8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 02:32:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:32:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:54 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 22 Apr 2026 02:33:09 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:33:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 02:33:25 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 02:33:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d77fe6e136fe8121f88c8e24891e2e3ce57d89ace081cd7917cd296bf2781`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c6fd13d86c4615402446553400ddbf811488b8652dfeaf1b30369df23a3d31`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 7.4 MB (7399499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977c5ff033346e1cf892081e6ed41c4dcce967c151c4974c113f4e0406b20fa`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 372.1 KB (372140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28cd61fdf1d3cba5a38ba01f0090a13b851c1b038b6006be4782108f438976`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51021d0991e21fdae5f82d151b8818f1a910d821b0e80cb74fe15fc244a157a`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd3c1758f3d8b894c1ccb4b9432456ec5f332ca1c028a3e5278050de5d9c034`  
		Last Modified: Wed, 22 Apr 2026 02:33:47 GMT  
		Size: 101.1 MB (101056387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1965c3cd4dcf03b89b4dcb613be010d7ad5bbebabff5b10e81f148444a4cf608`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6177a75af20c10e9eb4655cd66317f4b2a301ea9b0e8c6e3abe07b5764b33c3c`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f72a9ff25a97ad60e552b712c9bfc05a9ab2fd0d6801b33a3f77dcb8404fee1`  
		Last Modified: Wed, 22 Apr 2026 02:33:46 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf942b5dda4ee12459bead808567170200716b81bd5d5c791a10ca115b84c57`  
		Last Modified: Wed, 22 Apr 2026 02:33:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:ad5ccbec04df2f72fba8d7aeaa688573aba52ead2f2695672ab053b1fa88fee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3c5cbe3d0f03b9458aa22af27bbc6a0c259bb83ad5d180c6bbec5aca90b63e`

```dockerfile
```

-	Layers:
	-	`sha256:906b1434453c91788d486dd4a8dfd300a2576c794da0ae58cac2badd47a5530e`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2848d89da3b96589c1887032f7faf2ffb3ee0c02eee8826a01e50839cac6e44c`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:d52591b080e33aa21600c9f29e5f842c0d747ecd7254b5f7d47f080518fb7089
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
$ docker pull couchdb@sha256:6bef3997a59a7cb2920cd0a39773e7dac18a2a3f22b328a06ad1b3cabc1ac171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5637cb95392efea21d281e2b5aeabe64617798d49764037e46f57ae8048e6fab`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:40:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:40:06 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 01:40:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:23 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:23 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 01:40:27 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 01:40:27 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 01:40:27 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 01:40:27 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74980224cf758de90dca7d23ae81256f9bea075d12f56a4c3d2b1a37cf9a06c`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d04cecb0b1c5f6c24ed1d7536d1046e510e60e76d1ac9e79ca3e909c3085ed8`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 7.9 MB (7883603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e1af881e02d1c55b51d883ccf7f355c8e5e11d844edc411bd7c313527476cc`  
		Last Modified: Wed, 22 Apr 2026 01:40:50 GMT  
		Size: 77.4 MB (77381391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a31b79bfbbb57e9748c5a1f401e54713de3df23116b590290f1c6340452cc8`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 424.1 KB (424149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca78edf048bf6db58a97238f1a19c1bd6b5641ce16e15d2339754848a609a07`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 99.6 KB (99563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fc33302856959d39043c6a3f8956473a95630fbfa3497f5da8281bd1de8461`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356f9514689b1e9a5798e4606de863da2fa12c9e2625197bc67ed0cd8d4881c`  
		Last Modified: Wed, 22 Apr 2026 01:40:53 GMT  
		Size: 42.4 MB (42436138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31b4d7022e7af9a70b856a7c10e7e57ae93b7cb2caf9a72081413cd2d1b0e9f`  
		Last Modified: Wed, 22 Apr 2026 01:40:45 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:2cc08aa418b8ab792b15bbab673b9a5cf6e04dd8321db4c45db679beb118fba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54357c6db70c52095c0fa62fa4b956c14c004b21cfaf5dcb73cd8bbdedcae88`

```dockerfile
```

-	Layers:
	-	`sha256:ab5ea45e715310cad5acbfa29412e9118bc79c53a09eadd100588313927e5e3d`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 3.7 MB (3657789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a977a4cf972d069555b80ca29d7f9f6b1f205edfd4242931bf82d4436772bdb1`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:31cd35f39e090d1399586411eba70be29b6559d3154d3e68dc9774c4ffef8e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155359193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6b77c144bcdd007948c69b7bf72ed0b7446c984b71f415b9caeeb0052dbcaa`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:53:42 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:53:42 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 01:53:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:56 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:53:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:54:03 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:03 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:54:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 01:54:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 01:54:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 01:54:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 01:54:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbe4303bd634e433bad13e56a624b79813232f31588866523f27367b703536`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36879bf240b71d5f6ec1daf490f630aa31d3b6d15c0b2c213e09e660a23852f4`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 7.7 MB (7692639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99610dac3f8533dceaf66f91975c0d94ccb2609c2ffff95ea747132ff6f84a3`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 76.7 MB (76718126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da52a8d45ad5894e0106a9238542ec4ebd88ceb2ed170fdcdbfd03f05082b6e6`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 392.8 KB (392764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8de29903348f6ebf534e05ee8d72bfe2b298a9514992494f39f7641c804b81`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 99.5 KB (99491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3562ee2e2f5eab7217bb086ceed411aa4b38b90f8c335aa5ce50ea56160be600`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ba84238f0c87f98015ec9c84af4858ea0332a684bc5fb82d9fa13d4984333d`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 42.3 MB (42338123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821758f099d8e207718fbeb30e144d8c335be8281fc6accb9f30ea9ca5eed818`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:04b8267b9c537ae01f05b59cd691fad148a56bd824565afa38d6deef7ad1fbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c470a9b7156737bc94333ec58ad096e56ae8323db44359a7ae75e0a3f8441a04`

```dockerfile
```

-	Layers:
	-	`sha256:55f11ca8b1491eaa3537e2e4e932d02e0eab0bcca95ccd8152e6a59890294332`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 3.7 MB (3656453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0fa2e2d910ea4e1dc8791e25d849e7f6d495f31ca84bf308e455c72349ecec1`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 24.4 KB (24384 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:87d62235c5899f6b8907d6d4d6052e86ee6f8be2877b17b0af7052abc6c4042c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150103452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124203b7fdd33c82e55e3019842da1b15a5aadf747dbed322f77acb8361e075b`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:33:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:33:53 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 02:33:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:34:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:34:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:34:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:34:15 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:34:16 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:34:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 02:34:26 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 02:34:26 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 02:34:26 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 02:34:26 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914b93210cd7104243e5ef6ab5d6244ddaaa8e4de085d219730706cca0fe3d94`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dc676250eb3edb1c12ff88d7c3c575684b2b29286cc757826511fe4e5c3b0c`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 7.4 MB (7399490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d64a4027355a4a1e6262832fd770bc7012502c2b8fb82b11c7aa24f61cb3eae`  
		Last Modified: Wed, 22 Apr 2026 02:34:51 GMT  
		Size: 73.2 MB (73153346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b93a5b58af5fadbdabc90fd9607a01b6bca90a9c02603eae57979ebbd6eb6f8`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 394.5 KB (394515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504f5f76d401a46b2de1aac91467563b4e016283bd372f4f827c4ee31a4c5a49`  
		Last Modified: Wed, 22 Apr 2026 02:34:50 GMT  
		Size: 99.6 KB (99649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ad49d758a4bf3d10640373f237ee766837d40f3e80ac364ea8d6b014e5af8e`  
		Last Modified: Wed, 22 Apr 2026 02:34:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c474d8ca8378054e459b4a6a175057200e4e5828617e831437708f80e8073b`  
		Last Modified: Wed, 22 Apr 2026 02:34:52 GMT  
		Size: 42.2 MB (42163011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cce7429a46657a931d21e39205ddf60884e8a4843d28e80299597da82c7ba4d`  
		Last Modified: Wed, 22 Apr 2026 02:34:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c93092bd194fec0fd074d3d576df7bed91f15f4c7bb55bfd1528bcf0c8165594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d455e39274286509abd19f51cd4e94639bb87b113642f3be88adab47df5b060`

```dockerfile
```

-	Layers:
	-	`sha256:1a9ff45b41bfd52d342877ae4a67e32edb70f7d551bf260c870ccd22a27e31fb`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 3.6 MB (3648318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e65e2d2a818933f9de43c39f59679a82b6fb23b52b14ea074e9cd26464d9c295`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:64beda0d79cc192150ea851a283cee700f9700c999c8b3fd952d970decdd1bfe
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
$ docker pull couchdb@sha256:5428814b65a4e51c61950aacb1eb9f0547e7aa6813e82b5d758c6d01259c6230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139023493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac80a991e305b8c9783e99fe1f055d345c7f4e6bd982f6679d8b3e4e2b31ac4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:40:04 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:40:04 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 01:40:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:17 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 22 Apr 2026 01:40:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 01:40:29 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 01:40:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:40:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:30 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 01:40:30 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 01:40:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85e89b64bb046d626a907734ef7a9b40ff6c4ef8a01deedcdfc36dd6782d464`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b9cc78d51139e05e4e4b210d2e65d57a180a134a39598cf1ae533d15928ed7`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 7.9 MB (7883540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316153b895f76daaab8076cf011b6c8e5a177f55e48562af0e7a05283d8503fd`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 401.8 KB (401794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e805a04eabbeedab61d24437ad992d1f1fcec69bb934507f7d5e504ff607197`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 76.5 KB (76512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b66b657a671ac4a21dbfc6ae4cdcd7dcb43c9b2da99f8e926cd64c3a10382e`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f68875914be9bcaff4d3c42cf902b182678731d00e048ad985576031262b0f`  
		Last Modified: Wed, 22 Apr 2026 01:40:45 GMT  
		Size: 102.4 MB (102419968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423a9813d2f3ec90378081d6ad677feb6bab0cc43f7e777eb0b996eb78c92634`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d00bc280812ffb50673789dd6057b5c98f5d6bfb7b45b3ec18f9f32ed69e600`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ecd9d2ecd1bbff49f937712a0b920aad8ff0b3999ccd9b353d7685810cf96`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e6be45ae454f7dcb0b9845c58bceee7bdbc6668b3e1a70821c2eb35e3d0bc`  
		Last Modified: Wed, 22 Apr 2026 01:40:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:048c65e3a362c69f9cb3f18fd552ac18243e9d2e061d5f2768860080a1a6c3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b491106a4e23d95588bfd3c1184cb6e02336be9456a5ce7231db016b58c32012`

```dockerfile
```

-	Layers:
	-	`sha256:9ce1ad516d4e59603081f39ace6f4d622459aa4e9c14613dc9741c903b8c1d13`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb217b54b7504de5ae3d779581e2bb214209e93e933552a6b6f84ea8d375037`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e8b83813b3299c340511256900d7b8070839b467c6bffdeea7feb666c8b35ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138430400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ad3b510e2df1fa690ccf4ee313ff352396ea3a155e4ca1b018bfc3435efda4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:53:49 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:53:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 01:53:56 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:53:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:54:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:04 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 07 Apr 2026 01:54:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:54:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 01:54:16 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 01:54:16 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 01:54:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 01:54:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:54:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:54:16 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 01:54:16 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 01:54:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333b0923256009c9b4f47b48460d2ebf94c266585dd44f8d8c7052e3b30695f7`  
		Last Modified: Tue, 07 Apr 2026 01:54:30 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98f4fdb732465ca12dc6f95af56a9eec7525a7fe0ed6652b9b1c8ab01bb9f07`  
		Last Modified: Tue, 07 Apr 2026 01:54:30 GMT  
		Size: 7.7 MB (7692711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e01ebf0501fc43acae56530e935f79d4f4fe1adf6450f33720b8a89508906ec`  
		Last Modified: Tue, 07 Apr 2026 01:54:30 GMT  
		Size: 370.5 KB (370531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a41e3238b3187b65614a23c123381f6d53bb69febc2c96abe0a42603d71eb8`  
		Last Modified: Tue, 07 Apr 2026 01:54:30 GMT  
		Size: 76.5 KB (76513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6e828cfc50229de0c5dda4388d3c1d4b13d1421eb1323d34810ab6749a752e`  
		Last Modified: Tue, 07 Apr 2026 01:54:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a983f08d7d77566ad648db6741aff7416f4b02a89500eb33bb53d7d7a7248d`  
		Last Modified: Tue, 07 Apr 2026 01:54:34 GMT  
		Size: 102.2 MB (102169041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e14919234f63d25138edcfec3c8540f61c0468902a138437d3a64f1f4949fa5`  
		Last Modified: Tue, 07 Apr 2026 01:54:31 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a133c9358f4b1b282ded2dcaae15ea468bdc05794f95e057fab0964d437abb2b`  
		Last Modified: Tue, 07 Apr 2026 01:54:32 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9c567242f160a4afbf745d2a3fdc26774ea7d393511d91bcc16e20d6d06a16`  
		Last Modified: Tue, 07 Apr 2026 01:54:32 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dd72c04008677544a74776aa2215933bdb8ffc329da17c2bc5549b405cabd6`  
		Last Modified: Tue, 07 Apr 2026 01:54:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:090634e7c6506f11606e5b1499477ba0670324455cb7f11a59f1a211adbce6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596e755ac61bb03ea0a77b8d6f544a76b0f289ce4bc32101c711ae9a07a81a83`

```dockerfile
```

-	Layers:
	-	`sha256:b5696a22a091f3aead722430e856f9187e9d281f6b6423642c44541be2da1af2`  
		Last Modified: Tue, 07 Apr 2026 01:54:30 GMT  
		Size: 4.1 MB (4125664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ac97767f324e135edff981444072d2936f05b5bc6e6edbad595604a6ed09fb`  
		Last Modified: Tue, 07 Apr 2026 01:54:30 GMT  
		Size: 31.3 KB (31317 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:fe69688f8a8a9fc7e558a72a4ac5cbead8abdc92ed794bdff5d2f857bad642ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135801559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0db4c4038cfbb749e099a7e7d629ac585ff220f732a490ed133003b519f36b8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 02:32:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:32:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:54 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 22 Apr 2026 02:33:09 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 02:33:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:33:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 02:33:25 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 02:33:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d77fe6e136fe8121f88c8e24891e2e3ce57d89ace081cd7917cd296bf2781`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c6fd13d86c4615402446553400ddbf811488b8652dfeaf1b30369df23a3d31`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 7.4 MB (7399499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977c5ff033346e1cf892081e6ed41c4dcce967c151c4974c113f4e0406b20fa`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 372.1 KB (372140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28cd61fdf1d3cba5a38ba01f0090a13b851c1b038b6006be4782108f438976`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51021d0991e21fdae5f82d151b8818f1a910d821b0e80cb74fe15fc244a157a`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd3c1758f3d8b894c1ccb4b9432456ec5f332ca1c028a3e5278050de5d9c034`  
		Last Modified: Wed, 22 Apr 2026 02:33:47 GMT  
		Size: 101.1 MB (101056387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1965c3cd4dcf03b89b4dcb613be010d7ad5bbebabff5b10e81f148444a4cf608`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6177a75af20c10e9eb4655cd66317f4b2a301ea9b0e8c6e3abe07b5764b33c3c`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f72a9ff25a97ad60e552b712c9bfc05a9ab2fd0d6801b33a3f77dcb8404fee1`  
		Last Modified: Wed, 22 Apr 2026 02:33:46 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf942b5dda4ee12459bead808567170200716b81bd5d5c791a10ca115b84c57`  
		Last Modified: Wed, 22 Apr 2026 02:33:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ad5ccbec04df2f72fba8d7aeaa688573aba52ead2f2695672ab053b1fa88fee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3c5cbe3d0f03b9458aa22af27bbc6a0c259bb83ad5d180c6bbec5aca90b63e`

```dockerfile
```

-	Layers:
	-	`sha256:906b1434453c91788d486dd4a8dfd300a2576c794da0ae58cac2badd47a5530e`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2848d89da3b96589c1887032f7faf2ffb3ee0c02eee8826a01e50839cac6e44c`  
		Last Modified: Wed, 22 Apr 2026 02:33:45 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:d52591b080e33aa21600c9f29e5f842c0d747ecd7254b5f7d47f080518fb7089
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
$ docker pull couchdb@sha256:6bef3997a59a7cb2920cd0a39773e7dac18a2a3f22b328a06ad1b3cabc1ac171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5637cb95392efea21d281e2b5aeabe64617798d49764037e46f57ae8048e6fab`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:40:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:40:06 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 01:40:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:23 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:23 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 01:40:27 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 01:40:27 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 01:40:27 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 01:40:27 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74980224cf758de90dca7d23ae81256f9bea075d12f56a4c3d2b1a37cf9a06c`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d04cecb0b1c5f6c24ed1d7536d1046e510e60e76d1ac9e79ca3e909c3085ed8`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 7.9 MB (7883603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e1af881e02d1c55b51d883ccf7f355c8e5e11d844edc411bd7c313527476cc`  
		Last Modified: Wed, 22 Apr 2026 01:40:50 GMT  
		Size: 77.4 MB (77381391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a31b79bfbbb57e9748c5a1f401e54713de3df23116b590290f1c6340452cc8`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 424.1 KB (424149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca78edf048bf6db58a97238f1a19c1bd6b5641ce16e15d2339754848a609a07`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 99.6 KB (99563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fc33302856959d39043c6a3f8956473a95630fbfa3497f5da8281bd1de8461`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356f9514689b1e9a5798e4606de863da2fa12c9e2625197bc67ed0cd8d4881c`  
		Last Modified: Wed, 22 Apr 2026 01:40:53 GMT  
		Size: 42.4 MB (42436138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31b4d7022e7af9a70b856a7c10e7e57ae93b7cb2caf9a72081413cd2d1b0e9f`  
		Last Modified: Wed, 22 Apr 2026 01:40:45 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:2cc08aa418b8ab792b15bbab673b9a5cf6e04dd8321db4c45db679beb118fba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54357c6db70c52095c0fa62fa4b956c14c004b21cfaf5dcb73cd8bbdedcae88`

```dockerfile
```

-	Layers:
	-	`sha256:ab5ea45e715310cad5acbfa29412e9118bc79c53a09eadd100588313927e5e3d`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 3.7 MB (3657789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a977a4cf972d069555b80ca29d7f9f6b1f205edfd4242931bf82d4436772bdb1`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:31cd35f39e090d1399586411eba70be29b6559d3154d3e68dc9774c4ffef8e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155359193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6b77c144bcdd007948c69b7bf72ed0b7446c984b71f415b9caeeb0052dbcaa`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:53:42 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:53:42 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 01:53:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:56 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:53:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:54:03 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:03 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:54:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 01:54:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 01:54:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 01:54:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 01:54:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbe4303bd634e433bad13e56a624b79813232f31588866523f27367b703536`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36879bf240b71d5f6ec1daf490f630aa31d3b6d15c0b2c213e09e660a23852f4`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 7.7 MB (7692639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99610dac3f8533dceaf66f91975c0d94ccb2609c2ffff95ea747132ff6f84a3`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 76.7 MB (76718126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da52a8d45ad5894e0106a9238542ec4ebd88ceb2ed170fdcdbfd03f05082b6e6`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 392.8 KB (392764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8de29903348f6ebf534e05ee8d72bfe2b298a9514992494f39f7641c804b81`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 99.5 KB (99491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3562ee2e2f5eab7217bb086ceed411aa4b38b90f8c335aa5ce50ea56160be600`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ba84238f0c87f98015ec9c84af4858ea0332a684bc5fb82d9fa13d4984333d`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 42.3 MB (42338123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821758f099d8e207718fbeb30e144d8c335be8281fc6accb9f30ea9ca5eed818`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:04b8267b9c537ae01f05b59cd691fad148a56bd824565afa38d6deef7ad1fbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c470a9b7156737bc94333ec58ad096e56ae8323db44359a7ae75e0a3f8441a04`

```dockerfile
```

-	Layers:
	-	`sha256:55f11ca8b1491eaa3537e2e4e932d02e0eab0bcca95ccd8152e6a59890294332`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 3.7 MB (3656453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0fa2e2d910ea4e1dc8791e25d849e7f6d495f31ca84bf308e455c72349ecec1`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 24.4 KB (24384 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:87d62235c5899f6b8907d6d4d6052e86ee6f8be2877b17b0af7052abc6c4042c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150103452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124203b7fdd33c82e55e3019842da1b15a5aadf747dbed322f77acb8361e075b`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:33:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:33:53 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 02:33:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:34:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:34:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:34:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:34:15 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:34:16 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:34:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 02:34:26 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 02:34:26 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 02:34:26 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 02:34:26 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914b93210cd7104243e5ef6ab5d6244ddaaa8e4de085d219730706cca0fe3d94`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dc676250eb3edb1c12ff88d7c3c575684b2b29286cc757826511fe4e5c3b0c`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 7.4 MB (7399490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d64a4027355a4a1e6262832fd770bc7012502c2b8fb82b11c7aa24f61cb3eae`  
		Last Modified: Wed, 22 Apr 2026 02:34:51 GMT  
		Size: 73.2 MB (73153346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b93a5b58af5fadbdabc90fd9607a01b6bca90a9c02603eae57979ebbd6eb6f8`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 394.5 KB (394515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504f5f76d401a46b2de1aac91467563b4e016283bd372f4f827c4ee31a4c5a49`  
		Last Modified: Wed, 22 Apr 2026 02:34:50 GMT  
		Size: 99.6 KB (99649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ad49d758a4bf3d10640373f237ee766837d40f3e80ac364ea8d6b014e5af8e`  
		Last Modified: Wed, 22 Apr 2026 02:34:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c474d8ca8378054e459b4a6a175057200e4e5828617e831437708f80e8073b`  
		Last Modified: Wed, 22 Apr 2026 02:34:52 GMT  
		Size: 42.2 MB (42163011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cce7429a46657a931d21e39205ddf60884e8a4843d28e80299597da82c7ba4d`  
		Last Modified: Wed, 22 Apr 2026 02:34:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c93092bd194fec0fd074d3d576df7bed91f15f4c7bb55bfd1528bcf0c8165594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d455e39274286509abd19f51cd4e94639bb87b113642f3be88adab47df5b060`

```dockerfile
```

-	Layers:
	-	`sha256:1a9ff45b41bfd52d342877ae4a67e32edb70f7d551bf260c870ccd22a27e31fb`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 3.6 MB (3648318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e65e2d2a818933f9de43c39f59679a82b6fb23b52b14ea074e9cd26464d9c295`  
		Last Modified: Wed, 22 Apr 2026 02:34:49 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:61ab333a29552dc0f3ac33031ea1273b006c8b7b6684331195cb189a01d684a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5` - linux; amd64

```console
$ docker pull couchdb@sha256:8a1ba2a19a4c6981e0c903c2c3cd4d59602748cae0246666818090091a1645ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142061148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806bab74c1a4fb65ea85eca0df6cbfaf75e633a8fe12b041057efc047f8c1b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:39:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:39:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 01:40:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:08 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 01:40:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:21 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 01:40:21 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 01:40:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a53138b1d134d26fa4d53d9a2683c90141d93b6e7bd622b6f43e87123095de`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d90394d687f0d05c4649b956181d3345b324547ad48051ae0f177b448cbaaed`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 7.9 MB (7883631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de30193b9c2bab17ecfbda0bcf2a02b262bd8ceafd9a031e19a120fd8c8ac1`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 401.8 KB (401802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cdf8fec417a2a0f21a217bd1809c4ea2cc4f135d262f6b0dcc8078c9a7c044`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 76.5 KB (76502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34740f51296d6acfab2fa462e3b8b1803c8737e466de7bbf0fe68db4d70eae7`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9cb5cf3e1dbb2d8da0afe8b27d8c08d85851a5ced23b121452557a3d3c751`  
		Last Modified: Wed, 22 Apr 2026 01:40:55 GMT  
		Size: 105.5 MB (105457531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de039ed6bde8981bad1b825c982292ee098f74b12f1b17c1ba36cfe31305eb3`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a0c60ddabd96476377d89beffea94139f3abd519bfe2f9addbefde09deac10`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731d920f2d4fef22403d1c15d88dd6c5ea16f0ad88cf18a477d7d5b2f9149f63`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408fb10825775c8965247a872391b284439aa7ca55f219ee2b556cd7af7f8cb`  
		Last Modified: Wed, 22 Apr 2026 01:40:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:3401257267e59435bdfe64dbed14ef495900c94738868e5585c90a8b15a0bf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbd66bb44251165fea91e9881fd9bba6ac85de3eb92c8b0575a83327bd36503`

```dockerfile
```

-	Layers:
	-	`sha256:5885b7c7950112751264b2ad2b6bc61f53aa9cf3d431edef5ecfe318a9857788`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf6461ec6d2ed586ec7996683ff351ab2e0289226e87e971668647852e88b16`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:25741ebc7caf91ed9d3f77b731934efda60e3bc6dbe99f949c8b9c7c41ece647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141419343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe61aed3690aab99f0a235a4263a9f9c9a3785f0786ece5a7e5016bd8b3b9b79`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:53:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:53:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 01:53:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:53:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:53:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:54 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 07 Apr 2026 01:53:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:54:09 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 01:54:09 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 01:54:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25e6100f274d4fad4e9e9ba77343e40c40872e57af49b3ef94501927706423a`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51761292baba02e8cc6b325a8a92561dde7a133b58cf3c62a0c569cc6d64a54a`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 7.7 MB (7692587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2090762aaa6ab1f672c9d8d135fdea412d38773df771cc8db671307e3974e84`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 370.5 KB (370542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebb3ea62ed4b15e333d5a57f21c89fbf6c5b1a599faf3d618de8bbaa3a556e0`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 76.5 KB (76491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662a58e215e3d102141ab8599f618a79c7dfff9c679ac22f74c7ec8e919c40f`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7647cc4028672882df2c04dd03bc161774e5b6e5af8bb8ae5010084a14b0d8eb`  
		Last Modified: Tue, 07 Apr 2026 01:54:28 GMT  
		Size: 105.2 MB (105158122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce06203c4a2555180f96708d6f482320f2cdf9a7b3ffb75e5e4e74d4bfb9345`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcf9e5de529df7d3da223c65065087e3bc92f9fdbe998a9701f20407da98c3c`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40da19d60d2b59538a70925c616adb516c7617dffa57103ac83df030205ffa07`  
		Last Modified: Tue, 07 Apr 2026 01:54:26 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5c716b570fa44399cd2b2f84f0bf550c3c6bfb09147995e76e56ede1639fb5`  
		Last Modified: Tue, 07 Apr 2026 01:54:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:2f59213a4b9318ec690692056b54c0199d9521ab85957dc4a1d240649c7278d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa199a98dfdb472d01efbfc92c66f406f9507dc4580bd8d7575f411577ef3f48`

```dockerfile
```

-	Layers:
	-	`sha256:18388ec4f02d173bb0eae90a09140c1a68edd85cf6802cad4235d708c490cc8e`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6fc0ebcb5833f0098dc74a550a60001bc024f046776f5fcb86da346e048e2a0`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:877bc4f2e9cebde5f6dd5db0625e8c11c1d5fc1450749b8df1ca04eee385183f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225182040bb866da2edada7d68127d3de35b20144022da2ee5092b81a48ff243`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 02:32:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:32:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:54 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 02:32:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:33:12 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 02:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 02:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d77fe6e136fe8121f88c8e24891e2e3ce57d89ace081cd7917cd296bf2781`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c6fd13d86c4615402446553400ddbf811488b8652dfeaf1b30369df23a3d31`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 7.4 MB (7399499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977c5ff033346e1cf892081e6ed41c4dcce967c151c4974c113f4e0406b20fa`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 372.1 KB (372140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28cd61fdf1d3cba5a38ba01f0090a13b851c1b038b6006be4782108f438976`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0df2b1587eda8004175334929323a5430ee32ec7ca0ad93243315dcdfcb1c4d`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d01bd714bd29509eccc7ffd6d42cf54ecb8e91fdd75f00b3a997e6b6adbaf5`  
		Last Modified: Wed, 22 Apr 2026 02:33:35 GMT  
		Size: 104.0 MB (104028166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b90460439c32fbf3c5d889b6093560b179158059ea12b5c62a42ce21380a3fe`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d8c0832e7dbb36e1959f210cc39b9c2f06cded3a0918c38f62da8bb11fe9cc`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846e3f061b916fca388e65c142917fbb47748b12371a1cc92c23fb6caa3881ea`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2a413a15f2d3d0b12253a678fe2d6199c1424fe5ce4d2166204aefde16a81`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:9d0ddb4a733d4cb15d823ccf7fef246af5176b6fbaf3ea6aaef729aa2ddd8e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa74c39c384641d3f8ad817a1c998223d297e3d2453b62a75dbd87fc179ca1c5`

```dockerfile
```

-	Layers:
	-	`sha256:8ae251a1734f9ea12b57e27040fd43078355bb4d78477392c9868f468347d2e5`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cd4bab63ce540f1c9dc037237c27456a1710328cd50cf0b8b3606d11ee6480`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 31.7 KB (31737 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:2306286ff2049d2683cadf51be1d1b4e6f8ee813c1362118bfd5a94b900818ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:92cd36a141af320a0e396b3f186e488441d8f5a67a56fac69caf54c5c3c46cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156463311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faeb20718102ff657dc6a855312eda1db690059113db9d85bd5187756618b39`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:40:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:40:01 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 01:40:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 01:40:26 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 01:40:26 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3699c0bcc1c342ae39ac0c5795ee860204401b568e49f81e18539e9709faebc4`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec4bcefbaa2ddc5c5f850b85ffbe49c949b93ad9489b61b3f89cfb34180ffc6`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 7.9 MB (7883583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1541a282306121df04d871433c17b3b800404c707fb599c5a8f234b41af81494`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 77.4 MB (77381418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43036a360cced63fdca47587355730eb6ca55258262dd6b52e46567c797fea4`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 424.1 KB (424148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4a9d479467f6e24a6463d19d8543a2e02c577c849349b0ce23166c5d6413c4`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 99.6 KB (99590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a155df5e2bd3365d2f8221fd2d8deb9cce87e5d7dfe08b67981f61b3a117b392`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc59fcc663abe8a36653dc41b9a13683b410959194a214a77c63a0dfa7bf085`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 42.4 MB (42436440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9545a463d46340f4dc2317a6418c34656c03807cb0c7525ff875b6398b6619c`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7b18530a9ce9367951a915771a5a9595b716fca410e17a0b0ca29f7d32793208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640763ee15e9616ab3dd38c5eeb265cad1434dcea1e1ff5b39533fe8a6382db7`

```dockerfile
```

-	Layers:
	-	`sha256:5e2c3d5c92887b2a975e673d20f4dd218d7c5ffd8478ca1fb73ed1d26c39d70b`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e211ede0fc11c56aa53817d66bfbfdc5b86629c700866acedf8bf91383dbabdd`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9140c1e90c4668c82d1fc0f86d364a7168e5e5430c639e06ced9574b727246e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155360208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b2dcd7bad8ce8fb8847acbd65fbe4a42b612bb57d0daf8e0c3008051ecd79d`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:53:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:53:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 01:53:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:55 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:53:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:54:03 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:03 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 01:54:09 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 01:54:09 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d258e5f7ae5f1971dde27a179beef494fcb76f51d3c104e3148119beda4d3700`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390980d72a7e9ce4615f77822c0074883a0bb99ec4777020c3aafec9cae9cdb6`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 7.7 MB (7692646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621c0229e2890e11b009bf1678ec6ec716eaaa2aaad57d765d09aa549a3bd5`  
		Last Modified: Tue, 07 Apr 2026 01:54:27 GMT  
		Size: 76.7 MB (76718101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c900127ad59ab99b4ccf5f64b211ba22e325179a8f7f82447f4b5aea25cf5186`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 392.8 KB (392774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89177beba55df8f23373c2d7995557c42d596f92129e72b2d67ffb1a1642e4f2`  
		Last Modified: Tue, 07 Apr 2026 01:54:26 GMT  
		Size: 99.5 KB (99532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3562ee2e2f5eab7217bb086ceed411aa4b38b90f8c335aa5ce50ea56160be600`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecf093d8d4a3f64848a09b030db5314c7024b3c3674fa8dbb65f40020cb95e8`  
		Last Modified: Tue, 07 Apr 2026 01:54:27 GMT  
		Size: 42.3 MB (42339106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760f8ee828d2c630dbf3060c62b4fb3341a9604af4956c1773d3f407553229ee`  
		Last Modified: Tue, 07 Apr 2026 01:54:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:2aec03b2f25a41dc9ab40d739ebb8f527e65a2409f667371f0187c69383c00d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022707360bbfa52df4bcd20af17e457c3977dc02aed182962d54b696eefaf59b`

```dockerfile
```

-	Layers:
	-	`sha256:51a4ef763fa18ec15d5e0c79406d11fa3b6e3b5dda8247f3c90d415a637e3799`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 3.7 MB (3656771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:179425382c09ce0abe9a47dfd77e03fe096ee6a77107b8de0934bbfae9cc2773`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:cf725f5fc333ce5583c3a1bdc5c493b3ff2f80035acfe396b5d72fd91f07d765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150105066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1ee5ed95bc2b90e3a3e93630af5058bed2be6512d46323fed497d83ca3e700`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:42 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:42 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 02:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:33:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:33:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:33:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:33:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 02:33:14 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 02:33:14 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c72ad32031623d24cb015f06ba762b3e2605190b489f63556f5c5c54c26a174`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431023707f5f79b1f184ccc237ab2f994f164119af3c3c206647fa1a55b73464`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 7.4 MB (7399462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2ad2d5f20f69c12b06d18d0949dc33bc5c537de9fb95aed5c4c65874835f3f`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 73.2 MB (73153273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5a19190ca30575a8918e6cdfed0b8b8c654e027d95ebe94ec24fe7ec5dda88`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 394.5 KB (394500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a7dee933c23aaf5e57248fcb5d87c1681d5a3a500d396b2f887a7ad0cac2c1`  
		Last Modified: Wed, 22 Apr 2026 02:33:37 GMT  
		Size: 99.7 KB (99663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48cd1f38f663b0e9a746ae67a2609d0a3ca9beab4247f6c3c7a23d7bdfdddd3`  
		Last Modified: Wed, 22 Apr 2026 02:33:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69bf6b994e3969bc5a4a0775754d5e7e81ac5cef4e04e5b8a6af9fa2c1b111`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 42.2 MB (42164727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84df84af6c868bcfbf2fb72ac4d14ad4512360969fabab4f072bda72b3f84fe`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f219414bd8b1573e72b97f12aafa8a21443e21307c127870d5bbe6ca5c90b09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf901c9bcaad01ea643fb50cb373264849c48824372fd6cba1d9291c92aed21`

```dockerfile
```

-	Layers:
	-	`sha256:1deb324532a176476ff3b667e706dcf1f8598d923bdfb9840aa5c45a076f4312`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6937c36d9e12093fba3ca6879d372458ad4f0a5f2e8f698c480182ab3c45c58`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1`

```console
$ docker pull couchdb@sha256:61ab333a29552dc0f3ac33031ea1273b006c8b7b6684331195cb189a01d684a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.1` - linux; amd64

```console
$ docker pull couchdb@sha256:8a1ba2a19a4c6981e0c903c2c3cd4d59602748cae0246666818090091a1645ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142061148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806bab74c1a4fb65ea85eca0df6cbfaf75e633a8fe12b041057efc047f8c1b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:39:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:39:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 01:40:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:08 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 01:40:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:21 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 01:40:21 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 01:40:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a53138b1d134d26fa4d53d9a2683c90141d93b6e7bd622b6f43e87123095de`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d90394d687f0d05c4649b956181d3345b324547ad48051ae0f177b448cbaaed`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 7.9 MB (7883631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de30193b9c2bab17ecfbda0bcf2a02b262bd8ceafd9a031e19a120fd8c8ac1`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 401.8 KB (401802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cdf8fec417a2a0f21a217bd1809c4ea2cc4f135d262f6b0dcc8078c9a7c044`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 76.5 KB (76502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34740f51296d6acfab2fa462e3b8b1803c8737e466de7bbf0fe68db4d70eae7`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9cb5cf3e1dbb2d8da0afe8b27d8c08d85851a5ced23b121452557a3d3c751`  
		Last Modified: Wed, 22 Apr 2026 01:40:55 GMT  
		Size: 105.5 MB (105457531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de039ed6bde8981bad1b825c982292ee098f74b12f1b17c1ba36cfe31305eb3`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a0c60ddabd96476377d89beffea94139f3abd519bfe2f9addbefde09deac10`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731d920f2d4fef22403d1c15d88dd6c5ea16f0ad88cf18a477d7d5b2f9149f63`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408fb10825775c8965247a872391b284439aa7ca55f219ee2b556cd7af7f8cb`  
		Last Modified: Wed, 22 Apr 2026 01:40:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:3401257267e59435bdfe64dbed14ef495900c94738868e5585c90a8b15a0bf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbd66bb44251165fea91e9881fd9bba6ac85de3eb92c8b0575a83327bd36503`

```dockerfile
```

-	Layers:
	-	`sha256:5885b7c7950112751264b2ad2b6bc61f53aa9cf3d431edef5ecfe318a9857788`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf6461ec6d2ed586ec7996683ff351ab2e0289226e87e971668647852e88b16`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:25741ebc7caf91ed9d3f77b731934efda60e3bc6dbe99f949c8b9c7c41ece647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141419343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe61aed3690aab99f0a235a4263a9f9c9a3785f0786ece5a7e5016bd8b3b9b79`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:53:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:53:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 01:53:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:53:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:53:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:54 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 07 Apr 2026 01:53:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:54:09 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 01:54:09 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 01:54:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25e6100f274d4fad4e9e9ba77343e40c40872e57af49b3ef94501927706423a`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51761292baba02e8cc6b325a8a92561dde7a133b58cf3c62a0c569cc6d64a54a`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 7.7 MB (7692587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2090762aaa6ab1f672c9d8d135fdea412d38773df771cc8db671307e3974e84`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 370.5 KB (370542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebb3ea62ed4b15e333d5a57f21c89fbf6c5b1a599faf3d618de8bbaa3a556e0`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 76.5 KB (76491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662a58e215e3d102141ab8599f618a79c7dfff9c679ac22f74c7ec8e919c40f`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7647cc4028672882df2c04dd03bc161774e5b6e5af8bb8ae5010084a14b0d8eb`  
		Last Modified: Tue, 07 Apr 2026 01:54:28 GMT  
		Size: 105.2 MB (105158122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce06203c4a2555180f96708d6f482320f2cdf9a7b3ffb75e5e4e74d4bfb9345`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcf9e5de529df7d3da223c65065087e3bc92f9fdbe998a9701f20407da98c3c`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40da19d60d2b59538a70925c616adb516c7617dffa57103ac83df030205ffa07`  
		Last Modified: Tue, 07 Apr 2026 01:54:26 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5c716b570fa44399cd2b2f84f0bf550c3c6bfb09147995e76e56ede1639fb5`  
		Last Modified: Tue, 07 Apr 2026 01:54:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:2f59213a4b9318ec690692056b54c0199d9521ab85957dc4a1d240649c7278d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa199a98dfdb472d01efbfc92c66f406f9507dc4580bd8d7575f411577ef3f48`

```dockerfile
```

-	Layers:
	-	`sha256:18388ec4f02d173bb0eae90a09140c1a68edd85cf6802cad4235d708c490cc8e`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6fc0ebcb5833f0098dc74a550a60001bc024f046776f5fcb86da346e048e2a0`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; s390x

```console
$ docker pull couchdb@sha256:877bc4f2e9cebde5f6dd5db0625e8c11c1d5fc1450749b8df1ca04eee385183f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225182040bb866da2edada7d68127d3de35b20144022da2ee5092b81a48ff243`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 02:32:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:32:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:54 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 02:32:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:33:12 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 02:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 02:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d77fe6e136fe8121f88c8e24891e2e3ce57d89ace081cd7917cd296bf2781`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c6fd13d86c4615402446553400ddbf811488b8652dfeaf1b30369df23a3d31`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 7.4 MB (7399499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977c5ff033346e1cf892081e6ed41c4dcce967c151c4974c113f4e0406b20fa`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 372.1 KB (372140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28cd61fdf1d3cba5a38ba01f0090a13b851c1b038b6006be4782108f438976`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0df2b1587eda8004175334929323a5430ee32ec7ca0ad93243315dcdfcb1c4d`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d01bd714bd29509eccc7ffd6d42cf54ecb8e91fdd75f00b3a997e6b6adbaf5`  
		Last Modified: Wed, 22 Apr 2026 02:33:35 GMT  
		Size: 104.0 MB (104028166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b90460439c32fbf3c5d889b6093560b179158059ea12b5c62a42ce21380a3fe`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d8c0832e7dbb36e1959f210cc39b9c2f06cded3a0918c38f62da8bb11fe9cc`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846e3f061b916fca388e65c142917fbb47748b12371a1cc92c23fb6caa3881ea`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2a413a15f2d3d0b12253a678fe2d6199c1424fe5ce4d2166204aefde16a81`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:9d0ddb4a733d4cb15d823ccf7fef246af5176b6fbaf3ea6aaef729aa2ddd8e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa74c39c384641d3f8ad817a1c998223d297e3d2453b62a75dbd87fc179ca1c5`

```dockerfile
```

-	Layers:
	-	`sha256:8ae251a1734f9ea12b57e27040fd43078355bb4d78477392c9868f468347d2e5`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cd4bab63ce540f1c9dc037237c27456a1710328cd50cf0b8b3606d11ee6480`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 31.7 KB (31737 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1-nouveau`

```console
$ docker pull couchdb@sha256:2306286ff2049d2683cadf51be1d1b4e6f8ee813c1362118bfd5a94b900818ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.1-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:92cd36a141af320a0e396b3f186e488441d8f5a67a56fac69caf54c5c3c46cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156463311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faeb20718102ff657dc6a855312eda1db690059113db9d85bd5187756618b39`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:40:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:40:01 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 01:40:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 01:40:26 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 01:40:26 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3699c0bcc1c342ae39ac0c5795ee860204401b568e49f81e18539e9709faebc4`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec4bcefbaa2ddc5c5f850b85ffbe49c949b93ad9489b61b3f89cfb34180ffc6`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 7.9 MB (7883583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1541a282306121df04d871433c17b3b800404c707fb599c5a8f234b41af81494`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 77.4 MB (77381418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43036a360cced63fdca47587355730eb6ca55258262dd6b52e46567c797fea4`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 424.1 KB (424148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4a9d479467f6e24a6463d19d8543a2e02c577c849349b0ce23166c5d6413c4`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 99.6 KB (99590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a155df5e2bd3365d2f8221fd2d8deb9cce87e5d7dfe08b67981f61b3a117b392`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc59fcc663abe8a36653dc41b9a13683b410959194a214a77c63a0dfa7bf085`  
		Last Modified: Wed, 22 Apr 2026 01:40:43 GMT  
		Size: 42.4 MB (42436440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9545a463d46340f4dc2317a6418c34656c03807cb0c7525ff875b6398b6619c`  
		Last Modified: Wed, 22 Apr 2026 01:40:42 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7b18530a9ce9367951a915771a5a9595b716fca410e17a0b0ca29f7d32793208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640763ee15e9616ab3dd38c5eeb265cad1434dcea1e1ff5b39533fe8a6382db7`

```dockerfile
```

-	Layers:
	-	`sha256:5e2c3d5c92887b2a975e673d20f4dd218d7c5ffd8478ca1fb73ed1d26c39d70b`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e211ede0fc11c56aa53817d66bfbfdc5b86629c700866acedf8bf91383dbabdd`  
		Last Modified: Wed, 22 Apr 2026 01:40:40 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9140c1e90c4668c82d1fc0f86d364a7168e5e5430c639e06ced9574b727246e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155360208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b2dcd7bad8ce8fb8847acbd65fbe4a42b612bb57d0daf8e0c3008051ecd79d`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:53:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:53:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 01:53:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:55 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:53:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:54:03 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:03 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 01:54:09 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 01:54:09 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d258e5f7ae5f1971dde27a179beef494fcb76f51d3c104e3148119beda4d3700`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390980d72a7e9ce4615f77822c0074883a0bb99ec4777020c3aafec9cae9cdb6`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 7.7 MB (7692646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621c0229e2890e11b009bf1678ec6ec716eaaa2aaad57d765d09aa549a3bd5`  
		Last Modified: Tue, 07 Apr 2026 01:54:27 GMT  
		Size: 76.7 MB (76718101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c900127ad59ab99b4ccf5f64b211ba22e325179a8f7f82447f4b5aea25cf5186`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 392.8 KB (392774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89177beba55df8f23373c2d7995557c42d596f92129e72b2d67ffb1a1642e4f2`  
		Last Modified: Tue, 07 Apr 2026 01:54:26 GMT  
		Size: 99.5 KB (99532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3562ee2e2f5eab7217bb086ceed411aa4b38b90f8c335aa5ce50ea56160be600`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecf093d8d4a3f64848a09b030db5314c7024b3c3674fa8dbb65f40020cb95e8`  
		Last Modified: Tue, 07 Apr 2026 01:54:27 GMT  
		Size: 42.3 MB (42339106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760f8ee828d2c630dbf3060c62b4fb3341a9604af4956c1773d3f407553229ee`  
		Last Modified: Tue, 07 Apr 2026 01:54:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:2aec03b2f25a41dc9ab40d739ebb8f527e65a2409f667371f0187c69383c00d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022707360bbfa52df4bcd20af17e457c3977dc02aed182962d54b696eefaf59b`

```dockerfile
```

-	Layers:
	-	`sha256:51a4ef763fa18ec15d5e0c79406d11fa3b6e3b5dda8247f3c90d415a637e3799`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 3.7 MB (3656771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:179425382c09ce0abe9a47dfd77e03fe096ee6a77107b8de0934bbfae9cc2773`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:cf725f5fc333ce5583c3a1bdc5c493b3ff2f80035acfe396b5d72fd91f07d765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150105066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1ee5ed95bc2b90e3a3e93630af5058bed2be6512d46323fed497d83ca3e700`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:42 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:42 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 22 Apr 2026 02:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:33:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:33:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:33:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:33:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 22 Apr 2026 02:33:14 GMT
VOLUME [/opt/nouveau/data]
# Wed, 22 Apr 2026 02:33:14 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 22 Apr 2026 02:33:14 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c72ad32031623d24cb015f06ba762b3e2605190b489f63556f5c5c54c26a174`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431023707f5f79b1f184ccc237ab2f994f164119af3c3c206647fa1a55b73464`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 7.4 MB (7399462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2ad2d5f20f69c12b06d18d0949dc33bc5c537de9fb95aed5c4c65874835f3f`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 73.2 MB (73153273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5a19190ca30575a8918e6cdfed0b8b8c654e027d95ebe94ec24fe7ec5dda88`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 394.5 KB (394500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a7dee933c23aaf5e57248fcb5d87c1681d5a3a500d396b2f887a7ad0cac2c1`  
		Last Modified: Wed, 22 Apr 2026 02:33:37 GMT  
		Size: 99.7 KB (99663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48cd1f38f663b0e9a746ae67a2609d0a3ca9beab4247f6c3c7a23d7bdfdddd3`  
		Last Modified: Wed, 22 Apr 2026 02:33:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69bf6b994e3969bc5a4a0775754d5e7e81ac5cef4e04e5b8a6af9fa2c1b111`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 42.2 MB (42164727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84df84af6c868bcfbf2fb72ac4d14ad4512360969fabab4f072bda72b3f84fe`  
		Last Modified: Wed, 22 Apr 2026 02:33:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f219414bd8b1573e72b97f12aafa8a21443e21307c127870d5bbe6ca5c90b09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf901c9bcaad01ea643fb50cb373264849c48824372fd6cba1d9291c92aed21`

```dockerfile
```

-	Layers:
	-	`sha256:1deb324532a176476ff3b667e706dcf1f8598d923bdfb9840aa5c45a076f4312`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6937c36d9e12093fba3ca6879d372458ad4f0a5f2e8f698c480182ab3c45c58`  
		Last Modified: Wed, 22 Apr 2026 02:33:36 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:61ab333a29552dc0f3ac33031ea1273b006c8b7b6684331195cb189a01d684a3
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
$ docker pull couchdb@sha256:8a1ba2a19a4c6981e0c903c2c3cd4d59602748cae0246666818090091a1645ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142061148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806bab74c1a4fb65ea85eca0df6cbfaf75e633a8fe12b041057efc047f8c1b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:39:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 01:39:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 01:40:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 01:40:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 01:40:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:08 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 01:40:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:40:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:21 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 01:40:21 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 01:40:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a53138b1d134d26fa4d53d9a2683c90141d93b6e7bd622b6f43e87123095de`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d90394d687f0d05c4649b956181d3345b324547ad48051ae0f177b448cbaaed`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 7.9 MB (7883631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de30193b9c2bab17ecfbda0bcf2a02b262bd8ceafd9a031e19a120fd8c8ac1`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 401.8 KB (401802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cdf8fec417a2a0f21a217bd1809c4ea2cc4f135d262f6b0dcc8078c9a7c044`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 76.5 KB (76502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34740f51296d6acfab2fa462e3b8b1803c8737e466de7bbf0fe68db4d70eae7`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9cb5cf3e1dbb2d8da0afe8b27d8c08d85851a5ced23b121452557a3d3c751`  
		Last Modified: Wed, 22 Apr 2026 01:40:55 GMT  
		Size: 105.5 MB (105457531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de039ed6bde8981bad1b825c982292ee098f74b12f1b17c1ba36cfe31305eb3`  
		Last Modified: Wed, 22 Apr 2026 01:40:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a0c60ddabd96476377d89beffea94139f3abd519bfe2f9addbefde09deac10`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731d920f2d4fef22403d1c15d88dd6c5ea16f0ad88cf18a477d7d5b2f9149f63`  
		Last Modified: Wed, 22 Apr 2026 01:40:36 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408fb10825775c8965247a872391b284439aa7ca55f219ee2b556cd7af7f8cb`  
		Last Modified: Wed, 22 Apr 2026 01:40:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:3401257267e59435bdfe64dbed14ef495900c94738868e5585c90a8b15a0bf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbd66bb44251165fea91e9881fd9bba6ac85de3eb92c8b0575a83327bd36503`

```dockerfile
```

-	Layers:
	-	`sha256:5885b7c7950112751264b2ad2b6bc61f53aa9cf3d431edef5ecfe318a9857788`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf6461ec6d2ed586ec7996683ff351ab2e0289226e87e971668647852e88b16`  
		Last Modified: Wed, 22 Apr 2026 01:40:33 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:25741ebc7caf91ed9d3f77b731934efda60e3bc6dbe99f949c8b9c7c41ece647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141419343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe61aed3690aab99f0a235a4263a9f9c9a3785f0786ece5a7e5016bd8b3b9b79`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:53:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:53:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 01:53:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:53:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:53:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:53:54 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 07 Apr 2026 01:53:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:54:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:54:09 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 01:54:09 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 01:54:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25e6100f274d4fad4e9e9ba77343e40c40872e57af49b3ef94501927706423a`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51761292baba02e8cc6b325a8a92561dde7a133b58cf3c62a0c569cc6d64a54a`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 7.7 MB (7692587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2090762aaa6ab1f672c9d8d135fdea412d38773df771cc8db671307e3974e84`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 370.5 KB (370542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebb3ea62ed4b15e333d5a57f21c89fbf6c5b1a599faf3d618de8bbaa3a556e0`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 76.5 KB (76491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662a58e215e3d102141ab8599f618a79c7dfff9c679ac22f74c7ec8e919c40f`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7647cc4028672882df2c04dd03bc161774e5b6e5af8bb8ae5010084a14b0d8eb`  
		Last Modified: Tue, 07 Apr 2026 01:54:28 GMT  
		Size: 105.2 MB (105158122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce06203c4a2555180f96708d6f482320f2cdf9a7b3ffb75e5e4e74d4bfb9345`  
		Last Modified: Tue, 07 Apr 2026 01:54:24 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcf9e5de529df7d3da223c65065087e3bc92f9fdbe998a9701f20407da98c3c`  
		Last Modified: Tue, 07 Apr 2026 01:54:25 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40da19d60d2b59538a70925c616adb516c7617dffa57103ac83df030205ffa07`  
		Last Modified: Tue, 07 Apr 2026 01:54:26 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5c716b570fa44399cd2b2f84f0bf550c3c6bfb09147995e76e56ede1639fb5`  
		Last Modified: Tue, 07 Apr 2026 01:54:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:2f59213a4b9318ec690692056b54c0199d9521ab85957dc4a1d240649c7278d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa199a98dfdb472d01efbfc92c66f406f9507dc4580bd8d7575f411577ef3f48`

```dockerfile
```

-	Layers:
	-	`sha256:18388ec4f02d173bb0eae90a09140c1a68edd85cf6802cad4235d708c490cc8e`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6fc0ebcb5833f0098dc74a550a60001bc024f046776f5fcb86da346e048e2a0`  
		Last Modified: Tue, 07 Apr 2026 01:54:23 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:877bc4f2e9cebde5f6dd5db0625e8c11c1d5fc1450749b8df1ca04eee385183f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225182040bb866da2edada7d68127d3de35b20144022da2ee5092b81a48ff243`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Apr 2026 02:32:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 22 Apr 2026 02:32:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 22 Apr 2026 02:32:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 22 Apr 2026 02:32:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:54 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 22 Apr 2026 02:32:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 22 Apr 2026 02:33:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 02:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:33:12 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Apr 2026 02:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 22 Apr 2026 02:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d77fe6e136fe8121f88c8e24891e2e3ce57d89ace081cd7917cd296bf2781`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c6fd13d86c4615402446553400ddbf811488b8652dfeaf1b30369df23a3d31`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 7.4 MB (7399499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977c5ff033346e1cf892081e6ed41c4dcce967c151c4974c113f4e0406b20fa`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 372.1 KB (372140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28cd61fdf1d3cba5a38ba01f0090a13b851c1b038b6006be4782108f438976`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0df2b1587eda8004175334929323a5430ee32ec7ca0ad93243315dcdfcb1c4d`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d01bd714bd29509eccc7ffd6d42cf54ecb8e91fdd75f00b3a997e6b6adbaf5`  
		Last Modified: Wed, 22 Apr 2026 02:33:35 GMT  
		Size: 104.0 MB (104028166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b90460439c32fbf3c5d889b6093560b179158059ea12b5c62a42ce21380a3fe`  
		Last Modified: Wed, 22 Apr 2026 02:33:33 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d8c0832e7dbb36e1959f210cc39b9c2f06cded3a0918c38f62da8bb11fe9cc`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846e3f061b916fca388e65c142917fbb47748b12371a1cc92c23fb6caa3881ea`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2a413a15f2d3d0b12253a678fe2d6199c1424fe5ce4d2166204aefde16a81`  
		Last Modified: Wed, 22 Apr 2026 02:33:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:9d0ddb4a733d4cb15d823ccf7fef246af5176b6fbaf3ea6aaef729aa2ddd8e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa74c39c384641d3f8ad817a1c998223d297e3d2453b62a75dbd87fc179ca1c5`

```dockerfile
```

-	Layers:
	-	`sha256:8ae251a1734f9ea12b57e27040fd43078355bb4d78477392c9868f468347d2e5`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cd4bab63ce540f1c9dc037237c27456a1710328cd50cf0b8b3606d11ee6480`  
		Last Modified: Wed, 22 Apr 2026 02:33:32 GMT  
		Size: 31.7 KB (31737 bytes)  
		MIME: application/vnd.in-toto+json
