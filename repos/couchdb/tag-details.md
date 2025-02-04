<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3-nouveau`](#couchdb3-nouveau)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.3`](#couchdb333)
-	[`couchdb:3.4`](#couchdb34)
-	[`couchdb:3.4-nouveau`](#couchdb34-nouveau)
-	[`couchdb:3.4.2`](#couchdb342)
-	[`couchdb:3.4.2-nouveau`](#couchdb342-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:a385d09cba450e33deea4b2707908902b4048723f83e7df62f46b03040e99038
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
$ docker pull couchdb@sha256:e10c0f3e6c0c712e6063c116b9ed4d9530145cfa6c71b35973ab1288b718ce1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133224148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97276a50c66650259bff27f299b3879eb6f793a1ee385b854df88544e4bcf228`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620e8614251def9f3e21f2607dfb4ab6d91474b30fad9d43deacc5f0d48696ea`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d684a920aa356be64b82682bbf4c0f88d5abf94113387ecc4d0efb844a4ec2`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 7.9 MB (7874893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da294366959e243d3f089ff92fff1deb6ba777feb846c231be5187f356e33380`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 392.1 KB (392118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37af3863253f7bbaa9b21528b63d28fe9a00d77883df5b0e4b5f156a967e9e3d`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 76.3 KB (76267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346a8b8a4ffd80e156a8e419cc02193938388d350074b49d995fb53bda931cbf`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a024c30518341713bece7869318d94dec6795bd01ca6814983dd75b1f49c12`  
		Last Modified: Tue, 04 Feb 2025 04:39:03 GMT  
		Size: 96.7 MB (96663136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d163bbbd5791d7565e4860ced124ed43feae71b49f9200561f7855ef412aef75`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66582149d6e9c72698b767d96f223b0611f73576a5fa522694b22d9f47b230d`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0194a8b0180787f0b1df3a9dc9ec52591aa6dd41c33cc617f62bf6eab10f6937`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a13f3f3b60358a016fb2ee4601fe0f597688a87dc6ced132fe97e4e5191fc7a`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:5e051c5ecd6b3e5d50b2d30ebf489250d42ded305010a72563cd97ab46a8e8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054bf54b45ac2c98184be05a333ca8ee023c6fe407f51bdd237c2e488d81373b`

```dockerfile
```

-	Layers:
	-	`sha256:0baf39fa3a0bba9f04b4ec18984352fa1c76bfb3eff1875b60d0e66f2c0e1638`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 3.9 MB (3896283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1d84829d9b91d1749d30761f8b9be369dc2afb51fbadfa44edf6ec58c49edb`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:33ad9d3878354339233afe53bb87df412283410b29708a7ca796f9ac07f8b621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132524949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f1bc82926f249cbb136cfcfc223d28a194d2a83571874ab475e0fd4e4bbf1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a53b506eb957ed2ca989730c18ca42f6e0128157e3b16e04b417d5e3f6a46f`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0784cd6960fabd09529a3b70371d1a31ff9aec79c20d3905d9fbc1a2691c796`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 7.7 MB (7654466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79f2c1109f6989057dfe173d7350181a4d2c6c3094af18ca942f929b5893b99`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d118af51ca1a98ff6c7e8640d57cc57f54bf619a7beef5cfe3f06f5d8299b7`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 76.2 KB (76219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f6188d465363a65faca581e7a29deff62119c7229c06b69dee041e921beff`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4080fca21b251df01a293a38872fbe036647cd75dc3dc3d41eeacdcdc9f11e6`  
		Last Modified: Tue, 14 Jan 2025 07:04:13 GMT  
		Size: 96.4 MB (96398891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7570c55d2fc3d036f3606315986bce629111b93b08d0c34f0d640c69858cf107`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93840e26080be7ccca7b1d4b3b6eb7444f77b3ce0c1dc501a7758bd2dddd794`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349e54346d5fb87fe0546b92feeb3c137da315280a58ed267d31248215cee47c`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da7757a845ae5fd2495cc47db1219d3f9fa2fe4ce5b77dc66d72978d710e60`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:81d65dd5d6ce19f884c69e8e6f10a4bdeee710be6407fc88a62f4599fdd5733a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544e391940d4445a1238cc81cff3eb9c691a770fc7915e710bf9f5799eefb829`

```dockerfile
```

-	Layers:
	-	`sha256:2faae1cf4e6c027422c66213a29885c6bea7c0675ebb0d7bc08679fc799cd5b4`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 3.9 MB (3933852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1b443faafdd6eb68584662f9aa0484863d3df8417e5bcb83deb538bcc5d8a2`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:bbb98875c2e60d55251caf3ec546a6f399d0344b517aff3d9419956ecc5ca8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129973243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af20b8448a5fc255e2ca6ec2e4b21aa035fe206f22cc74cd6b4e5667d18eaf94`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669ae66225b713189254b710db60d969b0da76c3a6fbfb597d3800dd2869e819`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43419d0575fa54de01c352b29709b0d5ccf15c49d3d1bcc25378930552dfbb`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 7.4 MB (7387928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705dcc6c28fd9ac1b53e0c99842c5e89260eaab760fc90e0989d4a5882121d7e`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 355.6 KB (355637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6008ecd238bf91fc60b5f372ddfdaf51cdc8a9afc258c4548be4d79f12ca23f9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 76.3 KB (76344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfff5ef737373de6ea03d251c1b50454071af66acdb81e7b7c7e04dfdf59fc9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970c2190b221a43960164c74df60732029a7aa45d4eccacc86cf8ed02e90a486`  
		Last Modified: Tue, 04 Feb 2025 07:35:44 GMT  
		Size: 95.3 MB (95289278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbca118bd3ee0264e7ab445907d9c994fcbe1ed9648b8eda4ffe96039cb9a0e`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6160c94cff5d390694fc67808062b79858db1a3398572487e90b4dc650545e6`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e20f342f24eeb86e2afa69eadfe2557a8a501105122c12940a5cc51347802ab`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaf3ddd7aa622b677ecfa8bac5af11f43f3f7d9217667acddd3d79c7c6ea220`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:fdc5ff418ce8940a48676ecb4f18464d922e1b3d7497b403ed26212bee936858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e961e74e238ac3326e88c598f3bd0ca37edca382b81867b8408e055b2a6ec8f`

```dockerfile
```

-	Layers:
	-	`sha256:eb4ee4c1d3c17de162d0cbf896506cb6a51b80c7095de98122fc04b08426ba87`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 3.9 MB (3932647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08d8adad896f090fbd3dc0dfc0edeebf4ed61abaacf54431482a74e0343885f`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:35d66c57efa2d6793f4dbecca8669fa1b73848b30e122e0271fd55f94996defc
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
$ docker pull couchdb@sha256:3367d5bccdc6396d4dfceaefb7be51f7b620060687976d4cb9710ca25e74edf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155532459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d8f9304ca9fc9cd9e8cfc0eebe108b76ec0de354123c8ccb5c037d31fd7c8c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d037aa722688de92adccb49fc02c65a62c4c2cd27dcad1aeb2669f2bc91c80`  
		Last Modified: Tue, 04 Feb 2025 04:38:57 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e1d3bf05d75710981db4a96e2b04ef0c4afbbf6e85fd66a75f47fa297c4418`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 7.9 MB (7874966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6ca1ef4e87822fa39ec77697ee19ee6e4c576d95cd6abbc110cb78e304e7fd`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 77.3 MB (77297441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b372823eab782fcf3ece2ce60437b076a83b6c18a91556dffbe12dcda6b77afb`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 414.9 KB (414935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c576d613f05214b663520384e2869fbfc8f022d828d799aba2eec3f39b0938`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 99.3 KB (99256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c158c51f6fa6055b49d8c93af63541e2a089873c92e50b60fcfd0042c460906d`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8b077ccd40cbf7eb1c494f65740d7a239a1c73a17c6fde0c9ce8ce66110c20`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 41.6 MB (41631683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6b94af6e4c08acd7923e4e5a16820d970152112c37a2fad99d74c7699868cc`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:0de0127374b8540c659ab771f5b9745858025812986f54653259e636e896bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dae0896f708bd13ef93048d280814ecc91d146a5ad7bd37adb354883947042d`

```dockerfile
```

-	Layers:
	-	`sha256:a889570ca4ab953857162a24ba10a8455803b9bef0e936f01a53f75796efce8c`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 3.5 MB (3462052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d12304afa1e2544372cf3ebd188cbc02fb0d22a90f98f6add8b5b32f904428`  
		Last Modified: Tue, 04 Feb 2025 04:38:57 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ef7c562863a9fb584cc36263dc82db193a4a5c3956927ae78e18f702c0c5518e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154278229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b719cad0c7b5fdbfdbbac6dcb7a1e2ebde3550a3fe03266cf60522f6be67bab3`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79173b3fddb7da2629dd339e0d53b403ea8827bcbd9b247d684b58d32dff7cbf`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31829078e1f4de67fcedf6a2d2d8ca1872f489122c7b4bcfa3cd33532c8cb239`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 7.7 MB (7654485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3369295dc500f95559ea4509a427d2c0a4ee1c8ad2b7a79ee1dc560350241f77`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 76.6 MB (76582294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e5bbcf4591afaea2d2cdc136dc489080dd97d81c24bd3ccbe400297114b51b`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 371.7 KB (371693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acdad20d9a721bac2eb158329512906baee9555218f01a8e6ff0f9275510c66`  
		Last Modified: Tue, 14 Jan 2025 07:05:13 GMT  
		Size: 99.2 KB (99208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e627f9bf3e789b44c13cb9953004b89c6d68b322ee687562fe9fb76268a2d868`  
		Last Modified: Tue, 14 Jan 2025 07:05:13 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebeb5aa1e3f7f6837e61861bc4d688a7cb0e40daf66afe7b53355998b6c50ed`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 41.5 MB (41527641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10a636108d2adc58e1f2c66283165d3226827a0d533ede0055e897d2464c6ed`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:80be29eb1df008c822ee482e3954caa2ef94c11a5a1950dd74dbbaa0c6ace91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071743ecadfba0fe3591807a89eb13c2932c9c451dc0d4b7924bb78aef478550`

```dockerfile
```

-	Layers:
	-	`sha256:c09558bcbcbf4d95c177b3cde1b9c16427e89ea9acbaf37de09ff936af7f2e77`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 3.5 MB (3460732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1295fd7d68dfa423f317cb0bff79f1b1008e1459b1398163e931f34e6ccd895d`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:c7ef31bf2d0cf9cadfe093f47d3336284a052b7c09043f3baa84a0e3fa393386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149142669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4aeeab96a922d7a1ab78f8460fac69a2a816ca3b6e125fed1cb4a6eed7411b5`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a23a693d0435d9096a59c377a713b723450b592d3b5f06316fef9eeb38f17`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc051593c4a07ef7ad5fd762b44283836710587d01abf2ebeb0a56303ab6172`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 7.4 MB (7387901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f817f6fdb7f13d39c4df0f552ef9ca2bfa6e668a454e1da6ca2517a8efc439d9`  
		Last Modified: Tue, 04 Feb 2025 07:37:09 GMT  
		Size: 73.1 MB (73065167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0494d93c365c028f5059417ba8bf7f9b24d431a31b87fa6377d4e1d180e457af`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 378.0 KB (378017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7ebdc392d75cc71bd7cc7de5e4d9eea830b1b497cc592e1fec293906ad84a9`  
		Last Modified: Tue, 04 Feb 2025 07:37:07 GMT  
		Size: 99.4 KB (99372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4bcabe0e2faf2b52aaaa7bd8b12785b477e128f41870e5861a2fb57f266265`  
		Last Modified: Tue, 04 Feb 2025 07:37:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5594b52dc2ed41f07ca8731f1d3a1508f5f12286f3634272fb8051567df6b2`  
		Last Modified: Tue, 04 Feb 2025 07:37:08 GMT  
		Size: 41.4 MB (41351710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c8d679dc3d3d2968163532ab43de3cb43616f56858284de5bf2568d257228`  
		Last Modified: Tue, 04 Feb 2025 07:37:08 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:147ab9a2677c357e1185b231e231327efff5ee9bd4cb79ccd3cd7fee80e76849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e49dab81e90811dc3c065f49d460570083ed955142335d69205c40bcdf8370`

```dockerfile
```

-	Layers:
	-	`sha256:37f16ce50caae56e4424d9c7450676605d4306866eae78748dc06d4a5f21d5ac`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 3.5 MB (3455473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ef3b0df1d1e6be3ac92374cbf00a63eb24792839bf9e5fbd9a50931ab50a58`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:def04e063175244411cb15bef573038e7d5ccfba70061fb1be792474e74ebb6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:55b4f945aefb020feac3c3e3aeab6b58bd275a2ded32b7bb5d7bac48b331c31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96711817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea263a3c4a41b0ab84fa84f757b7491828b43874396212737a1634189c778b16`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58376d162d25fe80ee98f462c228456fb3c352e675348db0442ca2a1abbfd65f`  
		Last Modified: Tue, 04 Feb 2025 04:38:48 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd6d7f87d2a6c7d33df8048f27bcb0e4e33ad8e3938ddc9e3fadecf3dc076ae`  
		Last Modified: Tue, 04 Feb 2025 04:38:48 GMT  
		Size: 7.9 MB (7874912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bef4176df8018bc88f9e8d4aee9e889c876a1bf04b7d7d3c615c7fe4ef9a47e`  
		Last Modified: Tue, 04 Feb 2025 04:38:48 GMT  
		Size: 392.1 KB (392125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ed9be0eb984e322d2a1739043099b7bbb5dfe482cc520ea33c11759f35080`  
		Last Modified: Tue, 04 Feb 2025 04:38:48 GMT  
		Size: 76.3 KB (76274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5685345981ace635f5ad176ec032beda49ac1c5e3c91ed66be454b4602892066`  
		Last Modified: Tue, 04 Feb 2025 04:38:49 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133cfa0e6c305be10ddb1a67b98749c3de0d380cbe883edec7c8cd61c3068426`  
		Last Modified: Tue, 04 Feb 2025 04:38:50 GMT  
		Size: 60.2 MB (60150776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7207f8ca5452d62de2792b1cade725370968c721dd7ffc03b3fed7c02ee2b7eb`  
		Last Modified: Tue, 04 Feb 2025 04:38:49 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78b04c637adc92b39598c383a2fa3eeb52c32194242f54965b5b5e9cf13ef73`  
		Last Modified: Tue, 04 Feb 2025 04:38:49 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6b3e7c265253b4943c34b3c47bfcff4a4c25554b1275caf6d65133752059ab`  
		Last Modified: Tue, 04 Feb 2025 04:38:50 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1874ea04f61a9a21f98fe77975865a79aeeb3ad5a28daf6d0070898fdec5cdc2`  
		Last Modified: Tue, 04 Feb 2025 04:38:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:3beed3918969eef9ba76bde72061a1a722bc2ddb9cf77a02e455aabf60e864a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df503f1eb4cfa49ead05675be23ad539bf20d15a1aff306b44430bdf45b4e32`

```dockerfile
```

-	Layers:
	-	`sha256:579be4d6f0c65969a8eb0509ec3da85630d7941d64fbb1fa6d532d1a5f8df085`  
		Last Modified: Tue, 04 Feb 2025 04:38:48 GMT  
		Size: 3.7 MB (3698372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0776fc968375ae176ddeace34eaf88c5b8e4d29a374ef54d930f1a1e6cd2fc1f`  
		Last Modified: Tue, 04 Feb 2025 04:38:48 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c0bb87f69d46b18ec45cbcf834192896e3e859db5a46d877be6d100e0f2623dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96060414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d8092deae5348ef21718fe3fcbb35c16a1c8d64b135f940c0d25846069883c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a53b506eb957ed2ca989730c18ca42f6e0128157e3b16e04b417d5e3f6a46f`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0784cd6960fabd09529a3b70371d1a31ff9aec79c20d3905d9fbc1a2691c796`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 7.7 MB (7654466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79f2c1109f6989057dfe173d7350181a4d2c6c3094af18ca942f929b5893b99`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d118af51ca1a98ff6c7e8640d57cc57f54bf619a7beef5cfe3f06f5d8299b7`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 76.2 KB (76219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70acf8981345c4c2a35e1ef34d5db2157777309445979db5767b97fc3ed74380`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f95816f87e3225f4e1decf3e501fae6fbb6790fad0b7d8d65a087ae7b29ef8`  
		Last Modified: Tue, 14 Jan 2025 07:05:55 GMT  
		Size: 59.9 MB (59934359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2992763f8eefdb45c31411dd67a9d564ad9f745ddb5342c8d81ce027619b5f34`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18af3d99a0909022477de34e3cd41b27f0c05f808cc2e7a9cd993b773424965b`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22a682458745202fb57c949931140297950f9b433e640814950c8a46e89de1d`  
		Last Modified: Tue, 14 Jan 2025 07:05:54 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb4f8794b170cd72d38e6e6693c4646cfdc79bb031c87df8d7fee3e8a76e91`  
		Last Modified: Tue, 14 Jan 2025 07:05:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c6a13eba71489fc59cd9c92ca465c308193f05103cfb0b5c34af7a8699d65767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d682b7d719df0c02ea96d9b87369a7aa958d848c8c1ebf95abad2e067349a2`

```dockerfile
```

-	Layers:
	-	`sha256:01960cba2344e00884c069dc1c4d74378f68588eff6590d21e9c9edfcfcc8c64`  
		Last Modified: Tue, 14 Jan 2025 07:05:54 GMT  
		Size: 3.7 MB (3735107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0709b04a14934c67ffd272b0d10dfe004ebad1b15ebbbe8635eac9ff16d5fe1a`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 31.4 KB (31362 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:3a140313823911e3c1db2e48191bccd4898056e085244f920ade84619c31a564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102836846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4346fa901d234e41afc2509951d3c94bf195c55afda16eba9aeedf702bb484cf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6343a4b4aeeeab9c051546265872435047202642256c8e68f0ae9cf38160646d`  
		Last Modified: Tue, 04 Feb 2025 07:30:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae6aa5ed119eaf586e5c8e810cfa2eb7f882cee15d58183d83e04bacc30330c`  
		Last Modified: Tue, 04 Feb 2025 07:30:24 GMT  
		Size: 8.9 MB (8890118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbcf71734107ef1ef3b762a14fd302cbe93198eaab012f4121720ff816b7d24`  
		Last Modified: Tue, 04 Feb 2025 07:30:23 GMT  
		Size: 444.6 KB (444648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3397c8cee5e82679b80359ffc3aa332905e3da2f603b467945697aa7a49c848`  
		Last Modified: Tue, 04 Feb 2025 07:30:23 GMT  
		Size: 76.3 KB (76325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb1ade8161a8d909c332c77cf066875ffb3ebff866a893b0a3f6f9567ad1efc`  
		Last Modified: Tue, 04 Feb 2025 07:30:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd3a88468b6b8268a0185489fbedcab6987f2f571b373e5d6faf3ed3b375165`  
		Last Modified: Tue, 04 Feb 2025 07:30:26 GMT  
		Size: 61.4 MB (61375539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518f6d14e88f1111d4ece696bf35f1090f696deddee6ddac6d6f3ef5603428a3`  
		Last Modified: Tue, 04 Feb 2025 07:30:25 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eeae8294dc8b46567b271c4daa060f25df3eb9daf2d69c2a8673a8c217952ef`  
		Last Modified: Tue, 04 Feb 2025 07:30:25 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a03d0b866fa2083f92a671d2a641e28e8c9f70ecf4846efdec26d4897f616b`  
		Last Modified: Tue, 04 Feb 2025 07:30:25 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803685ece258ded148e69f52395badae1878657da87e6ecf7a6fdac4124f353a`  
		Last Modified: Tue, 04 Feb 2025 07:30:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:524c331b535631d2608bd3d311cb0f78246b4bd96c41ec574113644018d3161e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3770578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64a9c53480ab239da584f9b8a6fe1eab2908f1d41551b096a9f9fe0625903f5`

```dockerfile
```

-	Layers:
	-	`sha256:3a80b6d43a1c2bf465e5689c93b3ec527299a69077312e0d2c647b4e7a87a6a5`  
		Last Modified: Tue, 04 Feb 2025 07:30:23 GMT  
		Size: 3.7 MB (3739342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c9326de3c0112265b4cfb1be11354b2ddb6b81791886031aa2de8382725c74`  
		Last Modified: Tue, 04 Feb 2025 07:30:23 GMT  
		Size: 31.2 KB (31236 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:f806d0e8d48d723abd226bfe56f1ee66f0c105b023165fed8b0603088d35879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93424352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3120857c7cd5358be78df5d0a64f0ebdf454ae26e0ca620f6fba80bfd8cdb1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669ae66225b713189254b710db60d969b0da76c3a6fbfb597d3800dd2869e819`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43419d0575fa54de01c352b29709b0d5ccf15c49d3d1bcc25378930552dfbb`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 7.4 MB (7387928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705dcc6c28fd9ac1b53e0c99842c5e89260eaab760fc90e0989d4a5882121d7e`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 355.6 KB (355637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6008ecd238bf91fc60b5f372ddfdaf51cdc8a9afc258c4548be4d79f12ca23f9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 76.3 KB (76344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d368db74aca8069e746f41ea3262a15295a440bc0581103284d5f6a945bf8a3`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd1272845325e4cc432438bb9d5a803eb4077929c98b0caa67cddd2d5bc5204`  
		Last Modified: Tue, 04 Feb 2025 07:38:33 GMT  
		Size: 58.7 MB (58740382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5f89192dfb5c79e22c6858e946d89981fa419030667e29a8a2ade095453bc8`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ded5cd457c8f978623355726031c8b4bda96e9adc258fd3565df2bf02f7b6a1`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43362fd9147e5da284972e9d11a1386096074aec9e0e42612c3aa9edab0a0890`  
		Last Modified: Tue, 04 Feb 2025 07:38:32 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f555ef45dcf68ec7fdd9280dd9ac90cbaed985d644417539d7802a26f69b4ce7`  
		Last Modified: Tue, 04 Feb 2025 07:38:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:5d1912c62dc995a38321d928950f0e50585737b8de9f3e07185da9dff0bbb3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3765118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbba2b8fefee56480374411558cd98ed349cb446953d41abb2695bfe5dc7178`

```dockerfile
```

-	Layers:
	-	`sha256:46498bf7cc20271924d83a4520a85aa1ea05177e5ae9561e1b98874f42d65bcb`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 3.7 MB (3733926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f505cf7b3bcaeebd2cad48b853850d61e42f252a718718fa7cbb02ad4cf89a`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:def04e063175244411cb15bef573038e7d5ccfba70061fb1be792474e74ebb6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:55b4f945aefb020feac3c3e3aeab6b58bd275a2ded32b7bb5d7bac48b331c31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96711817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea263a3c4a41b0ab84fa84f757b7491828b43874396212737a1634189c778b16`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58376d162d25fe80ee98f462c228456fb3c352e675348db0442ca2a1abbfd65f`  
		Last Modified: Tue, 04 Feb 2025 04:38:48 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd6d7f87d2a6c7d33df8048f27bcb0e4e33ad8e3938ddc9e3fadecf3dc076ae`  
		Last Modified: Tue, 04 Feb 2025 04:38:48 GMT  
		Size: 7.9 MB (7874912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bef4176df8018bc88f9e8d4aee9e889c876a1bf04b7d7d3c615c7fe4ef9a47e`  
		Last Modified: Tue, 04 Feb 2025 04:38:48 GMT  
		Size: 392.1 KB (392125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ed9be0eb984e322d2a1739043099b7bbb5dfe482cc520ea33c11759f35080`  
		Last Modified: Tue, 04 Feb 2025 04:38:48 GMT  
		Size: 76.3 KB (76274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5685345981ace635f5ad176ec032beda49ac1c5e3c91ed66be454b4602892066`  
		Last Modified: Tue, 04 Feb 2025 04:38:49 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133cfa0e6c305be10ddb1a67b98749c3de0d380cbe883edec7c8cd61c3068426`  
		Last Modified: Tue, 04 Feb 2025 04:38:50 GMT  
		Size: 60.2 MB (60150776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7207f8ca5452d62de2792b1cade725370968c721dd7ffc03b3fed7c02ee2b7eb`  
		Last Modified: Tue, 04 Feb 2025 04:38:49 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78b04c637adc92b39598c383a2fa3eeb52c32194242f54965b5b5e9cf13ef73`  
		Last Modified: Tue, 04 Feb 2025 04:38:49 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6b3e7c265253b4943c34b3c47bfcff4a4c25554b1275caf6d65133752059ab`  
		Last Modified: Tue, 04 Feb 2025 04:38:50 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1874ea04f61a9a21f98fe77975865a79aeeb3ad5a28daf6d0070898fdec5cdc2`  
		Last Modified: Tue, 04 Feb 2025 04:38:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:3beed3918969eef9ba76bde72061a1a722bc2ddb9cf77a02e455aabf60e864a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df503f1eb4cfa49ead05675be23ad539bf20d15a1aff306b44430bdf45b4e32`

```dockerfile
```

-	Layers:
	-	`sha256:579be4d6f0c65969a8eb0509ec3da85630d7941d64fbb1fa6d532d1a5f8df085`  
		Last Modified: Tue, 04 Feb 2025 04:38:48 GMT  
		Size: 3.7 MB (3698372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0776fc968375ae176ddeace34eaf88c5b8e4d29a374ef54d930f1a1e6cd2fc1f`  
		Last Modified: Tue, 04 Feb 2025 04:38:48 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c0bb87f69d46b18ec45cbcf834192896e3e859db5a46d877be6d100e0f2623dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96060414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d8092deae5348ef21718fe3fcbb35c16a1c8d64b135f940c0d25846069883c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a53b506eb957ed2ca989730c18ca42f6e0128157e3b16e04b417d5e3f6a46f`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0784cd6960fabd09529a3b70371d1a31ff9aec79c20d3905d9fbc1a2691c796`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 7.7 MB (7654466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79f2c1109f6989057dfe173d7350181a4d2c6c3094af18ca942f929b5893b99`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d118af51ca1a98ff6c7e8640d57cc57f54bf619a7beef5cfe3f06f5d8299b7`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 76.2 KB (76219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70acf8981345c4c2a35e1ef34d5db2157777309445979db5767b97fc3ed74380`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f95816f87e3225f4e1decf3e501fae6fbb6790fad0b7d8d65a087ae7b29ef8`  
		Last Modified: Tue, 14 Jan 2025 07:05:55 GMT  
		Size: 59.9 MB (59934359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2992763f8eefdb45c31411dd67a9d564ad9f745ddb5342c8d81ce027619b5f34`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18af3d99a0909022477de34e3cd41b27f0c05f808cc2e7a9cd993b773424965b`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22a682458745202fb57c949931140297950f9b433e640814950c8a46e89de1d`  
		Last Modified: Tue, 14 Jan 2025 07:05:54 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb4f8794b170cd72d38e6e6693c4646cfdc79bb031c87df8d7fee3e8a76e91`  
		Last Modified: Tue, 14 Jan 2025 07:05:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c6a13eba71489fc59cd9c92ca465c308193f05103cfb0b5c34af7a8699d65767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d682b7d719df0c02ea96d9b87369a7aa958d848c8c1ebf95abad2e067349a2`

```dockerfile
```

-	Layers:
	-	`sha256:01960cba2344e00884c069dc1c4d74378f68588eff6590d21e9c9edfcfcc8c64`  
		Last Modified: Tue, 14 Jan 2025 07:05:54 GMT  
		Size: 3.7 MB (3735107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0709b04a14934c67ffd272b0d10dfe004ebad1b15ebbbe8635eac9ff16d5fe1a`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 31.4 KB (31362 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:3a140313823911e3c1db2e48191bccd4898056e085244f920ade84619c31a564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102836846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4346fa901d234e41afc2509951d3c94bf195c55afda16eba9aeedf702bb484cf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6343a4b4aeeeab9c051546265872435047202642256c8e68f0ae9cf38160646d`  
		Last Modified: Tue, 04 Feb 2025 07:30:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae6aa5ed119eaf586e5c8e810cfa2eb7f882cee15d58183d83e04bacc30330c`  
		Last Modified: Tue, 04 Feb 2025 07:30:24 GMT  
		Size: 8.9 MB (8890118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbcf71734107ef1ef3b762a14fd302cbe93198eaab012f4121720ff816b7d24`  
		Last Modified: Tue, 04 Feb 2025 07:30:23 GMT  
		Size: 444.6 KB (444648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3397c8cee5e82679b80359ffc3aa332905e3da2f603b467945697aa7a49c848`  
		Last Modified: Tue, 04 Feb 2025 07:30:23 GMT  
		Size: 76.3 KB (76325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb1ade8161a8d909c332c77cf066875ffb3ebff866a893b0a3f6f9567ad1efc`  
		Last Modified: Tue, 04 Feb 2025 07:30:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd3a88468b6b8268a0185489fbedcab6987f2f571b373e5d6faf3ed3b375165`  
		Last Modified: Tue, 04 Feb 2025 07:30:26 GMT  
		Size: 61.4 MB (61375539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518f6d14e88f1111d4ece696bf35f1090f696deddee6ddac6d6f3ef5603428a3`  
		Last Modified: Tue, 04 Feb 2025 07:30:25 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eeae8294dc8b46567b271c4daa060f25df3eb9daf2d69c2a8673a8c217952ef`  
		Last Modified: Tue, 04 Feb 2025 07:30:25 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a03d0b866fa2083f92a671d2a641e28e8c9f70ecf4846efdec26d4897f616b`  
		Last Modified: Tue, 04 Feb 2025 07:30:25 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803685ece258ded148e69f52395badae1878657da87e6ecf7a6fdac4124f353a`  
		Last Modified: Tue, 04 Feb 2025 07:30:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:524c331b535631d2608bd3d311cb0f78246b4bd96c41ec574113644018d3161e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3770578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64a9c53480ab239da584f9b8a6fe1eab2908f1d41551b096a9f9fe0625903f5`

```dockerfile
```

-	Layers:
	-	`sha256:3a80b6d43a1c2bf465e5689c93b3ec527299a69077312e0d2c647b4e7a87a6a5`  
		Last Modified: Tue, 04 Feb 2025 07:30:23 GMT  
		Size: 3.7 MB (3739342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c9326de3c0112265b4cfb1be11354b2ddb6b81791886031aa2de8382725c74`  
		Last Modified: Tue, 04 Feb 2025 07:30:23 GMT  
		Size: 31.2 KB (31236 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:f806d0e8d48d723abd226bfe56f1ee66f0c105b023165fed8b0603088d35879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93424352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3120857c7cd5358be78df5d0a64f0ebdf454ae26e0ca620f6fba80bfd8cdb1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669ae66225b713189254b710db60d969b0da76c3a6fbfb597d3800dd2869e819`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43419d0575fa54de01c352b29709b0d5ccf15c49d3d1bcc25378930552dfbb`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 7.4 MB (7387928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705dcc6c28fd9ac1b53e0c99842c5e89260eaab760fc90e0989d4a5882121d7e`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 355.6 KB (355637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6008ecd238bf91fc60b5f372ddfdaf51cdc8a9afc258c4548be4d79f12ca23f9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 76.3 KB (76344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d368db74aca8069e746f41ea3262a15295a440bc0581103284d5f6a945bf8a3`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd1272845325e4cc432438bb9d5a803eb4077929c98b0caa67cddd2d5bc5204`  
		Last Modified: Tue, 04 Feb 2025 07:38:33 GMT  
		Size: 58.7 MB (58740382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5f89192dfb5c79e22c6858e946d89981fa419030667e29a8a2ade095453bc8`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ded5cd457c8f978623355726031c8b4bda96e9adc258fd3565df2bf02f7b6a1`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43362fd9147e5da284972e9d11a1386096074aec9e0e42612c3aa9edab0a0890`  
		Last Modified: Tue, 04 Feb 2025 07:38:32 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f555ef45dcf68ec7fdd9280dd9ac90cbaed985d644417539d7802a26f69b4ce7`  
		Last Modified: Tue, 04 Feb 2025 07:38:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:5d1912c62dc995a38321d928950f0e50585737b8de9f3e07185da9dff0bbb3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3765118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbba2b8fefee56480374411558cd98ed349cb446953d41abb2695bfe5dc7178`

```dockerfile
```

-	Layers:
	-	`sha256:46498bf7cc20271924d83a4520a85aa1ea05177e5ae9561e1b98874f42d65bcb`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 3.7 MB (3733926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f505cf7b3bcaeebd2cad48b853850d61e42f252a718718fa7cbb02ad4cf89a`  
		Last Modified: Tue, 04 Feb 2025 07:38:31 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:a385d09cba450e33deea4b2707908902b4048723f83e7df62f46b03040e99038
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
$ docker pull couchdb@sha256:e10c0f3e6c0c712e6063c116b9ed4d9530145cfa6c71b35973ab1288b718ce1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133224148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97276a50c66650259bff27f299b3879eb6f793a1ee385b854df88544e4bcf228`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620e8614251def9f3e21f2607dfb4ab6d91474b30fad9d43deacc5f0d48696ea`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d684a920aa356be64b82682bbf4c0f88d5abf94113387ecc4d0efb844a4ec2`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 7.9 MB (7874893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da294366959e243d3f089ff92fff1deb6ba777feb846c231be5187f356e33380`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 392.1 KB (392118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37af3863253f7bbaa9b21528b63d28fe9a00d77883df5b0e4b5f156a967e9e3d`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 76.3 KB (76267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346a8b8a4ffd80e156a8e419cc02193938388d350074b49d995fb53bda931cbf`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a024c30518341713bece7869318d94dec6795bd01ca6814983dd75b1f49c12`  
		Last Modified: Tue, 04 Feb 2025 04:39:03 GMT  
		Size: 96.7 MB (96663136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d163bbbd5791d7565e4860ced124ed43feae71b49f9200561f7855ef412aef75`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66582149d6e9c72698b767d96f223b0611f73576a5fa522694b22d9f47b230d`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0194a8b0180787f0b1df3a9dc9ec52591aa6dd41c33cc617f62bf6eab10f6937`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a13f3f3b60358a016fb2ee4601fe0f597688a87dc6ced132fe97e4e5191fc7a`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:5e051c5ecd6b3e5d50b2d30ebf489250d42ded305010a72563cd97ab46a8e8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054bf54b45ac2c98184be05a333ca8ee023c6fe407f51bdd237c2e488d81373b`

```dockerfile
```

-	Layers:
	-	`sha256:0baf39fa3a0bba9f04b4ec18984352fa1c76bfb3eff1875b60d0e66f2c0e1638`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 3.9 MB (3896283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1d84829d9b91d1749d30761f8b9be369dc2afb51fbadfa44edf6ec58c49edb`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:33ad9d3878354339233afe53bb87df412283410b29708a7ca796f9ac07f8b621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132524949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f1bc82926f249cbb136cfcfc223d28a194d2a83571874ab475e0fd4e4bbf1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a53b506eb957ed2ca989730c18ca42f6e0128157e3b16e04b417d5e3f6a46f`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0784cd6960fabd09529a3b70371d1a31ff9aec79c20d3905d9fbc1a2691c796`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 7.7 MB (7654466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79f2c1109f6989057dfe173d7350181a4d2c6c3094af18ca942f929b5893b99`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d118af51ca1a98ff6c7e8640d57cc57f54bf619a7beef5cfe3f06f5d8299b7`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 76.2 KB (76219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f6188d465363a65faca581e7a29deff62119c7229c06b69dee041e921beff`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4080fca21b251df01a293a38872fbe036647cd75dc3dc3d41eeacdcdc9f11e6`  
		Last Modified: Tue, 14 Jan 2025 07:04:13 GMT  
		Size: 96.4 MB (96398891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7570c55d2fc3d036f3606315986bce629111b93b08d0c34f0d640c69858cf107`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93840e26080be7ccca7b1d4b3b6eb7444f77b3ce0c1dc501a7758bd2dddd794`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349e54346d5fb87fe0546b92feeb3c137da315280a58ed267d31248215cee47c`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da7757a845ae5fd2495cc47db1219d3f9fa2fe4ce5b77dc66d72978d710e60`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:81d65dd5d6ce19f884c69e8e6f10a4bdeee710be6407fc88a62f4599fdd5733a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544e391940d4445a1238cc81cff3eb9c691a770fc7915e710bf9f5799eefb829`

```dockerfile
```

-	Layers:
	-	`sha256:2faae1cf4e6c027422c66213a29885c6bea7c0675ebb0d7bc08679fc799cd5b4`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 3.9 MB (3933852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1b443faafdd6eb68584662f9aa0484863d3df8417e5bcb83deb538bcc5d8a2`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:bbb98875c2e60d55251caf3ec546a6f399d0344b517aff3d9419956ecc5ca8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129973243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af20b8448a5fc255e2ca6ec2e4b21aa035fe206f22cc74cd6b4e5667d18eaf94`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669ae66225b713189254b710db60d969b0da76c3a6fbfb597d3800dd2869e819`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43419d0575fa54de01c352b29709b0d5ccf15c49d3d1bcc25378930552dfbb`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 7.4 MB (7387928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705dcc6c28fd9ac1b53e0c99842c5e89260eaab760fc90e0989d4a5882121d7e`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 355.6 KB (355637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6008ecd238bf91fc60b5f372ddfdaf51cdc8a9afc258c4548be4d79f12ca23f9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 76.3 KB (76344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfff5ef737373de6ea03d251c1b50454071af66acdb81e7b7c7e04dfdf59fc9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970c2190b221a43960164c74df60732029a7aa45d4eccacc86cf8ed02e90a486`  
		Last Modified: Tue, 04 Feb 2025 07:35:44 GMT  
		Size: 95.3 MB (95289278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbca118bd3ee0264e7ab445907d9c994fcbe1ed9648b8eda4ffe96039cb9a0e`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6160c94cff5d390694fc67808062b79858db1a3398572487e90b4dc650545e6`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e20f342f24eeb86e2afa69eadfe2557a8a501105122c12940a5cc51347802ab`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaf3ddd7aa622b677ecfa8bac5af11f43f3f7d9217667acddd3d79c7c6ea220`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:fdc5ff418ce8940a48676ecb4f18464d922e1b3d7497b403ed26212bee936858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e961e74e238ac3326e88c598f3bd0ca37edca382b81867b8408e055b2a6ec8f`

```dockerfile
```

-	Layers:
	-	`sha256:eb4ee4c1d3c17de162d0cbf896506cb6a51b80c7095de98122fc04b08426ba87`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 3.9 MB (3932647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08d8adad896f090fbd3dc0dfc0edeebf4ed61abaacf54431482a74e0343885f`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:35d66c57efa2d6793f4dbecca8669fa1b73848b30e122e0271fd55f94996defc
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
$ docker pull couchdb@sha256:3367d5bccdc6396d4dfceaefb7be51f7b620060687976d4cb9710ca25e74edf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155532459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d8f9304ca9fc9cd9e8cfc0eebe108b76ec0de354123c8ccb5c037d31fd7c8c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d037aa722688de92adccb49fc02c65a62c4c2cd27dcad1aeb2669f2bc91c80`  
		Last Modified: Tue, 04 Feb 2025 04:38:57 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e1d3bf05d75710981db4a96e2b04ef0c4afbbf6e85fd66a75f47fa297c4418`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 7.9 MB (7874966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6ca1ef4e87822fa39ec77697ee19ee6e4c576d95cd6abbc110cb78e304e7fd`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 77.3 MB (77297441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b372823eab782fcf3ece2ce60437b076a83b6c18a91556dffbe12dcda6b77afb`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 414.9 KB (414935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c576d613f05214b663520384e2869fbfc8f022d828d799aba2eec3f39b0938`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 99.3 KB (99256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c158c51f6fa6055b49d8c93af63541e2a089873c92e50b60fcfd0042c460906d`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8b077ccd40cbf7eb1c494f65740d7a239a1c73a17c6fde0c9ce8ce66110c20`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 41.6 MB (41631683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6b94af6e4c08acd7923e4e5a16820d970152112c37a2fad99d74c7699868cc`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:0de0127374b8540c659ab771f5b9745858025812986f54653259e636e896bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dae0896f708bd13ef93048d280814ecc91d146a5ad7bd37adb354883947042d`

```dockerfile
```

-	Layers:
	-	`sha256:a889570ca4ab953857162a24ba10a8455803b9bef0e936f01a53f75796efce8c`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 3.5 MB (3462052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d12304afa1e2544372cf3ebd188cbc02fb0d22a90f98f6add8b5b32f904428`  
		Last Modified: Tue, 04 Feb 2025 04:38:57 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ef7c562863a9fb584cc36263dc82db193a4a5c3956927ae78e18f702c0c5518e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154278229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b719cad0c7b5fdbfdbbac6dcb7a1e2ebde3550a3fe03266cf60522f6be67bab3`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79173b3fddb7da2629dd339e0d53b403ea8827bcbd9b247d684b58d32dff7cbf`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31829078e1f4de67fcedf6a2d2d8ca1872f489122c7b4bcfa3cd33532c8cb239`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 7.7 MB (7654485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3369295dc500f95559ea4509a427d2c0a4ee1c8ad2b7a79ee1dc560350241f77`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 76.6 MB (76582294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e5bbcf4591afaea2d2cdc136dc489080dd97d81c24bd3ccbe400297114b51b`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 371.7 KB (371693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acdad20d9a721bac2eb158329512906baee9555218f01a8e6ff0f9275510c66`  
		Last Modified: Tue, 14 Jan 2025 07:05:13 GMT  
		Size: 99.2 KB (99208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e627f9bf3e789b44c13cb9953004b89c6d68b322ee687562fe9fb76268a2d868`  
		Last Modified: Tue, 14 Jan 2025 07:05:13 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebeb5aa1e3f7f6837e61861bc4d688a7cb0e40daf66afe7b53355998b6c50ed`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 41.5 MB (41527641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10a636108d2adc58e1f2c66283165d3226827a0d533ede0055e897d2464c6ed`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:80be29eb1df008c822ee482e3954caa2ef94c11a5a1950dd74dbbaa0c6ace91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071743ecadfba0fe3591807a89eb13c2932c9c451dc0d4b7924bb78aef478550`

```dockerfile
```

-	Layers:
	-	`sha256:c09558bcbcbf4d95c177b3cde1b9c16427e89ea9acbaf37de09ff936af7f2e77`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 3.5 MB (3460732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1295fd7d68dfa423f317cb0bff79f1b1008e1459b1398163e931f34e6ccd895d`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:c7ef31bf2d0cf9cadfe093f47d3336284a052b7c09043f3baa84a0e3fa393386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149142669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4aeeab96a922d7a1ab78f8460fac69a2a816ca3b6e125fed1cb4a6eed7411b5`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a23a693d0435d9096a59c377a713b723450b592d3b5f06316fef9eeb38f17`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc051593c4a07ef7ad5fd762b44283836710587d01abf2ebeb0a56303ab6172`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 7.4 MB (7387901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f817f6fdb7f13d39c4df0f552ef9ca2bfa6e668a454e1da6ca2517a8efc439d9`  
		Last Modified: Tue, 04 Feb 2025 07:37:09 GMT  
		Size: 73.1 MB (73065167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0494d93c365c028f5059417ba8bf7f9b24d431a31b87fa6377d4e1d180e457af`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 378.0 KB (378017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7ebdc392d75cc71bd7cc7de5e4d9eea830b1b497cc592e1fec293906ad84a9`  
		Last Modified: Tue, 04 Feb 2025 07:37:07 GMT  
		Size: 99.4 KB (99372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4bcabe0e2faf2b52aaaa7bd8b12785b477e128f41870e5861a2fb57f266265`  
		Last Modified: Tue, 04 Feb 2025 07:37:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5594b52dc2ed41f07ca8731f1d3a1508f5f12286f3634272fb8051567df6b2`  
		Last Modified: Tue, 04 Feb 2025 07:37:08 GMT  
		Size: 41.4 MB (41351710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c8d679dc3d3d2968163532ab43de3cb43616f56858284de5bf2568d257228`  
		Last Modified: Tue, 04 Feb 2025 07:37:08 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:147ab9a2677c357e1185b231e231327efff5ee9bd4cb79ccd3cd7fee80e76849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e49dab81e90811dc3c065f49d460570083ed955142335d69205c40bcdf8370`

```dockerfile
```

-	Layers:
	-	`sha256:37f16ce50caae56e4424d9c7450676605d4306866eae78748dc06d4a5f21d5ac`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 3.5 MB (3455473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ef3b0df1d1e6be3ac92374cbf00a63eb24792839bf9e5fbd9a50931ab50a58`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.2`

```console
$ docker pull couchdb@sha256:a385d09cba450e33deea4b2707908902b4048723f83e7df62f46b03040e99038
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.2` - linux; amd64

```console
$ docker pull couchdb@sha256:e10c0f3e6c0c712e6063c116b9ed4d9530145cfa6c71b35973ab1288b718ce1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133224148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97276a50c66650259bff27f299b3879eb6f793a1ee385b854df88544e4bcf228`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620e8614251def9f3e21f2607dfb4ab6d91474b30fad9d43deacc5f0d48696ea`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d684a920aa356be64b82682bbf4c0f88d5abf94113387ecc4d0efb844a4ec2`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 7.9 MB (7874893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da294366959e243d3f089ff92fff1deb6ba777feb846c231be5187f356e33380`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 392.1 KB (392118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37af3863253f7bbaa9b21528b63d28fe9a00d77883df5b0e4b5f156a967e9e3d`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 76.3 KB (76267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346a8b8a4ffd80e156a8e419cc02193938388d350074b49d995fb53bda931cbf`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a024c30518341713bece7869318d94dec6795bd01ca6814983dd75b1f49c12`  
		Last Modified: Tue, 04 Feb 2025 04:39:03 GMT  
		Size: 96.7 MB (96663136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d163bbbd5791d7565e4860ced124ed43feae71b49f9200561f7855ef412aef75`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66582149d6e9c72698b767d96f223b0611f73576a5fa522694b22d9f47b230d`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0194a8b0180787f0b1df3a9dc9ec52591aa6dd41c33cc617f62bf6eab10f6937`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a13f3f3b60358a016fb2ee4601fe0f597688a87dc6ced132fe97e4e5191fc7a`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:5e051c5ecd6b3e5d50b2d30ebf489250d42ded305010a72563cd97ab46a8e8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054bf54b45ac2c98184be05a333ca8ee023c6fe407f51bdd237c2e488d81373b`

```dockerfile
```

-	Layers:
	-	`sha256:0baf39fa3a0bba9f04b4ec18984352fa1c76bfb3eff1875b60d0e66f2c0e1638`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 3.9 MB (3896283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1d84829d9b91d1749d30761f8b9be369dc2afb51fbadfa44edf6ec58c49edb`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:33ad9d3878354339233afe53bb87df412283410b29708a7ca796f9ac07f8b621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132524949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f1bc82926f249cbb136cfcfc223d28a194d2a83571874ab475e0fd4e4bbf1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a53b506eb957ed2ca989730c18ca42f6e0128157e3b16e04b417d5e3f6a46f`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0784cd6960fabd09529a3b70371d1a31ff9aec79c20d3905d9fbc1a2691c796`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 7.7 MB (7654466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79f2c1109f6989057dfe173d7350181a4d2c6c3094af18ca942f929b5893b99`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d118af51ca1a98ff6c7e8640d57cc57f54bf619a7beef5cfe3f06f5d8299b7`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 76.2 KB (76219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f6188d465363a65faca581e7a29deff62119c7229c06b69dee041e921beff`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4080fca21b251df01a293a38872fbe036647cd75dc3dc3d41eeacdcdc9f11e6`  
		Last Modified: Tue, 14 Jan 2025 07:04:13 GMT  
		Size: 96.4 MB (96398891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7570c55d2fc3d036f3606315986bce629111b93b08d0c34f0d640c69858cf107`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93840e26080be7ccca7b1d4b3b6eb7444f77b3ce0c1dc501a7758bd2dddd794`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349e54346d5fb87fe0546b92feeb3c137da315280a58ed267d31248215cee47c`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da7757a845ae5fd2495cc47db1219d3f9fa2fe4ce5b77dc66d72978d710e60`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:81d65dd5d6ce19f884c69e8e6f10a4bdeee710be6407fc88a62f4599fdd5733a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544e391940d4445a1238cc81cff3eb9c691a770fc7915e710bf9f5799eefb829`

```dockerfile
```

-	Layers:
	-	`sha256:2faae1cf4e6c027422c66213a29885c6bea7c0675ebb0d7bc08679fc799cd5b4`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 3.9 MB (3933852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1b443faafdd6eb68584662f9aa0484863d3df8417e5bcb83deb538bcc5d8a2`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2` - linux; s390x

```console
$ docker pull couchdb@sha256:bbb98875c2e60d55251caf3ec546a6f399d0344b517aff3d9419956ecc5ca8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129973243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af20b8448a5fc255e2ca6ec2e4b21aa035fe206f22cc74cd6b4e5667d18eaf94`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669ae66225b713189254b710db60d969b0da76c3a6fbfb597d3800dd2869e819`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43419d0575fa54de01c352b29709b0d5ccf15c49d3d1bcc25378930552dfbb`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 7.4 MB (7387928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705dcc6c28fd9ac1b53e0c99842c5e89260eaab760fc90e0989d4a5882121d7e`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 355.6 KB (355637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6008ecd238bf91fc60b5f372ddfdaf51cdc8a9afc258c4548be4d79f12ca23f9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 76.3 KB (76344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfff5ef737373de6ea03d251c1b50454071af66acdb81e7b7c7e04dfdf59fc9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970c2190b221a43960164c74df60732029a7aa45d4eccacc86cf8ed02e90a486`  
		Last Modified: Tue, 04 Feb 2025 07:35:44 GMT  
		Size: 95.3 MB (95289278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbca118bd3ee0264e7ab445907d9c994fcbe1ed9648b8eda4ffe96039cb9a0e`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6160c94cff5d390694fc67808062b79858db1a3398572487e90b4dc650545e6`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e20f342f24eeb86e2afa69eadfe2557a8a501105122c12940a5cc51347802ab`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaf3ddd7aa622b677ecfa8bac5af11f43f3f7d9217667acddd3d79c7c6ea220`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:fdc5ff418ce8940a48676ecb4f18464d922e1b3d7497b403ed26212bee936858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e961e74e238ac3326e88c598f3bd0ca37edca382b81867b8408e055b2a6ec8f`

```dockerfile
```

-	Layers:
	-	`sha256:eb4ee4c1d3c17de162d0cbf896506cb6a51b80c7095de98122fc04b08426ba87`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 3.9 MB (3932647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08d8adad896f090fbd3dc0dfc0edeebf4ed61abaacf54431482a74e0343885f`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.2-nouveau`

```console
$ docker pull couchdb@sha256:35d66c57efa2d6793f4dbecca8669fa1b73848b30e122e0271fd55f94996defc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.2-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:3367d5bccdc6396d4dfceaefb7be51f7b620060687976d4cb9710ca25e74edf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155532459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d8f9304ca9fc9cd9e8cfc0eebe108b76ec0de354123c8ccb5c037d31fd7c8c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d037aa722688de92adccb49fc02c65a62c4c2cd27dcad1aeb2669f2bc91c80`  
		Last Modified: Tue, 04 Feb 2025 04:38:57 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e1d3bf05d75710981db4a96e2b04ef0c4afbbf6e85fd66a75f47fa297c4418`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 7.9 MB (7874966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6ca1ef4e87822fa39ec77697ee19ee6e4c576d95cd6abbc110cb78e304e7fd`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 77.3 MB (77297441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b372823eab782fcf3ece2ce60437b076a83b6c18a91556dffbe12dcda6b77afb`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 414.9 KB (414935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c576d613f05214b663520384e2869fbfc8f022d828d799aba2eec3f39b0938`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 99.3 KB (99256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c158c51f6fa6055b49d8c93af63541e2a089873c92e50b60fcfd0042c460906d`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8b077ccd40cbf7eb1c494f65740d7a239a1c73a17c6fde0c9ce8ce66110c20`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 41.6 MB (41631683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6b94af6e4c08acd7923e4e5a16820d970152112c37a2fad99d74c7699868cc`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:0de0127374b8540c659ab771f5b9745858025812986f54653259e636e896bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dae0896f708bd13ef93048d280814ecc91d146a5ad7bd37adb354883947042d`

```dockerfile
```

-	Layers:
	-	`sha256:a889570ca4ab953857162a24ba10a8455803b9bef0e936f01a53f75796efce8c`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 3.5 MB (3462052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d12304afa1e2544372cf3ebd188cbc02fb0d22a90f98f6add8b5b32f904428`  
		Last Modified: Tue, 04 Feb 2025 04:38:57 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ef7c562863a9fb584cc36263dc82db193a4a5c3956927ae78e18f702c0c5518e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154278229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b719cad0c7b5fdbfdbbac6dcb7a1e2ebde3550a3fe03266cf60522f6be67bab3`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79173b3fddb7da2629dd339e0d53b403ea8827bcbd9b247d684b58d32dff7cbf`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31829078e1f4de67fcedf6a2d2d8ca1872f489122c7b4bcfa3cd33532c8cb239`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 7.7 MB (7654485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3369295dc500f95559ea4509a427d2c0a4ee1c8ad2b7a79ee1dc560350241f77`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 76.6 MB (76582294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e5bbcf4591afaea2d2cdc136dc489080dd97d81c24bd3ccbe400297114b51b`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 371.7 KB (371693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acdad20d9a721bac2eb158329512906baee9555218f01a8e6ff0f9275510c66`  
		Last Modified: Tue, 14 Jan 2025 07:05:13 GMT  
		Size: 99.2 KB (99208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e627f9bf3e789b44c13cb9953004b89c6d68b322ee687562fe9fb76268a2d868`  
		Last Modified: Tue, 14 Jan 2025 07:05:13 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebeb5aa1e3f7f6837e61861bc4d688a7cb0e40daf66afe7b53355998b6c50ed`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 41.5 MB (41527641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10a636108d2adc58e1f2c66283165d3226827a0d533ede0055e897d2464c6ed`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:80be29eb1df008c822ee482e3954caa2ef94c11a5a1950dd74dbbaa0c6ace91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071743ecadfba0fe3591807a89eb13c2932c9c451dc0d4b7924bb78aef478550`

```dockerfile
```

-	Layers:
	-	`sha256:c09558bcbcbf4d95c177b3cde1b9c16427e89ea9acbaf37de09ff936af7f2e77`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 3.5 MB (3460732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1295fd7d68dfa423f317cb0bff79f1b1008e1459b1398163e931f34e6ccd895d`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:c7ef31bf2d0cf9cadfe093f47d3336284a052b7c09043f3baa84a0e3fa393386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149142669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4aeeab96a922d7a1ab78f8460fac69a2a816ca3b6e125fed1cb4a6eed7411b5`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a23a693d0435d9096a59c377a713b723450b592d3b5f06316fef9eeb38f17`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc051593c4a07ef7ad5fd762b44283836710587d01abf2ebeb0a56303ab6172`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 7.4 MB (7387901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f817f6fdb7f13d39c4df0f552ef9ca2bfa6e668a454e1da6ca2517a8efc439d9`  
		Last Modified: Tue, 04 Feb 2025 07:37:09 GMT  
		Size: 73.1 MB (73065167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0494d93c365c028f5059417ba8bf7f9b24d431a31b87fa6377d4e1d180e457af`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 378.0 KB (378017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7ebdc392d75cc71bd7cc7de5e4d9eea830b1b497cc592e1fec293906ad84a9`  
		Last Modified: Tue, 04 Feb 2025 07:37:07 GMT  
		Size: 99.4 KB (99372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4bcabe0e2faf2b52aaaa7bd8b12785b477e128f41870e5861a2fb57f266265`  
		Last Modified: Tue, 04 Feb 2025 07:37:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5594b52dc2ed41f07ca8731f1d3a1508f5f12286f3634272fb8051567df6b2`  
		Last Modified: Tue, 04 Feb 2025 07:37:08 GMT  
		Size: 41.4 MB (41351710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c8d679dc3d3d2968163532ab43de3cb43616f56858284de5bf2568d257228`  
		Last Modified: Tue, 04 Feb 2025 07:37:08 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:147ab9a2677c357e1185b231e231327efff5ee9bd4cb79ccd3cd7fee80e76849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e49dab81e90811dc3c065f49d460570083ed955142335d69205c40bcdf8370`

```dockerfile
```

-	Layers:
	-	`sha256:37f16ce50caae56e4424d9c7450676605d4306866eae78748dc06d4a5f21d5ac`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 3.5 MB (3455473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ef3b0df1d1e6be3ac92374cbf00a63eb24792839bf9e5fbd9a50931ab50a58`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:a385d09cba450e33deea4b2707908902b4048723f83e7df62f46b03040e99038
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
$ docker pull couchdb@sha256:e10c0f3e6c0c712e6063c116b9ed4d9530145cfa6c71b35973ab1288b718ce1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133224148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97276a50c66650259bff27f299b3879eb6f793a1ee385b854df88544e4bcf228`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620e8614251def9f3e21f2607dfb4ab6d91474b30fad9d43deacc5f0d48696ea`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d684a920aa356be64b82682bbf4c0f88d5abf94113387ecc4d0efb844a4ec2`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 7.9 MB (7874893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da294366959e243d3f089ff92fff1deb6ba777feb846c231be5187f356e33380`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 392.1 KB (392118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37af3863253f7bbaa9b21528b63d28fe9a00d77883df5b0e4b5f156a967e9e3d`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 76.3 KB (76267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346a8b8a4ffd80e156a8e419cc02193938388d350074b49d995fb53bda931cbf`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a024c30518341713bece7869318d94dec6795bd01ca6814983dd75b1f49c12`  
		Last Modified: Tue, 04 Feb 2025 04:39:03 GMT  
		Size: 96.7 MB (96663136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d163bbbd5791d7565e4860ced124ed43feae71b49f9200561f7855ef412aef75`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66582149d6e9c72698b767d96f223b0611f73576a5fa522694b22d9f47b230d`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0194a8b0180787f0b1df3a9dc9ec52591aa6dd41c33cc617f62bf6eab10f6937`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a13f3f3b60358a016fb2ee4601fe0f597688a87dc6ced132fe97e4e5191fc7a`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:5e051c5ecd6b3e5d50b2d30ebf489250d42ded305010a72563cd97ab46a8e8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054bf54b45ac2c98184be05a333ca8ee023c6fe407f51bdd237c2e488d81373b`

```dockerfile
```

-	Layers:
	-	`sha256:0baf39fa3a0bba9f04b4ec18984352fa1c76bfb3eff1875b60d0e66f2c0e1638`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 3.9 MB (3896283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1d84829d9b91d1749d30761f8b9be369dc2afb51fbadfa44edf6ec58c49edb`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:33ad9d3878354339233afe53bb87df412283410b29708a7ca796f9ac07f8b621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132524949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f1bc82926f249cbb136cfcfc223d28a194d2a83571874ab475e0fd4e4bbf1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a53b506eb957ed2ca989730c18ca42f6e0128157e3b16e04b417d5e3f6a46f`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0784cd6960fabd09529a3b70371d1a31ff9aec79c20d3905d9fbc1a2691c796`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 7.7 MB (7654466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79f2c1109f6989057dfe173d7350181a4d2c6c3094af18ca942f929b5893b99`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d118af51ca1a98ff6c7e8640d57cc57f54bf619a7beef5cfe3f06f5d8299b7`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 76.2 KB (76219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f6188d465363a65faca581e7a29deff62119c7229c06b69dee041e921beff`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4080fca21b251df01a293a38872fbe036647cd75dc3dc3d41eeacdcdc9f11e6`  
		Last Modified: Tue, 14 Jan 2025 07:04:13 GMT  
		Size: 96.4 MB (96398891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7570c55d2fc3d036f3606315986bce629111b93b08d0c34f0d640c69858cf107`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93840e26080be7ccca7b1d4b3b6eb7444f77b3ce0c1dc501a7758bd2dddd794`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349e54346d5fb87fe0546b92feeb3c137da315280a58ed267d31248215cee47c`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da7757a845ae5fd2495cc47db1219d3f9fa2fe4ce5b77dc66d72978d710e60`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:81d65dd5d6ce19f884c69e8e6f10a4bdeee710be6407fc88a62f4599fdd5733a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544e391940d4445a1238cc81cff3eb9c691a770fc7915e710bf9f5799eefb829`

```dockerfile
```

-	Layers:
	-	`sha256:2faae1cf4e6c027422c66213a29885c6bea7c0675ebb0d7bc08679fc799cd5b4`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 3.9 MB (3933852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1b443faafdd6eb68584662f9aa0484863d3df8417e5bcb83deb538bcc5d8a2`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:bbb98875c2e60d55251caf3ec546a6f399d0344b517aff3d9419956ecc5ca8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129973243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af20b8448a5fc255e2ca6ec2e4b21aa035fe206f22cc74cd6b4e5667d18eaf94`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669ae66225b713189254b710db60d969b0da76c3a6fbfb597d3800dd2869e819`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43419d0575fa54de01c352b29709b0d5ccf15c49d3d1bcc25378930552dfbb`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 7.4 MB (7387928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705dcc6c28fd9ac1b53e0c99842c5e89260eaab760fc90e0989d4a5882121d7e`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 355.6 KB (355637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6008ecd238bf91fc60b5f372ddfdaf51cdc8a9afc258c4548be4d79f12ca23f9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 76.3 KB (76344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfff5ef737373de6ea03d251c1b50454071af66acdb81e7b7c7e04dfdf59fc9`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970c2190b221a43960164c74df60732029a7aa45d4eccacc86cf8ed02e90a486`  
		Last Modified: Tue, 04 Feb 2025 07:35:44 GMT  
		Size: 95.3 MB (95289278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbca118bd3ee0264e7ab445907d9c994fcbe1ed9648b8eda4ffe96039cb9a0e`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6160c94cff5d390694fc67808062b79858db1a3398572487e90b4dc650545e6`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e20f342f24eeb86e2afa69eadfe2557a8a501105122c12940a5cc51347802ab`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaf3ddd7aa622b677ecfa8bac5af11f43f3f7d9217667acddd3d79c7c6ea220`  
		Last Modified: Tue, 04 Feb 2025 07:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:fdc5ff418ce8940a48676ecb4f18464d922e1b3d7497b403ed26212bee936858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e961e74e238ac3326e88c598f3bd0ca37edca382b81867b8408e055b2a6ec8f`

```dockerfile
```

-	Layers:
	-	`sha256:eb4ee4c1d3c17de162d0cbf896506cb6a51b80c7095de98122fc04b08426ba87`  
		Last Modified: Tue, 04 Feb 2025 07:35:42 GMT  
		Size: 3.9 MB (3932647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08d8adad896f090fbd3dc0dfc0edeebf4ed61abaacf54431482a74e0343885f`  
		Last Modified: Tue, 04 Feb 2025 07:35:41 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json
