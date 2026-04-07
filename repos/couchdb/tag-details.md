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
$ docker pull couchdb@sha256:297cd556c7ba358a408fd009e7b8e3b91318ccfc4d57c9b0264a2fb051ad9ef7
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
$ docker pull couchdb@sha256:412d9e2d2a795689aae4649c3ce39d850f581d79d2e2cdda0f43d43b5784a7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4185b9c82e0dd524ff836db1302a606fd925df3a257cb2fd5c4c38030e2ff46`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:50:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:50:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 01:50:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:50:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:50:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:42 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 07 Apr 2026 01:50:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 01:50:56 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 01:50:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab90cd4f34eb266e96c3482fcf0545119db98813f49cb92ef036a7103e2b92d`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093df5069fd65f58ffa038b8565d9b62483be3e0385143e12c03125a8ee93c95`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 7.9 MB (7883128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c7afa3df02f8694bc940eb924d5f1b861da49c7f4ad4149668795f5a9eebda`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 401.8 KB (401798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e9c492394e1d1450767fcfb1ae7d2b3505fe39529766f9f6db3fe5c968dce`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 76.5 KB (76501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b75143212388be3686d25237e656cc612e77bbf8f4d22eb7d1cd8797ef16108`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b4fded2be747fe7bf75086ec7f8680932c0b00414d011bdfbc64714adf6616`  
		Last Modified: Tue, 07 Apr 2026 01:51:13 GMT  
		Size: 105.5 MB (105456616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efff0887044294c3a41bf062af7be716e4546f5ce0d6dbcf3467a0350712e7b5`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1565854ce2481500397988a06f4d22e0e04c8ca419ba2761307b49b1b30e7d9`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947144fea77c7536716edb5e10b8e7db805e5596afd66c74ded4d57cd09f5340`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6ddb5c9391738501e19bfa879bd74a7ecf21e8ee43fdc3c00d05d4353c4b0`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ff2912e771a210d0468eb3642b93396fd21b02aeb75b5540608c671ac7358adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca3f4a5d6af0738c4ebfeae37ea86df346a879dba9189e447f6a598448bcd9d`

```dockerfile
```

-	Layers:
	-	`sha256:f07b8bfcb4a631b81fb400ad4dca9961d55a2e32ee7ea62e579a2655d82554e7`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d0c47b50673b86738db9192ced1c95bbd60da92277e16c85553429d1e26e3c`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
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
$ docker pull couchdb@sha256:cdbfc7dc13c7e84bce205cf0eb53f265cb615d2004aebf683c2b0428383c66da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138772786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b9631612e9613affbff05f7b39d8a84b83fc09bb0f7927c4b8c16dce5d72b1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:06:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 03:06:33 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 03:06:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:06:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 03:06:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 03:06:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:06:47 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 07 Apr 2026 03:06:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:07:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 03:07:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 03:07:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192343f77244f9b39a7ecfb9a796c0333f12d24bdbcae754cf0117a79f7f3934`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e5be0426e4ff4d1bf0334fb536bf055dfa3aeec7f489133ca20a1bc34d3c79`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 7.4 MB (7398861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f87c23fe5783e4304a5f717b05056909fda726aa92d0acf9f98817f997036f`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 372.1 KB (372118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d775362da2979c34fde865d14ad122d8553eb4fc5d6ace637c89477896127e6`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 76.5 KB (76513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9da8b7a3b5835503ffd44cdc3269dcd06969854d4814fcd0497cf8095e69606`  
		Last Modified: Tue, 07 Apr 2026 03:07:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951a55ad3b762664d23471edeca2bd8dfdfd061ef70dd69bdda14dbc60f7d3bf`  
		Last Modified: Tue, 07 Apr 2026 03:07:28 GMT  
		Size: 104.0 MB (104028227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9931be1abdbc7b505e6aa5b98d07b6f63a438ea9b338672e1f6d93e3f69fc30a`  
		Last Modified: Tue, 07 Apr 2026 03:07:26 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3268717766691d4b87f04d15e76af4daac8064116c3fc5778f26693781645a18`  
		Last Modified: Tue, 07 Apr 2026 03:07:27 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fa28adb917086950ef24369dc409fc275704c4c5a82b188d9fd4ca7e1ceed`  
		Last Modified: Tue, 07 Apr 2026 03:07:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c248872d02128bd249e2f94054c36a370b488ef81784ccde688d99cbb4d26f73`  
		Last Modified: Tue, 07 Apr 2026 03:07:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:58304d474775bc7d12994490c1199b324b5efbcac3ab7f09a010d04b1f1edc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6065d99a49523fc839f520abd1d5c74a084d236e36c3ff1489aab4936718cddf`

```dockerfile
```

-	Layers:
	-	`sha256:ad7949415d2685de52eb2f662e12403f20144faafda64063227fa25e40a8181f`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb520fe894dc058a0e9ba1ac3ab33141d8334bfd42807c6b532c314d55548cd`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:179da13196874c2255cc3e8c0a4624279caac00d7dbad139f3f85eeea2313c45
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
$ docker pull couchdb@sha256:657ef169bfd7f014963baf6b1992eb074fdf402d9b55ad15147a1391357a3035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3494def2ab9551ec1eb0108dfb41be1aa9ad1ee3e9a0a9af151b4a50e44d2359`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:50:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:50:29 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:50:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:50:48 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:48 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:50:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 01:50:54 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 01:50:54 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 01:50:54 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 01:50:54 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c7b5629854a3acf585666bc40a4979bdc4f42e9e98225255a9456e2a95a3e3`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60aafff22dcb7c2819587ccce92fdd239c550a61f6df1cce33ab4845ad4a256b`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 7.9 MB (7883108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75ca1d1d73f13865d9e804875c290a3d19d7aea1f4080aef925abc882b978c`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 77.4 MB (77381369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d32b0944d9ae9f2816e6065898abbe564cc41ab6ac91e3301d7bca82b28cd5`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 424.2 KB (424163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb7734eed702acd55ab06083b6e32c788ccf28788808ca4118b9dbc5efecddf`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 99.5 KB (99547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5febb709bc54f7434563c0b6dffc32e17a7f33096a79e52043c39f148c7558c3`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d5a4ab2f174abccd784c7a554a7ccef6fdd34e93c3322d292c6d4cd94b6d95`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 42.4 MB (42436354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849edbf67b92b7fb2207db29ecdba74c08b5efd6f4afbd78be8ec16cac3a3cf3`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:9d04dc75a22805bf43d1c4dc6478f895db2717f663b6608b462c54fa4f8339c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a4eaca88fa36f0d4e347c1e2cf476eaadf4e897e89f05648de14a220f0355e`

```dockerfile
```

-	Layers:
	-	`sha256:91e0bad29f5e7eb29f5c25b82a7564e7bf1dfd01accfb09f73caabbeec9fd956`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97d554f781be765811186c6201793988d749108cefcedea863a561d1d8f70707`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 24.5 KB (24520 bytes)  
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
$ docker pull couchdb@sha256:02c08aa6ccd1bbe4a447a2bf780bd2dd5e6b665903f1342fbf574185788b2093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150104623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4662915212583b4484ce482a73cb7454d4e842a7fe3238857ff6f3dded91a901`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:07:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 03:07:30 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 03:07:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:07:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:07:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 03:07:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 03:07:56 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:07:56 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 03:08:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 03:08:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 03:08:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 03:08:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 03:08:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0325c5665933ad6d36f23a167563d05f063e037b0a2c5885e5e6e0d32e45fe`  
		Last Modified: Tue, 07 Apr 2026 03:08:26 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f6a0e5096d62644eef9382998fa5e3b7391a049d1c0ef34a2e6b75cd04d50c`  
		Last Modified: Tue, 07 Apr 2026 03:08:26 GMT  
		Size: 7.4 MB (7398906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1d0aaedcc65435ec10b159ce6394e9f4a79609f73b0ebfa5e46841180e4442`  
		Last Modified: Tue, 07 Apr 2026 03:08:27 GMT  
		Size: 73.2 MB (73153280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab558a5b81cc27b318fbe7efcd4862f3fa497f79bf7782a55c7937a0b55ed5a`  
		Last Modified: Tue, 07 Apr 2026 03:08:26 GMT  
		Size: 394.5 KB (394495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e8877983b9bf2198d7b1fa4536e45bf6e2004d074a249d75432bd413d49c0d`  
		Last Modified: Tue, 07 Apr 2026 03:08:27 GMT  
		Size: 99.7 KB (99683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2594178fe921993d30fd126010c6a3ffc3e2639fa081e3e139d9ebe72d483703`  
		Last Modified: Tue, 07 Apr 2026 03:08:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee0b40b98099ffa399c4e8b9fb4e401c136761dabd8177780b8224b2cf820b7`  
		Last Modified: Tue, 07 Apr 2026 03:08:28 GMT  
		Size: 42.2 MB (42164742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40375fa77ddfa72c67d888b04cc843ec0b7109b8489e251f505a6911a4c0d599`  
		Last Modified: Tue, 07 Apr 2026 03:08:28 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:9e57551628416a255325fd065213a5642ab3c22bc89fcef4490d1d51f6668fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a52d9aa17864ef8b3fa2ee2a50e9b593652183091ee805fa4112c889985a3aa`

```dockerfile
```

-	Layers:
	-	`sha256:24f3bc47c33d9ae50e545635452114b765abb97e69cc439ab1f84fc4fd8ae999`  
		Last Modified: Tue, 07 Apr 2026 03:08:26 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff901c13c497dc7bf1fca4d00d0ae10d681831afeee470e8175323e37f2e04a`  
		Last Modified: Tue, 07 Apr 2026 03:08:25 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:625be8e930f8fce9f7be31e353aae789462590d62b87577322d8ea2be79911c0
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
$ docker pull couchdb@sha256:063b930d0516e19940dc467d653e1152d406798f73746d2a9c5d4045a524deee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139023246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268f7d4417b7ffe2155efcd5229c8bfce58853a82d572b0f5ed81db5bb043c3e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:50:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:50:23 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 01:50:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:50:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:50:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 07 Apr 2026 01:50:37 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:50:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 01:50:49 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 01:50:49 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 01:50:49 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 01:50:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:50:49 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 01:50:49 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 01:50:49 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e404007e6da8e855d068ee87b4c397de8f486dfb97062e85d3481421b00beb6`  
		Last Modified: Tue, 07 Apr 2026 01:51:02 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06507c289bea80d11cc4eed9e95ba196f6e58de946245748856b1d41fe76bad`  
		Last Modified: Tue, 07 Apr 2026 01:51:02 GMT  
		Size: 7.9 MB (7883154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be79f30d9dc3719ccb692c59be3c404ba0db3f722702693b25da53d3fc8d1e20`  
		Last Modified: Tue, 07 Apr 2026 01:51:02 GMT  
		Size: 401.8 KB (401795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ede0ceb2f5fcb386ce686b9ff7294beab8f5491efccb4920785dd4d6af221a`  
		Last Modified: Tue, 07 Apr 2026 01:51:02 GMT  
		Size: 76.5 KB (76502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7409821724d94b726bc8260339531f948899996702d02fe3c277acb0574829bc`  
		Last Modified: Tue, 07 Apr 2026 01:51:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c518dfd9acd418fe2513a13fce2d1085c6aab318341dc0d71eff385d649c57e3`  
		Last Modified: Tue, 07 Apr 2026 01:51:06 GMT  
		Size: 102.4 MB (102420032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4c5b9440b6639abd1a189466b5da2e79966d5d9980c177e439231663fccf78`  
		Last Modified: Tue, 07 Apr 2026 01:51:03 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8ecd5e9b3475aea49d97baa4438e3129746513755c2aa0f96d7db4cb27e52a`  
		Last Modified: Tue, 07 Apr 2026 01:51:04 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3133c3bd0c07fff86137de715e68c6071bd86038782063c8260e8ca5d47595`  
		Last Modified: Tue, 07 Apr 2026 01:51:04 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0003815ecdd46c83c9c8e02c76e05b99b98d6bb1e215e0ad33bb8131f98df6`  
		Last Modified: Tue, 07 Apr 2026 01:51:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:7e82044ccda10ed79f1064c01c6939487df7768652510b4cdd4cbb2eecb0e428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8182541b0ab5da460410070f54f7e3c5bf8ef28e68b3a7a13445f47a45d1838d`

```dockerfile
```

-	Layers:
	-	`sha256:cd0636d06563e8a712bee3667efff750a57e6026fa6c871de9bab5de78c62ccd`  
		Last Modified: Tue, 07 Apr 2026 01:51:02 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb72e9150d489f82c41f300359240f6a45f8d9d4c2b3a1d035147007ace03332`  
		Last Modified: Tue, 07 Apr 2026 01:51:02 GMT  
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
$ docker pull couchdb@sha256:f3f6e855b25ea760b6c8b6d334de90beadefb41a26eebaa3d40bc386413b9d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135800963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db3c9bb5d5976087a481a4f72c992ba2fc20eea91629be62b56e4de167ae3e7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:54:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 05:54:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 05:54:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:54:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 05:54:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 05:54:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:54:45 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 07 Apr 2026 05:54:45 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 05:55:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 05:55:04 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 05:55:04 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 05:55:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 05:55:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 05:55:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:55:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 05:55:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 05:55:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c4a941ff17934027ae69fd5b4d84e4106b83b95fc49dc9da63cac81e6af84a`  
		Last Modified: Tue, 07 Apr 2026 05:55:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845231bd4c6c225f706c29ed66d44607d79a3be890927d77aeb65b3b5d8fc63d`  
		Last Modified: Tue, 07 Apr 2026 05:55:25 GMT  
		Size: 7.4 MB (7398916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae74167b22686b2816d31efe48e11b2cfc86726e2898acf9875e31398d0b22d`  
		Last Modified: Tue, 07 Apr 2026 05:55:26 GMT  
		Size: 372.1 KB (372119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5689956a394ea56f2caea9eca829a57b002f0b48318d36c9687fa859f72d3a03`  
		Last Modified: Tue, 07 Apr 2026 05:55:25 GMT  
		Size: 76.5 KB (76544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a05575653b45cf4a739f7f2deac5d890275fc65c644555f49dc4b247f1fff2d`  
		Last Modified: Tue, 07 Apr 2026 05:55:26 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979de805765b53914f1cdec638d5b016b690a14988aca0dffa7562c67b71ce0e`  
		Last Modified: Tue, 07 Apr 2026 05:55:29 GMT  
		Size: 101.1 MB (101056318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7987359f695000fb24a3b63469c13035e88a23445796de21590f0c4761445d9b`  
		Last Modified: Tue, 07 Apr 2026 05:55:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25cabf799f7d5f64e6c1249bde35e7f8a02375c9ae7277e89f1662f86786eef`  
		Last Modified: Tue, 07 Apr 2026 05:55:27 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b291419f04ed1e829c0fa2c1c32aab96d8b2d80a58400d2b6e2033e8c0ff3974`  
		Last Modified: Tue, 07 Apr 2026 05:55:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d98da53a4690177e2af9b5a115eae5378d810d9c526500f1ba80bec37feb321`  
		Last Modified: Tue, 07 Apr 2026 05:55:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:648a37f329e1cbb9609bb220b09db523203d23ed6a6afb03e5fc08f071ea1660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a943ce036a0d5efc13a863dd2448f4ee8decaf89c6694f9c609d0166e403526d`

```dockerfile
```

-	Layers:
	-	`sha256:b46bed383b798b3c3d76002b8a50f0a4f76a4dc7c9aa5b19531f7ee1a1832a7a`  
		Last Modified: Tue, 07 Apr 2026 05:55:25 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f10fa4a857d127e6e7a031a000afae3f7c309990d706be4a3f9511dd42ccc8c`  
		Last Modified: Tue, 07 Apr 2026 05:55:25 GMT  
		Size: 31.1 KB (31147 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:87ebf3d9f2ee260f267789be59f036dd47740b9e8b324758c01023b2425260d9
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
$ docker pull couchdb@sha256:6d898a90a95e6423747505610b9ad0fa14a9e4d4111e83491ff3b62bb01d5772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf41a3881a8414a84af407c05971da07b88fc5ade26ed0a0a5fec645c33febaa`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:50:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:50:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 01:50:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:50:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:50:58 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:51:03 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 01:51:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 01:51:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 01:51:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 01:51:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f6380d7407dc11422702729ef79981ebc31272614c3a808d240e898a2d55ce`  
		Last Modified: Tue, 07 Apr 2026 01:51:18 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13498cf82450fac4d71fb8ed01b41b9eebbba11cfc657541dd54d6ae265a3721`  
		Last Modified: Tue, 07 Apr 2026 01:51:18 GMT  
		Size: 7.9 MB (7883148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a321c0ddf520d72a81c089e3aae17c54c1c0c9af50e2821b3214a1d23c50c05f`  
		Last Modified: Tue, 07 Apr 2026 01:51:20 GMT  
		Size: 77.4 MB (77381340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdb019ff24c1042d72d8168cf8412106d6cf1892a34d32cca9f05151fb2f39a`  
		Last Modified: Tue, 07 Apr 2026 01:51:18 GMT  
		Size: 424.2 KB (424179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dcabf9101c6369f3f7a0f5adddd40e4a305b3b02b07f369d9b6c5a71f44b2a`  
		Last Modified: Tue, 07 Apr 2026 01:51:19 GMT  
		Size: 99.6 KB (99573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc866681c6f15eab7520219f81badd60876c0069c9b73d9a7d7ce03b241a5bcf`  
		Last Modified: Tue, 07 Apr 2026 01:51:19 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ecd0aa75c9dbc867a63b555a6338952e915e0412eb50371b2b7541224502a1`  
		Last Modified: Tue, 07 Apr 2026 01:51:21 GMT  
		Size: 42.4 MB (42436139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e562aa5d228ea0ea45f056f00d2b5991b438e3317f8d336b387529a83504142`  
		Last Modified: Tue, 07 Apr 2026 01:51:20 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:449d458e41ac72fb9e3101c4772d315c3807cb40b7a965842a91ecc9b895953a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55e70f7a4026270a082faffe1e3931789d09af7c9ac45e4280ebf3d71814662`

```dockerfile
```

-	Layers:
	-	`sha256:3b69c23e7d26086171dac482d2456bdc5193fbc8c72612a2a6fc86573413ab17`  
		Last Modified: Tue, 07 Apr 2026 01:51:18 GMT  
		Size: 3.7 MB (3657789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a6e2fa4dc3990c37b28bf68987f2705f2b79f3499920d89348390a9042e5a47`  
		Last Modified: Tue, 07 Apr 2026 01:51:18 GMT  
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
$ docker pull couchdb@sha256:1c8c296fe64a2e001a69c1c53ce0957b5b92c551eb61a283054e8c060c3a8500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150102689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec26a586e6db296c2483d3e3569a534ca3fd4aa16579d3854f1545f74c30825`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:07:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 03:07:48 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 03:07:55 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 03:08:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 03:08:09 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:10 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 03:08:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 03:08:18 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 03:08:18 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 03:08:18 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 03:08:18 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690e0832feea180de92f9ff7b64e5d87cd39675f4eeed73ec1c2e5192f03eb2`  
		Last Modified: Tue, 07 Apr 2026 03:08:41 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77a910d15e79f3595c4bd070c9def471c424e8518d7a30a80225282cff0fbcd`  
		Last Modified: Tue, 07 Apr 2026 03:08:41 GMT  
		Size: 7.4 MB (7398822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2835ca1905d4ff097615b5e6bd74417661efd29f2e2458f4962251eec782a801`  
		Last Modified: Tue, 07 Apr 2026 03:08:42 GMT  
		Size: 73.2 MB (73153271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a0938be52b3fb1ecf5ee2a97e940c6c3befb8c1da32ae95df0f50840d50cb7`  
		Last Modified: Tue, 07 Apr 2026 03:08:41 GMT  
		Size: 394.5 KB (394497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798a506675ed007df7a2e927880c4d1fec4bfdca50d48108637f72c9b00f58b4`  
		Last Modified: Tue, 07 Apr 2026 03:08:42 GMT  
		Size: 99.6 KB (99637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908158129720ba665364a7d5a2b3ece234a6ed1c73502075003d762a5dbffd2b`  
		Last Modified: Tue, 07 Apr 2026 03:08:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13318d0c108fbd4ed691e26ee23ca58b06d5cc3e1698e801e6243d4e4d253628`  
		Last Modified: Tue, 07 Apr 2026 03:08:43 GMT  
		Size: 42.2 MB (42162948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb201b879d51d118b3a56b53b6dc5e70dbc16fbbee0f1829635129afd38dc6a`  
		Last Modified: Tue, 07 Apr 2026 03:08:43 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:73acd811040021f1511f48583af7b3507c0bf5975e6e563b27609d392ce4c2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d0fdd77c9629e79dfffa66ee8b2bdcdaddf0bdeaf23b5440285fea73ccf4f5`

```dockerfile
```

-	Layers:
	-	`sha256:9691ac71d5486cadb890799cbcbfaa11623ff5d1ba86e453037397fae6deb3af`  
		Last Modified: Tue, 07 Apr 2026 03:08:41 GMT  
		Size: 3.6 MB (3648318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12cc5b132053bf1a2bf5f8c12f3c61a594b5cc2b1df303a733de7b69a552e34`  
		Last Modified: Tue, 07 Apr 2026 03:08:41 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:625be8e930f8fce9f7be31e353aae789462590d62b87577322d8ea2be79911c0
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
$ docker pull couchdb@sha256:063b930d0516e19940dc467d653e1152d406798f73746d2a9c5d4045a524deee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139023246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268f7d4417b7ffe2155efcd5229c8bfce58853a82d572b0f5ed81db5bb043c3e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:50:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:50:23 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 01:50:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:50:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:50:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 07 Apr 2026 01:50:37 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:50:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 01:50:49 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 01:50:49 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 01:50:49 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 01:50:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:50:49 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 01:50:49 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 01:50:49 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e404007e6da8e855d068ee87b4c397de8f486dfb97062e85d3481421b00beb6`  
		Last Modified: Tue, 07 Apr 2026 01:51:02 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06507c289bea80d11cc4eed9e95ba196f6e58de946245748856b1d41fe76bad`  
		Last Modified: Tue, 07 Apr 2026 01:51:02 GMT  
		Size: 7.9 MB (7883154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be79f30d9dc3719ccb692c59be3c404ba0db3f722702693b25da53d3fc8d1e20`  
		Last Modified: Tue, 07 Apr 2026 01:51:02 GMT  
		Size: 401.8 KB (401795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ede0ceb2f5fcb386ce686b9ff7294beab8f5491efccb4920785dd4d6af221a`  
		Last Modified: Tue, 07 Apr 2026 01:51:02 GMT  
		Size: 76.5 KB (76502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7409821724d94b726bc8260339531f948899996702d02fe3c277acb0574829bc`  
		Last Modified: Tue, 07 Apr 2026 01:51:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c518dfd9acd418fe2513a13fce2d1085c6aab318341dc0d71eff385d649c57e3`  
		Last Modified: Tue, 07 Apr 2026 01:51:06 GMT  
		Size: 102.4 MB (102420032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4c5b9440b6639abd1a189466b5da2e79966d5d9980c177e439231663fccf78`  
		Last Modified: Tue, 07 Apr 2026 01:51:03 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8ecd5e9b3475aea49d97baa4438e3129746513755c2aa0f96d7db4cb27e52a`  
		Last Modified: Tue, 07 Apr 2026 01:51:04 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3133c3bd0c07fff86137de715e68c6071bd86038782063c8260e8ca5d47595`  
		Last Modified: Tue, 07 Apr 2026 01:51:04 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0003815ecdd46c83c9c8e02c76e05b99b98d6bb1e215e0ad33bb8131f98df6`  
		Last Modified: Tue, 07 Apr 2026 01:51:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:7e82044ccda10ed79f1064c01c6939487df7768652510b4cdd4cbb2eecb0e428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8182541b0ab5da460410070f54f7e3c5bf8ef28e68b3a7a13445f47a45d1838d`

```dockerfile
```

-	Layers:
	-	`sha256:cd0636d06563e8a712bee3667efff750a57e6026fa6c871de9bab5de78c62ccd`  
		Last Modified: Tue, 07 Apr 2026 01:51:02 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb72e9150d489f82c41f300359240f6a45f8d9d4c2b3a1d035147007ace03332`  
		Last Modified: Tue, 07 Apr 2026 01:51:02 GMT  
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
$ docker pull couchdb@sha256:f3f6e855b25ea760b6c8b6d334de90beadefb41a26eebaa3d40bc386413b9d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135800963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db3c9bb5d5976087a481a4f72c992ba2fc20eea91629be62b56e4de167ae3e7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:54:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 05:54:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 05:54:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:54:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 05:54:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 05:54:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:54:45 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 07 Apr 2026 05:54:45 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 05:55:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 05:55:04 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 05:55:04 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 05:55:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 05:55:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 05:55:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:55:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 05:55:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 05:55:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c4a941ff17934027ae69fd5b4d84e4106b83b95fc49dc9da63cac81e6af84a`  
		Last Modified: Tue, 07 Apr 2026 05:55:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845231bd4c6c225f706c29ed66d44607d79a3be890927d77aeb65b3b5d8fc63d`  
		Last Modified: Tue, 07 Apr 2026 05:55:25 GMT  
		Size: 7.4 MB (7398916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae74167b22686b2816d31efe48e11b2cfc86726e2898acf9875e31398d0b22d`  
		Last Modified: Tue, 07 Apr 2026 05:55:26 GMT  
		Size: 372.1 KB (372119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5689956a394ea56f2caea9eca829a57b002f0b48318d36c9687fa859f72d3a03`  
		Last Modified: Tue, 07 Apr 2026 05:55:25 GMT  
		Size: 76.5 KB (76544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a05575653b45cf4a739f7f2deac5d890275fc65c644555f49dc4b247f1fff2d`  
		Last Modified: Tue, 07 Apr 2026 05:55:26 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979de805765b53914f1cdec638d5b016b690a14988aca0dffa7562c67b71ce0e`  
		Last Modified: Tue, 07 Apr 2026 05:55:29 GMT  
		Size: 101.1 MB (101056318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7987359f695000fb24a3b63469c13035e88a23445796de21590f0c4761445d9b`  
		Last Modified: Tue, 07 Apr 2026 05:55:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25cabf799f7d5f64e6c1249bde35e7f8a02375c9ae7277e89f1662f86786eef`  
		Last Modified: Tue, 07 Apr 2026 05:55:27 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b291419f04ed1e829c0fa2c1c32aab96d8b2d80a58400d2b6e2033e8c0ff3974`  
		Last Modified: Tue, 07 Apr 2026 05:55:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d98da53a4690177e2af9b5a115eae5378d810d9c526500f1ba80bec37feb321`  
		Last Modified: Tue, 07 Apr 2026 05:55:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:648a37f329e1cbb9609bb220b09db523203d23ed6a6afb03e5fc08f071ea1660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a943ce036a0d5efc13a863dd2448f4ee8decaf89c6694f9c609d0166e403526d`

```dockerfile
```

-	Layers:
	-	`sha256:b46bed383b798b3c3d76002b8a50f0a4f76a4dc7c9aa5b19531f7ee1a1832a7a`  
		Last Modified: Tue, 07 Apr 2026 05:55:25 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f10fa4a857d127e6e7a031a000afae3f7c309990d706be4a3f9511dd42ccc8c`  
		Last Modified: Tue, 07 Apr 2026 05:55:25 GMT  
		Size: 31.1 KB (31147 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:87ebf3d9f2ee260f267789be59f036dd47740b9e8b324758c01023b2425260d9
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
$ docker pull couchdb@sha256:6d898a90a95e6423747505610b9ad0fa14a9e4d4111e83491ff3b62bb01d5772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf41a3881a8414a84af407c05971da07b88fc5ade26ed0a0a5fec645c33febaa`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:50:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:50:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 01:50:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:50:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:50:58 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:51:03 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 01:51:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 01:51:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 01:51:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 01:51:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f6380d7407dc11422702729ef79981ebc31272614c3a808d240e898a2d55ce`  
		Last Modified: Tue, 07 Apr 2026 01:51:18 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13498cf82450fac4d71fb8ed01b41b9eebbba11cfc657541dd54d6ae265a3721`  
		Last Modified: Tue, 07 Apr 2026 01:51:18 GMT  
		Size: 7.9 MB (7883148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a321c0ddf520d72a81c089e3aae17c54c1c0c9af50e2821b3214a1d23c50c05f`  
		Last Modified: Tue, 07 Apr 2026 01:51:20 GMT  
		Size: 77.4 MB (77381340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdb019ff24c1042d72d8168cf8412106d6cf1892a34d32cca9f05151fb2f39a`  
		Last Modified: Tue, 07 Apr 2026 01:51:18 GMT  
		Size: 424.2 KB (424179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dcabf9101c6369f3f7a0f5adddd40e4a305b3b02b07f369d9b6c5a71f44b2a`  
		Last Modified: Tue, 07 Apr 2026 01:51:19 GMT  
		Size: 99.6 KB (99573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc866681c6f15eab7520219f81badd60876c0069c9b73d9a7d7ce03b241a5bcf`  
		Last Modified: Tue, 07 Apr 2026 01:51:19 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ecd0aa75c9dbc867a63b555a6338952e915e0412eb50371b2b7541224502a1`  
		Last Modified: Tue, 07 Apr 2026 01:51:21 GMT  
		Size: 42.4 MB (42436139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e562aa5d228ea0ea45f056f00d2b5991b438e3317f8d336b387529a83504142`  
		Last Modified: Tue, 07 Apr 2026 01:51:20 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:449d458e41ac72fb9e3101c4772d315c3807cb40b7a965842a91ecc9b895953a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55e70f7a4026270a082faffe1e3931789d09af7c9ac45e4280ebf3d71814662`

```dockerfile
```

-	Layers:
	-	`sha256:3b69c23e7d26086171dac482d2456bdc5193fbc8c72612a2a6fc86573413ab17`  
		Last Modified: Tue, 07 Apr 2026 01:51:18 GMT  
		Size: 3.7 MB (3657789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a6e2fa4dc3990c37b28bf68987f2705f2b79f3499920d89348390a9042e5a47`  
		Last Modified: Tue, 07 Apr 2026 01:51:18 GMT  
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
$ docker pull couchdb@sha256:1c8c296fe64a2e001a69c1c53ce0957b5b92c551eb61a283054e8c060c3a8500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150102689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec26a586e6db296c2483d3e3569a534ca3fd4aa16579d3854f1545f74c30825`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:07:48 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 03:07:48 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 03:07:55 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 03:08:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 03:08:09 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:10 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 03:08:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 03:08:18 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 03:08:18 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 03:08:18 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 03:08:18 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690e0832feea180de92f9ff7b64e5d87cd39675f4eeed73ec1c2e5192f03eb2`  
		Last Modified: Tue, 07 Apr 2026 03:08:41 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77a910d15e79f3595c4bd070c9def471c424e8518d7a30a80225282cff0fbcd`  
		Last Modified: Tue, 07 Apr 2026 03:08:41 GMT  
		Size: 7.4 MB (7398822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2835ca1905d4ff097615b5e6bd74417661efd29f2e2458f4962251eec782a801`  
		Last Modified: Tue, 07 Apr 2026 03:08:42 GMT  
		Size: 73.2 MB (73153271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a0938be52b3fb1ecf5ee2a97e940c6c3befb8c1da32ae95df0f50840d50cb7`  
		Last Modified: Tue, 07 Apr 2026 03:08:41 GMT  
		Size: 394.5 KB (394497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798a506675ed007df7a2e927880c4d1fec4bfdca50d48108637f72c9b00f58b4`  
		Last Modified: Tue, 07 Apr 2026 03:08:42 GMT  
		Size: 99.6 KB (99637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908158129720ba665364a7d5a2b3ece234a6ed1c73502075003d762a5dbffd2b`  
		Last Modified: Tue, 07 Apr 2026 03:08:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13318d0c108fbd4ed691e26ee23ca58b06d5cc3e1698e801e6243d4e4d253628`  
		Last Modified: Tue, 07 Apr 2026 03:08:43 GMT  
		Size: 42.2 MB (42162948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb201b879d51d118b3a56b53b6dc5e70dbc16fbbee0f1829635129afd38dc6a`  
		Last Modified: Tue, 07 Apr 2026 03:08:43 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:73acd811040021f1511f48583af7b3507c0bf5975e6e563b27609d392ce4c2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d0fdd77c9629e79dfffa66ee8b2bdcdaddf0bdeaf23b5440285fea73ccf4f5`

```dockerfile
```

-	Layers:
	-	`sha256:9691ac71d5486cadb890799cbcbfaa11623ff5d1ba86e453037397fae6deb3af`  
		Last Modified: Tue, 07 Apr 2026 03:08:41 GMT  
		Size: 3.6 MB (3648318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12cc5b132053bf1a2bf5f8c12f3c61a594b5cc2b1df303a733de7b69a552e34`  
		Last Modified: Tue, 07 Apr 2026 03:08:41 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:297cd556c7ba358a408fd009e7b8e3b91318ccfc4d57c9b0264a2fb051ad9ef7
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
$ docker pull couchdb@sha256:412d9e2d2a795689aae4649c3ce39d850f581d79d2e2cdda0f43d43b5784a7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4185b9c82e0dd524ff836db1302a606fd925df3a257cb2fd5c4c38030e2ff46`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:50:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:50:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 01:50:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:50:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:50:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:42 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 07 Apr 2026 01:50:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 01:50:56 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 01:50:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab90cd4f34eb266e96c3482fcf0545119db98813f49cb92ef036a7103e2b92d`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093df5069fd65f58ffa038b8565d9b62483be3e0385143e12c03125a8ee93c95`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 7.9 MB (7883128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c7afa3df02f8694bc940eb924d5f1b861da49c7f4ad4149668795f5a9eebda`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 401.8 KB (401798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e9c492394e1d1450767fcfb1ae7d2b3505fe39529766f9f6db3fe5c968dce`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 76.5 KB (76501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b75143212388be3686d25237e656cc612e77bbf8f4d22eb7d1cd8797ef16108`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b4fded2be747fe7bf75086ec7f8680932c0b00414d011bdfbc64714adf6616`  
		Last Modified: Tue, 07 Apr 2026 01:51:13 GMT  
		Size: 105.5 MB (105456616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efff0887044294c3a41bf062af7be716e4546f5ce0d6dbcf3467a0350712e7b5`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1565854ce2481500397988a06f4d22e0e04c8ca419ba2761307b49b1b30e7d9`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947144fea77c7536716edb5e10b8e7db805e5596afd66c74ded4d57cd09f5340`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6ddb5c9391738501e19bfa879bd74a7ecf21e8ee43fdc3c00d05d4353c4b0`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:ff2912e771a210d0468eb3642b93396fd21b02aeb75b5540608c671ac7358adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca3f4a5d6af0738c4ebfeae37ea86df346a879dba9189e447f6a598448bcd9d`

```dockerfile
```

-	Layers:
	-	`sha256:f07b8bfcb4a631b81fb400ad4dca9961d55a2e32ee7ea62e579a2655d82554e7`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d0c47b50673b86738db9192ced1c95bbd60da92277e16c85553429d1e26e3c`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
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
$ docker pull couchdb@sha256:cdbfc7dc13c7e84bce205cf0eb53f265cb615d2004aebf683c2b0428383c66da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138772786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b9631612e9613affbff05f7b39d8a84b83fc09bb0f7927c4b8c16dce5d72b1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:06:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 03:06:33 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 03:06:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:06:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 03:06:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 03:06:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:06:47 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 07 Apr 2026 03:06:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:07:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 03:07:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 03:07:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192343f77244f9b39a7ecfb9a796c0333f12d24bdbcae754cf0117a79f7f3934`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e5be0426e4ff4d1bf0334fb536bf055dfa3aeec7f489133ca20a1bc34d3c79`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 7.4 MB (7398861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f87c23fe5783e4304a5f717b05056909fda726aa92d0acf9f98817f997036f`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 372.1 KB (372118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d775362da2979c34fde865d14ad122d8553eb4fc5d6ace637c89477896127e6`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 76.5 KB (76513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9da8b7a3b5835503ffd44cdc3269dcd06969854d4814fcd0497cf8095e69606`  
		Last Modified: Tue, 07 Apr 2026 03:07:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951a55ad3b762664d23471edeca2bd8dfdfd061ef70dd69bdda14dbc60f7d3bf`  
		Last Modified: Tue, 07 Apr 2026 03:07:28 GMT  
		Size: 104.0 MB (104028227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9931be1abdbc7b505e6aa5b98d07b6f63a438ea9b338672e1f6d93e3f69fc30a`  
		Last Modified: Tue, 07 Apr 2026 03:07:26 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3268717766691d4b87f04d15e76af4daac8064116c3fc5778f26693781645a18`  
		Last Modified: Tue, 07 Apr 2026 03:07:27 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fa28adb917086950ef24369dc409fc275704c4c5a82b188d9fd4ca7e1ceed`  
		Last Modified: Tue, 07 Apr 2026 03:07:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c248872d02128bd249e2f94054c36a370b488ef81784ccde688d99cbb4d26f73`  
		Last Modified: Tue, 07 Apr 2026 03:07:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:58304d474775bc7d12994490c1199b324b5efbcac3ab7f09a010d04b1f1edc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6065d99a49523fc839f520abd1d5c74a084d236e36c3ff1489aab4936718cddf`

```dockerfile
```

-	Layers:
	-	`sha256:ad7949415d2685de52eb2f662e12403f20144faafda64063227fa25e40a8181f`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb520fe894dc058a0e9ba1ac3ab33141d8334bfd42807c6b532c314d55548cd`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:179da13196874c2255cc3e8c0a4624279caac00d7dbad139f3f85eeea2313c45
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
$ docker pull couchdb@sha256:657ef169bfd7f014963baf6b1992eb074fdf402d9b55ad15147a1391357a3035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3494def2ab9551ec1eb0108dfb41be1aa9ad1ee3e9a0a9af151b4a50e44d2359`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:50:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:50:29 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:50:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:50:48 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:48 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:50:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 01:50:54 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 01:50:54 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 01:50:54 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 01:50:54 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c7b5629854a3acf585666bc40a4979bdc4f42e9e98225255a9456e2a95a3e3`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60aafff22dcb7c2819587ccce92fdd239c550a61f6df1cce33ab4845ad4a256b`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 7.9 MB (7883108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75ca1d1d73f13865d9e804875c290a3d19d7aea1f4080aef925abc882b978c`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 77.4 MB (77381369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d32b0944d9ae9f2816e6065898abbe564cc41ab6ac91e3301d7bca82b28cd5`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 424.2 KB (424163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb7734eed702acd55ab06083b6e32c788ccf28788808ca4118b9dbc5efecddf`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 99.5 KB (99547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5febb709bc54f7434563c0b6dffc32e17a7f33096a79e52043c39f148c7558c3`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d5a4ab2f174abccd784c7a554a7ccef6fdd34e93c3322d292c6d4cd94b6d95`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 42.4 MB (42436354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849edbf67b92b7fb2207db29ecdba74c08b5efd6f4afbd78be8ec16cac3a3cf3`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:9d04dc75a22805bf43d1c4dc6478f895db2717f663b6608b462c54fa4f8339c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a4eaca88fa36f0d4e347c1e2cf476eaadf4e897e89f05648de14a220f0355e`

```dockerfile
```

-	Layers:
	-	`sha256:91e0bad29f5e7eb29f5c25b82a7564e7bf1dfd01accfb09f73caabbeec9fd956`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97d554f781be765811186c6201793988d749108cefcedea863a561d1d8f70707`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 24.5 KB (24520 bytes)  
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
$ docker pull couchdb@sha256:02c08aa6ccd1bbe4a447a2bf780bd2dd5e6b665903f1342fbf574185788b2093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150104623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4662915212583b4484ce482a73cb7454d4e842a7fe3238857ff6f3dded91a901`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:07:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 03:07:30 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 03:07:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:07:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:07:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 03:07:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 03:07:56 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:07:56 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 03:08:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 03:08:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 03:08:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 03:08:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 03:08:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0325c5665933ad6d36f23a167563d05f063e037b0a2c5885e5e6e0d32e45fe`  
		Last Modified: Tue, 07 Apr 2026 03:08:26 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f6a0e5096d62644eef9382998fa5e3b7391a049d1c0ef34a2e6b75cd04d50c`  
		Last Modified: Tue, 07 Apr 2026 03:08:26 GMT  
		Size: 7.4 MB (7398906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1d0aaedcc65435ec10b159ce6394e9f4a79609f73b0ebfa5e46841180e4442`  
		Last Modified: Tue, 07 Apr 2026 03:08:27 GMT  
		Size: 73.2 MB (73153280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab558a5b81cc27b318fbe7efcd4862f3fa497f79bf7782a55c7937a0b55ed5a`  
		Last Modified: Tue, 07 Apr 2026 03:08:26 GMT  
		Size: 394.5 KB (394495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e8877983b9bf2198d7b1fa4536e45bf6e2004d074a249d75432bd413d49c0d`  
		Last Modified: Tue, 07 Apr 2026 03:08:27 GMT  
		Size: 99.7 KB (99683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2594178fe921993d30fd126010c6a3ffc3e2639fa081e3e139d9ebe72d483703`  
		Last Modified: Tue, 07 Apr 2026 03:08:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee0b40b98099ffa399c4e8b9fb4e401c136761dabd8177780b8224b2cf820b7`  
		Last Modified: Tue, 07 Apr 2026 03:08:28 GMT  
		Size: 42.2 MB (42164742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40375fa77ddfa72c67d888b04cc843ec0b7109b8489e251f505a6911a4c0d599`  
		Last Modified: Tue, 07 Apr 2026 03:08:28 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:9e57551628416a255325fd065213a5642ab3c22bc89fcef4490d1d51f6668fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a52d9aa17864ef8b3fa2ee2a50e9b593652183091ee805fa4112c889985a3aa`

```dockerfile
```

-	Layers:
	-	`sha256:24f3bc47c33d9ae50e545635452114b765abb97e69cc439ab1f84fc4fd8ae999`  
		Last Modified: Tue, 07 Apr 2026 03:08:26 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff901c13c497dc7bf1fca4d00d0ae10d681831afeee470e8175323e37f2e04a`  
		Last Modified: Tue, 07 Apr 2026 03:08:25 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1`

```console
$ docker pull couchdb@sha256:297cd556c7ba358a408fd009e7b8e3b91318ccfc4d57c9b0264a2fb051ad9ef7
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
$ docker pull couchdb@sha256:412d9e2d2a795689aae4649c3ce39d850f581d79d2e2cdda0f43d43b5784a7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4185b9c82e0dd524ff836db1302a606fd925df3a257cb2fd5c4c38030e2ff46`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:50:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:50:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 01:50:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:50:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:50:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:42 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 07 Apr 2026 01:50:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 01:50:56 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 01:50:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab90cd4f34eb266e96c3482fcf0545119db98813f49cb92ef036a7103e2b92d`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093df5069fd65f58ffa038b8565d9b62483be3e0385143e12c03125a8ee93c95`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 7.9 MB (7883128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c7afa3df02f8694bc940eb924d5f1b861da49c7f4ad4149668795f5a9eebda`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 401.8 KB (401798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e9c492394e1d1450767fcfb1ae7d2b3505fe39529766f9f6db3fe5c968dce`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 76.5 KB (76501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b75143212388be3686d25237e656cc612e77bbf8f4d22eb7d1cd8797ef16108`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b4fded2be747fe7bf75086ec7f8680932c0b00414d011bdfbc64714adf6616`  
		Last Modified: Tue, 07 Apr 2026 01:51:13 GMT  
		Size: 105.5 MB (105456616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efff0887044294c3a41bf062af7be716e4546f5ce0d6dbcf3467a0350712e7b5`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1565854ce2481500397988a06f4d22e0e04c8ca419ba2761307b49b1b30e7d9`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947144fea77c7536716edb5e10b8e7db805e5596afd66c74ded4d57cd09f5340`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6ddb5c9391738501e19bfa879bd74a7ecf21e8ee43fdc3c00d05d4353c4b0`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:ff2912e771a210d0468eb3642b93396fd21b02aeb75b5540608c671ac7358adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca3f4a5d6af0738c4ebfeae37ea86df346a879dba9189e447f6a598448bcd9d`

```dockerfile
```

-	Layers:
	-	`sha256:f07b8bfcb4a631b81fb400ad4dca9961d55a2e32ee7ea62e579a2655d82554e7`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d0c47b50673b86738db9192ced1c95bbd60da92277e16c85553429d1e26e3c`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
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
$ docker pull couchdb@sha256:cdbfc7dc13c7e84bce205cf0eb53f265cb615d2004aebf683c2b0428383c66da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138772786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b9631612e9613affbff05f7b39d8a84b83fc09bb0f7927c4b8c16dce5d72b1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:06:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 03:06:33 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 03:06:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:06:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 03:06:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 03:06:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:06:47 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 07 Apr 2026 03:06:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:07:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 03:07:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 03:07:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192343f77244f9b39a7ecfb9a796c0333f12d24bdbcae754cf0117a79f7f3934`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e5be0426e4ff4d1bf0334fb536bf055dfa3aeec7f489133ca20a1bc34d3c79`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 7.4 MB (7398861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f87c23fe5783e4304a5f717b05056909fda726aa92d0acf9f98817f997036f`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 372.1 KB (372118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d775362da2979c34fde865d14ad122d8553eb4fc5d6ace637c89477896127e6`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 76.5 KB (76513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9da8b7a3b5835503ffd44cdc3269dcd06969854d4814fcd0497cf8095e69606`  
		Last Modified: Tue, 07 Apr 2026 03:07:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951a55ad3b762664d23471edeca2bd8dfdfd061ef70dd69bdda14dbc60f7d3bf`  
		Last Modified: Tue, 07 Apr 2026 03:07:28 GMT  
		Size: 104.0 MB (104028227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9931be1abdbc7b505e6aa5b98d07b6f63a438ea9b338672e1f6d93e3f69fc30a`  
		Last Modified: Tue, 07 Apr 2026 03:07:26 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3268717766691d4b87f04d15e76af4daac8064116c3fc5778f26693781645a18`  
		Last Modified: Tue, 07 Apr 2026 03:07:27 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fa28adb917086950ef24369dc409fc275704c4c5a82b188d9fd4ca7e1ceed`  
		Last Modified: Tue, 07 Apr 2026 03:07:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c248872d02128bd249e2f94054c36a370b488ef81784ccde688d99cbb4d26f73`  
		Last Modified: Tue, 07 Apr 2026 03:07:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:58304d474775bc7d12994490c1199b324b5efbcac3ab7f09a010d04b1f1edc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6065d99a49523fc839f520abd1d5c74a084d236e36c3ff1489aab4936718cddf`

```dockerfile
```

-	Layers:
	-	`sha256:ad7949415d2685de52eb2f662e12403f20144faafda64063227fa25e40a8181f`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb520fe894dc058a0e9ba1ac3ab33141d8334bfd42807c6b532c314d55548cd`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1-nouveau`

```console
$ docker pull couchdb@sha256:179da13196874c2255cc3e8c0a4624279caac00d7dbad139f3f85eeea2313c45
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
$ docker pull couchdb@sha256:657ef169bfd7f014963baf6b1992eb074fdf402d9b55ad15147a1391357a3035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3494def2ab9551ec1eb0108dfb41be1aa9ad1ee3e9a0a9af151b4a50e44d2359`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:50:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:50:29 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:50:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:50:48 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:48 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:50:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 01:50:54 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 01:50:54 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 01:50:54 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 01:50:54 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c7b5629854a3acf585666bc40a4979bdc4f42e9e98225255a9456e2a95a3e3`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60aafff22dcb7c2819587ccce92fdd239c550a61f6df1cce33ab4845ad4a256b`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 7.9 MB (7883108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75ca1d1d73f13865d9e804875c290a3d19d7aea1f4080aef925abc882b978c`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 77.4 MB (77381369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d32b0944d9ae9f2816e6065898abbe564cc41ab6ac91e3301d7bca82b28cd5`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 424.2 KB (424163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb7734eed702acd55ab06083b6e32c788ccf28788808ca4118b9dbc5efecddf`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 99.5 KB (99547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5febb709bc54f7434563c0b6dffc32e17a7f33096a79e52043c39f148c7558c3`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d5a4ab2f174abccd784c7a554a7ccef6fdd34e93c3322d292c6d4cd94b6d95`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 42.4 MB (42436354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849edbf67b92b7fb2207db29ecdba74c08b5efd6f4afbd78be8ec16cac3a3cf3`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:9d04dc75a22805bf43d1c4dc6478f895db2717f663b6608b462c54fa4f8339c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a4eaca88fa36f0d4e347c1e2cf476eaadf4e897e89f05648de14a220f0355e`

```dockerfile
```

-	Layers:
	-	`sha256:91e0bad29f5e7eb29f5c25b82a7564e7bf1dfd01accfb09f73caabbeec9fd956`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97d554f781be765811186c6201793988d749108cefcedea863a561d1d8f70707`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 24.5 KB (24520 bytes)  
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
$ docker pull couchdb@sha256:02c08aa6ccd1bbe4a447a2bf780bd2dd5e6b665903f1342fbf574185788b2093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150104623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4662915212583b4484ce482a73cb7454d4e842a7fe3238857ff6f3dded91a901`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:07:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 03:07:30 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 07 Apr 2026 03:07:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:07:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:07:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 03:07:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 03:07:56 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:07:56 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 03:08:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 07 Apr 2026 03:08:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 07 Apr 2026 03:08:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 07 Apr 2026 03:08:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 07 Apr 2026 03:08:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0325c5665933ad6d36f23a167563d05f063e037b0a2c5885e5e6e0d32e45fe`  
		Last Modified: Tue, 07 Apr 2026 03:08:26 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f6a0e5096d62644eef9382998fa5e3b7391a049d1c0ef34a2e6b75cd04d50c`  
		Last Modified: Tue, 07 Apr 2026 03:08:26 GMT  
		Size: 7.4 MB (7398906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1d0aaedcc65435ec10b159ce6394e9f4a79609f73b0ebfa5e46841180e4442`  
		Last Modified: Tue, 07 Apr 2026 03:08:27 GMT  
		Size: 73.2 MB (73153280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab558a5b81cc27b318fbe7efcd4862f3fa497f79bf7782a55c7937a0b55ed5a`  
		Last Modified: Tue, 07 Apr 2026 03:08:26 GMT  
		Size: 394.5 KB (394495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e8877983b9bf2198d7b1fa4536e45bf6e2004d074a249d75432bd413d49c0d`  
		Last Modified: Tue, 07 Apr 2026 03:08:27 GMT  
		Size: 99.7 KB (99683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2594178fe921993d30fd126010c6a3ffc3e2639fa081e3e139d9ebe72d483703`  
		Last Modified: Tue, 07 Apr 2026 03:08:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee0b40b98099ffa399c4e8b9fb4e401c136761dabd8177780b8224b2cf820b7`  
		Last Modified: Tue, 07 Apr 2026 03:08:28 GMT  
		Size: 42.2 MB (42164742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40375fa77ddfa72c67d888b04cc843ec0b7109b8489e251f505a6911a4c0d599`  
		Last Modified: Tue, 07 Apr 2026 03:08:28 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:9e57551628416a255325fd065213a5642ab3c22bc89fcef4490d1d51f6668fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a52d9aa17864ef8b3fa2ee2a50e9b593652183091ee805fa4112c889985a3aa`

```dockerfile
```

-	Layers:
	-	`sha256:24f3bc47c33d9ae50e545635452114b765abb97e69cc439ab1f84fc4fd8ae999`  
		Last Modified: Tue, 07 Apr 2026 03:08:26 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff901c13c497dc7bf1fca4d00d0ae10d681831afeee470e8175323e37f2e04a`  
		Last Modified: Tue, 07 Apr 2026 03:08:25 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:297cd556c7ba358a408fd009e7b8e3b91318ccfc4d57c9b0264a2fb051ad9ef7
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
$ docker pull couchdb@sha256:412d9e2d2a795689aae4649c3ce39d850f581d79d2e2cdda0f43d43b5784a7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4185b9c82e0dd524ff836db1302a606fd925df3a257cb2fd5c4c38030e2ff46`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:50:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 01:50:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 01:50:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 01:50:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 01:50:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:42 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 07 Apr 2026 01:50:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:50:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 01:50:56 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 01:50:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab90cd4f34eb266e96c3482fcf0545119db98813f49cb92ef036a7103e2b92d`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093df5069fd65f58ffa038b8565d9b62483be3e0385143e12c03125a8ee93c95`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 7.9 MB (7883128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c7afa3df02f8694bc940eb924d5f1b861da49c7f4ad4149668795f5a9eebda`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 401.8 KB (401798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e9c492394e1d1450767fcfb1ae7d2b3505fe39529766f9f6db3fe5c968dce`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 76.5 KB (76501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b75143212388be3686d25237e656cc612e77bbf8f4d22eb7d1cd8797ef16108`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b4fded2be747fe7bf75086ec7f8680932c0b00414d011bdfbc64714adf6616`  
		Last Modified: Tue, 07 Apr 2026 01:51:13 GMT  
		Size: 105.5 MB (105456616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efff0887044294c3a41bf062af7be716e4546f5ce0d6dbcf3467a0350712e7b5`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1565854ce2481500397988a06f4d22e0e04c8ca419ba2761307b49b1b30e7d9`  
		Last Modified: Tue, 07 Apr 2026 01:51:11 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947144fea77c7536716edb5e10b8e7db805e5596afd66c74ded4d57cd09f5340`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6ddb5c9391738501e19bfa879bd74a7ecf21e8ee43fdc3c00d05d4353c4b0`  
		Last Modified: Tue, 07 Apr 2026 01:51:12 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:ff2912e771a210d0468eb3642b93396fd21b02aeb75b5540608c671ac7358adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca3f4a5d6af0738c4ebfeae37ea86df346a879dba9189e447f6a598448bcd9d`

```dockerfile
```

-	Layers:
	-	`sha256:f07b8bfcb4a631b81fb400ad4dca9961d55a2e32ee7ea62e579a2655d82554e7`  
		Last Modified: Tue, 07 Apr 2026 01:51:10 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d0c47b50673b86738db9192ced1c95bbd60da92277e16c85553429d1e26e3c`  
		Last Modified: Tue, 07 Apr 2026 01:51:09 GMT  
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
$ docker pull couchdb@sha256:cdbfc7dc13c7e84bce205cf0eb53f265cb615d2004aebf683c2b0428383c66da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138772786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b9631612e9613affbff05f7b39d8a84b83fc09bb0f7927c4b8c16dce5d72b1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:06:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 07 Apr 2026 03:06:33 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 07 Apr 2026 03:06:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:06:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 07 Apr 2026 03:06:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 07 Apr 2026 03:06:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:06:47 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 07 Apr 2026 03:06:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 03:07:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:07:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 07 Apr 2026 03:07:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 07 Apr 2026 03:07:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192343f77244f9b39a7ecfb9a796c0333f12d24bdbcae754cf0117a79f7f3934`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e5be0426e4ff4d1bf0334fb536bf055dfa3aeec7f489133ca20a1bc34d3c79`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 7.4 MB (7398861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f87c23fe5783e4304a5f717b05056909fda726aa92d0acf9f98817f997036f`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 372.1 KB (372118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d775362da2979c34fde865d14ad122d8553eb4fc5d6ace637c89477896127e6`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 76.5 KB (76513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9da8b7a3b5835503ffd44cdc3269dcd06969854d4814fcd0497cf8095e69606`  
		Last Modified: Tue, 07 Apr 2026 03:07:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951a55ad3b762664d23471edeca2bd8dfdfd061ef70dd69bdda14dbc60f7d3bf`  
		Last Modified: Tue, 07 Apr 2026 03:07:28 GMT  
		Size: 104.0 MB (104028227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9931be1abdbc7b505e6aa5b98d07b6f63a438ea9b338672e1f6d93e3f69fc30a`  
		Last Modified: Tue, 07 Apr 2026 03:07:26 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3268717766691d4b87f04d15e76af4daac8064116c3fc5778f26693781645a18`  
		Last Modified: Tue, 07 Apr 2026 03:07:27 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fa28adb917086950ef24369dc409fc275704c4c5a82b188d9fd4ca7e1ceed`  
		Last Modified: Tue, 07 Apr 2026 03:07:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c248872d02128bd249e2f94054c36a370b488ef81784ccde688d99cbb4d26f73`  
		Last Modified: Tue, 07 Apr 2026 03:07:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:58304d474775bc7d12994490c1199b324b5efbcac3ab7f09a010d04b1f1edc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6065d99a49523fc839f520abd1d5c74a084d236e36c3ff1489aab4936718cddf`

```dockerfile
```

-	Layers:
	-	`sha256:ad7949415d2685de52eb2f662e12403f20144faafda64063227fa25e40a8181f`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb520fe894dc058a0e9ba1ac3ab33141d8334bfd42807c6b532c314d55548cd`  
		Last Modified: Tue, 07 Apr 2026 03:07:25 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json
