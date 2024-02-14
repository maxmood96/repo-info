<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.2`](#couchdb312)
-	[`couchdb:3.2`](#couchdb32)
-	[`couchdb:3.2.3`](#couchdb323)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.3`](#couchdb333)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:c386bdae58d2c18e58581d9f9ec2eddce416adfdd80194f4f2a19f915fc168a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:80383de74598b295e382544e13a53574226d05e3b8f6293bf56f27f00940fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84169041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e309f7c1828f7087e95cf0ba19507a4aeb02f7a884f620ab16c0dc9461776b61`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:232125261662ceeb0126b96defe05092c121fecd55c99db5f76a03ab0c87d07e in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:789bca57d694bdff72d9fcb5bdc3f4684b63dee11402ed28245ae1c578d62ba3`  
		Last Modified: Tue, 13 Feb 2024 00:43:30 GMT  
		Size: 27.2 MB (27188190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b91f61f6301a3dec96508b2c97786e6f5f0221dc62a231d7316bcfe19957ad`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e80f4954bc9432fc6237e3be6e8a331bfd1b13a6b61800448576c40ccd224e`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 6.7 MB (6703566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122336ace0d79dce4d064680ffabce183a4c8c235e7e6346793cf0d3a6c4b400`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 1.0 MB (1046479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beafd30c1a1026c0c414fc2590ac27d58dcc39e6e1275274e22eedf4c79824ca`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 80.3 KB (80343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35cce46b847671d9b45e66ba1b59d3f2920f4edce1af98755f368912317ea04`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feec791ad121e40adb3a59c351541070d7cf03a64a769c045a484dfa8a657946`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 49.1 MB (49143540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957fb429ea1153c66d0457d7d04e089fe794aecfce225be2821b07e8d819e32f`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92692d14e642732ac1689b0040df870af19b16dc235e76f0ec7d1d87fff51fc2`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f04efcf37f2520a6963fc68822980973daa2e88843825b34ef6421ddd64d1`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6915c5098de94f2a090712fd944ad6b77e6540bf6adb78234fa51506bc43fc88`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2` - unknown; unknown

```console
$ docker pull couchdb@sha256:1bbf09eb5beff904b1ff1c4be6e52f171b638f012eff2fb479a23aefd9f1bbcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f473cac918935ae1aedf5b9eb875e41c192e2ecccd3a34d6a6f394e3928e993`

```dockerfile
```

-	Layers:
	-	`sha256:f34fd1af00b3d6cbc831ce1bc89dc79aa7dda3b23e8bad8a1bc83dfda62d3e97`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 3.5 MB (3517463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e80ecd9d59ec42815b78c137040582373947384d2371eef2ceee6396a604897`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 31.6 KB (31582 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:20ebde39990217b75eceef4f4f2a025fd99c4bbfaaa62c9c3bfa86480a1c62e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72615194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c4b87688dd73e2b2c4efc1ce9ec9b3f24c09ea3f6a4c20b341de26d7a50407`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:56f9fb4bf0b803f4553b7fe668c34676467e662e3ab02af10e815a93ebbde1d6 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e4e871d0a0087a92c664052d6406ee23eeb537f0b5f01894052aa0363fed45e3`  
		Last Modified: Tue, 13 Feb 2024 00:46:17 GMT  
		Size: 26.0 MB (25969810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdad9df7925d4242857f5b590381153abf4d2ca2cd81b1d01971fe48de48fa6`  
		Last Modified: Tue, 13 Feb 2024 16:12:24 GMT  
		Size: 3.4 KB (3350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c58d9a95c9feb7f3d04acfa4bcfbc6bb9d344ebb777515d4c92221332a09f`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 6.6 MB (6576631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199a3e8d4f8e2d476d5239461093c029e1325e526470c62f67d823ed7b3bd1c`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 951.3 KB (951345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0993f87b339c934abe2dc11bc2642d2a36cac08078ab169e469729699efc6786`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 80.2 KB (80229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b22fb64303a8514572fb7c7924167c071da82793253beffa274d4b9db938`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b562bef1604ee4740e981a1bac54e745bab7537790c128c85a23f683a944fbd0`  
		Last Modified: Tue, 13 Feb 2024 16:13:02 GMT  
		Size: 39.0 MB (39030230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc741761f6ea70e69675128d0b257b92b851c3af66dd8707686f3cead66caf6c`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1386b3a358ce6ae6935d7e8c849bea154d4dc6f0fcb79f826353394875a96e`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 764.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb728336efa718b035c24791438d39e60fe4a7586ce16b4e842caf73d061ee3a`  
		Last Modified: Tue, 13 Feb 2024 16:13:01 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1296c4254ff98b54d05ccd433cc7342fd28ab41b1c038e1b5f84ce26916038be`  
		Last Modified: Tue, 13 Feb 2024 16:13:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2` - unknown; unknown

```console
$ docker pull couchdb@sha256:7944b256b6b24fca5ba3ba83877dca123afd51603ecfc3d5adfc8b894b3e73fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2941978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f8a1380da3718d81af57d8398d011fd5244296bcc881bb326efd70c610c40e`

```dockerfile
```

-	Layers:
	-	`sha256:be970db93b945e9b5a939149c92bcdd4a8dbaa1305f3509f5d9ff039b6febbac`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 2.9 MB (2910563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d11827eff039a235001179c6e54035fc8f9fa95cc7134c28b90e843cd575c486`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 31.4 KB (31415 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:c386bdae58d2c18e58581d9f9ec2eddce416adfdd80194f4f2a19f915fc168a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:80383de74598b295e382544e13a53574226d05e3b8f6293bf56f27f00940fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84169041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e309f7c1828f7087e95cf0ba19507a4aeb02f7a884f620ab16c0dc9461776b61`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:232125261662ceeb0126b96defe05092c121fecd55c99db5f76a03ab0c87d07e in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:789bca57d694bdff72d9fcb5bdc3f4684b63dee11402ed28245ae1c578d62ba3`  
		Last Modified: Tue, 13 Feb 2024 00:43:30 GMT  
		Size: 27.2 MB (27188190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b91f61f6301a3dec96508b2c97786e6f5f0221dc62a231d7316bcfe19957ad`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e80f4954bc9432fc6237e3be6e8a331bfd1b13a6b61800448576c40ccd224e`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 6.7 MB (6703566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122336ace0d79dce4d064680ffabce183a4c8c235e7e6346793cf0d3a6c4b400`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 1.0 MB (1046479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beafd30c1a1026c0c414fc2590ac27d58dcc39e6e1275274e22eedf4c79824ca`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 80.3 KB (80343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35cce46b847671d9b45e66ba1b59d3f2920f4edce1af98755f368912317ea04`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feec791ad121e40adb3a59c351541070d7cf03a64a769c045a484dfa8a657946`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 49.1 MB (49143540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957fb429ea1153c66d0457d7d04e089fe794aecfce225be2821b07e8d819e32f`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92692d14e642732ac1689b0040df870af19b16dc235e76f0ec7d1d87fff51fc2`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f04efcf37f2520a6963fc68822980973daa2e88843825b34ef6421ddd64d1`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6915c5098de94f2a090712fd944ad6b77e6540bf6adb78234fa51506bc43fc88`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:1bbf09eb5beff904b1ff1c4be6e52f171b638f012eff2fb479a23aefd9f1bbcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f473cac918935ae1aedf5b9eb875e41c192e2ecccd3a34d6a6f394e3928e993`

```dockerfile
```

-	Layers:
	-	`sha256:f34fd1af00b3d6cbc831ce1bc89dc79aa7dda3b23e8bad8a1bc83dfda62d3e97`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 3.5 MB (3517463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e80ecd9d59ec42815b78c137040582373947384d2371eef2ceee6396a604897`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 31.6 KB (31582 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:20ebde39990217b75eceef4f4f2a025fd99c4bbfaaa62c9c3bfa86480a1c62e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72615194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c4b87688dd73e2b2c4efc1ce9ec9b3f24c09ea3f6a4c20b341de26d7a50407`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:56f9fb4bf0b803f4553b7fe668c34676467e662e3ab02af10e815a93ebbde1d6 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e4e871d0a0087a92c664052d6406ee23eeb537f0b5f01894052aa0363fed45e3`  
		Last Modified: Tue, 13 Feb 2024 00:46:17 GMT  
		Size: 26.0 MB (25969810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdad9df7925d4242857f5b590381153abf4d2ca2cd81b1d01971fe48de48fa6`  
		Last Modified: Tue, 13 Feb 2024 16:12:24 GMT  
		Size: 3.4 KB (3350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c58d9a95c9feb7f3d04acfa4bcfbc6bb9d344ebb777515d4c92221332a09f`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 6.6 MB (6576631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199a3e8d4f8e2d476d5239461093c029e1325e526470c62f67d823ed7b3bd1c`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 951.3 KB (951345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0993f87b339c934abe2dc11bc2642d2a36cac08078ab169e469729699efc6786`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 80.2 KB (80229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b22fb64303a8514572fb7c7924167c071da82793253beffa274d4b9db938`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b562bef1604ee4740e981a1bac54e745bab7537790c128c85a23f683a944fbd0`  
		Last Modified: Tue, 13 Feb 2024 16:13:02 GMT  
		Size: 39.0 MB (39030230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc741761f6ea70e69675128d0b257b92b851c3af66dd8707686f3cead66caf6c`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1386b3a358ce6ae6935d7e8c849bea154d4dc6f0fcb79f826353394875a96e`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 764.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb728336efa718b035c24791438d39e60fe4a7586ce16b4e842caf73d061ee3a`  
		Last Modified: Tue, 13 Feb 2024 16:13:01 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1296c4254ff98b54d05ccd433cc7342fd28ab41b1c038e1b5f84ce26916038be`  
		Last Modified: Tue, 13 Feb 2024 16:13:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:7944b256b6b24fca5ba3ba83877dca123afd51603ecfc3d5adfc8b894b3e73fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2941978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f8a1380da3718d81af57d8398d011fd5244296bcc881bb326efd70c610c40e`

```dockerfile
```

-	Layers:
	-	`sha256:be970db93b945e9b5a939149c92bcdd4a8dbaa1305f3509f5d9ff039b6febbac`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 2.9 MB (2910563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d11827eff039a235001179c6e54035fc8f9fa95cc7134c28b90e843cd575c486`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 31.4 KB (31415 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:c386bdae58d2c18e58581d9f9ec2eddce416adfdd80194f4f2a19f915fc168a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:80383de74598b295e382544e13a53574226d05e3b8f6293bf56f27f00940fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84169041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e309f7c1828f7087e95cf0ba19507a4aeb02f7a884f620ab16c0dc9461776b61`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:232125261662ceeb0126b96defe05092c121fecd55c99db5f76a03ab0c87d07e in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:789bca57d694bdff72d9fcb5bdc3f4684b63dee11402ed28245ae1c578d62ba3`  
		Last Modified: Tue, 13 Feb 2024 00:43:30 GMT  
		Size: 27.2 MB (27188190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b91f61f6301a3dec96508b2c97786e6f5f0221dc62a231d7316bcfe19957ad`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e80f4954bc9432fc6237e3be6e8a331bfd1b13a6b61800448576c40ccd224e`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 6.7 MB (6703566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122336ace0d79dce4d064680ffabce183a4c8c235e7e6346793cf0d3a6c4b400`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 1.0 MB (1046479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beafd30c1a1026c0c414fc2590ac27d58dcc39e6e1275274e22eedf4c79824ca`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 80.3 KB (80343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35cce46b847671d9b45e66ba1b59d3f2920f4edce1af98755f368912317ea04`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feec791ad121e40adb3a59c351541070d7cf03a64a769c045a484dfa8a657946`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 49.1 MB (49143540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957fb429ea1153c66d0457d7d04e089fe794aecfce225be2821b07e8d819e32f`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92692d14e642732ac1689b0040df870af19b16dc235e76f0ec7d1d87fff51fc2`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f04efcf37f2520a6963fc68822980973daa2e88843825b34ef6421ddd64d1`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6915c5098de94f2a090712fd944ad6b77e6540bf6adb78234fa51506bc43fc88`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:1bbf09eb5beff904b1ff1c4be6e52f171b638f012eff2fb479a23aefd9f1bbcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f473cac918935ae1aedf5b9eb875e41c192e2ecccd3a34d6a6f394e3928e993`

```dockerfile
```

-	Layers:
	-	`sha256:f34fd1af00b3d6cbc831ce1bc89dc79aa7dda3b23e8bad8a1bc83dfda62d3e97`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 3.5 MB (3517463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e80ecd9d59ec42815b78c137040582373947384d2371eef2ceee6396a604897`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 31.6 KB (31582 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:20ebde39990217b75eceef4f4f2a025fd99c4bbfaaa62c9c3bfa86480a1c62e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72615194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c4b87688dd73e2b2c4efc1ce9ec9b3f24c09ea3f6a4c20b341de26d7a50407`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:56f9fb4bf0b803f4553b7fe668c34676467e662e3ab02af10e815a93ebbde1d6 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e4e871d0a0087a92c664052d6406ee23eeb537f0b5f01894052aa0363fed45e3`  
		Last Modified: Tue, 13 Feb 2024 00:46:17 GMT  
		Size: 26.0 MB (25969810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdad9df7925d4242857f5b590381153abf4d2ca2cd81b1d01971fe48de48fa6`  
		Last Modified: Tue, 13 Feb 2024 16:12:24 GMT  
		Size: 3.4 KB (3350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c58d9a95c9feb7f3d04acfa4bcfbc6bb9d344ebb777515d4c92221332a09f`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 6.6 MB (6576631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199a3e8d4f8e2d476d5239461093c029e1325e526470c62f67d823ed7b3bd1c`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 951.3 KB (951345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0993f87b339c934abe2dc11bc2642d2a36cac08078ab169e469729699efc6786`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 80.2 KB (80229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b22fb64303a8514572fb7c7924167c071da82793253beffa274d4b9db938`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b562bef1604ee4740e981a1bac54e745bab7537790c128c85a23f683a944fbd0`  
		Last Modified: Tue, 13 Feb 2024 16:13:02 GMT  
		Size: 39.0 MB (39030230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc741761f6ea70e69675128d0b257b92b851c3af66dd8707686f3cead66caf6c`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1386b3a358ce6ae6935d7e8c849bea154d4dc6f0fcb79f826353394875a96e`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 764.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb728336efa718b035c24791438d39e60fe4a7586ce16b4e842caf73d061ee3a`  
		Last Modified: Tue, 13 Feb 2024 16:13:01 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1296c4254ff98b54d05ccd433cc7342fd28ab41b1c038e1b5f84ce26916038be`  
		Last Modified: Tue, 13 Feb 2024 16:13:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:7944b256b6b24fca5ba3ba83877dca123afd51603ecfc3d5adfc8b894b3e73fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2941978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f8a1380da3718d81af57d8398d011fd5244296bcc881bb326efd70c610c40e`

```dockerfile
```

-	Layers:
	-	`sha256:be970db93b945e9b5a939149c92bcdd4a8dbaa1305f3509f5d9ff039b6febbac`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 2.9 MB (2910563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d11827eff039a235001179c6e54035fc8f9fa95cc7134c28b90e843cd575c486`  
		Last Modified: Tue, 13 Feb 2024 16:13:00 GMT  
		Size: 31.4 KB (31415 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3`

```console
$ docker pull couchdb@sha256:9c1aa8993e59f5ac9469d7faee2cb3ef8033198cecb38c9b322f06f185ec889f
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

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:405419c4ecce18030dbd1dd7fe692e349f83a0d68df71b6d40238c0c0dd45c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89844973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3731fb1117f02a201e062576679a4d18a995cd23501c55013b528a2d549ee631`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a1605c575ce96487ffac541cf15846a8ea40db5a3ea5145e408c89b649b1b`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096352bc9320e7991dd9c0362807fb9a4d4597d01fce5fd6d3ba34c3bc92e6e1`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 5.2 MB (5223271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201c40b734425007bbe328cb186eb7b070adef02d02e0f334b7abf1c9769368f`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 394.3 KB (394334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e71ec88dde6821c3682b9f75ed25a997d664d50485223b87ab26b148fba8fdf`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 77.9 KB (77896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1569272dcfe8e19f61c84f94b9d94e9fbbf0ac368aff718c06b7649e0e9dbe0`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94053229a35c71f854d02cbb43092581e8b6cee7ef948f9b514acf1b9115c3b7`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 52.7 MB (52719476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5574179220fd2064c4c86791f51e71502c5eed795327da1c0271e0a3bdc15025`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb73ba5435db91092fe3694f3825701ad5cca6534fc4b12df96ef10ffe0ccf6`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c99e0ab115184508946862ec52009d68ac8c02cf34c37517727a457f107cb0`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635a5b575816fae0daa6b83453f0895a506e418b8b1ac15a657483365d4d3805`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d16ee81b162d4ab76c3d63eb24c759731f33182a74a0b8c127b6667ea743186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e5d61dcb6a671d4bfabf370e7f61ed671efdcc236747afce88263a09acbbce`

```dockerfile
```

-	Layers:
	-	`sha256:c6b83df7389ff8ad90817f27160f302f285cd712a01ec06c1a98bf8d1eb0de4c`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.4 MB (3387604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a6b40e9e902cc7e5708edcd2d223152519a7f697689ac57e6e6da3af916bcf3`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:be58c321d541acbfba2407766f082aad1b17fe3cb1f75b66857df3820a37f9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88285694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf0a24f3fa20b6a722498e59590b05bf305a9d9a9bd51e8d3be3c261792fc38`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0940302ddebdd72907f35204ddeddcb6558daeee5ce25fb0afbb0da16b37e5`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 3.3 KB (3349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b9aa8fa41dfc2df60b83b3b1f1444d68f461b1f3ae22341d4db85fd29c15e`  
		Last Modified: Tue, 13 Feb 2024 16:11:29 GMT  
		Size: 5.2 MB (5208005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b962b4e0eed624af7532f7645aec700105f9ed359b10d512009a9a6d0e5c8a`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 350.6 KB (350556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a829119ff8ca03d54dad1443ccd298ef7b93400e9b7ee29a339e1ce9967ab26`  
		Last Modified: Tue, 13 Feb 2024 16:11:29 GMT  
		Size: 77.8 KB (77806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558bcee564f63db46043facbb54b346b6ed9505006c33593e16a8f8287750109`  
		Last Modified: Tue, 13 Feb 2024 16:11:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989c693e21a9350e8fbed8b25fe07f6217db05b01694cba4e545a07e25d21e4`  
		Last Modified: Tue, 13 Feb 2024 16:11:32 GMT  
		Size: 52.6 MB (52570655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b84218f6806da7031ec2a5bd7271f97cb0178363b61866365e798feb76ef03`  
		Last Modified: Tue, 13 Feb 2024 16:11:30 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b2f659e714bf8958e21d377d4e0febfc5d426cea5051f56643c04b42ca5300`  
		Last Modified: Tue, 13 Feb 2024 16:11:31 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0255363cc93a9bba0ccc91c6d8fde9bc75637e711c317acf3af4fd4660b99209`  
		Last Modified: Tue, 13 Feb 2024 16:11:31 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22d2c4dc7e05522e1bb562e1c57f6c92261ddb4ab346983f78d690a5db85de1`  
		Last Modified: Tue, 13 Feb 2024 16:11:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ca8cd534d477e4382552b28525fc14c63cb17f15fb08b1b2a3338fbc1b695f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a3babe97e93717c146c4e033b6d8e01a07f9150b9c9ac05d4a7f4f96616e0b`

```dockerfile
```

-	Layers:
	-	`sha256:bca78453a61085c58a5e85c8b2085196ab19402b73ec4aa6ef2cdb8cbbd3699a`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 3.4 MB (3387952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7309e8f5e00fe6cfa26b782f31377a6cfe765ef733dad70eb91bae64a9b6dae0`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 31.7 KB (31736 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:c1fbc90ce6c6285acb4e2ea97cc84afc88251a12865f16a80e2aa46f4073a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95572094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77c9d8ebe5078875298615ed60f92b25c0e2f4e4182928e6b58f48881fdd091`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd2decc7ca44765775f9204873d3a70d223c86a597beffedfcd0af9b86fc373`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7691c771db0bad7870bf6a7b22232c7859dc4e73f7c5122b011eb60b232bef11`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 6.0 MB (6042459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67483bb19ff936b43254f9537a83209c4468d4e53ea9beea4db1e9b072b0fd8`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 446.6 KB (446646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a444fe3b60fbccb3983211f34944e5d014bd9f3ccd30b91bef6d889d2f6107`  
		Last Modified: Tue, 13 Feb 2024 14:25:58 GMT  
		Size: 77.8 KB (77843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa3f322a490e38f54465d6ecf24efd6041defcb5d7bf178de94895b422acfae`  
		Last Modified: Tue, 13 Feb 2024 14:25:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c6418e543cf94119e1f963401bb36d971f97925652362210cb6e30883d9f29`  
		Last Modified: Tue, 13 Feb 2024 14:26:01 GMT  
		Size: 53.7 MB (53699770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4d604efb6515e36030d14633b45b706ddfada1c81acc4060835987753e69d1`  
		Last Modified: Tue, 13 Feb 2024 14:25:59 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3927ab77e0b79fa0703f03e5e67d1e4925aab9e8f1d45b6013d2e874222576c7`  
		Last Modified: Tue, 13 Feb 2024 14:25:59 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a1621f507fd42d1e3b7cbd889a14febad45dc21f67c2479da2d2ea34b839`  
		Last Modified: Tue, 13 Feb 2024 14:26:00 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2af2dd0d2b54a385b48a12e1e3e71401527dcf87df8cb698fbf2155136b010`  
		Last Modified: Tue, 13 Feb 2024 14:26:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:60ed8360c04948be666533b5dddd6eb6e0b85ae5cca5d6ed69891a33b3a0e6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cf1627d5074b66fd09f79727ca95ce438c2b0c026f997e193eefa06a07c644`

```dockerfile
```

-	Layers:
	-	`sha256:34ca4f0a81f44992a6461bb8056e617c8e62348a2963072d776fc3e9bb19f66f`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 3.4 MB (3392244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36be88654b7bf23459b2879ac24f4b7562929959fcc4e1bb3c411b3327c7c957`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:0c5d89f5772671a96429ab0b00813f7dfecc4bcfefa3c5ffa2a90c543523103c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86585513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cef7411e39c6afb68b76b7d0995d26a5fc33cd016d6a095732009fb57e44113`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:08d247ddc5feae7a34870daaf7096c41de9c1bb9fc04bc305db02fe94b34d2e5 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2ac5fae051fa0d97737a12baa9ac705d62ae16e9a4ae39eed54e3f977616ce05`  
		Last Modified: Tue, 13 Feb 2024 01:30:53 GMT  
		Size: 29.7 MB (29660168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc9b0bbdfd6ba4352c739605365822347eae8d52964e2f1c6741c452d3847f0`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 3.4 KB (3350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8375d21a9dd303034178938990c3035033b7d062891bd3d3922aa1c037b0d69c`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 5.1 MB (5109302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d714f5dba7812eccb54c737dd3233c617cc6130881c964ffc771da64031f048d`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 357.5 KB (357469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6a308b7d28da1b0043bc3a0935a4b70c7f7d88c77ebb93120ed5441e512513`  
		Last Modified: Wed, 14 Feb 2024 06:12:09 GMT  
		Size: 77.9 KB (77872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04abad4b314678c1516487988bef13730245dc525d6777be254fdf35370a91b1`  
		Last Modified: Wed, 14 Feb 2024 06:12:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaedcfab5138ae27a972d57d3640a424ec97ca91c693156579f64d8c0c35c05`  
		Last Modified: Wed, 14 Feb 2024 06:12:11 GMT  
		Size: 51.4 MB (51373105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cd17a8071c52fec1e576e9a3387aebb243849f819402f7166ece51ad3fd1ad`  
		Last Modified: Wed, 14 Feb 2024 06:12:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40190cc214617580fc53273e3b929a281519bfafbcd397746602a0789051334`  
		Last Modified: Wed, 14 Feb 2024 06:12:10 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877bdfc68d8814c2576f84f9d40837bbd78ba248b4ef2da874a495629a88673d`  
		Last Modified: Wed, 14 Feb 2024 06:12:10 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c18a68169d44453b6bb30605eb870ba0ae97314dd2a1d0ee16e85940d5781`  
		Last Modified: Wed, 14 Feb 2024 06:12:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:0f20a056ecb71f70e2cad76df5b4129a53a96bff1fc98a574b4444544973cb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3418902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f925f8a024059e252540ff854329333c455500ac2ccb24e7c09762c8b4b8d67`

```dockerfile
```

-	Layers:
	-	`sha256:43606355dff6c2a9017ea9447b929880affa32f0269a613b29ab057ce100234c`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 3.4 MB (3387176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6337bbaf4ed4dc42fc09a8e164a25736ef503899473bdcda2615b5418e1208`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:82e17be0ec02503343a40b59f06d17e336b376a5c790bd4b2db0c1528ed27ccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:9f69b5df73d2604f1d431f57208b3b67471789ee19a630b9972440cbc97bda28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79644338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51254b5c6c1b53c748f02200ba0e7163322103535f6a2d467f0f38abaa1e0e4e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:232125261662ceeb0126b96defe05092c121fecd55c99db5f76a03ab0c87d07e in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:789bca57d694bdff72d9fcb5bdc3f4684b63dee11402ed28245ae1c578d62ba3`  
		Last Modified: Tue, 13 Feb 2024 00:43:30 GMT  
		Size: 27.2 MB (27188190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97ec5d84acae0304a42acf996678d3c4a4fcb79b43970bc84ec18743cc10cf`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c41aabfbc67c092464dc4193329dea62f71d05945fa0e4adc51ce65a07ae30e`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 6.7 MB (6703460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf929ddecd5b7bfe0cffb700785ee7a5f8e38daf3d03e9acc4cf4ad15627850`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 1.0 MB (1046480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9cef46cda574dc34449cdb5216a6d7e81f0062d6b7d2944de3d3b5e2f4fba9`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 80.3 KB (80328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647da4cbf72e81dcf4dcf5eb93602ebdb7fd85b7a8ebf99281fe255ba988f889`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c88c7a5e0d59787670de268289a6243924047cba8813a341c95a0326614d5c`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 44.6 MB (44618957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a927d8356d38f01f1db9ba1cb63668f1904ef09784c3dc38af28556ca2786a`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c29e8f6ac645e28519fd5b54619a2a925a59a739826863e4d248d4ab85fe3df`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f82947b5bcae2f0c5167ec5118e71f1a392e11f29864424858ceb148948968`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b22b9f6df8c6452b0e65728d1fb7b7492ab449e629444d0b078a5bd45ba605`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:81c8adc09251e6729758cb7268857a2b0516f4a83a69f0d2a7e30031e727c3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb60206eec6d85384d3698637c81943aba6e0b6768c18e0b54a592c6ec538d98`

```dockerfile
```

-	Layers:
	-	`sha256:d0d0c3de3547019209ab4124c409351bb5551f28cdb9a626e376132095bb0b71`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 3.0 MB (2955438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ca969026a576f8a4781405b8fbe8b9cd8dd181e31a7305b6483a8afa53fd650`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 31.3 KB (31282 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:64dbfd467825a89f59271334fa4cffcd199cd0223ca69cb6f3e14a61b13cec16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74709676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94369559702833a8081f50db1e5956dc024701674c5b0dcd52fb89e6071aa98`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:56f9fb4bf0b803f4553b7fe668c34676467e662e3ab02af10e815a93ebbde1d6 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e4e871d0a0087a92c664052d6406ee23eeb537f0b5f01894052aa0363fed45e3`  
		Last Modified: Tue, 13 Feb 2024 00:46:17 GMT  
		Size: 26.0 MB (25969810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdad9df7925d4242857f5b590381153abf4d2ca2cd81b1d01971fe48de48fa6`  
		Last Modified: Tue, 13 Feb 2024 16:12:24 GMT  
		Size: 3.4 KB (3350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c58d9a95c9feb7f3d04acfa4bcfbc6bb9d344ebb777515d4c92221332a09f`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 6.6 MB (6576631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199a3e8d4f8e2d476d5239461093c029e1325e526470c62f67d823ed7b3bd1c`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 951.3 KB (951345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0993f87b339c934abe2dc11bc2642d2a36cac08078ab169e469729699efc6786`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 80.2 KB (80229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717ed9eb935fbdba20e28e922056ecc24305d06b0db2b3873d16656e993eeb4b`  
		Last Modified: Tue, 13 Feb 2024 16:12:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101c1c07d29c86a37bd631483e1b9da9facfec170ee749f66594afcf776c994d`  
		Last Modified: Tue, 13 Feb 2024 16:12:27 GMT  
		Size: 41.1 MB (41124727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e67df88010ed801cbd13d0f86f6d0350ba8d5f216680d7a8f1c6ad6d7b116`  
		Last Modified: Tue, 13 Feb 2024 16:12:27 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4405470bc8683570ef96811f4de9ea949fde4cc9120f34a0dd07d0c52f158152`  
		Last Modified: Tue, 13 Feb 2024 16:12:27 GMT  
		Size: 763.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fb8fdb9c0f0bbafa1786c13740bea6b4e506523c99cc13f54b0c471a1d54a6`  
		Last Modified: Tue, 13 Feb 2024 16:12:27 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a6948454db737d8c9485272835970db6770ece51599311dde47551aef2ba38`  
		Last Modified: Tue, 13 Feb 2024 16:12:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:7d31f781e1a9df89282f6c649d07289390a3948a991d17436a8ad7885435b3b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8c9d162b375163e3297787a478ee686e865926090218dd7e4832f99563eeb9`

```dockerfile
```

-	Layers:
	-	`sha256:4184471012d568f7a960229c66916de9820f2c41afdb2304da9d77fe5c959d7f`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 3.0 MB (2961717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c49e5696003e20e016fb5a879dfb822eabbdb4e4dd4b58fafc5c34fd9e1b99`  
		Last Modified: Tue, 13 Feb 2024 16:12:24 GMT  
		Size: 31.3 KB (31280 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:82e17be0ec02503343a40b59f06d17e336b376a5c790bd4b2db0c1528ed27ccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:9f69b5df73d2604f1d431f57208b3b67471789ee19a630b9972440cbc97bda28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79644338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51254b5c6c1b53c748f02200ba0e7163322103535f6a2d467f0f38abaa1e0e4e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:232125261662ceeb0126b96defe05092c121fecd55c99db5f76a03ab0c87d07e in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:789bca57d694bdff72d9fcb5bdc3f4684b63dee11402ed28245ae1c578d62ba3`  
		Last Modified: Tue, 13 Feb 2024 00:43:30 GMT  
		Size: 27.2 MB (27188190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97ec5d84acae0304a42acf996678d3c4a4fcb79b43970bc84ec18743cc10cf`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c41aabfbc67c092464dc4193329dea62f71d05945fa0e4adc51ce65a07ae30e`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 6.7 MB (6703460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf929ddecd5b7bfe0cffb700785ee7a5f8e38daf3d03e9acc4cf4ad15627850`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 1.0 MB (1046480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9cef46cda574dc34449cdb5216a6d7e81f0062d6b7d2944de3d3b5e2f4fba9`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 80.3 KB (80328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647da4cbf72e81dcf4dcf5eb93602ebdb7fd85b7a8ebf99281fe255ba988f889`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c88c7a5e0d59787670de268289a6243924047cba8813a341c95a0326614d5c`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 44.6 MB (44618957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a927d8356d38f01f1db9ba1cb63668f1904ef09784c3dc38af28556ca2786a`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c29e8f6ac645e28519fd5b54619a2a925a59a739826863e4d248d4ab85fe3df`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f82947b5bcae2f0c5167ec5118e71f1a392e11f29864424858ceb148948968`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b22b9f6df8c6452b0e65728d1fb7b7492ab449e629444d0b078a5bd45ba605`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:81c8adc09251e6729758cb7268857a2b0516f4a83a69f0d2a7e30031e727c3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb60206eec6d85384d3698637c81943aba6e0b6768c18e0b54a592c6ec538d98`

```dockerfile
```

-	Layers:
	-	`sha256:d0d0c3de3547019209ab4124c409351bb5551f28cdb9a626e376132095bb0b71`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 3.0 MB (2955438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ca969026a576f8a4781405b8fbe8b9cd8dd181e31a7305b6483a8afa53fd650`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 31.3 KB (31282 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:64dbfd467825a89f59271334fa4cffcd199cd0223ca69cb6f3e14a61b13cec16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74709676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94369559702833a8081f50db1e5956dc024701674c5b0dcd52fb89e6071aa98`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:56f9fb4bf0b803f4553b7fe668c34676467e662e3ab02af10e815a93ebbde1d6 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e4e871d0a0087a92c664052d6406ee23eeb537f0b5f01894052aa0363fed45e3`  
		Last Modified: Tue, 13 Feb 2024 00:46:17 GMT  
		Size: 26.0 MB (25969810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdad9df7925d4242857f5b590381153abf4d2ca2cd81b1d01971fe48de48fa6`  
		Last Modified: Tue, 13 Feb 2024 16:12:24 GMT  
		Size: 3.4 KB (3350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c58d9a95c9feb7f3d04acfa4bcfbc6bb9d344ebb777515d4c92221332a09f`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 6.6 MB (6576631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199a3e8d4f8e2d476d5239461093c029e1325e526470c62f67d823ed7b3bd1c`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 951.3 KB (951345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0993f87b339c934abe2dc11bc2642d2a36cac08078ab169e469729699efc6786`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 80.2 KB (80229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717ed9eb935fbdba20e28e922056ecc24305d06b0db2b3873d16656e993eeb4b`  
		Last Modified: Tue, 13 Feb 2024 16:12:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101c1c07d29c86a37bd631483e1b9da9facfec170ee749f66594afcf776c994d`  
		Last Modified: Tue, 13 Feb 2024 16:12:27 GMT  
		Size: 41.1 MB (41124727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e67df88010ed801cbd13d0f86f6d0350ba8d5f216680d7a8f1c6ad6d7b116`  
		Last Modified: Tue, 13 Feb 2024 16:12:27 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4405470bc8683570ef96811f4de9ea949fde4cc9120f34a0dd07d0c52f158152`  
		Last Modified: Tue, 13 Feb 2024 16:12:27 GMT  
		Size: 763.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fb8fdb9c0f0bbafa1786c13740bea6b4e506523c99cc13f54b0c471a1d54a6`  
		Last Modified: Tue, 13 Feb 2024 16:12:27 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a6948454db737d8c9485272835970db6770ece51599311dde47551aef2ba38`  
		Last Modified: Tue, 13 Feb 2024 16:12:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:7d31f781e1a9df89282f6c649d07289390a3948a991d17436a8ad7885435b3b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8c9d162b375163e3297787a478ee686e865926090218dd7e4832f99563eeb9`

```dockerfile
```

-	Layers:
	-	`sha256:4184471012d568f7a960229c66916de9820f2c41afdb2304da9d77fe5c959d7f`  
		Last Modified: Tue, 13 Feb 2024 16:12:25 GMT  
		Size: 3.0 MB (2961717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c49e5696003e20e016fb5a879dfb822eabbdb4e4dd4b58fafc5c34fd9e1b99`  
		Last Modified: Tue, 13 Feb 2024 16:12:24 GMT  
		Size: 31.3 KB (31280 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:fc1df1a39fae773fbc631b50d97c8e54d66104937249318873e771678809e1ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:90eeaec3df9eb34c1ac3c3c5724f7aeb574ef92009570ff40bd39a736745f2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89311917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134b7edbd2b5200e1bac946bff625afd2b2ea987812b975cba5e5b686cdd7fdd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.2.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f76c15a31a40060f8e4542a337f59f0ef4e8b3d7c3c40bda47abb59d710083`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23baca0b107851d7b070618ef32ef9bda74227d6112c596fc62d58b236a383b8`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 5.2 MB (5223296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1798ebb20ea24aa2573ddb7a74e727668e07dd7625172670d6366c2d05581b4b`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 394.3 KB (394349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54685bc16356835ffc719166617150f43813594040700e7c96079a14630497fe`  
		Last Modified: Tue, 13 Feb 2024 01:53:29 GMT  
		Size: 77.9 KB (77906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f5343e4dcc05c0af6f62d36ad542542ed15e427fa88433acd985f8400a1f66`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492ae7e95dcd1bed263d36e5c981ecccf90c9857799eeb7f8f03bd44d4136553`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 52.2 MB (52186623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb78c43a96e4348395151d7315afe55398ece6c43d06c9b545d49ca5ee322893`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e5a829cb377336afd6d6eedf70239cb09e574e1799b11e862f561e45794513`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 997.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbe3c5549e391824078ff4c7680f80fa3c4ccd101b4a733ac4c4ff893248e7`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ff2b0ba295cfdcbe09f5008c94b0784c86ef7a8e674a99dc488ca6a0101b6f`  
		Last Modified: Tue, 13 Feb 2024 01:53:32 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:e8e6a443d790ec8d6690189a7c54eae4469d128d36249c2c8f0cd46fc63141b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3393754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832739f144a7e6e954456534adb63d9a77ed1e4be24305be7b4a13c525d9b8e5`

```dockerfile
```

-	Layers:
	-	`sha256:38c194de38d6e456e143a9bf1a5b9cd32b44febf1f5854f04bd13a5b69b8aa17`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 3.4 MB (3362621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daf8adb41724ea77b6a802a8d084d50753fd7f3f537753b2cf7713e7e99f9f11`  
		Last Modified: Tue, 13 Feb 2024 01:53:29 GMT  
		Size: 31.1 KB (31133 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.2.3`

```console
$ docker pull couchdb@sha256:fc1df1a39fae773fbc631b50d97c8e54d66104937249318873e771678809e1ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchdb:3.2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:90eeaec3df9eb34c1ac3c3c5724f7aeb574ef92009570ff40bd39a736745f2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89311917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134b7edbd2b5200e1bac946bff625afd2b2ea987812b975cba5e5b686cdd7fdd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.2.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f76c15a31a40060f8e4542a337f59f0ef4e8b3d7c3c40bda47abb59d710083`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23baca0b107851d7b070618ef32ef9bda74227d6112c596fc62d58b236a383b8`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 5.2 MB (5223296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1798ebb20ea24aa2573ddb7a74e727668e07dd7625172670d6366c2d05581b4b`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 394.3 KB (394349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54685bc16356835ffc719166617150f43813594040700e7c96079a14630497fe`  
		Last Modified: Tue, 13 Feb 2024 01:53:29 GMT  
		Size: 77.9 KB (77906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f5343e4dcc05c0af6f62d36ad542542ed15e427fa88433acd985f8400a1f66`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492ae7e95dcd1bed263d36e5c981ecccf90c9857799eeb7f8f03bd44d4136553`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 52.2 MB (52186623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb78c43a96e4348395151d7315afe55398ece6c43d06c9b545d49ca5ee322893`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e5a829cb377336afd6d6eedf70239cb09e574e1799b11e862f561e45794513`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 997.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbe3c5549e391824078ff4c7680f80fa3c4ccd101b4a733ac4c4ff893248e7`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ff2b0ba295cfdcbe09f5008c94b0784c86ef7a8e674a99dc488ca6a0101b6f`  
		Last Modified: Tue, 13 Feb 2024 01:53:32 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e8e6a443d790ec8d6690189a7c54eae4469d128d36249c2c8f0cd46fc63141b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3393754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832739f144a7e6e954456534adb63d9a77ed1e4be24305be7b4a13c525d9b8e5`

```dockerfile
```

-	Layers:
	-	`sha256:38c194de38d6e456e143a9bf1a5b9cd32b44febf1f5854f04bd13a5b69b8aa17`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 3.4 MB (3362621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daf8adb41724ea77b6a802a8d084d50753fd7f3f537753b2cf7713e7e99f9f11`  
		Last Modified: Tue, 13 Feb 2024 01:53:29 GMT  
		Size: 31.1 KB (31133 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:9c1aa8993e59f5ac9469d7faee2cb3ef8033198cecb38c9b322f06f185ec889f
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
$ docker pull couchdb@sha256:405419c4ecce18030dbd1dd7fe692e349f83a0d68df71b6d40238c0c0dd45c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89844973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3731fb1117f02a201e062576679a4d18a995cd23501c55013b528a2d549ee631`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a1605c575ce96487ffac541cf15846a8ea40db5a3ea5145e408c89b649b1b`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096352bc9320e7991dd9c0362807fb9a4d4597d01fce5fd6d3ba34c3bc92e6e1`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 5.2 MB (5223271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201c40b734425007bbe328cb186eb7b070adef02d02e0f334b7abf1c9769368f`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 394.3 KB (394334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e71ec88dde6821c3682b9f75ed25a997d664d50485223b87ab26b148fba8fdf`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 77.9 KB (77896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1569272dcfe8e19f61c84f94b9d94e9fbbf0ac368aff718c06b7649e0e9dbe0`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94053229a35c71f854d02cbb43092581e8b6cee7ef948f9b514acf1b9115c3b7`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 52.7 MB (52719476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5574179220fd2064c4c86791f51e71502c5eed795327da1c0271e0a3bdc15025`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb73ba5435db91092fe3694f3825701ad5cca6534fc4b12df96ef10ffe0ccf6`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c99e0ab115184508946862ec52009d68ac8c02cf34c37517727a457f107cb0`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635a5b575816fae0daa6b83453f0895a506e418b8b1ac15a657483365d4d3805`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d16ee81b162d4ab76c3d63eb24c759731f33182a74a0b8c127b6667ea743186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e5d61dcb6a671d4bfabf370e7f61ed671efdcc236747afce88263a09acbbce`

```dockerfile
```

-	Layers:
	-	`sha256:c6b83df7389ff8ad90817f27160f302f285cd712a01ec06c1a98bf8d1eb0de4c`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.4 MB (3387604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a6b40e9e902cc7e5708edcd2d223152519a7f697689ac57e6e6da3af916bcf3`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:be58c321d541acbfba2407766f082aad1b17fe3cb1f75b66857df3820a37f9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88285694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf0a24f3fa20b6a722498e59590b05bf305a9d9a9bd51e8d3be3c261792fc38`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0940302ddebdd72907f35204ddeddcb6558daeee5ce25fb0afbb0da16b37e5`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 3.3 KB (3349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b9aa8fa41dfc2df60b83b3b1f1444d68f461b1f3ae22341d4db85fd29c15e`  
		Last Modified: Tue, 13 Feb 2024 16:11:29 GMT  
		Size: 5.2 MB (5208005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b962b4e0eed624af7532f7645aec700105f9ed359b10d512009a9a6d0e5c8a`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 350.6 KB (350556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a829119ff8ca03d54dad1443ccd298ef7b93400e9b7ee29a339e1ce9967ab26`  
		Last Modified: Tue, 13 Feb 2024 16:11:29 GMT  
		Size: 77.8 KB (77806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558bcee564f63db46043facbb54b346b6ed9505006c33593e16a8f8287750109`  
		Last Modified: Tue, 13 Feb 2024 16:11:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989c693e21a9350e8fbed8b25fe07f6217db05b01694cba4e545a07e25d21e4`  
		Last Modified: Tue, 13 Feb 2024 16:11:32 GMT  
		Size: 52.6 MB (52570655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b84218f6806da7031ec2a5bd7271f97cb0178363b61866365e798feb76ef03`  
		Last Modified: Tue, 13 Feb 2024 16:11:30 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b2f659e714bf8958e21d377d4e0febfc5d426cea5051f56643c04b42ca5300`  
		Last Modified: Tue, 13 Feb 2024 16:11:31 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0255363cc93a9bba0ccc91c6d8fde9bc75637e711c317acf3af4fd4660b99209`  
		Last Modified: Tue, 13 Feb 2024 16:11:31 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22d2c4dc7e05522e1bb562e1c57f6c92261ddb4ab346983f78d690a5db85de1`  
		Last Modified: Tue, 13 Feb 2024 16:11:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ca8cd534d477e4382552b28525fc14c63cb17f15fb08b1b2a3338fbc1b695f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a3babe97e93717c146c4e033b6d8e01a07f9150b9c9ac05d4a7f4f96616e0b`

```dockerfile
```

-	Layers:
	-	`sha256:bca78453a61085c58a5e85c8b2085196ab19402b73ec4aa6ef2cdb8cbbd3699a`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 3.4 MB (3387952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7309e8f5e00fe6cfa26b782f31377a6cfe765ef733dad70eb91bae64a9b6dae0`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 31.7 KB (31736 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:c1fbc90ce6c6285acb4e2ea97cc84afc88251a12865f16a80e2aa46f4073a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95572094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77c9d8ebe5078875298615ed60f92b25c0e2f4e4182928e6b58f48881fdd091`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd2decc7ca44765775f9204873d3a70d223c86a597beffedfcd0af9b86fc373`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7691c771db0bad7870bf6a7b22232c7859dc4e73f7c5122b011eb60b232bef11`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 6.0 MB (6042459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67483bb19ff936b43254f9537a83209c4468d4e53ea9beea4db1e9b072b0fd8`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 446.6 KB (446646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a444fe3b60fbccb3983211f34944e5d014bd9f3ccd30b91bef6d889d2f6107`  
		Last Modified: Tue, 13 Feb 2024 14:25:58 GMT  
		Size: 77.8 KB (77843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa3f322a490e38f54465d6ecf24efd6041defcb5d7bf178de94895b422acfae`  
		Last Modified: Tue, 13 Feb 2024 14:25:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c6418e543cf94119e1f963401bb36d971f97925652362210cb6e30883d9f29`  
		Last Modified: Tue, 13 Feb 2024 14:26:01 GMT  
		Size: 53.7 MB (53699770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4d604efb6515e36030d14633b45b706ddfada1c81acc4060835987753e69d1`  
		Last Modified: Tue, 13 Feb 2024 14:25:59 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3927ab77e0b79fa0703f03e5e67d1e4925aab9e8f1d45b6013d2e874222576c7`  
		Last Modified: Tue, 13 Feb 2024 14:25:59 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a1621f507fd42d1e3b7cbd889a14febad45dc21f67c2479da2d2ea34b839`  
		Last Modified: Tue, 13 Feb 2024 14:26:00 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2af2dd0d2b54a385b48a12e1e3e71401527dcf87df8cb698fbf2155136b010`  
		Last Modified: Tue, 13 Feb 2024 14:26:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:60ed8360c04948be666533b5dddd6eb6e0b85ae5cca5d6ed69891a33b3a0e6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cf1627d5074b66fd09f79727ca95ce438c2b0c026f997e193eefa06a07c644`

```dockerfile
```

-	Layers:
	-	`sha256:34ca4f0a81f44992a6461bb8056e617c8e62348a2963072d776fc3e9bb19f66f`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 3.4 MB (3392244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36be88654b7bf23459b2879ac24f4b7562929959fcc4e1bb3c411b3327c7c957`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:0c5d89f5772671a96429ab0b00813f7dfecc4bcfefa3c5ffa2a90c543523103c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86585513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cef7411e39c6afb68b76b7d0995d26a5fc33cd016d6a095732009fb57e44113`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:08d247ddc5feae7a34870daaf7096c41de9c1bb9fc04bc305db02fe94b34d2e5 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2ac5fae051fa0d97737a12baa9ac705d62ae16e9a4ae39eed54e3f977616ce05`  
		Last Modified: Tue, 13 Feb 2024 01:30:53 GMT  
		Size: 29.7 MB (29660168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc9b0bbdfd6ba4352c739605365822347eae8d52964e2f1c6741c452d3847f0`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 3.4 KB (3350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8375d21a9dd303034178938990c3035033b7d062891bd3d3922aa1c037b0d69c`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 5.1 MB (5109302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d714f5dba7812eccb54c737dd3233c617cc6130881c964ffc771da64031f048d`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 357.5 KB (357469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6a308b7d28da1b0043bc3a0935a4b70c7f7d88c77ebb93120ed5441e512513`  
		Last Modified: Wed, 14 Feb 2024 06:12:09 GMT  
		Size: 77.9 KB (77872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04abad4b314678c1516487988bef13730245dc525d6777be254fdf35370a91b1`  
		Last Modified: Wed, 14 Feb 2024 06:12:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaedcfab5138ae27a972d57d3640a424ec97ca91c693156579f64d8c0c35c05`  
		Last Modified: Wed, 14 Feb 2024 06:12:11 GMT  
		Size: 51.4 MB (51373105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cd17a8071c52fec1e576e9a3387aebb243849f819402f7166ece51ad3fd1ad`  
		Last Modified: Wed, 14 Feb 2024 06:12:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40190cc214617580fc53273e3b929a281519bfafbcd397746602a0789051334`  
		Last Modified: Wed, 14 Feb 2024 06:12:10 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877bdfc68d8814c2576f84f9d40837bbd78ba248b4ef2da874a495629a88673d`  
		Last Modified: Wed, 14 Feb 2024 06:12:10 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c18a68169d44453b6bb30605eb870ba0ae97314dd2a1d0ee16e85940d5781`  
		Last Modified: Wed, 14 Feb 2024 06:12:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:0f20a056ecb71f70e2cad76df5b4129a53a96bff1fc98a574b4444544973cb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3418902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f925f8a024059e252540ff854329333c455500ac2ccb24e7c09762c8b4b8d67`

```dockerfile
```

-	Layers:
	-	`sha256:43606355dff6c2a9017ea9447b929880affa32f0269a613b29ab057ce100234c`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 3.4 MB (3387176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6337bbaf4ed4dc42fc09a8e164a25736ef503899473bdcda2615b5418e1208`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:9c1aa8993e59f5ac9469d7faee2cb3ef8033198cecb38c9b322f06f185ec889f
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
$ docker pull couchdb@sha256:405419c4ecce18030dbd1dd7fe692e349f83a0d68df71b6d40238c0c0dd45c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89844973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3731fb1117f02a201e062576679a4d18a995cd23501c55013b528a2d549ee631`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a1605c575ce96487ffac541cf15846a8ea40db5a3ea5145e408c89b649b1b`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096352bc9320e7991dd9c0362807fb9a4d4597d01fce5fd6d3ba34c3bc92e6e1`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 5.2 MB (5223271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201c40b734425007bbe328cb186eb7b070adef02d02e0f334b7abf1c9769368f`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 394.3 KB (394334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e71ec88dde6821c3682b9f75ed25a997d664d50485223b87ab26b148fba8fdf`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 77.9 KB (77896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1569272dcfe8e19f61c84f94b9d94e9fbbf0ac368aff718c06b7649e0e9dbe0`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94053229a35c71f854d02cbb43092581e8b6cee7ef948f9b514acf1b9115c3b7`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 52.7 MB (52719476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5574179220fd2064c4c86791f51e71502c5eed795327da1c0271e0a3bdc15025`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb73ba5435db91092fe3694f3825701ad5cca6534fc4b12df96ef10ffe0ccf6`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c99e0ab115184508946862ec52009d68ac8c02cf34c37517727a457f107cb0`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635a5b575816fae0daa6b83453f0895a506e418b8b1ac15a657483365d4d3805`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d16ee81b162d4ab76c3d63eb24c759731f33182a74a0b8c127b6667ea743186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e5d61dcb6a671d4bfabf370e7f61ed671efdcc236747afce88263a09acbbce`

```dockerfile
```

-	Layers:
	-	`sha256:c6b83df7389ff8ad90817f27160f302f285cd712a01ec06c1a98bf8d1eb0de4c`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.4 MB (3387604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a6b40e9e902cc7e5708edcd2d223152519a7f697689ac57e6e6da3af916bcf3`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:be58c321d541acbfba2407766f082aad1b17fe3cb1f75b66857df3820a37f9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88285694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf0a24f3fa20b6a722498e59590b05bf305a9d9a9bd51e8d3be3c261792fc38`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0940302ddebdd72907f35204ddeddcb6558daeee5ce25fb0afbb0da16b37e5`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 3.3 KB (3349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b9aa8fa41dfc2df60b83b3b1f1444d68f461b1f3ae22341d4db85fd29c15e`  
		Last Modified: Tue, 13 Feb 2024 16:11:29 GMT  
		Size: 5.2 MB (5208005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b962b4e0eed624af7532f7645aec700105f9ed359b10d512009a9a6d0e5c8a`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 350.6 KB (350556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a829119ff8ca03d54dad1443ccd298ef7b93400e9b7ee29a339e1ce9967ab26`  
		Last Modified: Tue, 13 Feb 2024 16:11:29 GMT  
		Size: 77.8 KB (77806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558bcee564f63db46043facbb54b346b6ed9505006c33593e16a8f8287750109`  
		Last Modified: Tue, 13 Feb 2024 16:11:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989c693e21a9350e8fbed8b25fe07f6217db05b01694cba4e545a07e25d21e4`  
		Last Modified: Tue, 13 Feb 2024 16:11:32 GMT  
		Size: 52.6 MB (52570655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b84218f6806da7031ec2a5bd7271f97cb0178363b61866365e798feb76ef03`  
		Last Modified: Tue, 13 Feb 2024 16:11:30 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b2f659e714bf8958e21d377d4e0febfc5d426cea5051f56643c04b42ca5300`  
		Last Modified: Tue, 13 Feb 2024 16:11:31 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0255363cc93a9bba0ccc91c6d8fde9bc75637e711c317acf3af4fd4660b99209`  
		Last Modified: Tue, 13 Feb 2024 16:11:31 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22d2c4dc7e05522e1bb562e1c57f6c92261ddb4ab346983f78d690a5db85de1`  
		Last Modified: Tue, 13 Feb 2024 16:11:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ca8cd534d477e4382552b28525fc14c63cb17f15fb08b1b2a3338fbc1b695f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a3babe97e93717c146c4e033b6d8e01a07f9150b9c9ac05d4a7f4f96616e0b`

```dockerfile
```

-	Layers:
	-	`sha256:bca78453a61085c58a5e85c8b2085196ab19402b73ec4aa6ef2cdb8cbbd3699a`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 3.4 MB (3387952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7309e8f5e00fe6cfa26b782f31377a6cfe765ef733dad70eb91bae64a9b6dae0`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 31.7 KB (31736 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:c1fbc90ce6c6285acb4e2ea97cc84afc88251a12865f16a80e2aa46f4073a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95572094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77c9d8ebe5078875298615ed60f92b25c0e2f4e4182928e6b58f48881fdd091`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd2decc7ca44765775f9204873d3a70d223c86a597beffedfcd0af9b86fc373`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7691c771db0bad7870bf6a7b22232c7859dc4e73f7c5122b011eb60b232bef11`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 6.0 MB (6042459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67483bb19ff936b43254f9537a83209c4468d4e53ea9beea4db1e9b072b0fd8`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 446.6 KB (446646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a444fe3b60fbccb3983211f34944e5d014bd9f3ccd30b91bef6d889d2f6107`  
		Last Modified: Tue, 13 Feb 2024 14:25:58 GMT  
		Size: 77.8 KB (77843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa3f322a490e38f54465d6ecf24efd6041defcb5d7bf178de94895b422acfae`  
		Last Modified: Tue, 13 Feb 2024 14:25:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c6418e543cf94119e1f963401bb36d971f97925652362210cb6e30883d9f29`  
		Last Modified: Tue, 13 Feb 2024 14:26:01 GMT  
		Size: 53.7 MB (53699770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4d604efb6515e36030d14633b45b706ddfada1c81acc4060835987753e69d1`  
		Last Modified: Tue, 13 Feb 2024 14:25:59 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3927ab77e0b79fa0703f03e5e67d1e4925aab9e8f1d45b6013d2e874222576c7`  
		Last Modified: Tue, 13 Feb 2024 14:25:59 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a1621f507fd42d1e3b7cbd889a14febad45dc21f67c2479da2d2ea34b839`  
		Last Modified: Tue, 13 Feb 2024 14:26:00 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2af2dd0d2b54a385b48a12e1e3e71401527dcf87df8cb698fbf2155136b010`  
		Last Modified: Tue, 13 Feb 2024 14:26:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:60ed8360c04948be666533b5dddd6eb6e0b85ae5cca5d6ed69891a33b3a0e6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cf1627d5074b66fd09f79727ca95ce438c2b0c026f997e193eefa06a07c644`

```dockerfile
```

-	Layers:
	-	`sha256:34ca4f0a81f44992a6461bb8056e617c8e62348a2963072d776fc3e9bb19f66f`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 3.4 MB (3392244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36be88654b7bf23459b2879ac24f4b7562929959fcc4e1bb3c411b3327c7c957`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:0c5d89f5772671a96429ab0b00813f7dfecc4bcfefa3c5ffa2a90c543523103c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86585513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cef7411e39c6afb68b76b7d0995d26a5fc33cd016d6a095732009fb57e44113`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:08d247ddc5feae7a34870daaf7096c41de9c1bb9fc04bc305db02fe94b34d2e5 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2ac5fae051fa0d97737a12baa9ac705d62ae16e9a4ae39eed54e3f977616ce05`  
		Last Modified: Tue, 13 Feb 2024 01:30:53 GMT  
		Size: 29.7 MB (29660168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc9b0bbdfd6ba4352c739605365822347eae8d52964e2f1c6741c452d3847f0`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 3.4 KB (3350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8375d21a9dd303034178938990c3035033b7d062891bd3d3922aa1c037b0d69c`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 5.1 MB (5109302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d714f5dba7812eccb54c737dd3233c617cc6130881c964ffc771da64031f048d`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 357.5 KB (357469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6a308b7d28da1b0043bc3a0935a4b70c7f7d88c77ebb93120ed5441e512513`  
		Last Modified: Wed, 14 Feb 2024 06:12:09 GMT  
		Size: 77.9 KB (77872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04abad4b314678c1516487988bef13730245dc525d6777be254fdf35370a91b1`  
		Last Modified: Wed, 14 Feb 2024 06:12:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaedcfab5138ae27a972d57d3640a424ec97ca91c693156579f64d8c0c35c05`  
		Last Modified: Wed, 14 Feb 2024 06:12:11 GMT  
		Size: 51.4 MB (51373105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cd17a8071c52fec1e576e9a3387aebb243849f819402f7166ece51ad3fd1ad`  
		Last Modified: Wed, 14 Feb 2024 06:12:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40190cc214617580fc53273e3b929a281519bfafbcd397746602a0789051334`  
		Last Modified: Wed, 14 Feb 2024 06:12:10 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877bdfc68d8814c2576f84f9d40837bbd78ba248b4ef2da874a495629a88673d`  
		Last Modified: Wed, 14 Feb 2024 06:12:10 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c18a68169d44453b6bb30605eb870ba0ae97314dd2a1d0ee16e85940d5781`  
		Last Modified: Wed, 14 Feb 2024 06:12:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:0f20a056ecb71f70e2cad76df5b4129a53a96bff1fc98a574b4444544973cb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3418902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f925f8a024059e252540ff854329333c455500ac2ccb24e7c09762c8b4b8d67`

```dockerfile
```

-	Layers:
	-	`sha256:43606355dff6c2a9017ea9447b929880affa32f0269a613b29ab057ce100234c`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 3.4 MB (3387176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6337bbaf4ed4dc42fc09a8e164a25736ef503899473bdcda2615b5418e1208`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:9c1aa8993e59f5ac9469d7faee2cb3ef8033198cecb38c9b322f06f185ec889f
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

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:405419c4ecce18030dbd1dd7fe692e349f83a0d68df71b6d40238c0c0dd45c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89844973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3731fb1117f02a201e062576679a4d18a995cd23501c55013b528a2d549ee631`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a1605c575ce96487ffac541cf15846a8ea40db5a3ea5145e408c89b649b1b`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096352bc9320e7991dd9c0362807fb9a4d4597d01fce5fd6d3ba34c3bc92e6e1`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 5.2 MB (5223271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201c40b734425007bbe328cb186eb7b070adef02d02e0f334b7abf1c9769368f`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 394.3 KB (394334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e71ec88dde6821c3682b9f75ed25a997d664d50485223b87ab26b148fba8fdf`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 77.9 KB (77896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1569272dcfe8e19f61c84f94b9d94e9fbbf0ac368aff718c06b7649e0e9dbe0`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94053229a35c71f854d02cbb43092581e8b6cee7ef948f9b514acf1b9115c3b7`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 52.7 MB (52719476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5574179220fd2064c4c86791f51e71502c5eed795327da1c0271e0a3bdc15025`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb73ba5435db91092fe3694f3825701ad5cca6534fc4b12df96ef10ffe0ccf6`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c99e0ab115184508946862ec52009d68ac8c02cf34c37517727a457f107cb0`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635a5b575816fae0daa6b83453f0895a506e418b8b1ac15a657483365d4d3805`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:d16ee81b162d4ab76c3d63eb24c759731f33182a74a0b8c127b6667ea743186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e5d61dcb6a671d4bfabf370e7f61ed671efdcc236747afce88263a09acbbce`

```dockerfile
```

-	Layers:
	-	`sha256:c6b83df7389ff8ad90817f27160f302f285cd712a01ec06c1a98bf8d1eb0de4c`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.4 MB (3387604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a6b40e9e902cc7e5708edcd2d223152519a7f697689ac57e6e6da3af916bcf3`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:be58c321d541acbfba2407766f082aad1b17fe3cb1f75b66857df3820a37f9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88285694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf0a24f3fa20b6a722498e59590b05bf305a9d9a9bd51e8d3be3c261792fc38`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0940302ddebdd72907f35204ddeddcb6558daeee5ce25fb0afbb0da16b37e5`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 3.3 KB (3349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b9aa8fa41dfc2df60b83b3b1f1444d68f461b1f3ae22341d4db85fd29c15e`  
		Last Modified: Tue, 13 Feb 2024 16:11:29 GMT  
		Size: 5.2 MB (5208005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b962b4e0eed624af7532f7645aec700105f9ed359b10d512009a9a6d0e5c8a`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 350.6 KB (350556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a829119ff8ca03d54dad1443ccd298ef7b93400e9b7ee29a339e1ce9967ab26`  
		Last Modified: Tue, 13 Feb 2024 16:11:29 GMT  
		Size: 77.8 KB (77806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558bcee564f63db46043facbb54b346b6ed9505006c33593e16a8f8287750109`  
		Last Modified: Tue, 13 Feb 2024 16:11:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989c693e21a9350e8fbed8b25fe07f6217db05b01694cba4e545a07e25d21e4`  
		Last Modified: Tue, 13 Feb 2024 16:11:32 GMT  
		Size: 52.6 MB (52570655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b84218f6806da7031ec2a5bd7271f97cb0178363b61866365e798feb76ef03`  
		Last Modified: Tue, 13 Feb 2024 16:11:30 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b2f659e714bf8958e21d377d4e0febfc5d426cea5051f56643c04b42ca5300`  
		Last Modified: Tue, 13 Feb 2024 16:11:31 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0255363cc93a9bba0ccc91c6d8fde9bc75637e711c317acf3af4fd4660b99209`  
		Last Modified: Tue, 13 Feb 2024 16:11:31 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22d2c4dc7e05522e1bb562e1c57f6c92261ddb4ab346983f78d690a5db85de1`  
		Last Modified: Tue, 13 Feb 2024 16:11:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:ca8cd534d477e4382552b28525fc14c63cb17f15fb08b1b2a3338fbc1b695f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a3babe97e93717c146c4e033b6d8e01a07f9150b9c9ac05d4a7f4f96616e0b`

```dockerfile
```

-	Layers:
	-	`sha256:bca78453a61085c58a5e85c8b2085196ab19402b73ec4aa6ef2cdb8cbbd3699a`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 3.4 MB (3387952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7309e8f5e00fe6cfa26b782f31377a6cfe765ef733dad70eb91bae64a9b6dae0`  
		Last Modified: Tue, 13 Feb 2024 16:11:28 GMT  
		Size: 31.7 KB (31736 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:c1fbc90ce6c6285acb4e2ea97cc84afc88251a12865f16a80e2aa46f4073a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95572094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77c9d8ebe5078875298615ed60f92b25c0e2f4e4182928e6b58f48881fdd091`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd2decc7ca44765775f9204873d3a70d223c86a597beffedfcd0af9b86fc373`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7691c771db0bad7870bf6a7b22232c7859dc4e73f7c5122b011eb60b232bef11`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 6.0 MB (6042459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67483bb19ff936b43254f9537a83209c4468d4e53ea9beea4db1e9b072b0fd8`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 446.6 KB (446646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a444fe3b60fbccb3983211f34944e5d014bd9f3ccd30b91bef6d889d2f6107`  
		Last Modified: Tue, 13 Feb 2024 14:25:58 GMT  
		Size: 77.8 KB (77843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa3f322a490e38f54465d6ecf24efd6041defcb5d7bf178de94895b422acfae`  
		Last Modified: Tue, 13 Feb 2024 14:25:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c6418e543cf94119e1f963401bb36d971f97925652362210cb6e30883d9f29`  
		Last Modified: Tue, 13 Feb 2024 14:26:01 GMT  
		Size: 53.7 MB (53699770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4d604efb6515e36030d14633b45b706ddfada1c81acc4060835987753e69d1`  
		Last Modified: Tue, 13 Feb 2024 14:25:59 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3927ab77e0b79fa0703f03e5e67d1e4925aab9e8f1d45b6013d2e874222576c7`  
		Last Modified: Tue, 13 Feb 2024 14:25:59 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a1621f507fd42d1e3b7cbd889a14febad45dc21f67c2479da2d2ea34b839`  
		Last Modified: Tue, 13 Feb 2024 14:26:00 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2af2dd0d2b54a385b48a12e1e3e71401527dcf87df8cb698fbf2155136b010`  
		Last Modified: Tue, 13 Feb 2024 14:26:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:60ed8360c04948be666533b5dddd6eb6e0b85ae5cca5d6ed69891a33b3a0e6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cf1627d5074b66fd09f79727ca95ce438c2b0c026f997e193eefa06a07c644`

```dockerfile
```

-	Layers:
	-	`sha256:34ca4f0a81f44992a6461bb8056e617c8e62348a2963072d776fc3e9bb19f66f`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 3.4 MB (3392244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36be88654b7bf23459b2879ac24f4b7562929959fcc4e1bb3c411b3327c7c957`  
		Last Modified: Tue, 13 Feb 2024 14:25:57 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:0c5d89f5772671a96429ab0b00813f7dfecc4bcfefa3c5ffa2a90c543523103c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86585513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cef7411e39c6afb68b76b7d0995d26a5fc33cd016d6a095732009fb57e44113`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:08d247ddc5feae7a34870daaf7096c41de9c1bb9fc04bc305db02fe94b34d2e5 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2ac5fae051fa0d97737a12baa9ac705d62ae16e9a4ae39eed54e3f977616ce05`  
		Last Modified: Tue, 13 Feb 2024 01:30:53 GMT  
		Size: 29.7 MB (29660168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc9b0bbdfd6ba4352c739605365822347eae8d52964e2f1c6741c452d3847f0`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 3.4 KB (3350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8375d21a9dd303034178938990c3035033b7d062891bd3d3922aa1c037b0d69c`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 5.1 MB (5109302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d714f5dba7812eccb54c737dd3233c617cc6130881c964ffc771da64031f048d`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 357.5 KB (357469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6a308b7d28da1b0043bc3a0935a4b70c7f7d88c77ebb93120ed5441e512513`  
		Last Modified: Wed, 14 Feb 2024 06:12:09 GMT  
		Size: 77.9 KB (77872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04abad4b314678c1516487988bef13730245dc525d6777be254fdf35370a91b1`  
		Last Modified: Wed, 14 Feb 2024 06:12:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaedcfab5138ae27a972d57d3640a424ec97ca91c693156579f64d8c0c35c05`  
		Last Modified: Wed, 14 Feb 2024 06:12:11 GMT  
		Size: 51.4 MB (51373105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cd17a8071c52fec1e576e9a3387aebb243849f819402f7166ece51ad3fd1ad`  
		Last Modified: Wed, 14 Feb 2024 06:12:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40190cc214617580fc53273e3b929a281519bfafbcd397746602a0789051334`  
		Last Modified: Wed, 14 Feb 2024 06:12:10 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877bdfc68d8814c2576f84f9d40837bbd78ba248b4ef2da874a495629a88673d`  
		Last Modified: Wed, 14 Feb 2024 06:12:10 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c18a68169d44453b6bb30605eb870ba0ae97314dd2a1d0ee16e85940d5781`  
		Last Modified: Wed, 14 Feb 2024 06:12:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:0f20a056ecb71f70e2cad76df5b4129a53a96bff1fc98a574b4444544973cb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3418902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f925f8a024059e252540ff854329333c455500ac2ccb24e7c09762c8b4b8d67`

```dockerfile
```

-	Layers:
	-	`sha256:43606355dff6c2a9017ea9447b929880affa32f0269a613b29ab057ce100234c`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 3.4 MB (3387176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6337bbaf4ed4dc42fc09a8e164a25736ef503899473bdcda2615b5418e1208`  
		Last Modified: Wed, 14 Feb 2024 06:12:08 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json
