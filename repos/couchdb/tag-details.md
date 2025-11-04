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
$ docker pull couchdb@sha256:ded0c7e661fb6166a03cb2ca4e4ea39acdae71cee1dff08f02e33741fdf39252
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
$ docker pull couchdb@sha256:876cd6d773a737ca0fc40328c5f37d4bb166e0c294740afdec975b0cbc6746e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139836220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8e506c0a7103186f40d3e17de63ff8f2b4b095b84ea07a34c40574db5f9562`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccba59d2d6fdd94f0e833f72f9af63d983c13867d5709d39e3c4c0fc2bfde94`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c547ab29dff3557e48ff250fcb5439e278dcb01d6a6353dbad99e93f6640be4`  
		Last Modified: Tue, 21 Oct 2025 01:44:20 GMT  
		Size: 7.9 MB (7881732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3475fb060a9f828c18e9be99a9aa32ca7f363043e5dc8a4642034b505f1095`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 401.7 KB (401742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaeebfbfe10d7e4da2bfc8472cc80dbce169528ed3a8f35b3fc668fbda315ae`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 76.5 KB (76509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53824741571091d49c151a857e49c95557191fe08b72dcd9917bb6b693879aa8`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31083cc8fd15ba245ed066467da47ef227799bfef57e40ba50ad280b3b6d593`  
		Last Modified: Tue, 21 Oct 2025 01:44:25 GMT  
		Size: 103.2 MB (103242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f0e59b90b6e849cbef734a33902ca29916db915cde791bb2ba771e5c71f45f`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57908fd9df4cf52afe6063f421b7dd3079536f41c7495d1eebb46350ebc71c8f`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd229623b464a1fe4db4d48a05b4218457c35ea0aa5bea66e747920acbd92bf`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6cead4fb824a4bc01338859cacddb34d7e8b122e13509e9257d20f4872a565`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ef78f0c06664901feceb2a4d47ab071a73c2ad7425efc6fc3ae091afab8e5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8af3ff4909a0bdaded74a5f6e59820f19b936c87fc71391862743fb969ab86`

```dockerfile
```

-	Layers:
	-	`sha256:e62e7da30aa7fd3905490a13fcd27ff0ea34037de9b466275bbff9d866b96f35`  
		Last Modified: Tue, 21 Oct 2025 10:33:22 GMT  
		Size: 4.1 MB (4141252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d24f8fb2005db7b0ec4f339c8bfd54568f4afcfcf14d35e060c445a048d318b`  
		Last Modified: Tue, 21 Oct 2025 10:33:23 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:167ee1978e782e3b93c9059c62224a7a901ca5355b48aa4ae2fd551f15ee320a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139156442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23ab11c3b8d5d3c4387a717994e6c9c6eade8dd5868ed58071fb0921ea94f63`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cbe78858b6df80e5e84dfbd9ddc674e346422db5d3e50dfb2fabb65d2be22d`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a631903dc8129c4263fa27259d60017e4de5862a6d1935712efebc8a5e0ab53`  
		Last Modified: Tue, 21 Oct 2025 01:48:29 GMT  
		Size: 7.7 MB (7691963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe9def5514cd9d26a91fd2848ca8ccef93236357c553fa60749f6309c1261be`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 370.5 KB (370476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf82e8a85189dd61246961802a3219751ab02f9b92a3755ef3eb45b1b608124`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 76.5 KB (76457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea7a511cde7ab19b6c8c13a3104d26d906bafd53cfee5e88eae75a3dac682b3`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca232b7d67c004ef410857c2ad98e635e8b41a0ac70a9deab0df53e6141be5de`  
		Last Modified: Tue, 21 Oct 2025 01:48:37 GMT  
		Size: 102.9 MB (102909925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2793c07e3ab6dd864fb7a688529f2ef627985c093b210584eafeea68f364e7a8`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3048ecef6353baae24e41d8de29c13c59296369b1e103d6a986d490b842397`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48cee154d685e327ddd7bad956862ba206742ef75b5aec21d946ce6a8587975`  
		Last Modified: Tue, 21 Oct 2025 01:48:29 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca24e1babe582be5164dbd25c401ed28a4904c97fd0e2eb04f2d30570f2f5c7`  
		Last Modified: Tue, 21 Oct 2025 01:48:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:2c8d58a5941ac9d372f991cacaa49d032f531c1dd5b1c97160bda0e0d727214e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3d2baecf0f9afd2bfaec01e0e477c22b8483821e77f88d1944f19292e160bc`

```dockerfile
```

-	Layers:
	-	`sha256:790cd11e186c2131cd2960c7883cab09fcd58074d7c1b8e083020d5b4ff36554`  
		Last Modified: Tue, 21 Oct 2025 10:33:27 GMT  
		Size: 4.1 MB (4141545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:502c465cbc0da92ff698c3693bc39af66e02138a84928e980945f6c7a0647f47`  
		Last Modified: Tue, 21 Oct 2025 10:33:28 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:02479c6a4b2c4e6eca165713de67c207e241d567d57eaee320af13d77cb95178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136536082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd77fa046e15f3286118b9d03c93caba58eab06cab3359e7bffdf5f5381ebbd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:17:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:17:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 03:17:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:17:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:28 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 04 Nov 2025 03:17:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 03:17:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:17:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:17:53 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 03:17:53 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 03:17:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ebf53fbc3e3d769a60213c6f4b514ac2a0bfef8d2cc98e421e7189ae613338`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7269136448c34c9267e49af25de0c0ee12a6b28019ce9018f963e546288181e5`  
		Last Modified: Tue, 04 Nov 2025 03:19:42 GMT  
		Size: 7.4 MB (7398114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d914dba9eba91885244c28bee6394a9e0abe6ffcb48d68e5a1955ad1bc21219e`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 372.1 KB (372121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6479c330dc7ea8c7bce7182bc9a7eb611c9491484db645a0e4f3f8e7885788fa`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 76.5 KB (76504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c9155aaae72bca21eb141f5ceacd8d28175c0985d9c4823eb67270e62e31d0`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d96ce10d80f81ecb337ff8afc320cec37dfef0cfad120722aa5df713cd31b7b`  
		Last Modified: Tue, 04 Nov 2025 03:19:59 GMT  
		Size: 101.8 MB (101799366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d9137a48a3c453b956a74b128304288bb1fe8b51dcdb2e9396cee3dc3233ce`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da03f19834c4a079266ac7ca7329d31cf7c81545e1c5caa3be7cea4f813bb09`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822f5be2eadf1536e38b496d2b445ea78542173cf650f24fcb0f59d736e4d867`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abac009acac406aef7713c56e997035b1e7581d0611f072f5e5ef0b7214f709`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:5e3d895f98791d4a799522295fb9419b5d59219b003bda29d1b184dab93eb6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aa89f113f66ef056d3d82db343578816627d46191613873a70f779aae6c7a8`

```dockerfile
```

-	Layers:
	-	`sha256:58c4e57db59e9a02f99789af35b3850ae4b6bbdb87fc76166045c4cdb7addaf6`  
		Last Modified: Tue, 04 Nov 2025 08:33:25 GMT  
		Size: 4.1 MB (4137448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5135cc5ce835005828aeaa3f499cd8fc9e8d233aba295ba2b8ba8c997f29244e`  
		Last Modified: Tue, 04 Nov 2025 08:33:26 GMT  
		Size: 31.7 KB (31737 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:326237f0552c116d1340a4abd47f0f7108fb3dbd1dc34d22cbcdbfc493e95a4c
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
$ docker pull couchdb@sha256:7bd253076622dcfcb6390cca1f7e0ef8fe83d3504e6b64619ba3090670eacbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81b0eb4603d1137e4adfdfc2f8785f91a0311569bf4cc7cd673f4079ac8a842`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1639cafcca63de311712b892899c6cc4aed9b5371718452f73380bcd6d15774`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fe5ecf3044eb58f2d7bb999fa2981b736f0433e5d8aafb88a1cf01b3c274ae`  
		Last Modified: Tue, 21 Oct 2025 01:44:15 GMT  
		Size: 7.9 MB (7881771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1706f57bdad1e318fdf510014d94c77ab287f8247cd180e39062e3109065b`  
		Last Modified: Tue, 21 Oct 2025 01:44:25 GMT  
		Size: 77.3 MB (77326889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32856d57f2141400969d53beba7c40d25dad6311f6709c266be89652f44f7cf2`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 424.1 KB (424064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce9b35b25040ddc65ea8f8e44b67cc3700ff2c7d6a1d7a1e9af3292d6d296cc`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 99.5 KB (99487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472adf561563b0ecd0f159f3fa8916f2b8d9757a4d6f1e5c473d706367c41280`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7880d7850c9a69d617f6f008c3ef14c95ad8e3d094439388b97c6551ca9e7051`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 42.4 MB (42436086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b827c26d71cef106323dddc4f16c6d5bea3d454c6c63f5d10dd630b965ce66`  
		Last Modified: Tue, 21 Oct 2025 01:44:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:353d203253063a16bb3ebefcb3e68999a8d5829ea8764433c3284b52347c42f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9e95b2bd113e2f279f39a4dcd398e62ea0a6106ee21cc82003119a5fa95e12`

```dockerfile
```

-	Layers:
	-	`sha256:a9941eaff4817d44a1e322cffe23af5051161dbc6dea017aea5806c3e3937b5c`  
		Last Modified: Tue, 21 Oct 2025 10:33:32 GMT  
		Size: 3.7 MB (3658049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a221761a19ff308c3e9acc58f511ffb2d53322d69e772e24f853ec43e9ae0605`  
		Last Modified: Tue, 21 Oct 2025 10:33:33 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e33829de3bae4d35bb957449de2e0a183c4f0aef75f46dfba71c4da45a6364f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155279417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25262966e44ddd3f261905517a41e46d230b9c0996f3d41602081d90ad5e5a88`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b23ec744cbf628e7915ee0abd034e7b1082b4d9f9f922d47a701c7b39c8fa0`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf943ff90737b14c37e7d4d2a8682196e70ebdf1ca2ca6fe7d852e7c60641c2c`  
		Last Modified: Tue, 21 Oct 2025 01:48:40 GMT  
		Size: 7.7 MB (7692029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1895b3861d497a754f77085690a46cc8ddc49ba295a2a9940469b045c2afce`  
		Last Modified: Tue, 21 Oct 2025 01:48:47 GMT  
		Size: 76.7 MB (76652724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f24b65d8dec75be45ffbae4e68f04f096f2000091d0766eec0e21e0beafa08`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 392.7 KB (392700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d801aaabd0aa70a3ef10379e047ab4cefe8a9dae46c5119341e03d62f7fcb6`  
		Last Modified: Tue, 21 Oct 2025 01:48:40 GMT  
		Size: 99.5 KB (99462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c62e1afce1ee387d8b513aeb417f5d2923b3c8effc353a803236d2997d6dbbc`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd698eb5dda21c64b725fc1f35382a140e35d2a8fcd394d2581666c65a5b4d8`  
		Last Modified: Tue, 21 Oct 2025 01:48:42 GMT  
		Size: 42.3 MB (42338433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a57ac6ba65a5db293fad3d0b56087e40b78f646d98984b94b4c80e6ef53118`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b3bfa3c9b78f805d794ed3b6cef47e55f6e156ae0c1c433975c0b2175ee95880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1faf9bfd155669dd6d67d932b17cee107705c6bf761944d1d9b886c24dddf5d2`

```dockerfile
```

-	Layers:
	-	`sha256:a86901657a28f2106c4989414d4464b32b17948db61b1fc52565b28bcc88c496`  
		Last Modified: Tue, 21 Oct 2025 10:33:37 GMT  
		Size: 3.7 MB (3656725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270b30851a2520992933292b5593e150437a79030176d467eb46b7b015c8032d`  
		Last Modified: Tue, 21 Oct 2025 10:33:38 GMT  
		Size: 24.7 KB (24745 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:e4c1cf464286a900ce86d7096170b79c191b0074671bbe641daeb58da6f1ac72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150084594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6dc22a341d88212c87b94678a78c8dbf8254d5dce3e2650d1438777fd86356c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:18:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:18:35 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 03:18:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:18:57 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:57 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:19:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 03:19:10 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 03:19:10 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 03:19:10 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 03:19:10 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7536539bf1ad715cf2dd300635c28f289b63af1cbb92522e91502eef246923`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526e0a76fba7a4a90e9f82e82a2d36b1fb986318a85518bfc9635401a95de3e9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 7.4 MB (7398078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce039d7896ebedadc57a51103ebe71649e42dcf66503771ad322910999b1c820`  
		Last Modified: Tue, 04 Nov 2025 03:19:46 GMT  
		Size: 73.1 MB (73142672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a2015e06dd327a6fa19c3c6249a4fce7b4de27b48d0ffe99bd89193cdc50d`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 394.4 KB (394429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2edba20a7c1a1e969e4475b2647e6299aa0a17f5c863767efe6b0eba76bd8b9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 99.6 KB (99633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758223be14bf6c71052fd32d6b25ffd5166b527a06b436acc6588a71754d8256`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a42ee912410feb134c1beae3caa7a5819b26a2805c5f5788a2f1c752a05596`  
		Last Modified: Tue, 04 Nov 2025 03:19:45 GMT  
		Size: 42.2 MB (42163353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28b2decc0bdb622a25486a906d92d47c9957614b0b2ddb085d111ec24b66527`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:11dfbbe0f26655b6dfe5283f838c837702a2801997b244b3a58e3a1ec15d5fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6db580cd46bc75bb51312e6ea0a2dfb655c8e7fe65b7510b23417a1d0c73e9`

```dockerfile
```

-	Layers:
	-	`sha256:1d791db3ab66f5870c8b313ea2a48f5fdf410625cdd00d14b2c3fe7fd8f612da`  
		Last Modified: Tue, 04 Nov 2025 08:33:32 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:908d204e4b43581a218031a0ded371c1bfa2b0e497370e7987e87a5c61463cfd`  
		Last Modified: Tue, 04 Nov 2025 08:33:32 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:96bf848471a2fbffe8a0e4dcc1eda80644f7a0092d8d45f5a56fd005363feae0
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
$ docker pull couchdb@sha256:7e9a7fcb306c6a3cf16f279eb208362f1bb065b2464706c89b254708396c7b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139013656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2713771e7b1e529b364028daccf47816dad278a83d5c450e5e424092131f1778`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
ENV COUCHDB_VERSION=3.4.3
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c556a051bd0f8fe639c952eb55c2e250d65668a73b32a1fc16b8fd0def51e1ce`  
		Last Modified: Tue, 21 Oct 2025 01:44:16 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9684b31bb0e39bb9dd62606c5a65416bb4821e85094cca0cb401157a758586a`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 7.9 MB (7881710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29a3c1360f3bd26d2a41dc18d3094753555be540bed2ba1c9554bf652b2a3d2`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 401.7 KB (401726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5677fece78c209baef87a38ff79164f77f432535ebea1df411bac55279d671f9`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 76.4 KB (76434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904e679722b1aaae082752a4e065907d9847c5e2923798c94d516519516c0dec`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2bcfb936d3031ae61edda1363de096e8212d969257442aa11cedef3fa8e60f`  
		Last Modified: Tue, 21 Oct 2025 01:44:26 GMT  
		Size: 102.4 MB (102420026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dded37efea869b2616bfa404900337928fa4d4ea1bc8d4e445f68393fc0d5815`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11b314f7eb1923991df1d1917ccb86b6cb4784e23939ad8abb18641a520c8db`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d5c6115f84414f0dc1ab398088dba546db46afb625d364570d5b0c35f9f827`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137544b5c2256362c904a85ddc40c7589f3dc3b91fc295f4aa89173b2d95c161`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:36550cd16cc7437935a0ff171db240a5dd08263c001548258760ce5646870b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522c1ea877c09694ba306c2185eabf22d23d00feec1f4104a606e0a6aa017275`

```dockerfile
```

-	Layers:
	-	`sha256:1560008f15aaf29056ef7830ad0e61fe28a6a7648939fd07fe4152cc1338fed6`  
		Last Modified: Tue, 21 Oct 2025 10:33:42 GMT  
		Size: 4.1 MB (4125385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2cce9ce4244373d65105145d77d6c82fde75dc22212915d69973665b4cc67e9`  
		Last Modified: Tue, 21 Oct 2025 10:33:42 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:01bb97b668028df5805c1e5a1cabacd6906478d8499e72f71440791d11062a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138415527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4d1424c312e9b5f057d442ffe25bf3c59ff2569c57de0273f9278278db476d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
ENV COUCHDB_VERSION=3.4.3
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc195e7b2156dafd8e6e53aa004f4c53331648a695ef7c64a4b78bb66ca15c1b`  
		Last Modified: Tue, 21 Oct 2025 01:48:38 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0190883da367774e32f4fab4ce5b0a7dd28dbd50e1c9b4f6b45689a9cb0a74dd`  
		Last Modified: Tue, 21 Oct 2025 01:48:40 GMT  
		Size: 7.7 MB (7692006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7673e3eb3e4091f0b9eb14baa270df069283245a8e203a74698a8f0503ebc153`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 370.5 KB (370485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a5cb23bdb6439d38c63732b4b6572fafeaaed2f9e489216a8b8d68ad1da8c9`  
		Last Modified: Tue, 21 Oct 2025 01:48:38 GMT  
		Size: 76.5 KB (76469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86630694d27d80302057ada882738c87530c584d00fa897f0deb020a59e3feea`  
		Last Modified: Tue, 21 Oct 2025 01:48:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d42ee26815bc719f604102cdd34cf08e65051d6f4d4bf19c3d57fbcb01e3aa6`  
		Last Modified: Tue, 21 Oct 2025 01:48:48 GMT  
		Size: 102.2 MB (102168944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c33ba21a13d30dd629ccf31b4bfe1dc36c9194af1451f914f5fdb7b5efff166`  
		Last Modified: Tue, 21 Oct 2025 01:48:38 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada24bbc6301a7122a2ca5b38265ae6a2300246b15f7ef6133b4c620af933962`  
		Last Modified: Tue, 21 Oct 2025 01:48:38 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a295ad4950760ee28ed307f1a8897c479ed0061350f5329588a663faa9fcdf4`  
		Last Modified: Tue, 21 Oct 2025 01:48:38 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea162cdc9bf0dccff7fa2196f1f058cd288ac8f4322473a7cb13288d325d1d16`  
		Last Modified: Tue, 21 Oct 2025 01:48:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:d8f0b105a5fec73195be7aec405d7d0a8847bd4e379f69f3d67149ae1766cbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64438ef828c67160bd95e90613e08a4965b03a295699f12c3262e4794bf2c68`

```dockerfile
```

-	Layers:
	-	`sha256:12a1d22666b83b766cf11ae076b2630d5013ed790aa799e2aedc68e3daa1d7c2`  
		Last Modified: Tue, 21 Oct 2025 10:33:46 GMT  
		Size: 4.1 MB (4125654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b59ec813e3f0b8f943ae91c7694a1235bfb35a4430046df9fe1c0086d770b8d1`  
		Last Modified: Tue, 21 Oct 2025 10:33:47 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:7d0d34b2bd8ccd9a33f1867591d6cf0fa624e3b1006bdbd5654025ac3f31e0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135793031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e587c91bb3579341c572872236fbd4ee2e326b1838d01b1136d13ca436e998`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:17:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:17:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 03:17:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:17:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:28 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 04 Nov 2025 03:19:52 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:20:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 03:20:15 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 03:20:15 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 03:20:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 03:20:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:20:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:20:16 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 03:20:16 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 03:20:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ebf53fbc3e3d769a60213c6f4b514ac2a0bfef8d2cc98e421e7189ae613338`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7269136448c34c9267e49af25de0c0ee12a6b28019ce9018f963e546288181e5`  
		Last Modified: Tue, 04 Nov 2025 03:19:42 GMT  
		Size: 7.4 MB (7398114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d914dba9eba91885244c28bee6394a9e0abe6ffcb48d68e5a1955ad1bc21219e`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 372.1 KB (372121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6479c330dc7ea8c7bce7182bc9a7eb611c9491484db645a0e4f3f8e7885788fa`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 76.5 KB (76504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9470edf29bf6994e89c47deecd6a558a242b0646ca9e3328a885918797f91c7`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b89a5f2d1111c22e5f41446d58663b1d82ab5d0329ba6b08582b2b987220305`  
		Last Modified: Tue, 04 Nov 2025 03:21:10 GMT  
		Size: 101.1 MB (101056323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e010a90a16de6beb0136e22206a21576e2a3e0046e04651d8719c1fa23b732f4`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262cf45231db5237eea2f3dd7dc7ff0edea47f8bc9ea2266a789d998a34952ff`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d0360c36779ed8466cb52e6a129b974f313d35840a7ea23bc8a3b28fa17bdd`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17675d30c8cd72b2e434e73f6c3a1f117f8d4c7c63b46f79e979bcffe1df958a`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:a2418d1f77c38958518731f52885b5971598e6cf401d327840b1ea34d9de9d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbb1adb9c833f0c36f50f5051b969eac60839b7da1b5ca1dc4857bd29d3aa6c`

```dockerfile
```

-	Layers:
	-	`sha256:56aed6f64c043e2e4a34464b6a8d5faf7545147543a4ec9b78c6a511bdfedbad`  
		Last Modified: Tue, 04 Nov 2025 08:33:37 GMT  
		Size: 4.1 MB (4121581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9103d442718ed0821b7b9235f5b81f678192a9d60fa0c28645ae8f1fbef723c`  
		Last Modified: Tue, 04 Nov 2025 08:33:38 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:aff035c1a133d26fa4506c51340dd9c17483efdebe2dd5331144dc90384c88f1
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
$ docker pull couchdb@sha256:b6dcd3f95dcae33dd28de6c620bccb0755a1f28b47d6560f3e26924d270b7e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf17ca971d488d3157bf1722bf003fbb0d6ef9bc10e396242dcddda611a3f72`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9330ec5670ed692da6ca85c1a85f34701c66e5e157602be1c1b11d48b42d0f48`  
		Last Modified: Tue, 21 Oct 2025 01:44:18 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc57843857ed7380a1c456be5a4fbec134c887526d3eaeb2ef9a4d823e0dc1`  
		Last Modified: Tue, 21 Oct 2025 01:44:19 GMT  
		Size: 7.9 MB (7881728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01479d7179623b60c76417af819daf3343c88d33a3592776137d821e242e364`  
		Last Modified: Tue, 21 Oct 2025 01:44:28 GMT  
		Size: 77.3 MB (77326951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafc2fa9037ca29e67b8768d9dafd8ff66e432f9d9530830fe7f966c7427d2cf`  
		Last Modified: Tue, 21 Oct 2025 01:44:18 GMT  
		Size: 424.1 KB (424068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8f2457b54ad3bb2b9e969839fdb0d9eb0b34c4479ba8bc221081125412e00b`  
		Last Modified: Tue, 21 Oct 2025 01:44:19 GMT  
		Size: 99.5 KB (99484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05469c31a7a49d28044637a5f3fc94d2d9cc149c5bb22e4169206f59bcce5f5`  
		Last Modified: Tue, 21 Oct 2025 01:44:19 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299c7fdacb4cdaaabf1d1d5dc93a4b8b2e57a89d1c20d337a5e2d0cb90f1881`  
		Last Modified: Tue, 21 Oct 2025 01:44:27 GMT  
		Size: 42.4 MB (42436006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651e7b0bfef572dd69bec04e3805089327e5f881d3ad68dda804de4272dce2a`  
		Last Modified: Tue, 21 Oct 2025 01:44:21 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:e88dd8bae7527f55c033479941d53a1295d152eba46d4ba5710873c088682258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428caee999890be096dd9488162ba3a1f34f77982a934e1a055d5e77965e9ce9`

```dockerfile
```

-	Layers:
	-	`sha256:c8ed9bedfc024da5a8c351a9f62b383c03e5037b5f4e666dd5d4eae1f738e80b`  
		Last Modified: Tue, 21 Oct 2025 10:33:53 GMT  
		Size: 3.7 MB (3657743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965162c4920717d5939edd4d5daa6f3f829946580d041ecad36ac0a991f21ba3`  
		Last Modified: Tue, 21 Oct 2025 10:33:54 GMT  
		Size: 24.3 KB (24258 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:bea781cad17a06c1f723798060ba2b280d4457ebdcbf15d3486f16d1a31fed48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155278969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883bbb3be13eb7a67b5990bb9638d74c7b32b81e28a8d25e3b4789a020e0efc1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb9da492379dde7bf264d0545261b779f68c4e59555f9c72664f905462aafbd`  
		Last Modified: Tue, 21 Oct 2025 01:48:43 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cafce2fe9ebe0965643d86216197121ea95f932b258aafb193db5fb158208a5`  
		Last Modified: Tue, 21 Oct 2025 01:48:44 GMT  
		Size: 7.7 MB (7692047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a9f16ec09716dc2e520ef4dab4a2cdd6a472124c743b1ce5536348c3c9b6bb`  
		Last Modified: Tue, 21 Oct 2025 01:48:57 GMT  
		Size: 76.7 MB (76652745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48df943bde23bb05dcae3c74ad52f6529f77658a3ec7da22c27c68200e9cf4a7`  
		Last Modified: Tue, 21 Oct 2025 01:48:43 GMT  
		Size: 392.7 KB (392692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46559953ae3e3e916aaea2004c4e0107f5aa27cedaa98af5347cc7ff4567fd06`  
		Last Modified: Tue, 21 Oct 2025 01:48:43 GMT  
		Size: 99.4 KB (99435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617957dcc1dab5c606f2b0caf3382379356f7eb4d348ebe19faaf939c026efc8`  
		Last Modified: Tue, 21 Oct 2025 01:48:43 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede0e07ded47c5fcc6a32d254fb7a3eaea9c65ad80340f2f8a6c2821c1bda61c`  
		Last Modified: Tue, 21 Oct 2025 01:48:52 GMT  
		Size: 42.3 MB (42337981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829cbb1109e177aaef3307037e48e7918edf5d1a15b7f48a0df9d7bdd91699cf`  
		Last Modified: Tue, 21 Oct 2025 01:48:44 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5a441bdd2edc4b0b1da94af8c6492bee47df2d3a4233f79db66a15584746454f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80adf8ef7a78b46f6be285560a2678eb2682475c15a6ed90180d9f5c89776d71`

```dockerfile
```

-	Layers:
	-	`sha256:39855a7207b2b33d83f02882d9e6cde8a82df02a48868944a3fbd567ea8826a9`  
		Last Modified: Tue, 21 Oct 2025 10:33:58 GMT  
		Size: 3.7 MB (3656407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a7afa6e096386649ed79322ea22136c5b17fe1e89aca8efb738d4d9be8c7616`  
		Last Modified: Tue, 21 Oct 2025 10:33:59 GMT  
		Size: 24.4 KB (24427 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:0145626e7a70b53d323a618d7d58a0d49fbf8a9ae8a6c4e3c14f3a07bbf31845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150084175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7128f59709ed6c5239688d86277670a1411bfdfaa882857f7464c74f52d057`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:18:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:18:35 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 03:18:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:18:57 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:57 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:21:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 03:21:06 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 03:21:06 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 03:21:06 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 03:21:06 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7536539bf1ad715cf2dd300635c28f289b63af1cbb92522e91502eef246923`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526e0a76fba7a4a90e9f82e82a2d36b1fb986318a85518bfc9635401a95de3e9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 7.4 MB (7398078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce039d7896ebedadc57a51103ebe71649e42dcf66503771ad322910999b1c820`  
		Last Modified: Tue, 04 Nov 2025 03:19:46 GMT  
		Size: 73.1 MB (73142672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a2015e06dd327a6fa19c3c6249a4fce7b4de27b48d0ffe99bd89193cdc50d`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 394.4 KB (394429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2edba20a7c1a1e969e4475b2647e6299aa0a17f5c863767efe6b0eba76bd8b9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 99.6 KB (99633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758223be14bf6c71052fd32d6b25ffd5166b527a06b436acc6588a71754d8256`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6861da6c97c304c8e2ed9d94c8e535e0c8458832ddb378851278a924f87d6c42`  
		Last Modified: Tue, 04 Nov 2025 03:21:39 GMT  
		Size: 42.2 MB (42162934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9448ee32852a3a6e4a52afc8f08dd53e824cd98ccac9d74db2c005669ad047a`  
		Last Modified: Tue, 04 Nov 2025 03:21:35 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:42efca8f483cddc63e12d8250d9dd8313f6bc23dfedc3abd3750403804d7b6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e394573be0abf17c648ec23cbf33dcee47e327345de502eb22e4b85fbfb7c3`

```dockerfile
```

-	Layers:
	-	`sha256:3ab20807afc48964b4c227c71583252efe4b22c63ff2a786aadd9701911640d6`  
		Last Modified: Tue, 04 Nov 2025 08:33:43 GMT  
		Size: 3.6 MB (3648276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3169b1aa8b6279ab34ad66ad409146b57db516796ebbafe05a4fcdcea3c45dea`  
		Last Modified: Tue, 04 Nov 2025 08:33:44 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:96bf848471a2fbffe8a0e4dcc1eda80644f7a0092d8d45f5a56fd005363feae0
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
$ docker pull couchdb@sha256:7e9a7fcb306c6a3cf16f279eb208362f1bb065b2464706c89b254708396c7b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139013656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2713771e7b1e529b364028daccf47816dad278a83d5c450e5e424092131f1778`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
ENV COUCHDB_VERSION=3.4.3
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c556a051bd0f8fe639c952eb55c2e250d65668a73b32a1fc16b8fd0def51e1ce`  
		Last Modified: Tue, 21 Oct 2025 01:44:16 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9684b31bb0e39bb9dd62606c5a65416bb4821e85094cca0cb401157a758586a`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 7.9 MB (7881710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29a3c1360f3bd26d2a41dc18d3094753555be540bed2ba1c9554bf652b2a3d2`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 401.7 KB (401726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5677fece78c209baef87a38ff79164f77f432535ebea1df411bac55279d671f9`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 76.4 KB (76434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904e679722b1aaae082752a4e065907d9847c5e2923798c94d516519516c0dec`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2bcfb936d3031ae61edda1363de096e8212d969257442aa11cedef3fa8e60f`  
		Last Modified: Tue, 21 Oct 2025 01:44:26 GMT  
		Size: 102.4 MB (102420026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dded37efea869b2616bfa404900337928fa4d4ea1bc8d4e445f68393fc0d5815`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11b314f7eb1923991df1d1917ccb86b6cb4784e23939ad8abb18641a520c8db`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d5c6115f84414f0dc1ab398088dba546db46afb625d364570d5b0c35f9f827`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137544b5c2256362c904a85ddc40c7589f3dc3b91fc295f4aa89173b2d95c161`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:36550cd16cc7437935a0ff171db240a5dd08263c001548258760ce5646870b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522c1ea877c09694ba306c2185eabf22d23d00feec1f4104a606e0a6aa017275`

```dockerfile
```

-	Layers:
	-	`sha256:1560008f15aaf29056ef7830ad0e61fe28a6a7648939fd07fe4152cc1338fed6`  
		Last Modified: Tue, 21 Oct 2025 10:33:42 GMT  
		Size: 4.1 MB (4125385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2cce9ce4244373d65105145d77d6c82fde75dc22212915d69973665b4cc67e9`  
		Last Modified: Tue, 21 Oct 2025 10:33:42 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:01bb97b668028df5805c1e5a1cabacd6906478d8499e72f71440791d11062a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138415527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4d1424c312e9b5f057d442ffe25bf3c59ff2569c57de0273f9278278db476d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
ENV COUCHDB_VERSION=3.4.3
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc195e7b2156dafd8e6e53aa004f4c53331648a695ef7c64a4b78bb66ca15c1b`  
		Last Modified: Tue, 21 Oct 2025 01:48:38 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0190883da367774e32f4fab4ce5b0a7dd28dbd50e1c9b4f6b45689a9cb0a74dd`  
		Last Modified: Tue, 21 Oct 2025 01:48:40 GMT  
		Size: 7.7 MB (7692006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7673e3eb3e4091f0b9eb14baa270df069283245a8e203a74698a8f0503ebc153`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 370.5 KB (370485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a5cb23bdb6439d38c63732b4b6572fafeaaed2f9e489216a8b8d68ad1da8c9`  
		Last Modified: Tue, 21 Oct 2025 01:48:38 GMT  
		Size: 76.5 KB (76469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86630694d27d80302057ada882738c87530c584d00fa897f0deb020a59e3feea`  
		Last Modified: Tue, 21 Oct 2025 01:48:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d42ee26815bc719f604102cdd34cf08e65051d6f4d4bf19c3d57fbcb01e3aa6`  
		Last Modified: Tue, 21 Oct 2025 01:48:48 GMT  
		Size: 102.2 MB (102168944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c33ba21a13d30dd629ccf31b4bfe1dc36c9194af1451f914f5fdb7b5efff166`  
		Last Modified: Tue, 21 Oct 2025 01:48:38 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada24bbc6301a7122a2ca5b38265ae6a2300246b15f7ef6133b4c620af933962`  
		Last Modified: Tue, 21 Oct 2025 01:48:38 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a295ad4950760ee28ed307f1a8897c479ed0061350f5329588a663faa9fcdf4`  
		Last Modified: Tue, 21 Oct 2025 01:48:38 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea162cdc9bf0dccff7fa2196f1f058cd288ac8f4322473a7cb13288d325d1d16`  
		Last Modified: Tue, 21 Oct 2025 01:48:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d8f0b105a5fec73195be7aec405d7d0a8847bd4e379f69f3d67149ae1766cbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64438ef828c67160bd95e90613e08a4965b03a295699f12c3262e4794bf2c68`

```dockerfile
```

-	Layers:
	-	`sha256:12a1d22666b83b766cf11ae076b2630d5013ed790aa799e2aedc68e3daa1d7c2`  
		Last Modified: Tue, 21 Oct 2025 10:33:46 GMT  
		Size: 4.1 MB (4125654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b59ec813e3f0b8f943ae91c7694a1235bfb35a4430046df9fe1c0086d770b8d1`  
		Last Modified: Tue, 21 Oct 2025 10:33:47 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:7d0d34b2bd8ccd9a33f1867591d6cf0fa624e3b1006bdbd5654025ac3f31e0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135793031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e587c91bb3579341c572872236fbd4ee2e326b1838d01b1136d13ca436e998`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:17:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:17:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 03:17:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:17:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:28 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 04 Nov 2025 03:19:52 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:20:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 03:20:15 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 03:20:15 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 03:20:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 03:20:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:20:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:20:16 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 03:20:16 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 03:20:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ebf53fbc3e3d769a60213c6f4b514ac2a0bfef8d2cc98e421e7189ae613338`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7269136448c34c9267e49af25de0c0ee12a6b28019ce9018f963e546288181e5`  
		Last Modified: Tue, 04 Nov 2025 03:19:42 GMT  
		Size: 7.4 MB (7398114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d914dba9eba91885244c28bee6394a9e0abe6ffcb48d68e5a1955ad1bc21219e`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 372.1 KB (372121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6479c330dc7ea8c7bce7182bc9a7eb611c9491484db645a0e4f3f8e7885788fa`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 76.5 KB (76504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9470edf29bf6994e89c47deecd6a558a242b0646ca9e3328a885918797f91c7`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b89a5f2d1111c22e5f41446d58663b1d82ab5d0329ba6b08582b2b987220305`  
		Last Modified: Tue, 04 Nov 2025 03:21:10 GMT  
		Size: 101.1 MB (101056323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e010a90a16de6beb0136e22206a21576e2a3e0046e04651d8719c1fa23b732f4`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262cf45231db5237eea2f3dd7dc7ff0edea47f8bc9ea2266a789d998a34952ff`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d0360c36779ed8466cb52e6a129b974f313d35840a7ea23bc8a3b28fa17bdd`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17675d30c8cd72b2e434e73f6c3a1f117f8d4c7c63b46f79e979bcffe1df958a`  
		Last Modified: Tue, 04 Nov 2025 03:20:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a2418d1f77c38958518731f52885b5971598e6cf401d327840b1ea34d9de9d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbb1adb9c833f0c36f50f5051b969eac60839b7da1b5ca1dc4857bd29d3aa6c`

```dockerfile
```

-	Layers:
	-	`sha256:56aed6f64c043e2e4a34464b6a8d5faf7545147543a4ec9b78c6a511bdfedbad`  
		Last Modified: Tue, 04 Nov 2025 08:33:37 GMT  
		Size: 4.1 MB (4121581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9103d442718ed0821b7b9235f5b81f678192a9d60fa0c28645ae8f1fbef723c`  
		Last Modified: Tue, 04 Nov 2025 08:33:38 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:aff035c1a133d26fa4506c51340dd9c17483efdebe2dd5331144dc90384c88f1
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
$ docker pull couchdb@sha256:b6dcd3f95dcae33dd28de6c620bccb0755a1f28b47d6560f3e26924d270b7e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf17ca971d488d3157bf1722bf003fbb0d6ef9bc10e396242dcddda611a3f72`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9330ec5670ed692da6ca85c1a85f34701c66e5e157602be1c1b11d48b42d0f48`  
		Last Modified: Tue, 21 Oct 2025 01:44:18 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc57843857ed7380a1c456be5a4fbec134c887526d3eaeb2ef9a4d823e0dc1`  
		Last Modified: Tue, 21 Oct 2025 01:44:19 GMT  
		Size: 7.9 MB (7881728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01479d7179623b60c76417af819daf3343c88d33a3592776137d821e242e364`  
		Last Modified: Tue, 21 Oct 2025 01:44:28 GMT  
		Size: 77.3 MB (77326951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafc2fa9037ca29e67b8768d9dafd8ff66e432f9d9530830fe7f966c7427d2cf`  
		Last Modified: Tue, 21 Oct 2025 01:44:18 GMT  
		Size: 424.1 KB (424068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8f2457b54ad3bb2b9e969839fdb0d9eb0b34c4479ba8bc221081125412e00b`  
		Last Modified: Tue, 21 Oct 2025 01:44:19 GMT  
		Size: 99.5 KB (99484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05469c31a7a49d28044637a5f3fc94d2d9cc149c5bb22e4169206f59bcce5f5`  
		Last Modified: Tue, 21 Oct 2025 01:44:19 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299c7fdacb4cdaaabf1d1d5dc93a4b8b2e57a89d1c20d337a5e2d0cb90f1881`  
		Last Modified: Tue, 21 Oct 2025 01:44:27 GMT  
		Size: 42.4 MB (42436006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651e7b0bfef572dd69bec04e3805089327e5f881d3ad68dda804de4272dce2a`  
		Last Modified: Tue, 21 Oct 2025 01:44:21 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:e88dd8bae7527f55c033479941d53a1295d152eba46d4ba5710873c088682258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428caee999890be096dd9488162ba3a1f34f77982a934e1a055d5e77965e9ce9`

```dockerfile
```

-	Layers:
	-	`sha256:c8ed9bedfc024da5a8c351a9f62b383c03e5037b5f4e666dd5d4eae1f738e80b`  
		Last Modified: Tue, 21 Oct 2025 10:33:53 GMT  
		Size: 3.7 MB (3657743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965162c4920717d5939edd4d5daa6f3f829946580d041ecad36ac0a991f21ba3`  
		Last Modified: Tue, 21 Oct 2025 10:33:54 GMT  
		Size: 24.3 KB (24258 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:bea781cad17a06c1f723798060ba2b280d4457ebdcbf15d3486f16d1a31fed48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155278969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883bbb3be13eb7a67b5990bb9638d74c7b32b81e28a8d25e3b4789a020e0efc1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb9da492379dde7bf264d0545261b779f68c4e59555f9c72664f905462aafbd`  
		Last Modified: Tue, 21 Oct 2025 01:48:43 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cafce2fe9ebe0965643d86216197121ea95f932b258aafb193db5fb158208a5`  
		Last Modified: Tue, 21 Oct 2025 01:48:44 GMT  
		Size: 7.7 MB (7692047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a9f16ec09716dc2e520ef4dab4a2cdd6a472124c743b1ce5536348c3c9b6bb`  
		Last Modified: Tue, 21 Oct 2025 01:48:57 GMT  
		Size: 76.7 MB (76652745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48df943bde23bb05dcae3c74ad52f6529f77658a3ec7da22c27c68200e9cf4a7`  
		Last Modified: Tue, 21 Oct 2025 01:48:43 GMT  
		Size: 392.7 KB (392692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46559953ae3e3e916aaea2004c4e0107f5aa27cedaa98af5347cc7ff4567fd06`  
		Last Modified: Tue, 21 Oct 2025 01:48:43 GMT  
		Size: 99.4 KB (99435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617957dcc1dab5c606f2b0caf3382379356f7eb4d348ebe19faaf939c026efc8`  
		Last Modified: Tue, 21 Oct 2025 01:48:43 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede0e07ded47c5fcc6a32d254fb7a3eaea9c65ad80340f2f8a6c2821c1bda61c`  
		Last Modified: Tue, 21 Oct 2025 01:48:52 GMT  
		Size: 42.3 MB (42337981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829cbb1109e177aaef3307037e48e7918edf5d1a15b7f48a0df9d7bdd91699cf`  
		Last Modified: Tue, 21 Oct 2025 01:48:44 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5a441bdd2edc4b0b1da94af8c6492bee47df2d3a4233f79db66a15584746454f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80adf8ef7a78b46f6be285560a2678eb2682475c15a6ed90180d9f5c89776d71`

```dockerfile
```

-	Layers:
	-	`sha256:39855a7207b2b33d83f02882d9e6cde8a82df02a48868944a3fbd567ea8826a9`  
		Last Modified: Tue, 21 Oct 2025 10:33:58 GMT  
		Size: 3.7 MB (3656407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a7afa6e096386649ed79322ea22136c5b17fe1e89aca8efb738d4d9be8c7616`  
		Last Modified: Tue, 21 Oct 2025 10:33:59 GMT  
		Size: 24.4 KB (24427 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:0145626e7a70b53d323a618d7d58a0d49fbf8a9ae8a6c4e3c14f3a07bbf31845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150084175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7128f59709ed6c5239688d86277670a1411bfdfaa882857f7464c74f52d057`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:18:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:18:35 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 03:18:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:18:57 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:57 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:21:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 03:21:06 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 03:21:06 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 03:21:06 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 03:21:06 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7536539bf1ad715cf2dd300635c28f289b63af1cbb92522e91502eef246923`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526e0a76fba7a4a90e9f82e82a2d36b1fb986318a85518bfc9635401a95de3e9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 7.4 MB (7398078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce039d7896ebedadc57a51103ebe71649e42dcf66503771ad322910999b1c820`  
		Last Modified: Tue, 04 Nov 2025 03:19:46 GMT  
		Size: 73.1 MB (73142672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a2015e06dd327a6fa19c3c6249a4fce7b4de27b48d0ffe99bd89193cdc50d`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 394.4 KB (394429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2edba20a7c1a1e969e4475b2647e6299aa0a17f5c863767efe6b0eba76bd8b9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 99.6 KB (99633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758223be14bf6c71052fd32d6b25ffd5166b527a06b436acc6588a71754d8256`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6861da6c97c304c8e2ed9d94c8e535e0c8458832ddb378851278a924f87d6c42`  
		Last Modified: Tue, 04 Nov 2025 03:21:39 GMT  
		Size: 42.2 MB (42162934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9448ee32852a3a6e4a52afc8f08dd53e824cd98ccac9d74db2c005669ad047a`  
		Last Modified: Tue, 04 Nov 2025 03:21:35 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:42efca8f483cddc63e12d8250d9dd8313f6bc23dfedc3abd3750403804d7b6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e394573be0abf17c648ec23cbf33dcee47e327345de502eb22e4b85fbfb7c3`

```dockerfile
```

-	Layers:
	-	`sha256:3ab20807afc48964b4c227c71583252efe4b22c63ff2a786aadd9701911640d6`  
		Last Modified: Tue, 04 Nov 2025 08:33:43 GMT  
		Size: 3.6 MB (3648276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3169b1aa8b6279ab34ad66ad409146b57db516796ebbafe05a4fcdcea3c45dea`  
		Last Modified: Tue, 04 Nov 2025 08:33:44 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:ded0c7e661fb6166a03cb2ca4e4ea39acdae71cee1dff08f02e33741fdf39252
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
$ docker pull couchdb@sha256:876cd6d773a737ca0fc40328c5f37d4bb166e0c294740afdec975b0cbc6746e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139836220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8e506c0a7103186f40d3e17de63ff8f2b4b095b84ea07a34c40574db5f9562`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccba59d2d6fdd94f0e833f72f9af63d983c13867d5709d39e3c4c0fc2bfde94`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c547ab29dff3557e48ff250fcb5439e278dcb01d6a6353dbad99e93f6640be4`  
		Last Modified: Tue, 21 Oct 2025 01:44:20 GMT  
		Size: 7.9 MB (7881732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3475fb060a9f828c18e9be99a9aa32ca7f363043e5dc8a4642034b505f1095`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 401.7 KB (401742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaeebfbfe10d7e4da2bfc8472cc80dbce169528ed3a8f35b3fc668fbda315ae`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 76.5 KB (76509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53824741571091d49c151a857e49c95557191fe08b72dcd9917bb6b693879aa8`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31083cc8fd15ba245ed066467da47ef227799bfef57e40ba50ad280b3b6d593`  
		Last Modified: Tue, 21 Oct 2025 01:44:25 GMT  
		Size: 103.2 MB (103242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f0e59b90b6e849cbef734a33902ca29916db915cde791bb2ba771e5c71f45f`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57908fd9df4cf52afe6063f421b7dd3079536f41c7495d1eebb46350ebc71c8f`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd229623b464a1fe4db4d48a05b4218457c35ea0aa5bea66e747920acbd92bf`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6cead4fb824a4bc01338859cacddb34d7e8b122e13509e9257d20f4872a565`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:ef78f0c06664901feceb2a4d47ab071a73c2ad7425efc6fc3ae091afab8e5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8af3ff4909a0bdaded74a5f6e59820f19b936c87fc71391862743fb969ab86`

```dockerfile
```

-	Layers:
	-	`sha256:e62e7da30aa7fd3905490a13fcd27ff0ea34037de9b466275bbff9d866b96f35`  
		Last Modified: Tue, 21 Oct 2025 10:33:22 GMT  
		Size: 4.1 MB (4141252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d24f8fb2005db7b0ec4f339c8bfd54568f4afcfcf14d35e060c445a048d318b`  
		Last Modified: Tue, 21 Oct 2025 10:33:23 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:167ee1978e782e3b93c9059c62224a7a901ca5355b48aa4ae2fd551f15ee320a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139156442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23ab11c3b8d5d3c4387a717994e6c9c6eade8dd5868ed58071fb0921ea94f63`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cbe78858b6df80e5e84dfbd9ddc674e346422db5d3e50dfb2fabb65d2be22d`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a631903dc8129c4263fa27259d60017e4de5862a6d1935712efebc8a5e0ab53`  
		Last Modified: Tue, 21 Oct 2025 01:48:29 GMT  
		Size: 7.7 MB (7691963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe9def5514cd9d26a91fd2848ca8ccef93236357c553fa60749f6309c1261be`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 370.5 KB (370476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf82e8a85189dd61246961802a3219751ab02f9b92a3755ef3eb45b1b608124`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 76.5 KB (76457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea7a511cde7ab19b6c8c13a3104d26d906bafd53cfee5e88eae75a3dac682b3`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca232b7d67c004ef410857c2ad98e635e8b41a0ac70a9deab0df53e6141be5de`  
		Last Modified: Tue, 21 Oct 2025 01:48:37 GMT  
		Size: 102.9 MB (102909925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2793c07e3ab6dd864fb7a688529f2ef627985c093b210584eafeea68f364e7a8`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3048ecef6353baae24e41d8de29c13c59296369b1e103d6a986d490b842397`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48cee154d685e327ddd7bad956862ba206742ef75b5aec21d946ce6a8587975`  
		Last Modified: Tue, 21 Oct 2025 01:48:29 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca24e1babe582be5164dbd25c401ed28a4904c97fd0e2eb04f2d30570f2f5c7`  
		Last Modified: Tue, 21 Oct 2025 01:48:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:2c8d58a5941ac9d372f991cacaa49d032f531c1dd5b1c97160bda0e0d727214e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3d2baecf0f9afd2bfaec01e0e477c22b8483821e77f88d1944f19292e160bc`

```dockerfile
```

-	Layers:
	-	`sha256:790cd11e186c2131cd2960c7883cab09fcd58074d7c1b8e083020d5b4ff36554`  
		Last Modified: Tue, 21 Oct 2025 10:33:27 GMT  
		Size: 4.1 MB (4141545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:502c465cbc0da92ff698c3693bc39af66e02138a84928e980945f6c7a0647f47`  
		Last Modified: Tue, 21 Oct 2025 10:33:28 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:02479c6a4b2c4e6eca165713de67c207e241d567d57eaee320af13d77cb95178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136536082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd77fa046e15f3286118b9d03c93caba58eab06cab3359e7bffdf5f5381ebbd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:17:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:17:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 03:17:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:17:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:28 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 04 Nov 2025 03:17:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 03:17:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:17:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:17:53 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 03:17:53 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 03:17:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ebf53fbc3e3d769a60213c6f4b514ac2a0bfef8d2cc98e421e7189ae613338`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7269136448c34c9267e49af25de0c0ee12a6b28019ce9018f963e546288181e5`  
		Last Modified: Tue, 04 Nov 2025 03:19:42 GMT  
		Size: 7.4 MB (7398114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d914dba9eba91885244c28bee6394a9e0abe6ffcb48d68e5a1955ad1bc21219e`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 372.1 KB (372121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6479c330dc7ea8c7bce7182bc9a7eb611c9491484db645a0e4f3f8e7885788fa`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 76.5 KB (76504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c9155aaae72bca21eb141f5ceacd8d28175c0985d9c4823eb67270e62e31d0`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d96ce10d80f81ecb337ff8afc320cec37dfef0cfad120722aa5df713cd31b7b`  
		Last Modified: Tue, 04 Nov 2025 03:19:59 GMT  
		Size: 101.8 MB (101799366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d9137a48a3c453b956a74b128304288bb1fe8b51dcdb2e9396cee3dc3233ce`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da03f19834c4a079266ac7ca7329d31cf7c81545e1c5caa3be7cea4f813bb09`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822f5be2eadf1536e38b496d2b445ea78542173cf650f24fcb0f59d736e4d867`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abac009acac406aef7713c56e997035b1e7581d0611f072f5e5ef0b7214f709`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:5e3d895f98791d4a799522295fb9419b5d59219b003bda29d1b184dab93eb6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aa89f113f66ef056d3d82db343578816627d46191613873a70f779aae6c7a8`

```dockerfile
```

-	Layers:
	-	`sha256:58c4e57db59e9a02f99789af35b3850ae4b6bbdb87fc76166045c4cdb7addaf6`  
		Last Modified: Tue, 04 Nov 2025 08:33:25 GMT  
		Size: 4.1 MB (4137448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5135cc5ce835005828aeaa3f499cd8fc9e8d233aba295ba2b8ba8c997f29244e`  
		Last Modified: Tue, 04 Nov 2025 08:33:26 GMT  
		Size: 31.7 KB (31737 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:326237f0552c116d1340a4abd47f0f7108fb3dbd1dc34d22cbcdbfc493e95a4c
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
$ docker pull couchdb@sha256:7bd253076622dcfcb6390cca1f7e0ef8fe83d3504e6b64619ba3090670eacbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81b0eb4603d1137e4adfdfc2f8785f91a0311569bf4cc7cd673f4079ac8a842`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1639cafcca63de311712b892899c6cc4aed9b5371718452f73380bcd6d15774`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fe5ecf3044eb58f2d7bb999fa2981b736f0433e5d8aafb88a1cf01b3c274ae`  
		Last Modified: Tue, 21 Oct 2025 01:44:15 GMT  
		Size: 7.9 MB (7881771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1706f57bdad1e318fdf510014d94c77ab287f8247cd180e39062e3109065b`  
		Last Modified: Tue, 21 Oct 2025 01:44:25 GMT  
		Size: 77.3 MB (77326889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32856d57f2141400969d53beba7c40d25dad6311f6709c266be89652f44f7cf2`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 424.1 KB (424064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce9b35b25040ddc65ea8f8e44b67cc3700ff2c7d6a1d7a1e9af3292d6d296cc`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 99.5 KB (99487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472adf561563b0ecd0f159f3fa8916f2b8d9757a4d6f1e5c473d706367c41280`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7880d7850c9a69d617f6f008c3ef14c95ad8e3d094439388b97c6551ca9e7051`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 42.4 MB (42436086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b827c26d71cef106323dddc4f16c6d5bea3d454c6c63f5d10dd630b965ce66`  
		Last Modified: Tue, 21 Oct 2025 01:44:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:353d203253063a16bb3ebefcb3e68999a8d5829ea8764433c3284b52347c42f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9e95b2bd113e2f279f39a4dcd398e62ea0a6106ee21cc82003119a5fa95e12`

```dockerfile
```

-	Layers:
	-	`sha256:a9941eaff4817d44a1e322cffe23af5051161dbc6dea017aea5806c3e3937b5c`  
		Last Modified: Tue, 21 Oct 2025 10:33:32 GMT  
		Size: 3.7 MB (3658049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a221761a19ff308c3e9acc58f511ffb2d53322d69e772e24f853ec43e9ae0605`  
		Last Modified: Tue, 21 Oct 2025 10:33:33 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e33829de3bae4d35bb957449de2e0a183c4f0aef75f46dfba71c4da45a6364f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155279417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25262966e44ddd3f261905517a41e46d230b9c0996f3d41602081d90ad5e5a88`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b23ec744cbf628e7915ee0abd034e7b1082b4d9f9f922d47a701c7b39c8fa0`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf943ff90737b14c37e7d4d2a8682196e70ebdf1ca2ca6fe7d852e7c60641c2c`  
		Last Modified: Tue, 21 Oct 2025 01:48:40 GMT  
		Size: 7.7 MB (7692029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1895b3861d497a754f77085690a46cc8ddc49ba295a2a9940469b045c2afce`  
		Last Modified: Tue, 21 Oct 2025 01:48:47 GMT  
		Size: 76.7 MB (76652724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f24b65d8dec75be45ffbae4e68f04f096f2000091d0766eec0e21e0beafa08`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 392.7 KB (392700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d801aaabd0aa70a3ef10379e047ab4cefe8a9dae46c5119341e03d62f7fcb6`  
		Last Modified: Tue, 21 Oct 2025 01:48:40 GMT  
		Size: 99.5 KB (99462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c62e1afce1ee387d8b513aeb417f5d2923b3c8effc353a803236d2997d6dbbc`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd698eb5dda21c64b725fc1f35382a140e35d2a8fcd394d2581666c65a5b4d8`  
		Last Modified: Tue, 21 Oct 2025 01:48:42 GMT  
		Size: 42.3 MB (42338433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a57ac6ba65a5db293fad3d0b56087e40b78f646d98984b94b4c80e6ef53118`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b3bfa3c9b78f805d794ed3b6cef47e55f6e156ae0c1c433975c0b2175ee95880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1faf9bfd155669dd6d67d932b17cee107705c6bf761944d1d9b886c24dddf5d2`

```dockerfile
```

-	Layers:
	-	`sha256:a86901657a28f2106c4989414d4464b32b17948db61b1fc52565b28bcc88c496`  
		Last Modified: Tue, 21 Oct 2025 10:33:37 GMT  
		Size: 3.7 MB (3656725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270b30851a2520992933292b5593e150437a79030176d467eb46b7b015c8032d`  
		Last Modified: Tue, 21 Oct 2025 10:33:38 GMT  
		Size: 24.7 KB (24745 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:e4c1cf464286a900ce86d7096170b79c191b0074671bbe641daeb58da6f1ac72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150084594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6dc22a341d88212c87b94678a78c8dbf8254d5dce3e2650d1438777fd86356c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:18:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:18:35 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 03:18:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:18:57 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:57 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:19:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 03:19:10 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 03:19:10 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 03:19:10 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 03:19:10 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7536539bf1ad715cf2dd300635c28f289b63af1cbb92522e91502eef246923`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526e0a76fba7a4a90e9f82e82a2d36b1fb986318a85518bfc9635401a95de3e9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 7.4 MB (7398078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce039d7896ebedadc57a51103ebe71649e42dcf66503771ad322910999b1c820`  
		Last Modified: Tue, 04 Nov 2025 03:19:46 GMT  
		Size: 73.1 MB (73142672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a2015e06dd327a6fa19c3c6249a4fce7b4de27b48d0ffe99bd89193cdc50d`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 394.4 KB (394429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2edba20a7c1a1e969e4475b2647e6299aa0a17f5c863767efe6b0eba76bd8b9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 99.6 KB (99633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758223be14bf6c71052fd32d6b25ffd5166b527a06b436acc6588a71754d8256`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a42ee912410feb134c1beae3caa7a5819b26a2805c5f5788a2f1c752a05596`  
		Last Modified: Tue, 04 Nov 2025 03:19:45 GMT  
		Size: 42.2 MB (42163353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28b2decc0bdb622a25486a906d92d47c9957614b0b2ddb085d111ec24b66527`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:11dfbbe0f26655b6dfe5283f838c837702a2801997b244b3a58e3a1ec15d5fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6db580cd46bc75bb51312e6ea0a2dfb655c8e7fe65b7510b23417a1d0c73e9`

```dockerfile
```

-	Layers:
	-	`sha256:1d791db3ab66f5870c8b313ea2a48f5fdf410625cdd00d14b2c3fe7fd8f612da`  
		Last Modified: Tue, 04 Nov 2025 08:33:32 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:908d204e4b43581a218031a0ded371c1bfa2b0e497370e7987e87a5c61463cfd`  
		Last Modified: Tue, 04 Nov 2025 08:33:32 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0`

```console
$ docker pull couchdb@sha256:ded0c7e661fb6166a03cb2ca4e4ea39acdae71cee1dff08f02e33741fdf39252
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
$ docker pull couchdb@sha256:876cd6d773a737ca0fc40328c5f37d4bb166e0c294740afdec975b0cbc6746e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139836220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8e506c0a7103186f40d3e17de63ff8f2b4b095b84ea07a34c40574db5f9562`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccba59d2d6fdd94f0e833f72f9af63d983c13867d5709d39e3c4c0fc2bfde94`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c547ab29dff3557e48ff250fcb5439e278dcb01d6a6353dbad99e93f6640be4`  
		Last Modified: Tue, 21 Oct 2025 01:44:20 GMT  
		Size: 7.9 MB (7881732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3475fb060a9f828c18e9be99a9aa32ca7f363043e5dc8a4642034b505f1095`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 401.7 KB (401742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaeebfbfe10d7e4da2bfc8472cc80dbce169528ed3a8f35b3fc668fbda315ae`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 76.5 KB (76509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53824741571091d49c151a857e49c95557191fe08b72dcd9917bb6b693879aa8`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31083cc8fd15ba245ed066467da47ef227799bfef57e40ba50ad280b3b6d593`  
		Last Modified: Tue, 21 Oct 2025 01:44:25 GMT  
		Size: 103.2 MB (103242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f0e59b90b6e849cbef734a33902ca29916db915cde791bb2ba771e5c71f45f`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57908fd9df4cf52afe6063f421b7dd3079536f41c7495d1eebb46350ebc71c8f`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd229623b464a1fe4db4d48a05b4218457c35ea0aa5bea66e747920acbd92bf`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6cead4fb824a4bc01338859cacddb34d7e8b122e13509e9257d20f4872a565`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:ef78f0c06664901feceb2a4d47ab071a73c2ad7425efc6fc3ae091afab8e5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8af3ff4909a0bdaded74a5f6e59820f19b936c87fc71391862743fb969ab86`

```dockerfile
```

-	Layers:
	-	`sha256:e62e7da30aa7fd3905490a13fcd27ff0ea34037de9b466275bbff9d866b96f35`  
		Last Modified: Tue, 21 Oct 2025 10:33:22 GMT  
		Size: 4.1 MB (4141252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d24f8fb2005db7b0ec4f339c8bfd54568f4afcfcf14d35e060c445a048d318b`  
		Last Modified: Tue, 21 Oct 2025 10:33:23 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:167ee1978e782e3b93c9059c62224a7a901ca5355b48aa4ae2fd551f15ee320a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139156442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23ab11c3b8d5d3c4387a717994e6c9c6eade8dd5868ed58071fb0921ea94f63`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cbe78858b6df80e5e84dfbd9ddc674e346422db5d3e50dfb2fabb65d2be22d`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a631903dc8129c4263fa27259d60017e4de5862a6d1935712efebc8a5e0ab53`  
		Last Modified: Tue, 21 Oct 2025 01:48:29 GMT  
		Size: 7.7 MB (7691963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe9def5514cd9d26a91fd2848ca8ccef93236357c553fa60749f6309c1261be`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 370.5 KB (370476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf82e8a85189dd61246961802a3219751ab02f9b92a3755ef3eb45b1b608124`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 76.5 KB (76457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea7a511cde7ab19b6c8c13a3104d26d906bafd53cfee5e88eae75a3dac682b3`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca232b7d67c004ef410857c2ad98e635e8b41a0ac70a9deab0df53e6141be5de`  
		Last Modified: Tue, 21 Oct 2025 01:48:37 GMT  
		Size: 102.9 MB (102909925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2793c07e3ab6dd864fb7a688529f2ef627985c093b210584eafeea68f364e7a8`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3048ecef6353baae24e41d8de29c13c59296369b1e103d6a986d490b842397`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48cee154d685e327ddd7bad956862ba206742ef75b5aec21d946ce6a8587975`  
		Last Modified: Tue, 21 Oct 2025 01:48:29 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca24e1babe582be5164dbd25c401ed28a4904c97fd0e2eb04f2d30570f2f5c7`  
		Last Modified: Tue, 21 Oct 2025 01:48:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:2c8d58a5941ac9d372f991cacaa49d032f531c1dd5b1c97160bda0e0d727214e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3d2baecf0f9afd2bfaec01e0e477c22b8483821e77f88d1944f19292e160bc`

```dockerfile
```

-	Layers:
	-	`sha256:790cd11e186c2131cd2960c7883cab09fcd58074d7c1b8e083020d5b4ff36554`  
		Last Modified: Tue, 21 Oct 2025 10:33:27 GMT  
		Size: 4.1 MB (4141545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:502c465cbc0da92ff698c3693bc39af66e02138a84928e980945f6c7a0647f47`  
		Last Modified: Tue, 21 Oct 2025 10:33:28 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; s390x

```console
$ docker pull couchdb@sha256:02479c6a4b2c4e6eca165713de67c207e241d567d57eaee320af13d77cb95178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136536082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd77fa046e15f3286118b9d03c93caba58eab06cab3359e7bffdf5f5381ebbd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:17:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:17:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 03:17:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:17:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:28 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 04 Nov 2025 03:17:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 03:17:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:17:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:17:53 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 03:17:53 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 03:17:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ebf53fbc3e3d769a60213c6f4b514ac2a0bfef8d2cc98e421e7189ae613338`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7269136448c34c9267e49af25de0c0ee12a6b28019ce9018f963e546288181e5`  
		Last Modified: Tue, 04 Nov 2025 03:19:42 GMT  
		Size: 7.4 MB (7398114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d914dba9eba91885244c28bee6394a9e0abe6ffcb48d68e5a1955ad1bc21219e`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 372.1 KB (372121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6479c330dc7ea8c7bce7182bc9a7eb611c9491484db645a0e4f3f8e7885788fa`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 76.5 KB (76504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c9155aaae72bca21eb141f5ceacd8d28175c0985d9c4823eb67270e62e31d0`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d96ce10d80f81ecb337ff8afc320cec37dfef0cfad120722aa5df713cd31b7b`  
		Last Modified: Tue, 04 Nov 2025 03:19:59 GMT  
		Size: 101.8 MB (101799366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d9137a48a3c453b956a74b128304288bb1fe8b51dcdb2e9396cee3dc3233ce`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da03f19834c4a079266ac7ca7329d31cf7c81545e1c5caa3be7cea4f813bb09`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822f5be2eadf1536e38b496d2b445ea78542173cf650f24fcb0f59d736e4d867`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abac009acac406aef7713c56e997035b1e7581d0611f072f5e5ef0b7214f709`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:5e3d895f98791d4a799522295fb9419b5d59219b003bda29d1b184dab93eb6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aa89f113f66ef056d3d82db343578816627d46191613873a70f779aae6c7a8`

```dockerfile
```

-	Layers:
	-	`sha256:58c4e57db59e9a02f99789af35b3850ae4b6bbdb87fc76166045c4cdb7addaf6`  
		Last Modified: Tue, 04 Nov 2025 08:33:25 GMT  
		Size: 4.1 MB (4137448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5135cc5ce835005828aeaa3f499cd8fc9e8d233aba295ba2b8ba8c997f29244e`  
		Last Modified: Tue, 04 Nov 2025 08:33:26 GMT  
		Size: 31.7 KB (31737 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0-nouveau`

```console
$ docker pull couchdb@sha256:326237f0552c116d1340a4abd47f0f7108fb3dbd1dc34d22cbcdbfc493e95a4c
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
$ docker pull couchdb@sha256:7bd253076622dcfcb6390cca1f7e0ef8fe83d3504e6b64619ba3090670eacbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81b0eb4603d1137e4adfdfc2f8785f91a0311569bf4cc7cd673f4079ac8a842`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1639cafcca63de311712b892899c6cc4aed9b5371718452f73380bcd6d15774`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fe5ecf3044eb58f2d7bb999fa2981b736f0433e5d8aafb88a1cf01b3c274ae`  
		Last Modified: Tue, 21 Oct 2025 01:44:15 GMT  
		Size: 7.9 MB (7881771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1706f57bdad1e318fdf510014d94c77ab287f8247cd180e39062e3109065b`  
		Last Modified: Tue, 21 Oct 2025 01:44:25 GMT  
		Size: 77.3 MB (77326889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32856d57f2141400969d53beba7c40d25dad6311f6709c266be89652f44f7cf2`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 424.1 KB (424064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce9b35b25040ddc65ea8f8e44b67cc3700ff2c7d6a1d7a1e9af3292d6d296cc`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 99.5 KB (99487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472adf561563b0ecd0f159f3fa8916f2b8d9757a4d6f1e5c473d706367c41280`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7880d7850c9a69d617f6f008c3ef14c95ad8e3d094439388b97c6551ca9e7051`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 42.4 MB (42436086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b827c26d71cef106323dddc4f16c6d5bea3d454c6c63f5d10dd630b965ce66`  
		Last Modified: Tue, 21 Oct 2025 01:44:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:353d203253063a16bb3ebefcb3e68999a8d5829ea8764433c3284b52347c42f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9e95b2bd113e2f279f39a4dcd398e62ea0a6106ee21cc82003119a5fa95e12`

```dockerfile
```

-	Layers:
	-	`sha256:a9941eaff4817d44a1e322cffe23af5051161dbc6dea017aea5806c3e3937b5c`  
		Last Modified: Tue, 21 Oct 2025 10:33:32 GMT  
		Size: 3.7 MB (3658049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a221761a19ff308c3e9acc58f511ffb2d53322d69e772e24f853ec43e9ae0605`  
		Last Modified: Tue, 21 Oct 2025 10:33:33 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e33829de3bae4d35bb957449de2e0a183c4f0aef75f46dfba71c4da45a6364f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155279417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25262966e44ddd3f261905517a41e46d230b9c0996f3d41602081d90ad5e5a88`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b23ec744cbf628e7915ee0abd034e7b1082b4d9f9f922d47a701c7b39c8fa0`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf943ff90737b14c37e7d4d2a8682196e70ebdf1ca2ca6fe7d852e7c60641c2c`  
		Last Modified: Tue, 21 Oct 2025 01:48:40 GMT  
		Size: 7.7 MB (7692029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1895b3861d497a754f77085690a46cc8ddc49ba295a2a9940469b045c2afce`  
		Last Modified: Tue, 21 Oct 2025 01:48:47 GMT  
		Size: 76.7 MB (76652724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f24b65d8dec75be45ffbae4e68f04f096f2000091d0766eec0e21e0beafa08`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 392.7 KB (392700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d801aaabd0aa70a3ef10379e047ab4cefe8a9dae46c5119341e03d62f7fcb6`  
		Last Modified: Tue, 21 Oct 2025 01:48:40 GMT  
		Size: 99.5 KB (99462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c62e1afce1ee387d8b513aeb417f5d2923b3c8effc353a803236d2997d6dbbc`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd698eb5dda21c64b725fc1f35382a140e35d2a8fcd394d2581666c65a5b4d8`  
		Last Modified: Tue, 21 Oct 2025 01:48:42 GMT  
		Size: 42.3 MB (42338433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a57ac6ba65a5db293fad3d0b56087e40b78f646d98984b94b4c80e6ef53118`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b3bfa3c9b78f805d794ed3b6cef47e55f6e156ae0c1c433975c0b2175ee95880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1faf9bfd155669dd6d67d932b17cee107705c6bf761944d1d9b886c24dddf5d2`

```dockerfile
```

-	Layers:
	-	`sha256:a86901657a28f2106c4989414d4464b32b17948db61b1fc52565b28bcc88c496`  
		Last Modified: Tue, 21 Oct 2025 10:33:37 GMT  
		Size: 3.7 MB (3656725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270b30851a2520992933292b5593e150437a79030176d467eb46b7b015c8032d`  
		Last Modified: Tue, 21 Oct 2025 10:33:38 GMT  
		Size: 24.7 KB (24745 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:e4c1cf464286a900ce86d7096170b79c191b0074671bbe641daeb58da6f1ac72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150084594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6dc22a341d88212c87b94678a78c8dbf8254d5dce3e2650d1438777fd86356c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:18:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:18:35 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 03:18:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:18:57 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:57 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:19:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 03:19:10 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 03:19:10 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 03:19:10 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 03:19:10 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7536539bf1ad715cf2dd300635c28f289b63af1cbb92522e91502eef246923`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526e0a76fba7a4a90e9f82e82a2d36b1fb986318a85518bfc9635401a95de3e9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 7.4 MB (7398078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce039d7896ebedadc57a51103ebe71649e42dcf66503771ad322910999b1c820`  
		Last Modified: Tue, 04 Nov 2025 03:19:46 GMT  
		Size: 73.1 MB (73142672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a2015e06dd327a6fa19c3c6249a4fce7b4de27b48d0ffe99bd89193cdc50d`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 394.4 KB (394429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2edba20a7c1a1e969e4475b2647e6299aa0a17f5c863767efe6b0eba76bd8b9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 99.6 KB (99633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758223be14bf6c71052fd32d6b25ffd5166b527a06b436acc6588a71754d8256`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a42ee912410feb134c1beae3caa7a5819b26a2805c5f5788a2f1c752a05596`  
		Last Modified: Tue, 04 Nov 2025 03:19:45 GMT  
		Size: 42.2 MB (42163353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28b2decc0bdb622a25486a906d92d47c9957614b0b2ddb085d111ec24b66527`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:11dfbbe0f26655b6dfe5283f838c837702a2801997b244b3a58e3a1ec15d5fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6db580cd46bc75bb51312e6ea0a2dfb655c8e7fe65b7510b23417a1d0c73e9`

```dockerfile
```

-	Layers:
	-	`sha256:1d791db3ab66f5870c8b313ea2a48f5fdf410625cdd00d14b2c3fe7fd8f612da`  
		Last Modified: Tue, 04 Nov 2025 08:33:32 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:908d204e4b43581a218031a0ded371c1bfa2b0e497370e7987e87a5c61463cfd`  
		Last Modified: Tue, 04 Nov 2025 08:33:32 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:ded0c7e661fb6166a03cb2ca4e4ea39acdae71cee1dff08f02e33741fdf39252
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
$ docker pull couchdb@sha256:876cd6d773a737ca0fc40328c5f37d4bb166e0c294740afdec975b0cbc6746e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139836220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8e506c0a7103186f40d3e17de63ff8f2b4b095b84ea07a34c40574db5f9562`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccba59d2d6fdd94f0e833f72f9af63d983c13867d5709d39e3c4c0fc2bfde94`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c547ab29dff3557e48ff250fcb5439e278dcb01d6a6353dbad99e93f6640be4`  
		Last Modified: Tue, 21 Oct 2025 01:44:20 GMT  
		Size: 7.9 MB (7881732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3475fb060a9f828c18e9be99a9aa32ca7f363043e5dc8a4642034b505f1095`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 401.7 KB (401742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaeebfbfe10d7e4da2bfc8472cc80dbce169528ed3a8f35b3fc668fbda315ae`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 76.5 KB (76509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53824741571091d49c151a857e49c95557191fe08b72dcd9917bb6b693879aa8`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31083cc8fd15ba245ed066467da47ef227799bfef57e40ba50ad280b3b6d593`  
		Last Modified: Tue, 21 Oct 2025 01:44:25 GMT  
		Size: 103.2 MB (103242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f0e59b90b6e849cbef734a33902ca29916db915cde791bb2ba771e5c71f45f`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57908fd9df4cf52afe6063f421b7dd3079536f41c7495d1eebb46350ebc71c8f`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd229623b464a1fe4db4d48a05b4218457c35ea0aa5bea66e747920acbd92bf`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6cead4fb824a4bc01338859cacddb34d7e8b122e13509e9257d20f4872a565`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:ef78f0c06664901feceb2a4d47ab071a73c2ad7425efc6fc3ae091afab8e5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8af3ff4909a0bdaded74a5f6e59820f19b936c87fc71391862743fb969ab86`

```dockerfile
```

-	Layers:
	-	`sha256:e62e7da30aa7fd3905490a13fcd27ff0ea34037de9b466275bbff9d866b96f35`  
		Last Modified: Tue, 21 Oct 2025 10:33:22 GMT  
		Size: 4.1 MB (4141252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d24f8fb2005db7b0ec4f339c8bfd54568f4afcfcf14d35e060c445a048d318b`  
		Last Modified: Tue, 21 Oct 2025 10:33:23 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:167ee1978e782e3b93c9059c62224a7a901ca5355b48aa4ae2fd551f15ee320a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139156442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23ab11c3b8d5d3c4387a717994e6c9c6eade8dd5868ed58071fb0921ea94f63`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cbe78858b6df80e5e84dfbd9ddc674e346422db5d3e50dfb2fabb65d2be22d`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a631903dc8129c4263fa27259d60017e4de5862a6d1935712efebc8a5e0ab53`  
		Last Modified: Tue, 21 Oct 2025 01:48:29 GMT  
		Size: 7.7 MB (7691963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe9def5514cd9d26a91fd2848ca8ccef93236357c553fa60749f6309c1261be`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 370.5 KB (370476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf82e8a85189dd61246961802a3219751ab02f9b92a3755ef3eb45b1b608124`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 76.5 KB (76457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea7a511cde7ab19b6c8c13a3104d26d906bafd53cfee5e88eae75a3dac682b3`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca232b7d67c004ef410857c2ad98e635e8b41a0ac70a9deab0df53e6141be5de`  
		Last Modified: Tue, 21 Oct 2025 01:48:37 GMT  
		Size: 102.9 MB (102909925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2793c07e3ab6dd864fb7a688529f2ef627985c093b210584eafeea68f364e7a8`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3048ecef6353baae24e41d8de29c13c59296369b1e103d6a986d490b842397`  
		Last Modified: Tue, 21 Oct 2025 01:48:28 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48cee154d685e327ddd7bad956862ba206742ef75b5aec21d946ce6a8587975`  
		Last Modified: Tue, 21 Oct 2025 01:48:29 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca24e1babe582be5164dbd25c401ed28a4904c97fd0e2eb04f2d30570f2f5c7`  
		Last Modified: Tue, 21 Oct 2025 01:48:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:2c8d58a5941ac9d372f991cacaa49d032f531c1dd5b1c97160bda0e0d727214e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3d2baecf0f9afd2bfaec01e0e477c22b8483821e77f88d1944f19292e160bc`

```dockerfile
```

-	Layers:
	-	`sha256:790cd11e186c2131cd2960c7883cab09fcd58074d7c1b8e083020d5b4ff36554`  
		Last Modified: Tue, 21 Oct 2025 10:33:27 GMT  
		Size: 4.1 MB (4141545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:502c465cbc0da92ff698c3693bc39af66e02138a84928e980945f6c7a0647f47`  
		Last Modified: Tue, 21 Oct 2025 10:33:28 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:02479c6a4b2c4e6eca165713de67c207e241d567d57eaee320af13d77cb95178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136536082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd77fa046e15f3286118b9d03c93caba58eab06cab3359e7bffdf5f5381ebbd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:17:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:17:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 03:17:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:17:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:17:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:28 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 04 Nov 2025 03:17:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 03:17:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 03:17:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:17:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:17:53 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 03:17:53 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 03:17:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ebf53fbc3e3d769a60213c6f4b514ac2a0bfef8d2cc98e421e7189ae613338`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7269136448c34c9267e49af25de0c0ee12a6b28019ce9018f963e546288181e5`  
		Last Modified: Tue, 04 Nov 2025 03:19:42 GMT  
		Size: 7.4 MB (7398114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d914dba9eba91885244c28bee6394a9e0abe6ffcb48d68e5a1955ad1bc21219e`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 372.1 KB (372121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6479c330dc7ea8c7bce7182bc9a7eb611c9491484db645a0e4f3f8e7885788fa`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 76.5 KB (76504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c9155aaae72bca21eb141f5ceacd8d28175c0985d9c4823eb67270e62e31d0`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d96ce10d80f81ecb337ff8afc320cec37dfef0cfad120722aa5df713cd31b7b`  
		Last Modified: Tue, 04 Nov 2025 03:19:59 GMT  
		Size: 101.8 MB (101799366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d9137a48a3c453b956a74b128304288bb1fe8b51dcdb2e9396cee3dc3233ce`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da03f19834c4a079266ac7ca7329d31cf7c81545e1c5caa3be7cea4f813bb09`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822f5be2eadf1536e38b496d2b445ea78542173cf650f24fcb0f59d736e4d867`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abac009acac406aef7713c56e997035b1e7581d0611f072f5e5ef0b7214f709`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:5e3d895f98791d4a799522295fb9419b5d59219b003bda29d1b184dab93eb6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aa89f113f66ef056d3d82db343578816627d46191613873a70f779aae6c7a8`

```dockerfile
```

-	Layers:
	-	`sha256:58c4e57db59e9a02f99789af35b3850ae4b6bbdb87fc76166045c4cdb7addaf6`  
		Last Modified: Tue, 04 Nov 2025 08:33:25 GMT  
		Size: 4.1 MB (4137448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5135cc5ce835005828aeaa3f499cd8fc9e8d233aba295ba2b8ba8c997f29244e`  
		Last Modified: Tue, 04 Nov 2025 08:33:26 GMT  
		Size: 31.7 KB (31737 bytes)  
		MIME: application/vnd.in-toto+json
