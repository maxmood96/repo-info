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
