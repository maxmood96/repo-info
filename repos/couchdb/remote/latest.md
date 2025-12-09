## `couchdb:latest`

```console
$ docker pull couchdb@sha256:a2c8839c86304962ae60df41c9aa51907925b7ca022b69acfcd45663a89daa77
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
$ docker pull couchdb@sha256:21fa430aae63671a3127673e38de2e2d071f0d3dbc8a31d8fac62214afc8f59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142051235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3b5c0109cce05b5ad263097797085346efb950cc7f38578fcdbe681a392fd9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:07:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:07:51 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 08 Dec 2025 23:07:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:08:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:08:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:05 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 08 Dec 2025 23:08:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:08:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:08:18 GMT
VOLUME [/opt/couchdb/data]
# Mon, 08 Dec 2025 23:08:18 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 08 Dec 2025 23:08:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c9c88e767d5012a0e2dfc399f43404f8f4c3ab262bac734533e8204099be56`  
		Last Modified: Mon, 08 Dec 2025 23:08:40 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716c80c273f8809bbb548458f931e4762b0f447aeca7508e13c19b9c51ff73c0`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 7.9 MB (7881739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609e5bdfa7b1f8218d7dca07b7adde8b80150cda1d87f1f29da51c3a313db82e`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 401.7 KB (401735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d5a41c17903fc51342b98f1560b681035cfe0f7d321a36b50f34de4387824e`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 76.5 KB (76465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b62383183a15d775ce3c4f9430de03b79d6935279d541adfff250dcc8dd91c1`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd726490d7d051e52d86d74f97c293416c4886a83478fc5a2d5b044d81865fee`  
		Last Modified: Mon, 08 Dec 2025 23:08:50 GMT  
		Size: 105.5 MB (105457448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8856ade7c27a5fad19081cfe83a474d6898d1154adff0b08e6d87e98b5c3de45`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2897b671832f132cfb5b6f0c62ea6b5e8c6575868e3a4e361ac25df1f27e196c`  
		Last Modified: Mon, 08 Dec 2025 23:08:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f82cbc9af1f4d32f1432c6cb4d15836c5891f1c431c9a75f8b08dfcd78e027a`  
		Last Modified: Mon, 08 Dec 2025 23:08:42 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b27282aaec507f7fcfa9a1efbb06f1abcd9cf46f8e39f236eb3c9a77a315e3`  
		Last Modified: Mon, 08 Dec 2025 23:08:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:aa6793cd8ef71d7ec06be94d34a9b693f27c315496b3d2778f2a2b406ffae798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087563041a4b7312487736498a1de80ea1d6f4ad2593c2b5efec7ae033626675`

```dockerfile
```

-	Layers:
	-	`sha256:e5384526458d9c66863e4dfe7e78e0b8c04ba19babd32f7e9d6cca6e9e683745`  
		Last Modified: Mon, 08 Dec 2025 23:34:23 GMT  
		Size: 4.2 MB (4184411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb9654333a4a6f0527c5d6d3686a1f350ad41a8b9d6ffa53b3e61c8d0be6a619`  
		Last Modified: Mon, 08 Dec 2025 23:34:24 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f1e92cf2901262cd034b1f9530b4bee200962755fa6dd125c025535926927e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141405024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3997adb6ec4d362257df7005caaa0d1e48141a808fceafd14ead1cf4f8466e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:11:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:11:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 08 Dec 2025 23:11:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:11:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:11:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:48 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 08 Dec 2025 23:11:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:12:01 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 08 Dec 2025 23:12:01 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 08 Dec 2025 23:12:01 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 08 Dec 2025 23:12:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 08 Dec 2025 23:12:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:12:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:12:01 GMT
VOLUME [/opt/couchdb/data]
# Mon, 08 Dec 2025 23:12:01 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 08 Dec 2025 23:12:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eac3ac086f4442b467b0df99ae5095a87be68fd28ef2d937dcb20ea2e875526`  
		Last Modified: Mon, 08 Dec 2025 23:12:25 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e82e75f5f1785c96b91eafbac53b93f11c8334675eaf40e7e1ee34043f2da0f`  
		Last Modified: Mon, 08 Dec 2025 23:12:26 GMT  
		Size: 7.7 MB (7692032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fe52f0ef87aa2c9f9d7f26dabad80b25e721105bd2b81d30d352a21f401ed8`  
		Last Modified: Mon, 08 Dec 2025 23:12:26 GMT  
		Size: 370.5 KB (370488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45819f207006702e1f587aab112f4da6b7d488eaa5e77dd23f9971160cb1b58`  
		Last Modified: Mon, 08 Dec 2025 23:12:25 GMT  
		Size: 76.5 KB (76460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2a457404becdc45a33081dbba53cd3088da6937d9bc551da38eff2e99638fc`  
		Last Modified: Mon, 08 Dec 2025 23:12:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadeafca4687c8c0493290c4bd119c0289671238efec178d1fa88b3210577f65`  
		Last Modified: Mon, 08 Dec 2025 23:12:34 GMT  
		Size: 105.2 MB (105158383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65aa9651b337f1798cf35004e8d641570bccd7479ecc8329fdabc674478225d`  
		Last Modified: Mon, 08 Dec 2025 23:12:25 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe8d350f59fee0fd36eedae9cf227654852937ee5e92433c188f27a26c53f60`  
		Last Modified: Mon, 08 Dec 2025 23:12:25 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ec0599cd19dffec83792d746d4ca0df31725f6d2451cf75c6b8b5c3f474ada`  
		Last Modified: Mon, 08 Dec 2025 23:12:25 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03016c5721a190600b93f30a83867690dd90a140e414fdbe08e3810c84d73e7`  
		Last Modified: Mon, 08 Dec 2025 23:12:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:f7bce22bfacba2a67d64498a57eb261adbfd659b6d59d7a272e2af9b1c1444aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef8d8ba9c836428241d987648dc118e90abd46ff0d23cf93aa5917eadf0c1da`

```dockerfile
```

-	Layers:
	-	`sha256:5d4e12184c2a91c43c416ee6c43249ae6e2b3f7d193cce28d2197ce3f69acca4`  
		Last Modified: Tue, 09 Dec 2025 05:33:29 GMT  
		Size: 4.2 MB (4184704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d09d2f4e7c902739e398af0692a004b05e702b70d57ba14ed2c3e8f12a1aae85`  
		Last Modified: Tue, 09 Dec 2025 05:33:30 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:c9a410eba40de845f009bd7e7034f257568c0b2d032050720dc43d773ccbc6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d610f8d7a2c99fd1337112307b105aa162a3c7aa8f7523d2f5097f9b4d352cd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:12:01 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Dec 2025 00:12:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 09 Dec 2025 00:12:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 09 Dec 2025 00:12:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 09 Dec 2025 00:12:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:14 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 09 Dec 2025 00:12:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:12:31 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:12:31 GMT
VOLUME [/opt/couchdb/data]
# Tue, 09 Dec 2025 00:12:31 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 09 Dec 2025 00:12:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf35cfc495ac6ff70615ca926f57eb6f3961039055b8e0bc78d371b81d66cdcc`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a773213be6f84f3b269baecb1e4cc68f15241c5c383b48b907976c4eb946677`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 7.4 MB (7398139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d5b33ae2cd1bbd5548a76327f0d452ff6f8ba5339ec9c241cbd71a9f453f10`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 372.1 KB (372110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec7e4611c56c4658d750fa9a9cfa1506d45b7d5ad3a68ff8bd891309614c227`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 76.5 KB (76496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fb144940d3c8de5b68011f7c579283d7e04801dd5de76eb64f57bfa89926d3`  
		Last Modified: Tue, 09 Dec 2025 00:12:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e990b9456e92e62ad8b10a958d9038d178a054f7af24c13a64841bba8bc484fe`  
		Last Modified: Tue, 09 Dec 2025 00:13:09 GMT  
		Size: 104.0 MB (104028693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de0c37a96fc881df0e067b4af3e9225be9f50b23eb987ee9b2b6bf242797f41`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845f1a6ee7ce778b2591bbfcde5ad849f34d69c6549c658cfab4f83234163c29`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ab7d725557e60a9b08e9efe0c6be7f3c6a76862af340465be69f3142fe7fd9`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324d82d39cdac56ca6ab5048a5efec1f0303825b13de2695e0014941f79017a2`  
		Last Modified: Tue, 09 Dec 2025 00:12:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:0c524c076ae68a0db10ef651ba126d5920fb123c6c7e6231b335c5b1153dd8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8210e9735ca6eef17803a45249133dedbb0fd46a7f39421c806f22e8329ecff3`

```dockerfile
```

-	Layers:
	-	`sha256:b31d81caa581677e3119d98b84d301af6dff06dc539097e3313a88ee79d4513f`  
		Last Modified: Tue, 09 Dec 2025 02:33:47 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0a65d403bfce6cbe8353b601006c63d5ec489b6ecd9989117ad8bc072515784`  
		Last Modified: Tue, 09 Dec 2025 02:33:48 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json
