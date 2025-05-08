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
-	[`couchdb:3.5.0`](#couchdb350)
-	[`couchdb:3.5.0-nouveau`](#couchdb350-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:1b28dc51a240436da6056e1abe8f20c7d3c3da31d177660604154757417098e5
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
$ docker pull couchdb@sha256:7faf0e7902f40804f1163d3842c5c167a81554c45ea16eebab1789db7c93c25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139818838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3c757ceb5923d408b8124eebb02e65b37da8856a005b4200c30a4273989c8a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe1974f056aad23a64cbbdc03852bf1efafc7eaa4817ee2d7a24366574455ae`  
		Last Modified: Thu, 08 May 2025 17:06:57 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6aa47f14243ca5639fe2147fa59167504a6725e4941fb61bd972b1024531d9`  
		Last Modified: Thu, 08 May 2025 17:06:58 GMT  
		Size: 7.9 MB (7874895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8056ef4d8d40cf0ca156161ff732ca53cc5825d673e10720bded43fc514608c0`  
		Last Modified: Thu, 08 May 2025 17:06:57 GMT  
		Size: 392.1 KB (392135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f973ae9dcc0b553fee469a8b06577ad5d8a0132288ff88f04b021d4e471d5d`  
		Last Modified: Thu, 08 May 2025 17:06:58 GMT  
		Size: 76.3 KB (76265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d671e8f13231ab470c06c84eb87f86d79b14fe895e65fef490baadf5fff32`  
		Last Modified: Thu, 08 May 2025 17:06:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ae3f30105e1b7fe0121c8772acb185ada59719319a9f83dcb52b5c2b191287`  
		Last Modified: Thu, 08 May 2025 17:07:10 GMT  
		Size: 103.2 MB (103242477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932bc8e4f38e3db1d1a0d301f20f034811d9d004e4e192a4a9a738e4ac0fc3ec`  
		Last Modified: Thu, 08 May 2025 17:06:59 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe83f3f27f8053db9fe06b1de54707d16dbaca154ff2542eb5262944db60f06`  
		Last Modified: Thu, 08 May 2025 17:06:59 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8075ffc8d54d78cb8f879b54f93017cd6cfa3aa40967815a04bcd2b217d4ccc5`  
		Last Modified: Thu, 08 May 2025 17:07:01 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b3d9977391b67379ebb07fbcfb945142d7a688cdf8cdd3df14f694861f9f26`  
		Last Modified: Thu, 08 May 2025 17:07:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:1ff371a8f5fd0166ef045d2c7436fc504e44a2500becfb70a7ed1fd74aca3f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480cf8b4695682d7e0040075485be64ecd2c679fde58bb22acd015dff1c919bc`

```dockerfile
```

-	Layers:
	-	`sha256:9ba495f0841ba1c78683893a8d96ed43a644c92f1a4931bed4fb95e4f63ad8d2`  
		Last Modified: Tue, 06 May 2025 17:18:00 GMT  
		Size: 4.0 MB (3977471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e178e62addd76c26e3f436bff538589513a603a18ea290728943c4a05672eec`  
		Last Modified: Tue, 06 May 2025 17:17:59 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2e5d6e31ba5b9b92989e29faa365e2bffb92af2c68d74ece6a2ca43016ba6648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139041917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11de94aa647367ba5fe5a4ea744897e9a6e24f0ab3c0db12740c8cafca9ee4d4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fda7edaf9e5fa4bff22f8647fc45ace1dec9a2413c557a56f3d209571bb03d3`  
		Last Modified: Thu, 08 May 2025 17:20:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f44d3c9be40e352cbd13efebb94c5b86d4cd047a37cb05e1470b3799da491`  
		Last Modified: Thu, 08 May 2025 17:20:52 GMT  
		Size: 7.7 MB (7654565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77c2f410b4ff91dda61e7492f539cf3280b1e296b0f87b974582537e952a860`  
		Last Modified: Thu, 08 May 2025 17:20:32 GMT  
		Size: 348.9 KB (348949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f245645ed55f34a29dc8f3628a26a2df51feae716273e621d28255c5cd0366fc`  
		Last Modified: Thu, 08 May 2025 17:20:34 GMT  
		Size: 76.3 KB (76313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5710c3924976aed640fb8f738d4e47e35ecd4a5fcf0b2511f68afe7d1146528`  
		Last Modified: Thu, 08 May 2025 17:20:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0454c720549b1dcd1cdef601206f434cdd971e17c9a772d65ba3975f97b969`  
		Last Modified: Thu, 08 May 2025 17:20:41 GMT  
		Size: 102.9 MB (102890031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a994b43877b24b8e8eb646784ca98c6cc75ae1c83f06754649a2bd484c7b1831`  
		Last Modified: Thu, 08 May 2025 17:20:35 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c16e2d34057757eb1428efb7c184e238c3794dd98268e3bd294f2f244475f`  
		Last Modified: Thu, 08 May 2025 17:20:36 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc5813c77ab5a6b2305995bddd3c3e4d7a17f36fc53dbf8de965c6d9d85f0a`  
		Last Modified: Thu, 08 May 2025 17:20:37 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc85c73a0cbd10b91c9982c83b79f58e9b9deab4cf54e563375a8a928c2dffa`  
		Last Modified: Thu, 08 May 2025 17:20:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:fe60acaabade72ceee44fb2665c04f57bc8c5b0c47358f52c9b5043925401920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b478e56c588977ce65a82fb0d0c0f20cc1f87c7ea3af87f9bbd3fdaeae84d40c`

```dockerfile
```

-	Layers:
	-	`sha256:89d3e99d85d7bb933bd62e346a0a1620c97bdf09d7c859d291d8a37233ee45df`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 4.0 MB (3977764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:112e82b651057c0dc11627c3143fd48ca8640c788a42c40bdf853c248d46e608`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:23e6b543536c4f919d516d896ddad6febe9e2b79c019c2ed57a80fb63e84f7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136507495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28d1a2f6d3a6ebb844c9b3e00454a69db63e0666205058c975ff3245b112f3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d172d2bfaf767f3cb6dcee5c5b927a5fcb2cbf6fba23e77b7d6d238ee1181070`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166f60a9ad581cf5c3e56f0033e20a007be898003f412505863a8402ec5b56d5`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 7.4 MB (7387956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66cb9d7c369d14b26c71241ff405bf1cf763d2c76b0409042f00e496f8d2435`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 355.6 KB (355632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3fc1101f198fa75489c4894c40c6e5a2634d0aad28cca95fe802b0052f54a4`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 76.4 KB (76357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5102ac0f24ddaa96a8dab9dce6614f7465dddd84d57f0067fbdde372cb70c46`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039462e57e15e2dd4efecdf541ec4fb6143c1ee4cbce599b00fd62687df905ca`  
		Last Modified: Tue, 06 May 2025 17:48:48 GMT  
		Size: 101.8 MB (101797250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2aad07663621ff4d626933ddca7de8011e57180d89b0e433d93ddd7c6548740`  
		Last Modified: Tue, 06 May 2025 17:48:46 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60d749f2931d7ad4dac37189f1cb2075824085ef47d1d727a6bc4695f5c4faa`  
		Last Modified: Tue, 06 May 2025 17:48:46 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6003fd81da531264f065c3ae78d02e6b7443de4561084bda151895b47a9773`  
		Last Modified: Tue, 06 May 2025 17:48:47 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d813ece651fa98d923ee07da19c9d34bcb67a9c30fc55e7e5c24bed96e88f82a`  
		Last Modified: Tue, 06 May 2025 17:48:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:fff7c0dc5628836e642e15a73ebef0f7a5b8a5b74eb3edffedf6a6f87d8a52d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4008340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dff6521380d733c9a781d2fae34659010abbe4ce5bd29d0138647f68d46c9b`

```dockerfile
```

-	Layers:
	-	`sha256:c19a624b1e77b49254ce1f1eb761fedea0fc0c1bdf9055b4344f6ebd52a88a81`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 4.0 MB (3976559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667c87d1160616974874711a6d46f9f867b5a80450d39daef980c0b06af56063`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:baf9a64c1d285d7824eadca2ced5920e99f79d5d1eb2cfd742f7961a60994625
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
$ docker pull couchdb@sha256:0760441508a04c4c9039005042bc8fbb7d4e9c441efe5c054be88d39fcc4af8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156378033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4018243b6579b4ebbc2e674d251bfaef1baa084734761f1a266b9f719cd443`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feab75aebd886c9be0ee7b4ee28339e431a0b497e089561a987558b673ad6797`  
		Last Modified: Tue, 06 May 2025 17:17:31 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852a92f1ebda0c1224152be98b6d9700950524c8a6a9bcd6986fcb00e9ed673d`  
		Last Modified: Tue, 06 May 2025 17:17:32 GMT  
		Size: 7.9 MB (7874878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4461ff2ea16a599621941b4fcee4711521ba84e86d5314a74cd1d375b0d54da4`  
		Last Modified: Tue, 06 May 2025 17:17:34 GMT  
		Size: 77.3 MB (77325051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b0dd7438e7247e12182be2d5b9548c538a9ceb566a2ccbbcaaad1efeb7399`  
		Last Modified: Tue, 06 May 2025 17:17:31 GMT  
		Size: 415.0 KB (414979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f354970eb1ee9dfb1cf1fe1754e7f486629e6854765524e66af1feb9990e5ff`  
		Last Modified: Tue, 06 May 2025 17:17:32 GMT  
		Size: 99.3 KB (99331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31beb4795edca4e38687b771af5cd0e185edc50c9f01f15b7437033faf9358`  
		Last Modified: Tue, 06 May 2025 17:17:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c466b712155d38ccf933748cb87fbda79c3452f6ab7f4a56c7be924115b4b0`  
		Last Modified: Tue, 06 May 2025 17:17:35 GMT  
		Size: 42.4 MB (42434265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72bf32f2e446080d1db9fcb3e5be1d590d01308eb7a93af4ed2955dcf15098b`  
		Last Modified: Tue, 06 May 2025 17:17:34 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7e749f49becf3b999fbf6e4f1a836c3b8477d0a7d906120ee9fc18278df74c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f63f27268a030a521eed2b0958a40303b245ef5df08551b0f85654fc3e3cc27`

```dockerfile
```

-	Layers:
	-	`sha256:f9841b3c7c4b5ba2c2017fb4b6470f955f9181693cdfc9d317a99aa72c60e5ac`  
		Last Modified: Tue, 06 May 2025 17:17:31 GMT  
		Size: 3.5 MB (3468472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66bc4962c889a3aae3880bcd640e64dc8746f8bd434cd016c5f18ab265d066a`  
		Last Modified: Tue, 06 May 2025 17:17:31 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7fdb1df7e89b35ae184e2975f8ed5d5c72acd6e651588d7854923639ea383648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155180531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90792137fb7d00afa09943655aa32c8b56afb2ed23f9ca819aef6c02127e89b0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104637e2eb67ec32ff000f153eebca995c5a32bdca49fe1b16015251fd887842`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc58e96c4d79f04a31e09066efeea0f21f93f87a60cd80b537546b799ebbff9`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 7.7 MB (7654542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f58f87545a1ea3e85e36bc4f13c6528480a4d096cabe6e23b6919d84a3a21fa`  
		Last Modified: Tue, 06 May 2025 17:58:59 GMT  
		Size: 76.7 MB (76653670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886a375283a50138292c4ab34c2a2cd473c86f479a0657d206917439b9293ef4`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 371.7 KB (371732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccf50ebfde2d6eb28578d23558bec7ad3fcf33ed5edbbda390b0c02b37636ab`  
		Last Modified: Tue, 06 May 2025 17:58:56 GMT  
		Size: 99.3 KB (99262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a67aafe8a97aa0a8dd806d49d1da627072a88c7e466a6957064c3b1ac9f579`  
		Last Modified: Tue, 06 May 2025 17:58:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd40dddaef0fcda5c486a0d107b1aeac5eae87d112d92a7f8babc07a9c2bc5b`  
		Last Modified: Tue, 06 May 2025 17:58:59 GMT  
		Size: 42.3 MB (42332820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ead4ac28d2805b9ad7d4bc386937a7df61b55d7493ee5c9fa48d6eab8baa75c`  
		Last Modified: Tue, 06 May 2025 17:58:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc0f7d743c3b12042d2363c435ba9a3136bffb0e8741d2777c0e9501b34fb0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b851a388ca66506c60d98b25da2535df558b509b5464f97e568dcd7055452f`

```dockerfile
```

-	Layers:
	-	`sha256:926a4dc0d56e3c9be08d364b9e30b94d534c9a7d479ce49b32d9a7fac0b85348`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 3.5 MB (3467148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22075a440bd6b34723136a723584525e19f147bda33189d33a6d6199161fb556`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:6894b9d3fdf6f9a5176261f14ca3c651730ec73db9ce0a765a15e7a388d3c6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149988948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def79bef4e97280e0c980f63684e324dcc092b868ebffdca3086d2acd9046879`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a964195047607539333a13346b03ad72f2ad2936f990c34030f96b711db4d8d6`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35944b8be452548cffc3b1e219d96ee2c781cd22bfcf9556e2189bc35b49b2f0`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 7.4 MB (7387884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37c28b87d08942391748734f64343e220c6ce718982c62cadfe473b0e7eadde`  
		Last Modified: Tue, 06 May 2025 17:50:05 GMT  
		Size: 73.1 MB (73076016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1fdb13b6204813e6a2b61535f8a84ab797314b04528ddfbc414041076fb881`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 378.1 KB (378084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63fee4f0f8bf582bdc0669dc2b702f84f1a6f98705c8a64b90b76089c9c0e17`  
		Last Modified: Tue, 06 May 2025 17:50:04 GMT  
		Size: 99.4 KB (99430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212ed74fe9c91ae5451882f5fce49cce5b47e5b6ea72f551f1d1afe3baa15df8`  
		Last Modified: Tue, 06 May 2025 17:50:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d65d8e4597eadb5b291238e3185b9f77f85e1b800168cc2bf13e44ec6c6663`  
		Last Modified: Tue, 06 May 2025 17:50:05 GMT  
		Size: 42.2 MB (42160785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c1cb17e9fbd6a9bb9d287e74d4e34aae2758743989aa26f811b27e477b142`  
		Last Modified: Tue, 06 May 2025 17:50:05 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d9b219d92f16a58e3cb1a7e838a3f1c08b8df07533420880d740fdab7986c446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80ac1a179e7abb201a9085ecfe46c8e1753c07accd3bada6a559bdd2b2b9beb`

```dockerfile
```

-	Layers:
	-	`sha256:9e60d3321d2c177f7279a87c7a52d401cd66706f2abc46b4774c75118fe11837`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 3.5 MB (3461893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5585a3fbd006fe2392f7b475da7f2e476800ea78a189a415cb5e70900d9b61`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:eaccac1af6288e7c81f62ccb093a5ec4a03d7762ea85347fb00a1793571a57f6
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
$ docker pull couchdb@sha256:29bda1ef06e431703b2b2ae415afbd8e39cc0bfd5e618aec2ef4afd9b6e8c708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138996025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577f5a2bf8281f310410466f9ff2dbcabfe1473b4e50a8384be08b36ecf99607`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8bb06f1e12481f1734930caaf5aec605aaa24e1a4a714390080ff8d49a9bae`  
		Last Modified: Thu, 08 May 2025 17:45:57 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c643e44c289be880b7e1077b20be39cc8aa46c96dc275d3c274d9f4285b16e89`  
		Last Modified: Thu, 08 May 2025 17:45:57 GMT  
		Size: 7.9 MB (7874898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139f130bffc490d838a88a0d05accd783a68e9f617fd52025ac774f55bfe8b96`  
		Last Modified: Thu, 08 May 2025 17:45:57 GMT  
		Size: 392.2 KB (392157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482d9e178fbe5fbe5cfad58aa00c10b65769efe8fb24ae45ec9a43b2389fb87b`  
		Last Modified: Thu, 08 May 2025 17:45:57 GMT  
		Size: 76.3 KB (76322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662901ec9a4cb6ba009d3607b9ad113b7bdd517130e2eec9112df2d01a05d6cb`  
		Last Modified: Thu, 08 May 2025 17:45:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e060d223a8335af42564a119d05c7671db6bf1f629900166eac7b8c0e939a`  
		Last Modified: Thu, 08 May 2025 17:46:06 GMT  
		Size: 102.4 MB (102419585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a1370ccd45c896adc8fd7170cfbeb3eeac84209a0219dd34aec6210e1ab02`  
		Last Modified: Thu, 08 May 2025 17:45:58 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1e127bb37e749c471a816e789f4ded13248cb110d7e3f9e4e17c8f7191e9d6`  
		Last Modified: Thu, 08 May 2025 17:45:59 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87be8d54aedb6022da943334261c18e1eed1d602beb1ea3baf8af2a328b975`  
		Last Modified: Thu, 08 May 2025 17:45:59 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133652bc69003427ae7004295dfcdea96aa5a003479ceaa3742c9e0e88528555`  
		Last Modified: Thu, 08 May 2025 17:46:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:42c546356d24d3788c955b5d00eb4bcd393a46bc59e6fd076597281b2fe6b7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e2799689e298289b95db4b12008b49d684dc9a4297f34dd80dbfa169f6da0a`

```dockerfile
```

-	Layers:
	-	`sha256:a3f7e3b29115dda76e014b52b775a8dc0168d756776e2e5f0c6569ab4e764c88`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 4.0 MB (3962194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f550c2045c0da081acd88fb3e06f2f1cfe56c8b3010ee2d89946189a639dff5`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:15729596c86dda15cc99edf750fc425cb57ef4edce5babce54d068a426a45a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138301136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cf79497d5220986281ff560d275803bb04fb7bc51e1cbb7a936f6d973a73c8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2633edfbe42095655e8e06326a2bb09e72f60054163cab4d32ecdf090a957da`  
		Last Modified: Thu, 08 May 2025 17:09:43 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0cf2efaa368539937e0c9e20e80322a37f0973ca6529dc176891bc2b6b4343`  
		Last Modified: Thu, 08 May 2025 17:09:46 GMT  
		Size: 7.7 MB (7654571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb956e71c0e68ceaea25a9a17c3479c71593de51c3e3883402da9bddd458ce9`  
		Last Modified: Thu, 08 May 2025 17:09:44 GMT  
		Size: 348.9 KB (348927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a6383735d775aae8622e383ef33c77472eab8ffce56113ccda5df7ac6cfa1c`  
		Last Modified: Thu, 08 May 2025 17:09:46 GMT  
		Size: 76.3 KB (76324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f979f73832f1924be9ae9da8592cf4f4e6c7eadc7cb4338f2bd8e4ce317e44`  
		Last Modified: Thu, 08 May 2025 18:37:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16239f6235a9d3bcdaf9c38f9927cd1e232df55ee863031a4353daadfea769b9`  
		Last Modified: Thu, 08 May 2025 18:37:54 GMT  
		Size: 102.1 MB (102149270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8220ab79af616850c33eb5221da223f95894f9c6a1ae7da136c296c3d03b510`  
		Last Modified: Thu, 08 May 2025 18:37:39 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6e43f89922d88c83e3806dff1d4bf75ccc80c4a4d308b57a4de073a5a1eca1`  
		Last Modified: Thu, 08 May 2025 18:37:38 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3804f08bee9c27c0fece5ba72adbe467bd4b68926d439c1c516309ffa3e74a2e`  
		Last Modified: Thu, 08 May 2025 18:37:40 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b49f429faf76187d67cc6f28f9db32073e600dab35eb869191557acfa4cde4`  
		Last Modified: Thu, 08 May 2025 18:37:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:df8ec2e03ec5c103efc80684aae3d7a53433bb17f2c2714e448b58288d74630b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fe7f0e4c9ec3c47ecda169839158b3abbe56f06752386e568d2c2c5df04c0e`

```dockerfile
```

-	Layers:
	-	`sha256:92ed9cd6274d1b94036200dcd5171f298f315f6db22e8327bba08ebd9992df49`  
		Last Modified: Tue, 29 Apr 2025 01:50:53 GMT  
		Size: 4.0 MB (3962487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:425cc3db72cabb981f4a91737562f7be0699079a61ccb18f8f8fe8d4369a21ab`  
		Last Modified: Tue, 29 Apr 2025 01:50:53 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:7819b07037fe98ec994ca26a121fbb8c9a601772df54fa0f3af9f7ba85e50a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135766171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220713081441f1810d0218f5900376c97d27ed09c05e86c7476f16287ab5794`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c8a4385111079823034d1e8ed702e9672cd681f79562137fa525d16803eea`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c0f7f5b2751909f18f45844094309abfc54100ace7c37207440666c3dd916`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 7.4 MB (7387937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b6aeef9cd48451c7352e0d027a4ab68782567fd1af8b1aeed4283756407f74`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 355.6 KB (355644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a016c259437b9920b9c085f993abedb656356821d7571071cb17db40433ce23`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf854b3c69326f429e568061da038a651efb11e32516f8571b1eb6c2fa4f676`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63c8fe755b51ffd8fbe51e653149697f4db50ec5f2e547f3cdacddcf23a8cc`  
		Last Modified: Tue, 29 Apr 2025 00:03:42 GMT  
		Size: 101.1 MB (101055957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702504975d7b1931a864c2373bbe22a5a0c200b6689e356d0e589bee6a061932`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c449b40f1681890fb4190af1efe37d7714370d105e051af05596c701a932f57`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094a79dad673e9d7ae35052d26551314238c734e732e0fb16915e7266b6547ad`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1480727e9ec140937813aea1076b6378bf266665e18b0e20314a588367868a3b`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:88af6693555cb508b2d025acdc1cf32ed693329c7425a63e3ca33fcae9d6527d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cd21e53513802102079ed3d78030c64a5a73292fb437f3f01cd3c37abebb08`

```dockerfile
```

-	Layers:
	-	`sha256:899e8cbc1e36d790e687a9f1f9b1b0d69e11609f8e383484c7a552377bdc224b`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 4.0 MB (3961282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5195173997f32afdbc21e62b738eca6b36722bdcbe2527bfd1b80cc09e348e`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:21ade5564867292f2d134e3ac5d61c3a530fafe26df5409f4b184e47959923b0
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
$ docker pull couchdb@sha256:77ffe59ff29af9d3c5219482f72482fbcb2a0ff2483c083e2d49fb115673bb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156349834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a27220813b744db3146ca8ced46f5cabde9a8fb7793a6c920793d220354a0f6`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a837b37dbc4aaf872f53093cddc1be6d7ef890b0711392143a9af72cef98aa9`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75c714820d9f6c5cbd4bf86389324df57d7541f49cf758a529ba5491022d8f`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 7.9 MB (7874927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe12777043dbe4709756fe502296dc6f6c3bbd613e3ef916bf1734214b192ba7`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 77.3 MB (77297600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78ba57999ae720b3c4071011a08e9999098f55ed42ff9b6ed3f3803132698e6`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 415.0 KB (414976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29364f5cdb32bc05cdd929c02986311ed94c76e959a4e263ba9cf30cd49229ce`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 99.3 KB (99309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bc17ee849dc1a4faaa61126db10e65016ed2a4c2710bd1d2ad98c07f3660bf`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9cc3233d493f6ccb82dbb845f9bf89aedb7a809588f957dff97a8a417b20bd`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 42.4 MB (42433507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fa03def47bdb76fe273a3779236c9b64f6cbba548c826afab19c88bef4e4d`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a6081534b52d88c51815ba521ecff693dea686881b9966a95ee75abfab2e5fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ce8df7d14f7982fb816dce683b26a15fde337ce687af08ea53c0ade53063f9`

```dockerfile
```

-	Layers:
	-	`sha256:a76c0ac78c05527f8220cc9ae241667389856abc3b537b0574c27f99d4400106`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 3.5 MB (3468472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a08d555edab0c60d4bcb148bd4978664d1b20f9aae43f6e9a2097f7d4c7bdf4`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0fc5bf7f8656c738548765f26d845e06e1f397e2ba7769a12f072ed480ea2192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155151224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5839b1b3d1b63e9c6218041f808c4f01c7d9c791f10d4af997c8168ace78fd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac2fb37a32e5d32440fe31bf070b4f898cd1be575a07c97cb79545c9b0185ba`  
		Last Modified: Tue, 29 Apr 2025 01:51:45 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01d9b43b431ef17b69173455b60689597c4625f6f6c4f7eb221a030ab004321`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 7.7 MB (7654523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3825b273ce4e5eb6867f90ff56927c439343cdddf5b9851536108096d71a168f`  
		Last Modified: Tue, 29 Apr 2025 01:51:48 GMT  
		Size: 76.6 MB (76624178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6a8d76ed8c03ee5297cc4c2d41c92edfb6fa1335a48b18b7dd5b4bd3c123b`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 371.7 KB (371743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19359905d9ad3145a133462b7a4bb5f7b0ec3e6fdba00b937fd82721789cf935`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 99.3 KB (99267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e15435482689c2ae429169c378e85e1689ad1fcbf407d2afc7d57623eed71a`  
		Last Modified: Tue, 29 Apr 2025 01:51:47 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad50cd5577f3297510ebe03234b653c4bda90d45cc8ca400513aca09e0446e0`  
		Last Modified: Tue, 29 Apr 2025 01:51:48 GMT  
		Size: 42.3 MB (42333012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a49280d94a95e153d3e016076b7e5188cfdc8ab11ad546a46ab8a4c31f8340`  
		Last Modified: Tue, 29 Apr 2025 01:51:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:02e17f86ce17541e3ff54b18c1e75db26776c37e7a0f04eb985686e8706efd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb40c217bb4ab0e4de428c0aba3fc79410576e35dcd21a2d1e4f0df951d7348`

```dockerfile
```

-	Layers:
	-	`sha256:e1a0a1588545666af4b5a0101d887a0dae635f9389deab9ea94282c17c799abd`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 3.5 MB (3467148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f6b2e21e354c6da21bec28182224c1de6a2a046a3b09e39131690d219a25642`  
		Last Modified: Tue, 29 Apr 2025 01:51:45 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:567f3e53824961c5f506118d23c53e6c44333ede5da72ca9fc0453ee8df3559f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149977892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d2af33615aa36bcba2719f0280f43028b632981cf48362c439c8774e5a7e08`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeb9febea926497c6b73a956a66c5ec7705a80ed96a88acd22e023a12bb07b9`  
		Last Modified: Tue, 29 Apr 2025 00:04:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb3720e0f56a097c25a4a4a982b82bafb5b5cd40ac87ffefca40556227f213f`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 7.4 MB (7387952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce679ce7dd142ab1209f6b1e198804851164e290d7c9412f489110386d84a3c4`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 73.1 MB (73065225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ea5e69fb0ac2e8ec68ad79d4ed32a98475e57dec15e01433a7aac1c8d2bcff`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 378.1 KB (378103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8084ad1ebf84dff15753e78e53bdc8cfdccdcb39266f1bf8e231f251d78a64e3`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 99.4 KB (99449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a49819b32ddd9c0fe27e1ed0f760870d4d9170232838540cc48f818ef2606e`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cd8bce374995c6a118e0965c0b2ebf3fa93ae834354a829cc1b3cd0f830219`  
		Last Modified: Tue, 29 Apr 2025 00:04:49 GMT  
		Size: 42.2 MB (42160416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55bbc492280b5c45b056b641e8fec35f5fb54bc50068de783a4c110b4beb376`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:77c04fe246e4b659963c87d866f2678b43426ef3984aac6cc092e602b0dc0ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f22a5e7194519b1d9eff220c23222179736285e22078c6328ae14eda1ca0b0`

```dockerfile
```

-	Layers:
	-	`sha256:e581491861b03880116342ed4b02be1373f61f3ac37d5e781506fac9e30a02d5`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 3.5 MB (3461893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e144eeff7b03258ac15dcb32b9ea1e2ff7892643f844b7df4a7b15118c6c87e3`  
		Last Modified: Tue, 29 Apr 2025 00:04:46 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:eaccac1af6288e7c81f62ccb093a5ec4a03d7762ea85347fb00a1793571a57f6
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
$ docker pull couchdb@sha256:29bda1ef06e431703b2b2ae415afbd8e39cc0bfd5e618aec2ef4afd9b6e8c708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138996025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577f5a2bf8281f310410466f9ff2dbcabfe1473b4e50a8384be08b36ecf99607`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8bb06f1e12481f1734930caaf5aec605aaa24e1a4a714390080ff8d49a9bae`  
		Last Modified: Thu, 08 May 2025 17:45:57 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c643e44c289be880b7e1077b20be39cc8aa46c96dc275d3c274d9f4285b16e89`  
		Last Modified: Thu, 08 May 2025 17:45:57 GMT  
		Size: 7.9 MB (7874898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139f130bffc490d838a88a0d05accd783a68e9f617fd52025ac774f55bfe8b96`  
		Last Modified: Thu, 08 May 2025 17:45:57 GMT  
		Size: 392.2 KB (392157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482d9e178fbe5fbe5cfad58aa00c10b65769efe8fb24ae45ec9a43b2389fb87b`  
		Last Modified: Thu, 08 May 2025 17:45:57 GMT  
		Size: 76.3 KB (76322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662901ec9a4cb6ba009d3607b9ad113b7bdd517130e2eec9112df2d01a05d6cb`  
		Last Modified: Thu, 08 May 2025 17:45:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e060d223a8335af42564a119d05c7671db6bf1f629900166eac7b8c0e939a`  
		Last Modified: Thu, 08 May 2025 17:46:06 GMT  
		Size: 102.4 MB (102419585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a1370ccd45c896adc8fd7170cfbeb3eeac84209a0219dd34aec6210e1ab02`  
		Last Modified: Thu, 08 May 2025 17:45:58 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1e127bb37e749c471a816e789f4ded13248cb110d7e3f9e4e17c8f7191e9d6`  
		Last Modified: Thu, 08 May 2025 17:45:59 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87be8d54aedb6022da943334261c18e1eed1d602beb1ea3baf8af2a328b975`  
		Last Modified: Thu, 08 May 2025 17:45:59 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133652bc69003427ae7004295dfcdea96aa5a003479ceaa3742c9e0e88528555`  
		Last Modified: Thu, 08 May 2025 17:46:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:42c546356d24d3788c955b5d00eb4bcd393a46bc59e6fd076597281b2fe6b7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e2799689e298289b95db4b12008b49d684dc9a4297f34dd80dbfa169f6da0a`

```dockerfile
```

-	Layers:
	-	`sha256:a3f7e3b29115dda76e014b52b775a8dc0168d756776e2e5f0c6569ab4e764c88`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 4.0 MB (3962194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f550c2045c0da081acd88fb3e06f2f1cfe56c8b3010ee2d89946189a639dff5`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:15729596c86dda15cc99edf750fc425cb57ef4edce5babce54d068a426a45a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138301136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cf79497d5220986281ff560d275803bb04fb7bc51e1cbb7a936f6d973a73c8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2633edfbe42095655e8e06326a2bb09e72f60054163cab4d32ecdf090a957da`  
		Last Modified: Thu, 08 May 2025 17:09:43 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0cf2efaa368539937e0c9e20e80322a37f0973ca6529dc176891bc2b6b4343`  
		Last Modified: Thu, 08 May 2025 17:09:46 GMT  
		Size: 7.7 MB (7654571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb956e71c0e68ceaea25a9a17c3479c71593de51c3e3883402da9bddd458ce9`  
		Last Modified: Thu, 08 May 2025 17:09:44 GMT  
		Size: 348.9 KB (348927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a6383735d775aae8622e383ef33c77472eab8ffce56113ccda5df7ac6cfa1c`  
		Last Modified: Thu, 08 May 2025 17:09:46 GMT  
		Size: 76.3 KB (76324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f979f73832f1924be9ae9da8592cf4f4e6c7eadc7cb4338f2bd8e4ce317e44`  
		Last Modified: Thu, 08 May 2025 18:37:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16239f6235a9d3bcdaf9c38f9927cd1e232df55ee863031a4353daadfea769b9`  
		Last Modified: Thu, 08 May 2025 18:37:54 GMT  
		Size: 102.1 MB (102149270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8220ab79af616850c33eb5221da223f95894f9c6a1ae7da136c296c3d03b510`  
		Last Modified: Thu, 08 May 2025 18:37:39 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6e43f89922d88c83e3806dff1d4bf75ccc80c4a4d308b57a4de073a5a1eca1`  
		Last Modified: Thu, 08 May 2025 18:37:38 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3804f08bee9c27c0fece5ba72adbe467bd4b68926d439c1c516309ffa3e74a2e`  
		Last Modified: Thu, 08 May 2025 18:37:40 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b49f429faf76187d67cc6f28f9db32073e600dab35eb869191557acfa4cde4`  
		Last Modified: Thu, 08 May 2025 18:37:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:df8ec2e03ec5c103efc80684aae3d7a53433bb17f2c2714e448b58288d74630b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fe7f0e4c9ec3c47ecda169839158b3abbe56f06752386e568d2c2c5df04c0e`

```dockerfile
```

-	Layers:
	-	`sha256:92ed9cd6274d1b94036200dcd5171f298f315f6db22e8327bba08ebd9992df49`  
		Last Modified: Tue, 29 Apr 2025 01:50:53 GMT  
		Size: 4.0 MB (3962487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:425cc3db72cabb981f4a91737562f7be0699079a61ccb18f8f8fe8d4369a21ab`  
		Last Modified: Tue, 29 Apr 2025 01:50:53 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:7819b07037fe98ec994ca26a121fbb8c9a601772df54fa0f3af9f7ba85e50a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135766171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220713081441f1810d0218f5900376c97d27ed09c05e86c7476f16287ab5794`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c8a4385111079823034d1e8ed702e9672cd681f79562137fa525d16803eea`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c0f7f5b2751909f18f45844094309abfc54100ace7c37207440666c3dd916`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 7.4 MB (7387937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b6aeef9cd48451c7352e0d027a4ab68782567fd1af8b1aeed4283756407f74`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 355.6 KB (355644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a016c259437b9920b9c085f993abedb656356821d7571071cb17db40433ce23`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf854b3c69326f429e568061da038a651efb11e32516f8571b1eb6c2fa4f676`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63c8fe755b51ffd8fbe51e653149697f4db50ec5f2e547f3cdacddcf23a8cc`  
		Last Modified: Tue, 29 Apr 2025 00:03:42 GMT  
		Size: 101.1 MB (101055957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702504975d7b1931a864c2373bbe22a5a0c200b6689e356d0e589bee6a061932`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c449b40f1681890fb4190af1efe37d7714370d105e051af05596c701a932f57`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094a79dad673e9d7ae35052d26551314238c734e732e0fb16915e7266b6547ad`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1480727e9ec140937813aea1076b6378bf266665e18b0e20314a588367868a3b`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:88af6693555cb508b2d025acdc1cf32ed693329c7425a63e3ca33fcae9d6527d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cd21e53513802102079ed3d78030c64a5a73292fb437f3f01cd3c37abebb08`

```dockerfile
```

-	Layers:
	-	`sha256:899e8cbc1e36d790e687a9f1f9b1b0d69e11609f8e383484c7a552377bdc224b`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 4.0 MB (3961282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5195173997f32afdbc21e62b738eca6b36722bdcbe2527bfd1b80cc09e348e`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:21ade5564867292f2d134e3ac5d61c3a530fafe26df5409f4b184e47959923b0
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
$ docker pull couchdb@sha256:77ffe59ff29af9d3c5219482f72482fbcb2a0ff2483c083e2d49fb115673bb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156349834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a27220813b744db3146ca8ced46f5cabde9a8fb7793a6c920793d220354a0f6`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a837b37dbc4aaf872f53093cddc1be6d7ef890b0711392143a9af72cef98aa9`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75c714820d9f6c5cbd4bf86389324df57d7541f49cf758a529ba5491022d8f`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 7.9 MB (7874927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe12777043dbe4709756fe502296dc6f6c3bbd613e3ef916bf1734214b192ba7`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 77.3 MB (77297600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78ba57999ae720b3c4071011a08e9999098f55ed42ff9b6ed3f3803132698e6`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 415.0 KB (414976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29364f5cdb32bc05cdd929c02986311ed94c76e959a4e263ba9cf30cd49229ce`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 99.3 KB (99309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bc17ee849dc1a4faaa61126db10e65016ed2a4c2710bd1d2ad98c07f3660bf`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9cc3233d493f6ccb82dbb845f9bf89aedb7a809588f957dff97a8a417b20bd`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 42.4 MB (42433507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fa03def47bdb76fe273a3779236c9b64f6cbba548c826afab19c88bef4e4d`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a6081534b52d88c51815ba521ecff693dea686881b9966a95ee75abfab2e5fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ce8df7d14f7982fb816dce683b26a15fde337ce687af08ea53c0ade53063f9`

```dockerfile
```

-	Layers:
	-	`sha256:a76c0ac78c05527f8220cc9ae241667389856abc3b537b0574c27f99d4400106`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 3.5 MB (3468472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a08d555edab0c60d4bcb148bd4978664d1b20f9aae43f6e9a2097f7d4c7bdf4`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0fc5bf7f8656c738548765f26d845e06e1f397e2ba7769a12f072ed480ea2192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155151224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5839b1b3d1b63e9c6218041f808c4f01c7d9c791f10d4af997c8168ace78fd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac2fb37a32e5d32440fe31bf070b4f898cd1be575a07c97cb79545c9b0185ba`  
		Last Modified: Tue, 29 Apr 2025 01:51:45 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01d9b43b431ef17b69173455b60689597c4625f6f6c4f7eb221a030ab004321`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 7.7 MB (7654523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3825b273ce4e5eb6867f90ff56927c439343cdddf5b9851536108096d71a168f`  
		Last Modified: Tue, 29 Apr 2025 01:51:48 GMT  
		Size: 76.6 MB (76624178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6a8d76ed8c03ee5297cc4c2d41c92edfb6fa1335a48b18b7dd5b4bd3c123b`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 371.7 KB (371743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19359905d9ad3145a133462b7a4bb5f7b0ec3e6fdba00b937fd82721789cf935`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 99.3 KB (99267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e15435482689c2ae429169c378e85e1689ad1fcbf407d2afc7d57623eed71a`  
		Last Modified: Tue, 29 Apr 2025 01:51:47 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad50cd5577f3297510ebe03234b653c4bda90d45cc8ca400513aca09e0446e0`  
		Last Modified: Tue, 29 Apr 2025 01:51:48 GMT  
		Size: 42.3 MB (42333012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a49280d94a95e153d3e016076b7e5188cfdc8ab11ad546a46ab8a4c31f8340`  
		Last Modified: Tue, 29 Apr 2025 01:51:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:02e17f86ce17541e3ff54b18c1e75db26776c37e7a0f04eb985686e8706efd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb40c217bb4ab0e4de428c0aba3fc79410576e35dcd21a2d1e4f0df951d7348`

```dockerfile
```

-	Layers:
	-	`sha256:e1a0a1588545666af4b5a0101d887a0dae635f9389deab9ea94282c17c799abd`  
		Last Modified: Tue, 29 Apr 2025 01:51:46 GMT  
		Size: 3.5 MB (3467148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f6b2e21e354c6da21bec28182224c1de6a2a046a3b09e39131690d219a25642`  
		Last Modified: Tue, 29 Apr 2025 01:51:45 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:567f3e53824961c5f506118d23c53e6c44333ede5da72ca9fc0453ee8df3559f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149977892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d2af33615aa36bcba2719f0280f43028b632981cf48362c439c8774e5a7e08`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeb9febea926497c6b73a956a66c5ec7705a80ed96a88acd22e023a12bb07b9`  
		Last Modified: Tue, 29 Apr 2025 00:04:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb3720e0f56a097c25a4a4a982b82bafb5b5cd40ac87ffefca40556227f213f`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 7.4 MB (7387952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce679ce7dd142ab1209f6b1e198804851164e290d7c9412f489110386d84a3c4`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 73.1 MB (73065225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ea5e69fb0ac2e8ec68ad79d4ed32a98475e57dec15e01433a7aac1c8d2bcff`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 378.1 KB (378103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8084ad1ebf84dff15753e78e53bdc8cfdccdcb39266f1bf8e231f251d78a64e3`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 99.4 KB (99449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a49819b32ddd9c0fe27e1ed0f760870d4d9170232838540cc48f818ef2606e`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cd8bce374995c6a118e0965c0b2ebf3fa93ae834354a829cc1b3cd0f830219`  
		Last Modified: Tue, 29 Apr 2025 00:04:49 GMT  
		Size: 42.2 MB (42160416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55bbc492280b5c45b056b641e8fec35f5fb54bc50068de783a4c110b4beb376`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:77c04fe246e4b659963c87d866f2678b43426ef3984aac6cc092e602b0dc0ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f22a5e7194519b1d9eff220c23222179736285e22078c6328ae14eda1ca0b0`

```dockerfile
```

-	Layers:
	-	`sha256:e581491861b03880116342ed4b02be1373f61f3ac37d5e781506fac9e30a02d5`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 3.5 MB (3461893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e144eeff7b03258ac15dcb32b9ea1e2ff7892643f844b7df4a7b15118c6c87e3`  
		Last Modified: Tue, 29 Apr 2025 00:04:46 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:1b28dc51a240436da6056e1abe8f20c7d3c3da31d177660604154757417098e5
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
$ docker pull couchdb@sha256:7faf0e7902f40804f1163d3842c5c167a81554c45ea16eebab1789db7c93c25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139818838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3c757ceb5923d408b8124eebb02e65b37da8856a005b4200c30a4273989c8a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe1974f056aad23a64cbbdc03852bf1efafc7eaa4817ee2d7a24366574455ae`  
		Last Modified: Thu, 08 May 2025 17:06:57 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6aa47f14243ca5639fe2147fa59167504a6725e4941fb61bd972b1024531d9`  
		Last Modified: Thu, 08 May 2025 17:06:58 GMT  
		Size: 7.9 MB (7874895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8056ef4d8d40cf0ca156161ff732ca53cc5825d673e10720bded43fc514608c0`  
		Last Modified: Thu, 08 May 2025 17:06:57 GMT  
		Size: 392.1 KB (392135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f973ae9dcc0b553fee469a8b06577ad5d8a0132288ff88f04b021d4e471d5d`  
		Last Modified: Thu, 08 May 2025 17:06:58 GMT  
		Size: 76.3 KB (76265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d671e8f13231ab470c06c84eb87f86d79b14fe895e65fef490baadf5fff32`  
		Last Modified: Thu, 08 May 2025 17:06:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ae3f30105e1b7fe0121c8772acb185ada59719319a9f83dcb52b5c2b191287`  
		Last Modified: Thu, 08 May 2025 17:07:10 GMT  
		Size: 103.2 MB (103242477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932bc8e4f38e3db1d1a0d301f20f034811d9d004e4e192a4a9a738e4ac0fc3ec`  
		Last Modified: Thu, 08 May 2025 17:06:59 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe83f3f27f8053db9fe06b1de54707d16dbaca154ff2542eb5262944db60f06`  
		Last Modified: Thu, 08 May 2025 17:06:59 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8075ffc8d54d78cb8f879b54f93017cd6cfa3aa40967815a04bcd2b217d4ccc5`  
		Last Modified: Thu, 08 May 2025 17:07:01 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b3d9977391b67379ebb07fbcfb945142d7a688cdf8cdd3df14f694861f9f26`  
		Last Modified: Thu, 08 May 2025 17:07:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:1ff371a8f5fd0166ef045d2c7436fc504e44a2500becfb70a7ed1fd74aca3f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480cf8b4695682d7e0040075485be64ecd2c679fde58bb22acd015dff1c919bc`

```dockerfile
```

-	Layers:
	-	`sha256:9ba495f0841ba1c78683893a8d96ed43a644c92f1a4931bed4fb95e4f63ad8d2`  
		Last Modified: Tue, 06 May 2025 17:18:00 GMT  
		Size: 4.0 MB (3977471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e178e62addd76c26e3f436bff538589513a603a18ea290728943c4a05672eec`  
		Last Modified: Tue, 06 May 2025 17:17:59 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2e5d6e31ba5b9b92989e29faa365e2bffb92af2c68d74ece6a2ca43016ba6648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139041917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11de94aa647367ba5fe5a4ea744897e9a6e24f0ab3c0db12740c8cafca9ee4d4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fda7edaf9e5fa4bff22f8647fc45ace1dec9a2413c557a56f3d209571bb03d3`  
		Last Modified: Thu, 08 May 2025 17:20:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f44d3c9be40e352cbd13efebb94c5b86d4cd047a37cb05e1470b3799da491`  
		Last Modified: Thu, 08 May 2025 17:20:52 GMT  
		Size: 7.7 MB (7654565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77c2f410b4ff91dda61e7492f539cf3280b1e296b0f87b974582537e952a860`  
		Last Modified: Thu, 08 May 2025 17:20:32 GMT  
		Size: 348.9 KB (348949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f245645ed55f34a29dc8f3628a26a2df51feae716273e621d28255c5cd0366fc`  
		Last Modified: Thu, 08 May 2025 17:20:34 GMT  
		Size: 76.3 KB (76313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5710c3924976aed640fb8f738d4e47e35ecd4a5fcf0b2511f68afe7d1146528`  
		Last Modified: Thu, 08 May 2025 17:20:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0454c720549b1dcd1cdef601206f434cdd971e17c9a772d65ba3975f97b969`  
		Last Modified: Thu, 08 May 2025 17:20:41 GMT  
		Size: 102.9 MB (102890031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a994b43877b24b8e8eb646784ca98c6cc75ae1c83f06754649a2bd484c7b1831`  
		Last Modified: Thu, 08 May 2025 17:20:35 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c16e2d34057757eb1428efb7c184e238c3794dd98268e3bd294f2f244475f`  
		Last Modified: Thu, 08 May 2025 17:20:36 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc5813c77ab5a6b2305995bddd3c3e4d7a17f36fc53dbf8de965c6d9d85f0a`  
		Last Modified: Thu, 08 May 2025 17:20:37 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc85c73a0cbd10b91c9982c83b79f58e9b9deab4cf54e563375a8a928c2dffa`  
		Last Modified: Thu, 08 May 2025 17:20:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:fe60acaabade72ceee44fb2665c04f57bc8c5b0c47358f52c9b5043925401920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b478e56c588977ce65a82fb0d0c0f20cc1f87c7ea3af87f9bbd3fdaeae84d40c`

```dockerfile
```

-	Layers:
	-	`sha256:89d3e99d85d7bb933bd62e346a0a1620c97bdf09d7c859d291d8a37233ee45df`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 4.0 MB (3977764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:112e82b651057c0dc11627c3143fd48ca8640c788a42c40bdf853c248d46e608`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:23e6b543536c4f919d516d896ddad6febe9e2b79c019c2ed57a80fb63e84f7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136507495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28d1a2f6d3a6ebb844c9b3e00454a69db63e0666205058c975ff3245b112f3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d172d2bfaf767f3cb6dcee5c5b927a5fcb2cbf6fba23e77b7d6d238ee1181070`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166f60a9ad581cf5c3e56f0033e20a007be898003f412505863a8402ec5b56d5`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 7.4 MB (7387956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66cb9d7c369d14b26c71241ff405bf1cf763d2c76b0409042f00e496f8d2435`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 355.6 KB (355632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3fc1101f198fa75489c4894c40c6e5a2634d0aad28cca95fe802b0052f54a4`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 76.4 KB (76357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5102ac0f24ddaa96a8dab9dce6614f7465dddd84d57f0067fbdde372cb70c46`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039462e57e15e2dd4efecdf541ec4fb6143c1ee4cbce599b00fd62687df905ca`  
		Last Modified: Tue, 06 May 2025 17:48:48 GMT  
		Size: 101.8 MB (101797250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2aad07663621ff4d626933ddca7de8011e57180d89b0e433d93ddd7c6548740`  
		Last Modified: Tue, 06 May 2025 17:48:46 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60d749f2931d7ad4dac37189f1cb2075824085ef47d1d727a6bc4695f5c4faa`  
		Last Modified: Tue, 06 May 2025 17:48:46 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6003fd81da531264f065c3ae78d02e6b7443de4561084bda151895b47a9773`  
		Last Modified: Tue, 06 May 2025 17:48:47 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d813ece651fa98d923ee07da19c9d34bcb67a9c30fc55e7e5c24bed96e88f82a`  
		Last Modified: Tue, 06 May 2025 17:48:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:fff7c0dc5628836e642e15a73ebef0f7a5b8a5b74eb3edffedf6a6f87d8a52d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4008340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dff6521380d733c9a781d2fae34659010abbe4ce5bd29d0138647f68d46c9b`

```dockerfile
```

-	Layers:
	-	`sha256:c19a624b1e77b49254ce1f1eb761fedea0fc0c1bdf9055b4344f6ebd52a88a81`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 4.0 MB (3976559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667c87d1160616974874711a6d46f9f867b5a80450d39daef980c0b06af56063`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:baf9a64c1d285d7824eadca2ced5920e99f79d5d1eb2cfd742f7961a60994625
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
$ docker pull couchdb@sha256:0760441508a04c4c9039005042bc8fbb7d4e9c441efe5c054be88d39fcc4af8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156378033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4018243b6579b4ebbc2e674d251bfaef1baa084734761f1a266b9f719cd443`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feab75aebd886c9be0ee7b4ee28339e431a0b497e089561a987558b673ad6797`  
		Last Modified: Tue, 06 May 2025 17:17:31 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852a92f1ebda0c1224152be98b6d9700950524c8a6a9bcd6986fcb00e9ed673d`  
		Last Modified: Tue, 06 May 2025 17:17:32 GMT  
		Size: 7.9 MB (7874878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4461ff2ea16a599621941b4fcee4711521ba84e86d5314a74cd1d375b0d54da4`  
		Last Modified: Tue, 06 May 2025 17:17:34 GMT  
		Size: 77.3 MB (77325051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b0dd7438e7247e12182be2d5b9548c538a9ceb566a2ccbbcaaad1efeb7399`  
		Last Modified: Tue, 06 May 2025 17:17:31 GMT  
		Size: 415.0 KB (414979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f354970eb1ee9dfb1cf1fe1754e7f486629e6854765524e66af1feb9990e5ff`  
		Last Modified: Tue, 06 May 2025 17:17:32 GMT  
		Size: 99.3 KB (99331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31beb4795edca4e38687b771af5cd0e185edc50c9f01f15b7437033faf9358`  
		Last Modified: Tue, 06 May 2025 17:17:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c466b712155d38ccf933748cb87fbda79c3452f6ab7f4a56c7be924115b4b0`  
		Last Modified: Tue, 06 May 2025 17:17:35 GMT  
		Size: 42.4 MB (42434265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72bf32f2e446080d1db9fcb3e5be1d590d01308eb7a93af4ed2955dcf15098b`  
		Last Modified: Tue, 06 May 2025 17:17:34 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7e749f49becf3b999fbf6e4f1a836c3b8477d0a7d906120ee9fc18278df74c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f63f27268a030a521eed2b0958a40303b245ef5df08551b0f85654fc3e3cc27`

```dockerfile
```

-	Layers:
	-	`sha256:f9841b3c7c4b5ba2c2017fb4b6470f955f9181693cdfc9d317a99aa72c60e5ac`  
		Last Modified: Tue, 06 May 2025 17:17:31 GMT  
		Size: 3.5 MB (3468472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66bc4962c889a3aae3880bcd640e64dc8746f8bd434cd016c5f18ab265d066a`  
		Last Modified: Tue, 06 May 2025 17:17:31 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7fdb1df7e89b35ae184e2975f8ed5d5c72acd6e651588d7854923639ea383648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155180531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90792137fb7d00afa09943655aa32c8b56afb2ed23f9ca819aef6c02127e89b0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104637e2eb67ec32ff000f153eebca995c5a32bdca49fe1b16015251fd887842`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc58e96c4d79f04a31e09066efeea0f21f93f87a60cd80b537546b799ebbff9`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 7.7 MB (7654542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f58f87545a1ea3e85e36bc4f13c6528480a4d096cabe6e23b6919d84a3a21fa`  
		Last Modified: Tue, 06 May 2025 17:58:59 GMT  
		Size: 76.7 MB (76653670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886a375283a50138292c4ab34c2a2cd473c86f479a0657d206917439b9293ef4`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 371.7 KB (371732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccf50ebfde2d6eb28578d23558bec7ad3fcf33ed5edbbda390b0c02b37636ab`  
		Last Modified: Tue, 06 May 2025 17:58:56 GMT  
		Size: 99.3 KB (99262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a67aafe8a97aa0a8dd806d49d1da627072a88c7e466a6957064c3b1ac9f579`  
		Last Modified: Tue, 06 May 2025 17:58:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd40dddaef0fcda5c486a0d107b1aeac5eae87d112d92a7f8babc07a9c2bc5b`  
		Last Modified: Tue, 06 May 2025 17:58:59 GMT  
		Size: 42.3 MB (42332820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ead4ac28d2805b9ad7d4bc386937a7df61b55d7493ee5c9fa48d6eab8baa75c`  
		Last Modified: Tue, 06 May 2025 17:58:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc0f7d743c3b12042d2363c435ba9a3136bffb0e8741d2777c0e9501b34fb0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b851a388ca66506c60d98b25da2535df558b509b5464f97e568dcd7055452f`

```dockerfile
```

-	Layers:
	-	`sha256:926a4dc0d56e3c9be08d364b9e30b94d534c9a7d479ce49b32d9a7fac0b85348`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 3.5 MB (3467148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22075a440bd6b34723136a723584525e19f147bda33189d33a6d6199161fb556`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:6894b9d3fdf6f9a5176261f14ca3c651730ec73db9ce0a765a15e7a388d3c6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149988948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def79bef4e97280e0c980f63684e324dcc092b868ebffdca3086d2acd9046879`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a964195047607539333a13346b03ad72f2ad2936f990c34030f96b711db4d8d6`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35944b8be452548cffc3b1e219d96ee2c781cd22bfcf9556e2189bc35b49b2f0`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 7.4 MB (7387884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37c28b87d08942391748734f64343e220c6ce718982c62cadfe473b0e7eadde`  
		Last Modified: Tue, 06 May 2025 17:50:05 GMT  
		Size: 73.1 MB (73076016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1fdb13b6204813e6a2b61535f8a84ab797314b04528ddfbc414041076fb881`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 378.1 KB (378084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63fee4f0f8bf582bdc0669dc2b702f84f1a6f98705c8a64b90b76089c9c0e17`  
		Last Modified: Tue, 06 May 2025 17:50:04 GMT  
		Size: 99.4 KB (99430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212ed74fe9c91ae5451882f5fce49cce5b47e5b6ea72f551f1d1afe3baa15df8`  
		Last Modified: Tue, 06 May 2025 17:50:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d65d8e4597eadb5b291238e3185b9f77f85e1b800168cc2bf13e44ec6c6663`  
		Last Modified: Tue, 06 May 2025 17:50:05 GMT  
		Size: 42.2 MB (42160785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c1cb17e9fbd6a9bb9d287e74d4e34aae2758743989aa26f811b27e477b142`  
		Last Modified: Tue, 06 May 2025 17:50:05 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d9b219d92f16a58e3cb1a7e838a3f1c08b8df07533420880d740fdab7986c446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80ac1a179e7abb201a9085ecfe46c8e1753c07accd3bada6a559bdd2b2b9beb`

```dockerfile
```

-	Layers:
	-	`sha256:9e60d3321d2c177f7279a87c7a52d401cd66706f2abc46b4774c75118fe11837`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 3.5 MB (3461893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5585a3fbd006fe2392f7b475da7f2e476800ea78a189a415cb5e70900d9b61`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0`

```console
$ docker pull couchdb@sha256:1b28dc51a240436da6056e1abe8f20c7d3c3da31d177660604154757417098e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.0` - linux; amd64

```console
$ docker pull couchdb@sha256:7faf0e7902f40804f1163d3842c5c167a81554c45ea16eebab1789db7c93c25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139818838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3c757ceb5923d408b8124eebb02e65b37da8856a005b4200c30a4273989c8a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe1974f056aad23a64cbbdc03852bf1efafc7eaa4817ee2d7a24366574455ae`  
		Last Modified: Thu, 08 May 2025 17:06:57 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6aa47f14243ca5639fe2147fa59167504a6725e4941fb61bd972b1024531d9`  
		Last Modified: Thu, 08 May 2025 17:06:58 GMT  
		Size: 7.9 MB (7874895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8056ef4d8d40cf0ca156161ff732ca53cc5825d673e10720bded43fc514608c0`  
		Last Modified: Thu, 08 May 2025 17:06:57 GMT  
		Size: 392.1 KB (392135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f973ae9dcc0b553fee469a8b06577ad5d8a0132288ff88f04b021d4e471d5d`  
		Last Modified: Thu, 08 May 2025 17:06:58 GMT  
		Size: 76.3 KB (76265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d671e8f13231ab470c06c84eb87f86d79b14fe895e65fef490baadf5fff32`  
		Last Modified: Thu, 08 May 2025 17:06:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ae3f30105e1b7fe0121c8772acb185ada59719319a9f83dcb52b5c2b191287`  
		Last Modified: Thu, 08 May 2025 17:07:10 GMT  
		Size: 103.2 MB (103242477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932bc8e4f38e3db1d1a0d301f20f034811d9d004e4e192a4a9a738e4ac0fc3ec`  
		Last Modified: Thu, 08 May 2025 17:06:59 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe83f3f27f8053db9fe06b1de54707d16dbaca154ff2542eb5262944db60f06`  
		Last Modified: Thu, 08 May 2025 17:06:59 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8075ffc8d54d78cb8f879b54f93017cd6cfa3aa40967815a04bcd2b217d4ccc5`  
		Last Modified: Thu, 08 May 2025 17:07:01 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b3d9977391b67379ebb07fbcfb945142d7a688cdf8cdd3df14f694861f9f26`  
		Last Modified: Thu, 08 May 2025 17:07:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:1ff371a8f5fd0166ef045d2c7436fc504e44a2500becfb70a7ed1fd74aca3f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480cf8b4695682d7e0040075485be64ecd2c679fde58bb22acd015dff1c919bc`

```dockerfile
```

-	Layers:
	-	`sha256:9ba495f0841ba1c78683893a8d96ed43a644c92f1a4931bed4fb95e4f63ad8d2`  
		Last Modified: Tue, 06 May 2025 17:18:00 GMT  
		Size: 4.0 MB (3977471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e178e62addd76c26e3f436bff538589513a603a18ea290728943c4a05672eec`  
		Last Modified: Tue, 06 May 2025 17:17:59 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2e5d6e31ba5b9b92989e29faa365e2bffb92af2c68d74ece6a2ca43016ba6648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139041917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11de94aa647367ba5fe5a4ea744897e9a6e24f0ab3c0db12740c8cafca9ee4d4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fda7edaf9e5fa4bff22f8647fc45ace1dec9a2413c557a56f3d209571bb03d3`  
		Last Modified: Thu, 08 May 2025 17:20:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f44d3c9be40e352cbd13efebb94c5b86d4cd047a37cb05e1470b3799da491`  
		Last Modified: Thu, 08 May 2025 17:20:52 GMT  
		Size: 7.7 MB (7654565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77c2f410b4ff91dda61e7492f539cf3280b1e296b0f87b974582537e952a860`  
		Last Modified: Thu, 08 May 2025 17:20:32 GMT  
		Size: 348.9 KB (348949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f245645ed55f34a29dc8f3628a26a2df51feae716273e621d28255c5cd0366fc`  
		Last Modified: Thu, 08 May 2025 17:20:34 GMT  
		Size: 76.3 KB (76313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5710c3924976aed640fb8f738d4e47e35ecd4a5fcf0b2511f68afe7d1146528`  
		Last Modified: Thu, 08 May 2025 17:20:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0454c720549b1dcd1cdef601206f434cdd971e17c9a772d65ba3975f97b969`  
		Last Modified: Thu, 08 May 2025 17:20:41 GMT  
		Size: 102.9 MB (102890031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a994b43877b24b8e8eb646784ca98c6cc75ae1c83f06754649a2bd484c7b1831`  
		Last Modified: Thu, 08 May 2025 17:20:35 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c16e2d34057757eb1428efb7c184e238c3794dd98268e3bd294f2f244475f`  
		Last Modified: Thu, 08 May 2025 17:20:36 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc5813c77ab5a6b2305995bddd3c3e4d7a17f36fc53dbf8de965c6d9d85f0a`  
		Last Modified: Thu, 08 May 2025 17:20:37 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc85c73a0cbd10b91c9982c83b79f58e9b9deab4cf54e563375a8a928c2dffa`  
		Last Modified: Thu, 08 May 2025 17:20:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:fe60acaabade72ceee44fb2665c04f57bc8c5b0c47358f52c9b5043925401920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b478e56c588977ce65a82fb0d0c0f20cc1f87c7ea3af87f9bbd3fdaeae84d40c`

```dockerfile
```

-	Layers:
	-	`sha256:89d3e99d85d7bb933bd62e346a0a1620c97bdf09d7c859d291d8a37233ee45df`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 4.0 MB (3977764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:112e82b651057c0dc11627c3143fd48ca8640c788a42c40bdf853c248d46e608`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; s390x

```console
$ docker pull couchdb@sha256:23e6b543536c4f919d516d896ddad6febe9e2b79c019c2ed57a80fb63e84f7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136507495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28d1a2f6d3a6ebb844c9b3e00454a69db63e0666205058c975ff3245b112f3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d172d2bfaf767f3cb6dcee5c5b927a5fcb2cbf6fba23e77b7d6d238ee1181070`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166f60a9ad581cf5c3e56f0033e20a007be898003f412505863a8402ec5b56d5`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 7.4 MB (7387956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66cb9d7c369d14b26c71241ff405bf1cf763d2c76b0409042f00e496f8d2435`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 355.6 KB (355632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3fc1101f198fa75489c4894c40c6e5a2634d0aad28cca95fe802b0052f54a4`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 76.4 KB (76357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5102ac0f24ddaa96a8dab9dce6614f7465dddd84d57f0067fbdde372cb70c46`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039462e57e15e2dd4efecdf541ec4fb6143c1ee4cbce599b00fd62687df905ca`  
		Last Modified: Tue, 06 May 2025 17:48:48 GMT  
		Size: 101.8 MB (101797250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2aad07663621ff4d626933ddca7de8011e57180d89b0e433d93ddd7c6548740`  
		Last Modified: Tue, 06 May 2025 17:48:46 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60d749f2931d7ad4dac37189f1cb2075824085ef47d1d727a6bc4695f5c4faa`  
		Last Modified: Tue, 06 May 2025 17:48:46 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6003fd81da531264f065c3ae78d02e6b7443de4561084bda151895b47a9773`  
		Last Modified: Tue, 06 May 2025 17:48:47 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d813ece651fa98d923ee07da19c9d34bcb67a9c30fc55e7e5c24bed96e88f82a`  
		Last Modified: Tue, 06 May 2025 17:48:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:fff7c0dc5628836e642e15a73ebef0f7a5b8a5b74eb3edffedf6a6f87d8a52d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4008340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dff6521380d733c9a781d2fae34659010abbe4ce5bd29d0138647f68d46c9b`

```dockerfile
```

-	Layers:
	-	`sha256:c19a624b1e77b49254ce1f1eb761fedea0fc0c1bdf9055b4344f6ebd52a88a81`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 4.0 MB (3976559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667c87d1160616974874711a6d46f9f867b5a80450d39daef980c0b06af56063`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0-nouveau`

```console
$ docker pull couchdb@sha256:baf9a64c1d285d7824eadca2ced5920e99f79d5d1eb2cfd742f7961a60994625
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.0-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:0760441508a04c4c9039005042bc8fbb7d4e9c441efe5c054be88d39fcc4af8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156378033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4018243b6579b4ebbc2e674d251bfaef1baa084734761f1a266b9f719cd443`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feab75aebd886c9be0ee7b4ee28339e431a0b497e089561a987558b673ad6797`  
		Last Modified: Tue, 06 May 2025 17:17:31 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852a92f1ebda0c1224152be98b6d9700950524c8a6a9bcd6986fcb00e9ed673d`  
		Last Modified: Tue, 06 May 2025 17:17:32 GMT  
		Size: 7.9 MB (7874878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4461ff2ea16a599621941b4fcee4711521ba84e86d5314a74cd1d375b0d54da4`  
		Last Modified: Tue, 06 May 2025 17:17:34 GMT  
		Size: 77.3 MB (77325051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b0dd7438e7247e12182be2d5b9548c538a9ceb566a2ccbbcaaad1efeb7399`  
		Last Modified: Tue, 06 May 2025 17:17:31 GMT  
		Size: 415.0 KB (414979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f354970eb1ee9dfb1cf1fe1754e7f486629e6854765524e66af1feb9990e5ff`  
		Last Modified: Tue, 06 May 2025 17:17:32 GMT  
		Size: 99.3 KB (99331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31beb4795edca4e38687b771af5cd0e185edc50c9f01f15b7437033faf9358`  
		Last Modified: Tue, 06 May 2025 17:17:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c466b712155d38ccf933748cb87fbda79c3452f6ab7f4a56c7be924115b4b0`  
		Last Modified: Tue, 06 May 2025 17:17:35 GMT  
		Size: 42.4 MB (42434265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72bf32f2e446080d1db9fcb3e5be1d590d01308eb7a93af4ed2955dcf15098b`  
		Last Modified: Tue, 06 May 2025 17:17:34 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7e749f49becf3b999fbf6e4f1a836c3b8477d0a7d906120ee9fc18278df74c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f63f27268a030a521eed2b0958a40303b245ef5df08551b0f85654fc3e3cc27`

```dockerfile
```

-	Layers:
	-	`sha256:f9841b3c7c4b5ba2c2017fb4b6470f955f9181693cdfc9d317a99aa72c60e5ac`  
		Last Modified: Tue, 06 May 2025 17:17:31 GMT  
		Size: 3.5 MB (3468472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66bc4962c889a3aae3880bcd640e64dc8746f8bd434cd016c5f18ab265d066a`  
		Last Modified: Tue, 06 May 2025 17:17:31 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7fdb1df7e89b35ae184e2975f8ed5d5c72acd6e651588d7854923639ea383648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155180531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90792137fb7d00afa09943655aa32c8b56afb2ed23f9ca819aef6c02127e89b0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104637e2eb67ec32ff000f153eebca995c5a32bdca49fe1b16015251fd887842`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc58e96c4d79f04a31e09066efeea0f21f93f87a60cd80b537546b799ebbff9`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 7.7 MB (7654542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f58f87545a1ea3e85e36bc4f13c6528480a4d096cabe6e23b6919d84a3a21fa`  
		Last Modified: Tue, 06 May 2025 17:58:59 GMT  
		Size: 76.7 MB (76653670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886a375283a50138292c4ab34c2a2cd473c86f479a0657d206917439b9293ef4`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 371.7 KB (371732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccf50ebfde2d6eb28578d23558bec7ad3fcf33ed5edbbda390b0c02b37636ab`  
		Last Modified: Tue, 06 May 2025 17:58:56 GMT  
		Size: 99.3 KB (99262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a67aafe8a97aa0a8dd806d49d1da627072a88c7e466a6957064c3b1ac9f579`  
		Last Modified: Tue, 06 May 2025 17:58:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd40dddaef0fcda5c486a0d107b1aeac5eae87d112d92a7f8babc07a9c2bc5b`  
		Last Modified: Tue, 06 May 2025 17:58:59 GMT  
		Size: 42.3 MB (42332820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ead4ac28d2805b9ad7d4bc386937a7df61b55d7493ee5c9fa48d6eab8baa75c`  
		Last Modified: Tue, 06 May 2025 17:58:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc0f7d743c3b12042d2363c435ba9a3136bffb0e8741d2777c0e9501b34fb0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b851a388ca66506c60d98b25da2535df558b509b5464f97e568dcd7055452f`

```dockerfile
```

-	Layers:
	-	`sha256:926a4dc0d56e3c9be08d364b9e30b94d534c9a7d479ce49b32d9a7fac0b85348`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 3.5 MB (3467148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22075a440bd6b34723136a723584525e19f147bda33189d33a6d6199161fb556`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:6894b9d3fdf6f9a5176261f14ca3c651730ec73db9ce0a765a15e7a388d3c6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149988948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def79bef4e97280e0c980f63684e324dcc092b868ebffdca3086d2acd9046879`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a964195047607539333a13346b03ad72f2ad2936f990c34030f96b711db4d8d6`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35944b8be452548cffc3b1e219d96ee2c781cd22bfcf9556e2189bc35b49b2f0`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 7.4 MB (7387884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37c28b87d08942391748734f64343e220c6ce718982c62cadfe473b0e7eadde`  
		Last Modified: Tue, 06 May 2025 17:50:05 GMT  
		Size: 73.1 MB (73076016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1fdb13b6204813e6a2b61535f8a84ab797314b04528ddfbc414041076fb881`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 378.1 KB (378084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63fee4f0f8bf582bdc0669dc2b702f84f1a6f98705c8a64b90b76089c9c0e17`  
		Last Modified: Tue, 06 May 2025 17:50:04 GMT  
		Size: 99.4 KB (99430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212ed74fe9c91ae5451882f5fce49cce5b47e5b6ea72f551f1d1afe3baa15df8`  
		Last Modified: Tue, 06 May 2025 17:50:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d65d8e4597eadb5b291238e3185b9f77f85e1b800168cc2bf13e44ec6c6663`  
		Last Modified: Tue, 06 May 2025 17:50:05 GMT  
		Size: 42.2 MB (42160785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c1cb17e9fbd6a9bb9d287e74d4e34aae2758743989aa26f811b27e477b142`  
		Last Modified: Tue, 06 May 2025 17:50:05 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d9b219d92f16a58e3cb1a7e838a3f1c08b8df07533420880d740fdab7986c446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80ac1a179e7abb201a9085ecfe46c8e1753c07accd3bada6a559bdd2b2b9beb`

```dockerfile
```

-	Layers:
	-	`sha256:9e60d3321d2c177f7279a87c7a52d401cd66706f2abc46b4774c75118fe11837`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 3.5 MB (3461893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5585a3fbd006fe2392f7b475da7f2e476800ea78a189a415cb5e70900d9b61`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:1b28dc51a240436da6056e1abe8f20c7d3c3da31d177660604154757417098e5
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
$ docker pull couchdb@sha256:7faf0e7902f40804f1163d3842c5c167a81554c45ea16eebab1789db7c93c25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139818838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3c757ceb5923d408b8124eebb02e65b37da8856a005b4200c30a4273989c8a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe1974f056aad23a64cbbdc03852bf1efafc7eaa4817ee2d7a24366574455ae`  
		Last Modified: Thu, 08 May 2025 17:06:57 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6aa47f14243ca5639fe2147fa59167504a6725e4941fb61bd972b1024531d9`  
		Last Modified: Thu, 08 May 2025 17:06:58 GMT  
		Size: 7.9 MB (7874895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8056ef4d8d40cf0ca156161ff732ca53cc5825d673e10720bded43fc514608c0`  
		Last Modified: Thu, 08 May 2025 17:06:57 GMT  
		Size: 392.1 KB (392135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f973ae9dcc0b553fee469a8b06577ad5d8a0132288ff88f04b021d4e471d5d`  
		Last Modified: Thu, 08 May 2025 17:06:58 GMT  
		Size: 76.3 KB (76265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d671e8f13231ab470c06c84eb87f86d79b14fe895e65fef490baadf5fff32`  
		Last Modified: Thu, 08 May 2025 17:06:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ae3f30105e1b7fe0121c8772acb185ada59719319a9f83dcb52b5c2b191287`  
		Last Modified: Thu, 08 May 2025 17:07:10 GMT  
		Size: 103.2 MB (103242477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932bc8e4f38e3db1d1a0d301f20f034811d9d004e4e192a4a9a738e4ac0fc3ec`  
		Last Modified: Thu, 08 May 2025 17:06:59 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe83f3f27f8053db9fe06b1de54707d16dbaca154ff2542eb5262944db60f06`  
		Last Modified: Thu, 08 May 2025 17:06:59 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8075ffc8d54d78cb8f879b54f93017cd6cfa3aa40967815a04bcd2b217d4ccc5`  
		Last Modified: Thu, 08 May 2025 17:07:01 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b3d9977391b67379ebb07fbcfb945142d7a688cdf8cdd3df14f694861f9f26`  
		Last Modified: Thu, 08 May 2025 17:07:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:1ff371a8f5fd0166ef045d2c7436fc504e44a2500becfb70a7ed1fd74aca3f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480cf8b4695682d7e0040075485be64ecd2c679fde58bb22acd015dff1c919bc`

```dockerfile
```

-	Layers:
	-	`sha256:9ba495f0841ba1c78683893a8d96ed43a644c92f1a4931bed4fb95e4f63ad8d2`  
		Last Modified: Tue, 06 May 2025 17:18:00 GMT  
		Size: 4.0 MB (3977471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e178e62addd76c26e3f436bff538589513a603a18ea290728943c4a05672eec`  
		Last Modified: Tue, 06 May 2025 17:17:59 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2e5d6e31ba5b9b92989e29faa365e2bffb92af2c68d74ece6a2ca43016ba6648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139041917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11de94aa647367ba5fe5a4ea744897e9a6e24f0ab3c0db12740c8cafca9ee4d4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fda7edaf9e5fa4bff22f8647fc45ace1dec9a2413c557a56f3d209571bb03d3`  
		Last Modified: Thu, 08 May 2025 17:20:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f44d3c9be40e352cbd13efebb94c5b86d4cd047a37cb05e1470b3799da491`  
		Last Modified: Thu, 08 May 2025 17:20:52 GMT  
		Size: 7.7 MB (7654565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77c2f410b4ff91dda61e7492f539cf3280b1e296b0f87b974582537e952a860`  
		Last Modified: Thu, 08 May 2025 17:20:32 GMT  
		Size: 348.9 KB (348949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f245645ed55f34a29dc8f3628a26a2df51feae716273e621d28255c5cd0366fc`  
		Last Modified: Thu, 08 May 2025 17:20:34 GMT  
		Size: 76.3 KB (76313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5710c3924976aed640fb8f738d4e47e35ecd4a5fcf0b2511f68afe7d1146528`  
		Last Modified: Thu, 08 May 2025 17:20:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0454c720549b1dcd1cdef601206f434cdd971e17c9a772d65ba3975f97b969`  
		Last Modified: Thu, 08 May 2025 17:20:41 GMT  
		Size: 102.9 MB (102890031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a994b43877b24b8e8eb646784ca98c6cc75ae1c83f06754649a2bd484c7b1831`  
		Last Modified: Thu, 08 May 2025 17:20:35 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c16e2d34057757eb1428efb7c184e238c3794dd98268e3bd294f2f244475f`  
		Last Modified: Thu, 08 May 2025 17:20:36 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc5813c77ab5a6b2305995bddd3c3e4d7a17f36fc53dbf8de965c6d9d85f0a`  
		Last Modified: Thu, 08 May 2025 17:20:37 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc85c73a0cbd10b91c9982c83b79f58e9b9deab4cf54e563375a8a928c2dffa`  
		Last Modified: Thu, 08 May 2025 17:20:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:fe60acaabade72ceee44fb2665c04f57bc8c5b0c47358f52c9b5043925401920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b478e56c588977ce65a82fb0d0c0f20cc1f87c7ea3af87f9bbd3fdaeae84d40c`

```dockerfile
```

-	Layers:
	-	`sha256:89d3e99d85d7bb933bd62e346a0a1620c97bdf09d7c859d291d8a37233ee45df`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 4.0 MB (3977764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:112e82b651057c0dc11627c3143fd48ca8640c788a42c40bdf853c248d46e608`  
		Last Modified: Tue, 06 May 2025 17:58:01 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:23e6b543536c4f919d516d896ddad6febe9e2b79c019c2ed57a80fb63e84f7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136507495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28d1a2f6d3a6ebb844c9b3e00454a69db63e0666205058c975ff3245b112f3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d172d2bfaf767f3cb6dcee5c5b927a5fcb2cbf6fba23e77b7d6d238ee1181070`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166f60a9ad581cf5c3e56f0033e20a007be898003f412505863a8402ec5b56d5`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 7.4 MB (7387956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66cb9d7c369d14b26c71241ff405bf1cf763d2c76b0409042f00e496f8d2435`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 355.6 KB (355632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3fc1101f198fa75489c4894c40c6e5a2634d0aad28cca95fe802b0052f54a4`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 76.4 KB (76357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5102ac0f24ddaa96a8dab9dce6614f7465dddd84d57f0067fbdde372cb70c46`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039462e57e15e2dd4efecdf541ec4fb6143c1ee4cbce599b00fd62687df905ca`  
		Last Modified: Tue, 06 May 2025 17:48:48 GMT  
		Size: 101.8 MB (101797250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2aad07663621ff4d626933ddca7de8011e57180d89b0e433d93ddd7c6548740`  
		Last Modified: Tue, 06 May 2025 17:48:46 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60d749f2931d7ad4dac37189f1cb2075824085ef47d1d727a6bc4695f5c4faa`  
		Last Modified: Tue, 06 May 2025 17:48:46 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6003fd81da531264f065c3ae78d02e6b7443de4561084bda151895b47a9773`  
		Last Modified: Tue, 06 May 2025 17:48:47 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d813ece651fa98d923ee07da19c9d34bcb67a9c30fc55e7e5c24bed96e88f82a`  
		Last Modified: Tue, 06 May 2025 17:48:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:fff7c0dc5628836e642e15a73ebef0f7a5b8a5b74eb3edffedf6a6f87d8a52d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4008340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dff6521380d733c9a781d2fae34659010abbe4ce5bd29d0138647f68d46c9b`

```dockerfile
```

-	Layers:
	-	`sha256:c19a624b1e77b49254ce1f1eb761fedea0fc0c1bdf9055b4344f6ebd52a88a81`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 4.0 MB (3976559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667c87d1160616974874711a6d46f9f867b5a80450d39daef980c0b06af56063`  
		Last Modified: Tue, 06 May 2025 17:48:45 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json
