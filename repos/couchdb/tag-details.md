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
$ docker pull couchdb@sha256:469f5bb7a03d071f304dc50c6d9cebd2c6ce4fcd69f01036df74bd5d14d549bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:28ce087cdc4569354b139df8aaee2130435b3a01ff72cffaf7cbb611f9653905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84170463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a062f4075583170d723db8089cd55cec86d38514153b04cb0c9422e810b2e12f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e64f92c07598d7a1e58a8116342198e837ea4ed870cac2c252323c261b270566 in / 
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
	-	`sha256:4a21b857313366ffd622f19e31c4300a81dce92b023b4ff6583ca167179804ac`  
		Last Modified: Tue, 12 Mar 2024 01:26:59 GMT  
		Size: 27.2 MB (27188304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73712c6c51981e2a54cb928784bbb545750dc51680369b3556582daaaaddeaf`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80eb20de900a88337cb9d7847544449483ae0ffbc3c7d38d07840186c19f020`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 6.7 MB (6703482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8685482e56123f6ce8ac3e67d95d2695fa266c304288e03bd9f287721c646348`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 1.0 MB (1046500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042bde60de9252b2a903b58a850fa1fddf386b78c924f9f5f24d92f36d3eef7f`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 80.3 KB (80322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c5eed56c28639d6eae0a4e9b1d2d6f1e08093efb6915532ce5771b2bb25bd8`  
		Last Modified: Tue, 12 Mar 2024 01:55:14 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153a71463bfa0bf3d7425b967594826926739dab5a18e160097c6ccd93fd435c`  
		Last Modified: Tue, 12 Mar 2024 01:55:15 GMT  
		Size: 49.1 MB (49144928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d5af8de32bc53560aaccf85bf395a8c35676e9574719f6d2318ec8c8150ee4`  
		Last Modified: Tue, 12 Mar 2024 01:55:14 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88362620e8cb2ac279da4f60e472fe41c521be7eebc7c3a54dcd56685c29ea68`  
		Last Modified: Tue, 12 Mar 2024 01:55:14 GMT  
		Size: 763.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91479f290183987d8118baff5c76a1ac4f51bc5d677052d27df852243c6ae2d0`  
		Last Modified: Tue, 12 Mar 2024 01:55:15 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b9c921affdfb25ea5a4e4e121c43959bf117008aeb8f61823828a93ca59ff0`  
		Last Modified: Tue, 12 Mar 2024 01:55:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2` - unknown; unknown

```console
$ docker pull couchdb@sha256:68b241c0d1afd373b6bea510db4fad9b282a7e24b54b4888e571266cb1e3c893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec0553f5abe2ba72751a44402599abc8304f66d0a8da1ab4c10e697b5316c73`

```dockerfile
```

-	Layers:
	-	`sha256:e907aea3b3eef8bbf8f9982b2809d703950ff149f48ba6ac014575f7e471ce81`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 4.1 MB (4081929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16986ffca61c219d30a230e8c4d2ea80a6a4e08ab69c5017654578cc96e65ad`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
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
$ docker pull couchdb@sha256:469f5bb7a03d071f304dc50c6d9cebd2c6ce4fcd69f01036df74bd5d14d549bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:28ce087cdc4569354b139df8aaee2130435b3a01ff72cffaf7cbb611f9653905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84170463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a062f4075583170d723db8089cd55cec86d38514153b04cb0c9422e810b2e12f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e64f92c07598d7a1e58a8116342198e837ea4ed870cac2c252323c261b270566 in / 
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
	-	`sha256:4a21b857313366ffd622f19e31c4300a81dce92b023b4ff6583ca167179804ac`  
		Last Modified: Tue, 12 Mar 2024 01:26:59 GMT  
		Size: 27.2 MB (27188304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73712c6c51981e2a54cb928784bbb545750dc51680369b3556582daaaaddeaf`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80eb20de900a88337cb9d7847544449483ae0ffbc3c7d38d07840186c19f020`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 6.7 MB (6703482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8685482e56123f6ce8ac3e67d95d2695fa266c304288e03bd9f287721c646348`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 1.0 MB (1046500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042bde60de9252b2a903b58a850fa1fddf386b78c924f9f5f24d92f36d3eef7f`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 80.3 KB (80322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c5eed56c28639d6eae0a4e9b1d2d6f1e08093efb6915532ce5771b2bb25bd8`  
		Last Modified: Tue, 12 Mar 2024 01:55:14 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153a71463bfa0bf3d7425b967594826926739dab5a18e160097c6ccd93fd435c`  
		Last Modified: Tue, 12 Mar 2024 01:55:15 GMT  
		Size: 49.1 MB (49144928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d5af8de32bc53560aaccf85bf395a8c35676e9574719f6d2318ec8c8150ee4`  
		Last Modified: Tue, 12 Mar 2024 01:55:14 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88362620e8cb2ac279da4f60e472fe41c521be7eebc7c3a54dcd56685c29ea68`  
		Last Modified: Tue, 12 Mar 2024 01:55:14 GMT  
		Size: 763.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91479f290183987d8118baff5c76a1ac4f51bc5d677052d27df852243c6ae2d0`  
		Last Modified: Tue, 12 Mar 2024 01:55:15 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b9c921affdfb25ea5a4e4e121c43959bf117008aeb8f61823828a93ca59ff0`  
		Last Modified: Tue, 12 Mar 2024 01:55:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:68b241c0d1afd373b6bea510db4fad9b282a7e24b54b4888e571266cb1e3c893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec0553f5abe2ba72751a44402599abc8304f66d0a8da1ab4c10e697b5316c73`

```dockerfile
```

-	Layers:
	-	`sha256:e907aea3b3eef8bbf8f9982b2809d703950ff149f48ba6ac014575f7e471ce81`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 4.1 MB (4081929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16986ffca61c219d30a230e8c4d2ea80a6a4e08ab69c5017654578cc96e65ad`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
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
$ docker pull couchdb@sha256:469f5bb7a03d071f304dc50c6d9cebd2c6ce4fcd69f01036df74bd5d14d549bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:28ce087cdc4569354b139df8aaee2130435b3a01ff72cffaf7cbb611f9653905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84170463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a062f4075583170d723db8089cd55cec86d38514153b04cb0c9422e810b2e12f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e64f92c07598d7a1e58a8116342198e837ea4ed870cac2c252323c261b270566 in / 
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
	-	`sha256:4a21b857313366ffd622f19e31c4300a81dce92b023b4ff6583ca167179804ac`  
		Last Modified: Tue, 12 Mar 2024 01:26:59 GMT  
		Size: 27.2 MB (27188304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73712c6c51981e2a54cb928784bbb545750dc51680369b3556582daaaaddeaf`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80eb20de900a88337cb9d7847544449483ae0ffbc3c7d38d07840186c19f020`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 6.7 MB (6703482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8685482e56123f6ce8ac3e67d95d2695fa266c304288e03bd9f287721c646348`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 1.0 MB (1046500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042bde60de9252b2a903b58a850fa1fddf386b78c924f9f5f24d92f36d3eef7f`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 80.3 KB (80322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c5eed56c28639d6eae0a4e9b1d2d6f1e08093efb6915532ce5771b2bb25bd8`  
		Last Modified: Tue, 12 Mar 2024 01:55:14 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153a71463bfa0bf3d7425b967594826926739dab5a18e160097c6ccd93fd435c`  
		Last Modified: Tue, 12 Mar 2024 01:55:15 GMT  
		Size: 49.1 MB (49144928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d5af8de32bc53560aaccf85bf395a8c35676e9574719f6d2318ec8c8150ee4`  
		Last Modified: Tue, 12 Mar 2024 01:55:14 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88362620e8cb2ac279da4f60e472fe41c521be7eebc7c3a54dcd56685c29ea68`  
		Last Modified: Tue, 12 Mar 2024 01:55:14 GMT  
		Size: 763.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91479f290183987d8118baff5c76a1ac4f51bc5d677052d27df852243c6ae2d0`  
		Last Modified: Tue, 12 Mar 2024 01:55:15 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b9c921affdfb25ea5a4e4e121c43959bf117008aeb8f61823828a93ca59ff0`  
		Last Modified: Tue, 12 Mar 2024 01:55:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:68b241c0d1afd373b6bea510db4fad9b282a7e24b54b4888e571266cb1e3c893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec0553f5abe2ba72751a44402599abc8304f66d0a8da1ab4c10e697b5316c73`

```dockerfile
```

-	Layers:
	-	`sha256:e907aea3b3eef8bbf8f9982b2809d703950ff149f48ba6ac014575f7e471ce81`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 4.1 MB (4081929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16986ffca61c219d30a230e8c4d2ea80a6a4e08ab69c5017654578cc96e65ad`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
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
$ docker pull couchdb@sha256:486e8dc7b0f13a3dbd0047d6a445976a0aca4a2437a2c3c00ec397f30341fd2d
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
$ docker pull couchdb@sha256:128bea3044a6b715a9ec0b063db35d81dde409e90069e90e40fbbf798c86e0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89845595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d610ac3edbe74ad8f21e8167fc9f2c75ae02b2051afab93d585431d2f7a85e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
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
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c574efc63818fa0e037c4e0969c9fd3eb6b2cfe79608a16889498e17e2a4ce`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a4663271ce0ca2c19a6b77e95128ce13bcb4d1e6b33fcd5f55624fa4b5f8f2`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 5.2 MB (5223292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03654e97b888420e6f618137e0214d08e328aff08f55c3bd96cd00883cc6cbef`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 394.3 KB (394340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40457217ea148f864b30c5d41a342ecc394fcebfa8c36f6996c1a79175e08346`  
		Last Modified: Tue, 12 Mar 2024 01:55:09 GMT  
		Size: 77.9 KB (77884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773f4cf7eb790ab73b126512fc3ef8881aeda9b4e0bc66af9a8e2ec06e15c570`  
		Last Modified: Tue, 12 Mar 2024 01:55:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6f8ff995d65ec3847915eca070ff454fc1b1f376f145a6198edc7f727bcc50`  
		Last Modified: Tue, 12 Mar 2024 01:55:10 GMT  
		Size: 52.7 MB (52720018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0e1a5e9413519972edff179b1d5ad3915720fb0a3f0bd08386cf3f66b4f8d7`  
		Last Modified: Tue, 12 Mar 2024 01:55:07 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dcc52c9d8d65c573512a8b601660f662ab7144a9d1168fdbc6b9ff223ded43`  
		Last Modified: Tue, 12 Mar 2024 01:55:10 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e7039168554e3c4884e60580d57a737b349ed9b6c845597bb521826a76839c`  
		Last Modified: Tue, 12 Mar 2024 01:55:10 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136a4821a63b048ddb74fc09fee521674fe40967967922128fb124ab1ee66e8`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ef31ea760e4f0a589b1fcbf5ffc58987377d9244a9836b0dc0d7f7b5f88cb508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c96afc8e0d31180d78ab927a74fbe596b68e238713f7516db43cb6f90e65e`

```dockerfile
```

-	Layers:
	-	`sha256:f80e31c2413c820792147acbcd00566d5965fef02e88ac59b85b4b9b69e738c1`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 4.0 MB (3964852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce778357c2a1bbd4801960efd356f2074acb0f560d46cd647a64d15c81b02f5`  
		Last Modified: Tue, 12 Mar 2024 01:55:07 GMT  
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
$ docker pull couchdb@sha256:632aaeec22c6a3df320351a63346a5650252431d1a9ea9d5dda98c6566e83568
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:0c2306d962f0303fe9da15fabcc1dc9a23017d786fcbc1773c49eb686da6dc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79645105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee9abdfaf242343e156dd3273e5068e3349b5a6cf68a538f9049cfa8afa61b8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e64f92c07598d7a1e58a8116342198e837ea4ed870cac2c252323c261b270566 in / 
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
	-	`sha256:4a21b857313366ffd622f19e31c4300a81dce92b023b4ff6583ca167179804ac`  
		Last Modified: Tue, 12 Mar 2024 01:26:59 GMT  
		Size: 27.2 MB (27188304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513161a3dd7328b960f3415cca4c3d199aa5efef1da00892353471072e637043`  
		Last Modified: Tue, 12 Mar 2024 01:55:06 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7ce7636b7f099c346adf73e39ec1ec1938b13fc9f8a28606b8887b8d5ae3f8`  
		Last Modified: Tue, 12 Mar 2024 01:55:06 GMT  
		Size: 6.7 MB (6703506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f40f98ee56c8506405a695ff227dbb790c86d344946088ca1b4403dca012bae`  
		Last Modified: Tue, 12 Mar 2024 01:55:06 GMT  
		Size: 1.0 MB (1046505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082de6b9063a87035e16509fa8e1e7cdedadb3694c18fbef26f1d676f7b8be5d`  
		Last Modified: Tue, 12 Mar 2024 01:55:07 GMT  
		Size: 80.3 KB (80323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34175578b2bb618865d187746a06f15e2945c3a3c48dfca6d3569756f6a98f5`  
		Last Modified: Tue, 12 Mar 2024 01:55:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bc64a90bae2aefe11ebb5c5daf0991201b77589f6665cf5feb2dd481f07e11`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 44.6 MB (44619549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0e1a5e9413519972edff179b1d5ad3915720fb0a3f0bd08386cf3f66b4f8d7`  
		Last Modified: Tue, 12 Mar 2024 01:55:07 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a485bc8fa933d3d5ccb3d4b8bb7532b86539b0cd20d4d8353a84335d4040cd`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721d7d15b9c2ee1e740d6b1b6c9a25db5718bb247947c723223bd20ff30ef02a`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136a4821a63b048ddb74fc09fee521674fe40967967922128fb124ab1ee66e8`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:dd2b838fd939799740f88c9a70f9816d30575b266879274a905ac9e9782a3f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3482186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8d660bec139f4ea49f00b7543cd9766db7ca2fe3c4ad8cf9b3767e189ec7d4`

```dockerfile
```

-	Layers:
	-	`sha256:9b7a415c19c667b83ee066c336e2ccd89e3961122f70f834073cf4d6331bffe3`  
		Last Modified: Tue, 12 Mar 2024 01:55:06 GMT  
		Size: 3.5 MB (3450904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c94de7ba8de7a8b8185e66243844385add7705c7a5738da0a601f1fea7516d8`  
		Last Modified: Tue, 12 Mar 2024 01:55:06 GMT  
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
$ docker pull couchdb@sha256:632aaeec22c6a3df320351a63346a5650252431d1a9ea9d5dda98c6566e83568
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:0c2306d962f0303fe9da15fabcc1dc9a23017d786fcbc1773c49eb686da6dc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79645105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee9abdfaf242343e156dd3273e5068e3349b5a6cf68a538f9049cfa8afa61b8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e64f92c07598d7a1e58a8116342198e837ea4ed870cac2c252323c261b270566 in / 
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
	-	`sha256:4a21b857313366ffd622f19e31c4300a81dce92b023b4ff6583ca167179804ac`  
		Last Modified: Tue, 12 Mar 2024 01:26:59 GMT  
		Size: 27.2 MB (27188304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513161a3dd7328b960f3415cca4c3d199aa5efef1da00892353471072e637043`  
		Last Modified: Tue, 12 Mar 2024 01:55:06 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7ce7636b7f099c346adf73e39ec1ec1938b13fc9f8a28606b8887b8d5ae3f8`  
		Last Modified: Tue, 12 Mar 2024 01:55:06 GMT  
		Size: 6.7 MB (6703506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f40f98ee56c8506405a695ff227dbb790c86d344946088ca1b4403dca012bae`  
		Last Modified: Tue, 12 Mar 2024 01:55:06 GMT  
		Size: 1.0 MB (1046505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082de6b9063a87035e16509fa8e1e7cdedadb3694c18fbef26f1d676f7b8be5d`  
		Last Modified: Tue, 12 Mar 2024 01:55:07 GMT  
		Size: 80.3 KB (80323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34175578b2bb618865d187746a06f15e2945c3a3c48dfca6d3569756f6a98f5`  
		Last Modified: Tue, 12 Mar 2024 01:55:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bc64a90bae2aefe11ebb5c5daf0991201b77589f6665cf5feb2dd481f07e11`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 44.6 MB (44619549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0e1a5e9413519972edff179b1d5ad3915720fb0a3f0bd08386cf3f66b4f8d7`  
		Last Modified: Tue, 12 Mar 2024 01:55:07 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a485bc8fa933d3d5ccb3d4b8bb7532b86539b0cd20d4d8353a84335d4040cd`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721d7d15b9c2ee1e740d6b1b6c9a25db5718bb247947c723223bd20ff30ef02a`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136a4821a63b048ddb74fc09fee521674fe40967967922128fb124ab1ee66e8`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:dd2b838fd939799740f88c9a70f9816d30575b266879274a905ac9e9782a3f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3482186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8d660bec139f4ea49f00b7543cd9766db7ca2fe3c4ad8cf9b3767e189ec7d4`

```dockerfile
```

-	Layers:
	-	`sha256:9b7a415c19c667b83ee066c336e2ccd89e3961122f70f834073cf4d6331bffe3`  
		Last Modified: Tue, 12 Mar 2024 01:55:06 GMT  
		Size: 3.5 MB (3450904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c94de7ba8de7a8b8185e66243844385add7705c7a5738da0a601f1fea7516d8`  
		Last Modified: Tue, 12 Mar 2024 01:55:06 GMT  
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
$ docker pull couchdb@sha256:97f19d7e442521d2cb33ecd53434f1c28671d5a084ed5338156487062d3c2df0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:e93f5f7160f778d896487b4deb7a853b87514249dd940ab20174d52388e1c414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89309810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf1d84e28daed300b7eb2a6b9942c4f3d862e34780b9a2edfdef2cf29a4aa15`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
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
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a986ddb960d98b40ba2063c368c2048d4015572f08498d20b7d58a0d3279f70`  
		Last Modified: Tue, 12 Mar 2024 01:55:11 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936fcef7595b0ce9f42de56ea862ee2b8a0afc3d29b616a1c122e24bdf07c12f`  
		Last Modified: Tue, 12 Mar 2024 01:55:12 GMT  
		Size: 5.2 MB (5223267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a13db0fac8663ec77b3ed33ba3e21966757a378a37980ce724d4ac28531e8fc`  
		Last Modified: Tue, 12 Mar 2024 01:55:11 GMT  
		Size: 394.3 KB (394333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d52f3c8e08b8702e4376d123ed80c3e9aa204ab7451be99fa077dabc3775fb3`  
		Last Modified: Tue, 12 Mar 2024 01:55:11 GMT  
		Size: 77.9 KB (77879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f3b2c24ef6f02128d6edd4890f708890de23b5a063d282b74fe91a139891b0`  
		Last Modified: Tue, 12 Mar 2024 01:55:12 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e2ecab9bb7b1e2f9bd5617ec21f7d8d1e26801372eb8460d190f8da6e92cf5`  
		Last Modified: Tue, 12 Mar 2024 01:55:15 GMT  
		Size: 52.2 MB (52184519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22d0444f93951fa22f0e70be1347c069d44218cc3eda9f2bceab5e83bb621b6`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe719f2ef9596b12244cc5df6ecce3f24ebb8fb46257614b5315a157e231314`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 995.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b47ab28324c9a169c81af6f233cf877183aba0ca17081762cb012f28339e535`  
		Last Modified: Tue, 12 Mar 2024 01:55:14 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800b0261e1d40624d14d706a945db94e272e6d4b1553defb776d053dc6b842d4`  
		Last Modified: Tue, 12 Mar 2024 01:55:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:e5f8db4f81e677d529470a9a2d35be023dafa2bcc82fec99a782154314314836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c3c7c22bd8a4ea3a21becaae419d7de482854e1b8e9033a9d0c2de302acb58`

```dockerfile
```

-	Layers:
	-	`sha256:7dd6c4edf5a42447051ecd1763a9a9013a49091f17a4e2b71751a100170ee4ae`  
		Last Modified: Tue, 12 Mar 2024 01:55:12 GMT  
		Size: 3.9 MB (3935714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90a36e077081288244635fa0eafc2dc3adc848793d7760277ccebbba9f13b972`  
		Last Modified: Tue, 12 Mar 2024 01:55:11 GMT  
		Size: 31.1 KB (31132 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.2.3`

```console
$ docker pull couchdb@sha256:97f19d7e442521d2cb33ecd53434f1c28671d5a084ed5338156487062d3c2df0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchdb:3.2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:e93f5f7160f778d896487b4deb7a853b87514249dd940ab20174d52388e1c414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89309810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf1d84e28daed300b7eb2a6b9942c4f3d862e34780b9a2edfdef2cf29a4aa15`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
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
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a986ddb960d98b40ba2063c368c2048d4015572f08498d20b7d58a0d3279f70`  
		Last Modified: Tue, 12 Mar 2024 01:55:11 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936fcef7595b0ce9f42de56ea862ee2b8a0afc3d29b616a1c122e24bdf07c12f`  
		Last Modified: Tue, 12 Mar 2024 01:55:12 GMT  
		Size: 5.2 MB (5223267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a13db0fac8663ec77b3ed33ba3e21966757a378a37980ce724d4ac28531e8fc`  
		Last Modified: Tue, 12 Mar 2024 01:55:11 GMT  
		Size: 394.3 KB (394333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d52f3c8e08b8702e4376d123ed80c3e9aa204ab7451be99fa077dabc3775fb3`  
		Last Modified: Tue, 12 Mar 2024 01:55:11 GMT  
		Size: 77.9 KB (77879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f3b2c24ef6f02128d6edd4890f708890de23b5a063d282b74fe91a139891b0`  
		Last Modified: Tue, 12 Mar 2024 01:55:12 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e2ecab9bb7b1e2f9bd5617ec21f7d8d1e26801372eb8460d190f8da6e92cf5`  
		Last Modified: Tue, 12 Mar 2024 01:55:15 GMT  
		Size: 52.2 MB (52184519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22d0444f93951fa22f0e70be1347c069d44218cc3eda9f2bceab5e83bb621b6`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe719f2ef9596b12244cc5df6ecce3f24ebb8fb46257614b5315a157e231314`  
		Last Modified: Tue, 12 Mar 2024 01:55:13 GMT  
		Size: 995.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b47ab28324c9a169c81af6f233cf877183aba0ca17081762cb012f28339e535`  
		Last Modified: Tue, 12 Mar 2024 01:55:14 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800b0261e1d40624d14d706a945db94e272e6d4b1553defb776d053dc6b842d4`  
		Last Modified: Tue, 12 Mar 2024 01:55:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e5f8db4f81e677d529470a9a2d35be023dafa2bcc82fec99a782154314314836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c3c7c22bd8a4ea3a21becaae419d7de482854e1b8e9033a9d0c2de302acb58`

```dockerfile
```

-	Layers:
	-	`sha256:7dd6c4edf5a42447051ecd1763a9a9013a49091f17a4e2b71751a100170ee4ae`  
		Last Modified: Tue, 12 Mar 2024 01:55:12 GMT  
		Size: 3.9 MB (3935714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90a36e077081288244635fa0eafc2dc3adc848793d7760277ccebbba9f13b972`  
		Last Modified: Tue, 12 Mar 2024 01:55:11 GMT  
		Size: 31.1 KB (31132 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:486e8dc7b0f13a3dbd0047d6a445976a0aca4a2437a2c3c00ec397f30341fd2d
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
$ docker pull couchdb@sha256:128bea3044a6b715a9ec0b063db35d81dde409e90069e90e40fbbf798c86e0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89845595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d610ac3edbe74ad8f21e8167fc9f2c75ae02b2051afab93d585431d2f7a85e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
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
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c574efc63818fa0e037c4e0969c9fd3eb6b2cfe79608a16889498e17e2a4ce`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a4663271ce0ca2c19a6b77e95128ce13bcb4d1e6b33fcd5f55624fa4b5f8f2`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 5.2 MB (5223292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03654e97b888420e6f618137e0214d08e328aff08f55c3bd96cd00883cc6cbef`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 394.3 KB (394340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40457217ea148f864b30c5d41a342ecc394fcebfa8c36f6996c1a79175e08346`  
		Last Modified: Tue, 12 Mar 2024 01:55:09 GMT  
		Size: 77.9 KB (77884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773f4cf7eb790ab73b126512fc3ef8881aeda9b4e0bc66af9a8e2ec06e15c570`  
		Last Modified: Tue, 12 Mar 2024 01:55:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6f8ff995d65ec3847915eca070ff454fc1b1f376f145a6198edc7f727bcc50`  
		Last Modified: Tue, 12 Mar 2024 01:55:10 GMT  
		Size: 52.7 MB (52720018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0e1a5e9413519972edff179b1d5ad3915720fb0a3f0bd08386cf3f66b4f8d7`  
		Last Modified: Tue, 12 Mar 2024 01:55:07 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dcc52c9d8d65c573512a8b601660f662ab7144a9d1168fdbc6b9ff223ded43`  
		Last Modified: Tue, 12 Mar 2024 01:55:10 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e7039168554e3c4884e60580d57a737b349ed9b6c845597bb521826a76839c`  
		Last Modified: Tue, 12 Mar 2024 01:55:10 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136a4821a63b048ddb74fc09fee521674fe40967967922128fb124ab1ee66e8`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ef31ea760e4f0a589b1fcbf5ffc58987377d9244a9836b0dc0d7f7b5f88cb508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c96afc8e0d31180d78ab927a74fbe596b68e238713f7516db43cb6f90e65e`

```dockerfile
```

-	Layers:
	-	`sha256:f80e31c2413c820792147acbcd00566d5965fef02e88ac59b85b4b9b69e738c1`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 4.0 MB (3964852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce778357c2a1bbd4801960efd356f2074acb0f560d46cd647a64d15c81b02f5`  
		Last Modified: Tue, 12 Mar 2024 01:55:07 GMT  
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
$ docker pull couchdb@sha256:486e8dc7b0f13a3dbd0047d6a445976a0aca4a2437a2c3c00ec397f30341fd2d
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
$ docker pull couchdb@sha256:128bea3044a6b715a9ec0b063db35d81dde409e90069e90e40fbbf798c86e0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89845595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d610ac3edbe74ad8f21e8167fc9f2c75ae02b2051afab93d585431d2f7a85e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
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
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c574efc63818fa0e037c4e0969c9fd3eb6b2cfe79608a16889498e17e2a4ce`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a4663271ce0ca2c19a6b77e95128ce13bcb4d1e6b33fcd5f55624fa4b5f8f2`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 5.2 MB (5223292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03654e97b888420e6f618137e0214d08e328aff08f55c3bd96cd00883cc6cbef`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 394.3 KB (394340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40457217ea148f864b30c5d41a342ecc394fcebfa8c36f6996c1a79175e08346`  
		Last Modified: Tue, 12 Mar 2024 01:55:09 GMT  
		Size: 77.9 KB (77884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773f4cf7eb790ab73b126512fc3ef8881aeda9b4e0bc66af9a8e2ec06e15c570`  
		Last Modified: Tue, 12 Mar 2024 01:55:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6f8ff995d65ec3847915eca070ff454fc1b1f376f145a6198edc7f727bcc50`  
		Last Modified: Tue, 12 Mar 2024 01:55:10 GMT  
		Size: 52.7 MB (52720018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0e1a5e9413519972edff179b1d5ad3915720fb0a3f0bd08386cf3f66b4f8d7`  
		Last Modified: Tue, 12 Mar 2024 01:55:07 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dcc52c9d8d65c573512a8b601660f662ab7144a9d1168fdbc6b9ff223ded43`  
		Last Modified: Tue, 12 Mar 2024 01:55:10 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e7039168554e3c4884e60580d57a737b349ed9b6c845597bb521826a76839c`  
		Last Modified: Tue, 12 Mar 2024 01:55:10 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136a4821a63b048ddb74fc09fee521674fe40967967922128fb124ab1ee66e8`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ef31ea760e4f0a589b1fcbf5ffc58987377d9244a9836b0dc0d7f7b5f88cb508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c96afc8e0d31180d78ab927a74fbe596b68e238713f7516db43cb6f90e65e`

```dockerfile
```

-	Layers:
	-	`sha256:f80e31c2413c820792147acbcd00566d5965fef02e88ac59b85b4b9b69e738c1`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 4.0 MB (3964852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce778357c2a1bbd4801960efd356f2074acb0f560d46cd647a64d15c81b02f5`  
		Last Modified: Tue, 12 Mar 2024 01:55:07 GMT  
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
$ docker pull couchdb@sha256:486e8dc7b0f13a3dbd0047d6a445976a0aca4a2437a2c3c00ec397f30341fd2d
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
$ docker pull couchdb@sha256:128bea3044a6b715a9ec0b063db35d81dde409e90069e90e40fbbf798c86e0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89845595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d610ac3edbe74ad8f21e8167fc9f2c75ae02b2051afab93d585431d2f7a85e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
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
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c574efc63818fa0e037c4e0969c9fd3eb6b2cfe79608a16889498e17e2a4ce`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a4663271ce0ca2c19a6b77e95128ce13bcb4d1e6b33fcd5f55624fa4b5f8f2`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 5.2 MB (5223292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03654e97b888420e6f618137e0214d08e328aff08f55c3bd96cd00883cc6cbef`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 394.3 KB (394340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40457217ea148f864b30c5d41a342ecc394fcebfa8c36f6996c1a79175e08346`  
		Last Modified: Tue, 12 Mar 2024 01:55:09 GMT  
		Size: 77.9 KB (77884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773f4cf7eb790ab73b126512fc3ef8881aeda9b4e0bc66af9a8e2ec06e15c570`  
		Last Modified: Tue, 12 Mar 2024 01:55:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6f8ff995d65ec3847915eca070ff454fc1b1f376f145a6198edc7f727bcc50`  
		Last Modified: Tue, 12 Mar 2024 01:55:10 GMT  
		Size: 52.7 MB (52720018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0e1a5e9413519972edff179b1d5ad3915720fb0a3f0bd08386cf3f66b4f8d7`  
		Last Modified: Tue, 12 Mar 2024 01:55:07 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dcc52c9d8d65c573512a8b601660f662ab7144a9d1168fdbc6b9ff223ded43`  
		Last Modified: Tue, 12 Mar 2024 01:55:10 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e7039168554e3c4884e60580d57a737b349ed9b6c845597bb521826a76839c`  
		Last Modified: Tue, 12 Mar 2024 01:55:10 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136a4821a63b048ddb74fc09fee521674fe40967967922128fb124ab1ee66e8`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:ef31ea760e4f0a589b1fcbf5ffc58987377d9244a9836b0dc0d7f7b5f88cb508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c96afc8e0d31180d78ab927a74fbe596b68e238713f7516db43cb6f90e65e`

```dockerfile
```

-	Layers:
	-	`sha256:f80e31c2413c820792147acbcd00566d5965fef02e88ac59b85b4b9b69e738c1`  
		Last Modified: Tue, 12 Mar 2024 01:55:08 GMT  
		Size: 4.0 MB (3964852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce778357c2a1bbd4801960efd356f2074acb0f560d46cd647a64d15c81b02f5`  
		Last Modified: Tue, 12 Mar 2024 01:55:07 GMT  
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
