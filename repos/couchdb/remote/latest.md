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
