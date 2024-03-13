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
$ docker pull couchdb@sha256:00fc995c8e9938fb934829420e841cebba42d1163b14cca402a71a4b826efa2e
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
$ docker pull couchdb@sha256:175fe9129bc0591b0d08d965ae2c6530971788264ad69b6bdeb33a3367e4cc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72615928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7868f17cf74b73d734838edcd71de349280357b29859b69b1c481a5c5db45844`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:01e6303e5bd3d7bb8200a616ab1d931421cd756c837936b3f897727814cb89c3 in / 
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
	-	`sha256:f109bca8a22fa25fc80b89d2ad693f6f3e7832d4386218a35d068f3b37b0e808`  
		Last Modified: Tue, 12 Mar 2024 00:50:11 GMT  
		Size: 26.0 MB (25970589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38430b6e3a72be5255ca5b311d24c972d153c47439e7609bb203455afd298ad`  
		Last Modified: Tue, 12 Mar 2024 14:37:16 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aef5570b590253907fc08258878a9e319ff97e664df46046e31a31d19c9bbc`  
		Last Modified: Tue, 12 Mar 2024 14:37:17 GMT  
		Size: 6.6 MB (6576632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d73160802cb88bc79de964e604893620491ffc2e60f9c9e2d76ce7fda7dbe9`  
		Last Modified: Tue, 12 Mar 2024 14:37:16 GMT  
		Size: 951.3 KB (951346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b781e456d606875eb2964a20402cfecc080abd24aaeadc79e289ba27b4b4a7`  
		Last Modified: Tue, 12 Mar 2024 14:37:17 GMT  
		Size: 80.2 KB (80192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21404b33d737e1c53b197545d7f2c68faf58abc204554859bbe6592f2ee8149`  
		Last Modified: Tue, 12 Mar 2024 14:37:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c823adf7d731226a51dad8409c7df4029a1134d62a404c241e034e0e1e4f19`  
		Last Modified: Tue, 12 Mar 2024 14:37:59 GMT  
		Size: 39.0 MB (39030221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3642f558134fefe91cf344cdeef6a7238accb8bbb2a6134cb70270bfadefcaec`  
		Last Modified: Tue, 12 Mar 2024 14:37:58 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd891aad830aacd611fe0bbdd59eb1017c3d27ac2fabbeadf9c6ee500cbc9cda`  
		Last Modified: Tue, 12 Mar 2024 14:37:58 GMT  
		Size: 764.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44141b4c4fcbb71305a27f3c4a96bb34fbe5aa228668ff1cd9fe487c80ab50a5`  
		Last Modified: Tue, 12 Mar 2024 14:37:59 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e5387a878c691a84131769d6df32001bb6705b61672aaf2e631a854b3b905a`  
		Last Modified: Tue, 12 Mar 2024 14:37:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2` - unknown; unknown

```console
$ docker pull couchdb@sha256:4edb82db0c8c3d89003ee7fe4080320cecdd196e5eeaf123b2e9318713c986bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3425036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff8b696f047998db20b1e3fe083fcf241c1fc4458357b82c09f01064360675c`

```dockerfile
```

-	Layers:
	-	`sha256:d14e70d34989aa60a17e15d6c706bcadf53509bb86346d59783c1053f3d02532`  
		Last Modified: Tue, 12 Mar 2024 14:37:58 GMT  
		Size: 3.4 MB (3393621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eadaa394c5f336a57c2321153d5d501d11559e80e9214f731b329c72ef59ddd5`  
		Last Modified: Tue, 12 Mar 2024 14:37:57 GMT  
		Size: 31.4 KB (31415 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:00fc995c8e9938fb934829420e841cebba42d1163b14cca402a71a4b826efa2e
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
$ docker pull couchdb@sha256:175fe9129bc0591b0d08d965ae2c6530971788264ad69b6bdeb33a3367e4cc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72615928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7868f17cf74b73d734838edcd71de349280357b29859b69b1c481a5c5db45844`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:01e6303e5bd3d7bb8200a616ab1d931421cd756c837936b3f897727814cb89c3 in / 
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
	-	`sha256:f109bca8a22fa25fc80b89d2ad693f6f3e7832d4386218a35d068f3b37b0e808`  
		Last Modified: Tue, 12 Mar 2024 00:50:11 GMT  
		Size: 26.0 MB (25970589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38430b6e3a72be5255ca5b311d24c972d153c47439e7609bb203455afd298ad`  
		Last Modified: Tue, 12 Mar 2024 14:37:16 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aef5570b590253907fc08258878a9e319ff97e664df46046e31a31d19c9bbc`  
		Last Modified: Tue, 12 Mar 2024 14:37:17 GMT  
		Size: 6.6 MB (6576632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d73160802cb88bc79de964e604893620491ffc2e60f9c9e2d76ce7fda7dbe9`  
		Last Modified: Tue, 12 Mar 2024 14:37:16 GMT  
		Size: 951.3 KB (951346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b781e456d606875eb2964a20402cfecc080abd24aaeadc79e289ba27b4b4a7`  
		Last Modified: Tue, 12 Mar 2024 14:37:17 GMT  
		Size: 80.2 KB (80192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21404b33d737e1c53b197545d7f2c68faf58abc204554859bbe6592f2ee8149`  
		Last Modified: Tue, 12 Mar 2024 14:37:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c823adf7d731226a51dad8409c7df4029a1134d62a404c241e034e0e1e4f19`  
		Last Modified: Tue, 12 Mar 2024 14:37:59 GMT  
		Size: 39.0 MB (39030221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3642f558134fefe91cf344cdeef6a7238accb8bbb2a6134cb70270bfadefcaec`  
		Last Modified: Tue, 12 Mar 2024 14:37:58 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd891aad830aacd611fe0bbdd59eb1017c3d27ac2fabbeadf9c6ee500cbc9cda`  
		Last Modified: Tue, 12 Mar 2024 14:37:58 GMT  
		Size: 764.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44141b4c4fcbb71305a27f3c4a96bb34fbe5aa228668ff1cd9fe487c80ab50a5`  
		Last Modified: Tue, 12 Mar 2024 14:37:59 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e5387a878c691a84131769d6df32001bb6705b61672aaf2e631a854b3b905a`  
		Last Modified: Tue, 12 Mar 2024 14:37:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:4edb82db0c8c3d89003ee7fe4080320cecdd196e5eeaf123b2e9318713c986bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3425036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff8b696f047998db20b1e3fe083fcf241c1fc4458357b82c09f01064360675c`

```dockerfile
```

-	Layers:
	-	`sha256:d14e70d34989aa60a17e15d6c706bcadf53509bb86346d59783c1053f3d02532`  
		Last Modified: Tue, 12 Mar 2024 14:37:58 GMT  
		Size: 3.4 MB (3393621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eadaa394c5f336a57c2321153d5d501d11559e80e9214f731b329c72ef59ddd5`  
		Last Modified: Tue, 12 Mar 2024 14:37:57 GMT  
		Size: 31.4 KB (31415 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:00fc995c8e9938fb934829420e841cebba42d1163b14cca402a71a4b826efa2e
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
$ docker pull couchdb@sha256:175fe9129bc0591b0d08d965ae2c6530971788264ad69b6bdeb33a3367e4cc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72615928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7868f17cf74b73d734838edcd71de349280357b29859b69b1c481a5c5db45844`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:01e6303e5bd3d7bb8200a616ab1d931421cd756c837936b3f897727814cb89c3 in / 
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
	-	`sha256:f109bca8a22fa25fc80b89d2ad693f6f3e7832d4386218a35d068f3b37b0e808`  
		Last Modified: Tue, 12 Mar 2024 00:50:11 GMT  
		Size: 26.0 MB (25970589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38430b6e3a72be5255ca5b311d24c972d153c47439e7609bb203455afd298ad`  
		Last Modified: Tue, 12 Mar 2024 14:37:16 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aef5570b590253907fc08258878a9e319ff97e664df46046e31a31d19c9bbc`  
		Last Modified: Tue, 12 Mar 2024 14:37:17 GMT  
		Size: 6.6 MB (6576632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d73160802cb88bc79de964e604893620491ffc2e60f9c9e2d76ce7fda7dbe9`  
		Last Modified: Tue, 12 Mar 2024 14:37:16 GMT  
		Size: 951.3 KB (951346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b781e456d606875eb2964a20402cfecc080abd24aaeadc79e289ba27b4b4a7`  
		Last Modified: Tue, 12 Mar 2024 14:37:17 GMT  
		Size: 80.2 KB (80192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21404b33d737e1c53b197545d7f2c68faf58abc204554859bbe6592f2ee8149`  
		Last Modified: Tue, 12 Mar 2024 14:37:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c823adf7d731226a51dad8409c7df4029a1134d62a404c241e034e0e1e4f19`  
		Last Modified: Tue, 12 Mar 2024 14:37:59 GMT  
		Size: 39.0 MB (39030221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3642f558134fefe91cf344cdeef6a7238accb8bbb2a6134cb70270bfadefcaec`  
		Last Modified: Tue, 12 Mar 2024 14:37:58 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd891aad830aacd611fe0bbdd59eb1017c3d27ac2fabbeadf9c6ee500cbc9cda`  
		Last Modified: Tue, 12 Mar 2024 14:37:58 GMT  
		Size: 764.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44141b4c4fcbb71305a27f3c4a96bb34fbe5aa228668ff1cd9fe487c80ab50a5`  
		Last Modified: Tue, 12 Mar 2024 14:37:59 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e5387a878c691a84131769d6df32001bb6705b61672aaf2e631a854b3b905a`  
		Last Modified: Tue, 12 Mar 2024 14:37:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:4edb82db0c8c3d89003ee7fe4080320cecdd196e5eeaf123b2e9318713c986bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3425036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff8b696f047998db20b1e3fe083fcf241c1fc4458357b82c09f01064360675c`

```dockerfile
```

-	Layers:
	-	`sha256:d14e70d34989aa60a17e15d6c706bcadf53509bb86346d59783c1053f3d02532`  
		Last Modified: Tue, 12 Mar 2024 14:37:58 GMT  
		Size: 3.4 MB (3393621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eadaa394c5f336a57c2321153d5d501d11559e80e9214f731b329c72ef59ddd5`  
		Last Modified: Tue, 12 Mar 2024 14:37:57 GMT  
		Size: 31.4 KB (31415 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3`

```console
$ docker pull couchdb@sha256:7b60b651baacd33a8bc9cc9c048afb4aa81354681ebfae8bdd288d577e02bb57
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
$ docker pull couchdb@sha256:b30e6d23f4c4fe8a4b342eb574e371e3124b1e618ee2b368f6a9e2bb46553f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88286584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9481027d4e3eec91bcafb56ec50872bbdf5d4d23e68ff85be32362a9e8e8c362`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
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
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463acd6d68b4345c1eaa163bfd81d069ed7126d29cc7e3202f1063f90824412b`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41173148c73e8a129b29b9f540d64c8253a103cd95f3f851c59a676b0a22ffbb`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 5.2 MB (5208021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0677b4e15e3308d202ef2bec353dfbf59bc20bcf69033850af15cb605f71a689`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 350.5 KB (350543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9a4a5a0e4631055e487480267fbdf92ad450a5d2a356a12423ec1b94d72565`  
		Last Modified: Tue, 12 Mar 2024 14:36:21 GMT  
		Size: 77.8 KB (77785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544e5d6b202dd1fbb148536b5eaa5db07c4b9dfbc06a9a0d11893c1b454ca573`  
		Last Modified: Tue, 12 Mar 2024 14:36:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cba4a9a7e7fd947404e38d278b453c01d3cba852e1584dc9fce80fb8a59b0e`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 52.6 MB (52571512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373cc69b69ae865e6767eb5dee7ebddb1a6347c9d4ffa9ad1ee0fb180720f07c`  
		Last Modified: Tue, 12 Mar 2024 14:36:22 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8593b99b429341a6b0941b93a3d9ef64832a86654189f12637e340186f773b5`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6bb5429219bff94dc75fddb64f0e195934d3e066e0f88e66fe96d07208586c`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11eb3094a926106632c5c6a03439c59a3084027e8c804eabd1e4bcae53ce1baa`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:61209dfc1ea8129540bc8f3f527bd9b0dc092919b4dac88120eecd8b431b066a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b666ad88071ab046dbdc71ce6abf82cc6b5169d9f1ac9812d4a471018b8082`

```dockerfile
```

-	Layers:
	-	`sha256:7a182b0fbf5f71fe0e5d506bc971cdcb07dcf9fc8f00277f98ddd4292d60a1e2`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 4.0 MB (3965094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f0dc84a2fc33f0506821127895c3d1f06d7d963ebad6fb2b9fd0bab6103fc60`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 31.7 KB (31736 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:b8ff0acf04b78b8fea4b2b2ec74682d93e34f2aa2ca72fbeba02137c899f9a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95572353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce76029afa4c63d7555c64091961d489f80a7f70b966c8681f03d49ce466e090`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
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
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06cb2dd86e1b10e4634199f9c3973046ee081ce2e3b4eab364a1c0607b055f3`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39b71c2ca731395dff6754910b5f0f94dcbe5b1213f3efbc3c79e5e92b94e0d`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 6.0 MB (6042512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f039259cd371a1c4a2aaf5db8aa0329078dd4551a5eaf09db4389dfbf062e99c`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 446.7 KB (446656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc3f03b79aebe627023f165883fa4afb8d27a823bc1a95f87fac188bf29733d`  
		Last Modified: Tue, 12 Mar 2024 19:35:38 GMT  
		Size: 77.8 KB (77841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56f85cfb3cdcfcf570a86091c67c1657e158c68e0b97186ff78c791b16008ce`  
		Last Modified: Tue, 12 Mar 2024 19:35:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805f6eaf9f41b846f9a9a4e112f99e7a5a263583f91ff0f843e19459da572da6`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 53.7 MB (53699764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c688fdd5676f9300b17f0702cdb0b6fb0ba55c6916567d6ba7f87023f1092`  
		Last Modified: Tue, 12 Mar 2024 19:35:39 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00d1425e7f6da85549f5395f27906837a91a6033335c5d5d5062c3319158edd`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972716b5e7985a7a86e83b34383c5949b159078aa8fd71235d0c127f64f6065`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce0a5c75620215e0e6dd9864f3d801a9d3f6eca085b12e8eb92dcbc363a4dd9`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc9bc2208b953947418ae53feb245a1feb061a62345b5eaf876bb963caaf0ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fcf57039d5535a1529d2d686d9c0549dcde375dd1ea402804de5d2f6cb7974`

```dockerfile
```

-	Layers:
	-	`sha256:1de56ac16f12a1eae5b73fed95e5773b6b3f1cfcef1d14a705d4115d67219dd8`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 4.0 MB (3969386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b0841ee6c445fbcd02ca141fa48dc4c47a73bf04588f394a5d5ed926345bc4`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:0da3f2c45fe947e70c429ce6a80e489fc7af202bc7890539f81319aaf9e48e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86585706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04498e8701a99b1d9e284225ac887dac0f28b0ac5f2a0257d1c5b3f6708a203a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e121f5164f2335792d17befe564e4a4caf1dec33d5039c8245ce418144782215 in / 
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
	-	`sha256:840335d52e6c781c13aaaed8df36659831a5cb0747048da9bf578dd19a02b30e`  
		Last Modified: Tue, 12 Mar 2024 01:21:45 GMT  
		Size: 29.7 MB (29660245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc29d412a86c9bb1d3f309751aabf00a48127e9881e13951c317e94af85fd9b`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 3.3 KB (3347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a68cfae36a1f9b9177dbaa8e464778bdbfab63131398c63ef4a0120e7f8eaa`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 5.1 MB (5109274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49194257445d97cd95d18dfad61977dbe170d352aac7c9a6ed87faf3dbabdf28`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 357.5 KB (357476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cce9afe5b29ea6e53ec0a17ecd2c9a8d5b41981ceeda4087378a1fd2513adc7`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 77.8 KB (77817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39be4f4afc8fd3f4a0f0231127342c94aefacd8475ab4799a696dc8db62fdd9`  
		Last Modified: Tue, 12 Mar 2024 20:38:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e3bba10728d859dd4104f17048ac9e4b2b0a4e42969eb3e070828048018b2b`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 51.4 MB (51373301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59cc9a209cbe0d8ea4e6a4784bffbebf525d6c7ed1056e15ae9d9f4f51d1dea`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99300506f8cd321549fb6c67be4fc0bbe579bb10c6f1e284ed86d23a6c83dd5d`  
		Last Modified: Tue, 12 Mar 2024 20:38:38 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef61d060418410a198f7929b49f4364b6b52c5daaa090b205911f585c50b0569`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a102a80c253aae9e4afafc94115d5b80a38c15c1dafd012263460940e51725`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc2439ed0b9d225b49e7dcebb1dc57afbd8dad9b3ee1a334baedcb5058f9b639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af20321f5bb71925340f87452348321257292150a0ea4a50303abeaff27bda34`

```dockerfile
```

-	Layers:
	-	`sha256:6ac9c5ca993674968ed8fce38354e553a4ec9f24fe684b3e70223ac147d0bcc1`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 4.0 MB (3964424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e43a90811aeb106a69b953165e1ccbbae90a2a341815a5961edce992d3a1bde`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:cbcc515ba21894f7beb75a77732d06cb806631b9d3abfc83c4dc5361a7ab12dd
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
$ docker pull couchdb@sha256:6fabd186b4e8d2ca337a086cc7bbb9a7c13e8496a72f7baab9ca971975375a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74710527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b447324915e611aeee7b650030cd22ce682a2d7536efcbd99a84743b5796b25`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:01e6303e5bd3d7bb8200a616ab1d931421cd756c837936b3f897727814cb89c3 in / 
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
	-	`sha256:f109bca8a22fa25fc80b89d2ad693f6f3e7832d4386218a35d068f3b37b0e808`  
		Last Modified: Tue, 12 Mar 2024 00:50:11 GMT  
		Size: 26.0 MB (25970589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38430b6e3a72be5255ca5b311d24c972d153c47439e7609bb203455afd298ad`  
		Last Modified: Tue, 12 Mar 2024 14:37:16 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aef5570b590253907fc08258878a9e319ff97e664df46046e31a31d19c9bbc`  
		Last Modified: Tue, 12 Mar 2024 14:37:17 GMT  
		Size: 6.6 MB (6576632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d73160802cb88bc79de964e604893620491ffc2e60f9c9e2d76ce7fda7dbe9`  
		Last Modified: Tue, 12 Mar 2024 14:37:16 GMT  
		Size: 951.3 KB (951346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b781e456d606875eb2964a20402cfecc080abd24aaeadc79e289ba27b4b4a7`  
		Last Modified: Tue, 12 Mar 2024 14:37:17 GMT  
		Size: 80.2 KB (80192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7511bca92139aa432dcc6a6b49b75af355ebb83c1387feb7dbc60cfa40c204d3`  
		Last Modified: Tue, 12 Mar 2024 14:37:18 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672354e1dcdf344594853bf21a2f3702bb3a2f50b2edb784b8a4b3297e62375`  
		Last Modified: Tue, 12 Mar 2024 14:37:21 GMT  
		Size: 41.1 MB (41124826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557f41347b8ac1b5ab48133466a83036aefa814c4d44ac8ddb280df22219bdb1`  
		Last Modified: Tue, 12 Mar 2024 14:37:18 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f32aee9b34552262be8e8f0562c7d13ed2244f8b63d35575f3db29f33e734aa`  
		Last Modified: Tue, 12 Mar 2024 14:37:18 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d817ff815a10056deca145607152d4e11ba422fd193e46b78bad1ef7854cf8b3`  
		Last Modified: Tue, 12 Mar 2024 14:37:19 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060d220f6efa07ab7b05ad17647f70f5cd36f0387edef2c5b2dc7654f9883afe`  
		Last Modified: Tue, 12 Mar 2024 14:37:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:02a04c9e17597f515afbe5f68c1beb9d5857e37262979b4b119f9cc82b6577be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52901a24ed15710212dabc73312f4ba52cc83f72a6fa03d9b6e7b6182fae5d9c`

```dockerfile
```

-	Layers:
	-	`sha256:25e3d60c541bf5734a4f42f25fe945868ef71dc27faaa8e0d1eea279e3c8f575`  
		Last Modified: Tue, 12 Mar 2024 14:37:17 GMT  
		Size: 3.5 MB (3457501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b006926992f6c7495b3ad1b82f3d86311b7bba617e1cef512e619d60692d7de1`  
		Last Modified: Tue, 12 Mar 2024 14:37:16 GMT  
		Size: 31.3 KB (31280 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:cbcc515ba21894f7beb75a77732d06cb806631b9d3abfc83c4dc5361a7ab12dd
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
$ docker pull couchdb@sha256:6fabd186b4e8d2ca337a086cc7bbb9a7c13e8496a72f7baab9ca971975375a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74710527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b447324915e611aeee7b650030cd22ce682a2d7536efcbd99a84743b5796b25`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:01e6303e5bd3d7bb8200a616ab1d931421cd756c837936b3f897727814cb89c3 in / 
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
	-	`sha256:f109bca8a22fa25fc80b89d2ad693f6f3e7832d4386218a35d068f3b37b0e808`  
		Last Modified: Tue, 12 Mar 2024 00:50:11 GMT  
		Size: 26.0 MB (25970589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38430b6e3a72be5255ca5b311d24c972d153c47439e7609bb203455afd298ad`  
		Last Modified: Tue, 12 Mar 2024 14:37:16 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aef5570b590253907fc08258878a9e319ff97e664df46046e31a31d19c9bbc`  
		Last Modified: Tue, 12 Mar 2024 14:37:17 GMT  
		Size: 6.6 MB (6576632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d73160802cb88bc79de964e604893620491ffc2e60f9c9e2d76ce7fda7dbe9`  
		Last Modified: Tue, 12 Mar 2024 14:37:16 GMT  
		Size: 951.3 KB (951346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b781e456d606875eb2964a20402cfecc080abd24aaeadc79e289ba27b4b4a7`  
		Last Modified: Tue, 12 Mar 2024 14:37:17 GMT  
		Size: 80.2 KB (80192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7511bca92139aa432dcc6a6b49b75af355ebb83c1387feb7dbc60cfa40c204d3`  
		Last Modified: Tue, 12 Mar 2024 14:37:18 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672354e1dcdf344594853bf21a2f3702bb3a2f50b2edb784b8a4b3297e62375`  
		Last Modified: Tue, 12 Mar 2024 14:37:21 GMT  
		Size: 41.1 MB (41124826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557f41347b8ac1b5ab48133466a83036aefa814c4d44ac8ddb280df22219bdb1`  
		Last Modified: Tue, 12 Mar 2024 14:37:18 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f32aee9b34552262be8e8f0562c7d13ed2244f8b63d35575f3db29f33e734aa`  
		Last Modified: Tue, 12 Mar 2024 14:37:18 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d817ff815a10056deca145607152d4e11ba422fd193e46b78bad1ef7854cf8b3`  
		Last Modified: Tue, 12 Mar 2024 14:37:19 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060d220f6efa07ab7b05ad17647f70f5cd36f0387edef2c5b2dc7654f9883afe`  
		Last Modified: Tue, 12 Mar 2024 14:37:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:02a04c9e17597f515afbe5f68c1beb9d5857e37262979b4b119f9cc82b6577be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52901a24ed15710212dabc73312f4ba52cc83f72a6fa03d9b6e7b6182fae5d9c`

```dockerfile
```

-	Layers:
	-	`sha256:25e3d60c541bf5734a4f42f25fe945868ef71dc27faaa8e0d1eea279e3c8f575`  
		Last Modified: Tue, 12 Mar 2024 14:37:17 GMT  
		Size: 3.5 MB (3457501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b006926992f6c7495b3ad1b82f3d86311b7bba617e1cef512e619d60692d7de1`  
		Last Modified: Tue, 12 Mar 2024 14:37:16 GMT  
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
$ docker pull couchdb@sha256:7b60b651baacd33a8bc9cc9c048afb4aa81354681ebfae8bdd288d577e02bb57
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
$ docker pull couchdb@sha256:b30e6d23f4c4fe8a4b342eb574e371e3124b1e618ee2b368f6a9e2bb46553f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88286584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9481027d4e3eec91bcafb56ec50872bbdf5d4d23e68ff85be32362a9e8e8c362`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
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
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463acd6d68b4345c1eaa163bfd81d069ed7126d29cc7e3202f1063f90824412b`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41173148c73e8a129b29b9f540d64c8253a103cd95f3f851c59a676b0a22ffbb`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 5.2 MB (5208021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0677b4e15e3308d202ef2bec353dfbf59bc20bcf69033850af15cb605f71a689`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 350.5 KB (350543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9a4a5a0e4631055e487480267fbdf92ad450a5d2a356a12423ec1b94d72565`  
		Last Modified: Tue, 12 Mar 2024 14:36:21 GMT  
		Size: 77.8 KB (77785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544e5d6b202dd1fbb148536b5eaa5db07c4b9dfbc06a9a0d11893c1b454ca573`  
		Last Modified: Tue, 12 Mar 2024 14:36:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cba4a9a7e7fd947404e38d278b453c01d3cba852e1584dc9fce80fb8a59b0e`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 52.6 MB (52571512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373cc69b69ae865e6767eb5dee7ebddb1a6347c9d4ffa9ad1ee0fb180720f07c`  
		Last Modified: Tue, 12 Mar 2024 14:36:22 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8593b99b429341a6b0941b93a3d9ef64832a86654189f12637e340186f773b5`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6bb5429219bff94dc75fddb64f0e195934d3e066e0f88e66fe96d07208586c`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11eb3094a926106632c5c6a03439c59a3084027e8c804eabd1e4bcae53ce1baa`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:61209dfc1ea8129540bc8f3f527bd9b0dc092919b4dac88120eecd8b431b066a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b666ad88071ab046dbdc71ce6abf82cc6b5169d9f1ac9812d4a471018b8082`

```dockerfile
```

-	Layers:
	-	`sha256:7a182b0fbf5f71fe0e5d506bc971cdcb07dcf9fc8f00277f98ddd4292d60a1e2`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 4.0 MB (3965094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f0dc84a2fc33f0506821127895c3d1f06d7d963ebad6fb2b9fd0bab6103fc60`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 31.7 KB (31736 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:b8ff0acf04b78b8fea4b2b2ec74682d93e34f2aa2ca72fbeba02137c899f9a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95572353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce76029afa4c63d7555c64091961d489f80a7f70b966c8681f03d49ce466e090`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
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
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06cb2dd86e1b10e4634199f9c3973046ee081ce2e3b4eab364a1c0607b055f3`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39b71c2ca731395dff6754910b5f0f94dcbe5b1213f3efbc3c79e5e92b94e0d`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 6.0 MB (6042512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f039259cd371a1c4a2aaf5db8aa0329078dd4551a5eaf09db4389dfbf062e99c`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 446.7 KB (446656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc3f03b79aebe627023f165883fa4afb8d27a823bc1a95f87fac188bf29733d`  
		Last Modified: Tue, 12 Mar 2024 19:35:38 GMT  
		Size: 77.8 KB (77841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56f85cfb3cdcfcf570a86091c67c1657e158c68e0b97186ff78c791b16008ce`  
		Last Modified: Tue, 12 Mar 2024 19:35:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805f6eaf9f41b846f9a9a4e112f99e7a5a263583f91ff0f843e19459da572da6`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 53.7 MB (53699764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c688fdd5676f9300b17f0702cdb0b6fb0ba55c6916567d6ba7f87023f1092`  
		Last Modified: Tue, 12 Mar 2024 19:35:39 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00d1425e7f6da85549f5395f27906837a91a6033335c5d5d5062c3319158edd`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972716b5e7985a7a86e83b34383c5949b159078aa8fd71235d0c127f64f6065`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce0a5c75620215e0e6dd9864f3d801a9d3f6eca085b12e8eb92dcbc363a4dd9`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc9bc2208b953947418ae53feb245a1feb061a62345b5eaf876bb963caaf0ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fcf57039d5535a1529d2d686d9c0549dcde375dd1ea402804de5d2f6cb7974`

```dockerfile
```

-	Layers:
	-	`sha256:1de56ac16f12a1eae5b73fed95e5773b6b3f1cfcef1d14a705d4115d67219dd8`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 4.0 MB (3969386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b0841ee6c445fbcd02ca141fa48dc4c47a73bf04588f394a5d5ed926345bc4`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:0da3f2c45fe947e70c429ce6a80e489fc7af202bc7890539f81319aaf9e48e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86585706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04498e8701a99b1d9e284225ac887dac0f28b0ac5f2a0257d1c5b3f6708a203a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e121f5164f2335792d17befe564e4a4caf1dec33d5039c8245ce418144782215 in / 
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
	-	`sha256:840335d52e6c781c13aaaed8df36659831a5cb0747048da9bf578dd19a02b30e`  
		Last Modified: Tue, 12 Mar 2024 01:21:45 GMT  
		Size: 29.7 MB (29660245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc29d412a86c9bb1d3f309751aabf00a48127e9881e13951c317e94af85fd9b`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 3.3 KB (3347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a68cfae36a1f9b9177dbaa8e464778bdbfab63131398c63ef4a0120e7f8eaa`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 5.1 MB (5109274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49194257445d97cd95d18dfad61977dbe170d352aac7c9a6ed87faf3dbabdf28`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 357.5 KB (357476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cce9afe5b29ea6e53ec0a17ecd2c9a8d5b41981ceeda4087378a1fd2513adc7`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 77.8 KB (77817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39be4f4afc8fd3f4a0f0231127342c94aefacd8475ab4799a696dc8db62fdd9`  
		Last Modified: Tue, 12 Mar 2024 20:38:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e3bba10728d859dd4104f17048ac9e4b2b0a4e42969eb3e070828048018b2b`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 51.4 MB (51373301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59cc9a209cbe0d8ea4e6a4784bffbebf525d6c7ed1056e15ae9d9f4f51d1dea`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99300506f8cd321549fb6c67be4fc0bbe579bb10c6f1e284ed86d23a6c83dd5d`  
		Last Modified: Tue, 12 Mar 2024 20:38:38 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef61d060418410a198f7929b49f4364b6b52c5daaa090b205911f585c50b0569`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a102a80c253aae9e4afafc94115d5b80a38c15c1dafd012263460940e51725`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc2439ed0b9d225b49e7dcebb1dc57afbd8dad9b3ee1a334baedcb5058f9b639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af20321f5bb71925340f87452348321257292150a0ea4a50303abeaff27bda34`

```dockerfile
```

-	Layers:
	-	`sha256:6ac9c5ca993674968ed8fce38354e553a4ec9f24fe684b3e70223ac147d0bcc1`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 4.0 MB (3964424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e43a90811aeb106a69b953165e1ccbbae90a2a341815a5961edce992d3a1bde`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:7b60b651baacd33a8bc9cc9c048afb4aa81354681ebfae8bdd288d577e02bb57
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
$ docker pull couchdb@sha256:b30e6d23f4c4fe8a4b342eb574e371e3124b1e618ee2b368f6a9e2bb46553f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88286584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9481027d4e3eec91bcafb56ec50872bbdf5d4d23e68ff85be32362a9e8e8c362`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
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
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463acd6d68b4345c1eaa163bfd81d069ed7126d29cc7e3202f1063f90824412b`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41173148c73e8a129b29b9f540d64c8253a103cd95f3f851c59a676b0a22ffbb`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 5.2 MB (5208021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0677b4e15e3308d202ef2bec353dfbf59bc20bcf69033850af15cb605f71a689`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 350.5 KB (350543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9a4a5a0e4631055e487480267fbdf92ad450a5d2a356a12423ec1b94d72565`  
		Last Modified: Tue, 12 Mar 2024 14:36:21 GMT  
		Size: 77.8 KB (77785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544e5d6b202dd1fbb148536b5eaa5db07c4b9dfbc06a9a0d11893c1b454ca573`  
		Last Modified: Tue, 12 Mar 2024 14:36:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cba4a9a7e7fd947404e38d278b453c01d3cba852e1584dc9fce80fb8a59b0e`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 52.6 MB (52571512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373cc69b69ae865e6767eb5dee7ebddb1a6347c9d4ffa9ad1ee0fb180720f07c`  
		Last Modified: Tue, 12 Mar 2024 14:36:22 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8593b99b429341a6b0941b93a3d9ef64832a86654189f12637e340186f773b5`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6bb5429219bff94dc75fddb64f0e195934d3e066e0f88e66fe96d07208586c`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11eb3094a926106632c5c6a03439c59a3084027e8c804eabd1e4bcae53ce1baa`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:61209dfc1ea8129540bc8f3f527bd9b0dc092919b4dac88120eecd8b431b066a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b666ad88071ab046dbdc71ce6abf82cc6b5169d9f1ac9812d4a471018b8082`

```dockerfile
```

-	Layers:
	-	`sha256:7a182b0fbf5f71fe0e5d506bc971cdcb07dcf9fc8f00277f98ddd4292d60a1e2`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 4.0 MB (3965094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f0dc84a2fc33f0506821127895c3d1f06d7d963ebad6fb2b9fd0bab6103fc60`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 31.7 KB (31736 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:b8ff0acf04b78b8fea4b2b2ec74682d93e34f2aa2ca72fbeba02137c899f9a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95572353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce76029afa4c63d7555c64091961d489f80a7f70b966c8681f03d49ce466e090`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
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
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06cb2dd86e1b10e4634199f9c3973046ee081ce2e3b4eab364a1c0607b055f3`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39b71c2ca731395dff6754910b5f0f94dcbe5b1213f3efbc3c79e5e92b94e0d`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 6.0 MB (6042512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f039259cd371a1c4a2aaf5db8aa0329078dd4551a5eaf09db4389dfbf062e99c`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 446.7 KB (446656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc3f03b79aebe627023f165883fa4afb8d27a823bc1a95f87fac188bf29733d`  
		Last Modified: Tue, 12 Mar 2024 19:35:38 GMT  
		Size: 77.8 KB (77841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56f85cfb3cdcfcf570a86091c67c1657e158c68e0b97186ff78c791b16008ce`  
		Last Modified: Tue, 12 Mar 2024 19:35:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805f6eaf9f41b846f9a9a4e112f99e7a5a263583f91ff0f843e19459da572da6`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 53.7 MB (53699764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c688fdd5676f9300b17f0702cdb0b6fb0ba55c6916567d6ba7f87023f1092`  
		Last Modified: Tue, 12 Mar 2024 19:35:39 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00d1425e7f6da85549f5395f27906837a91a6033335c5d5d5062c3319158edd`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972716b5e7985a7a86e83b34383c5949b159078aa8fd71235d0c127f64f6065`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce0a5c75620215e0e6dd9864f3d801a9d3f6eca085b12e8eb92dcbc363a4dd9`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc9bc2208b953947418ae53feb245a1feb061a62345b5eaf876bb963caaf0ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fcf57039d5535a1529d2d686d9c0549dcde375dd1ea402804de5d2f6cb7974`

```dockerfile
```

-	Layers:
	-	`sha256:1de56ac16f12a1eae5b73fed95e5773b6b3f1cfcef1d14a705d4115d67219dd8`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 4.0 MB (3969386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b0841ee6c445fbcd02ca141fa48dc4c47a73bf04588f394a5d5ed926345bc4`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:0da3f2c45fe947e70c429ce6a80e489fc7af202bc7890539f81319aaf9e48e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86585706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04498e8701a99b1d9e284225ac887dac0f28b0ac5f2a0257d1c5b3f6708a203a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e121f5164f2335792d17befe564e4a4caf1dec33d5039c8245ce418144782215 in / 
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
	-	`sha256:840335d52e6c781c13aaaed8df36659831a5cb0747048da9bf578dd19a02b30e`  
		Last Modified: Tue, 12 Mar 2024 01:21:45 GMT  
		Size: 29.7 MB (29660245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc29d412a86c9bb1d3f309751aabf00a48127e9881e13951c317e94af85fd9b`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 3.3 KB (3347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a68cfae36a1f9b9177dbaa8e464778bdbfab63131398c63ef4a0120e7f8eaa`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 5.1 MB (5109274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49194257445d97cd95d18dfad61977dbe170d352aac7c9a6ed87faf3dbabdf28`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 357.5 KB (357476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cce9afe5b29ea6e53ec0a17ecd2c9a8d5b41981ceeda4087378a1fd2513adc7`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 77.8 KB (77817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39be4f4afc8fd3f4a0f0231127342c94aefacd8475ab4799a696dc8db62fdd9`  
		Last Modified: Tue, 12 Mar 2024 20:38:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e3bba10728d859dd4104f17048ac9e4b2b0a4e42969eb3e070828048018b2b`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 51.4 MB (51373301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59cc9a209cbe0d8ea4e6a4784bffbebf525d6c7ed1056e15ae9d9f4f51d1dea`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99300506f8cd321549fb6c67be4fc0bbe579bb10c6f1e284ed86d23a6c83dd5d`  
		Last Modified: Tue, 12 Mar 2024 20:38:38 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef61d060418410a198f7929b49f4364b6b52c5daaa090b205911f585c50b0569`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a102a80c253aae9e4afafc94115d5b80a38c15c1dafd012263460940e51725`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc2439ed0b9d225b49e7dcebb1dc57afbd8dad9b3ee1a334baedcb5058f9b639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af20321f5bb71925340f87452348321257292150a0ea4a50303abeaff27bda34`

```dockerfile
```

-	Layers:
	-	`sha256:6ac9c5ca993674968ed8fce38354e553a4ec9f24fe684b3e70223ac147d0bcc1`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 4.0 MB (3964424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e43a90811aeb106a69b953165e1ccbbae90a2a341815a5961edce992d3a1bde`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:7b60b651baacd33a8bc9cc9c048afb4aa81354681ebfae8bdd288d577e02bb57
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
$ docker pull couchdb@sha256:b30e6d23f4c4fe8a4b342eb574e371e3124b1e618ee2b368f6a9e2bb46553f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88286584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9481027d4e3eec91bcafb56ec50872bbdf5d4d23e68ff85be32362a9e8e8c362`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
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
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463acd6d68b4345c1eaa163bfd81d069ed7126d29cc7e3202f1063f90824412b`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41173148c73e8a129b29b9f540d64c8253a103cd95f3f851c59a676b0a22ffbb`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 5.2 MB (5208021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0677b4e15e3308d202ef2bec353dfbf59bc20bcf69033850af15cb605f71a689`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 350.5 KB (350543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9a4a5a0e4631055e487480267fbdf92ad450a5d2a356a12423ec1b94d72565`  
		Last Modified: Tue, 12 Mar 2024 14:36:21 GMT  
		Size: 77.8 KB (77785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544e5d6b202dd1fbb148536b5eaa5db07c4b9dfbc06a9a0d11893c1b454ca573`  
		Last Modified: Tue, 12 Mar 2024 14:36:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cba4a9a7e7fd947404e38d278b453c01d3cba852e1584dc9fce80fb8a59b0e`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 52.6 MB (52571512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373cc69b69ae865e6767eb5dee7ebddb1a6347c9d4ffa9ad1ee0fb180720f07c`  
		Last Modified: Tue, 12 Mar 2024 14:36:22 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8593b99b429341a6b0941b93a3d9ef64832a86654189f12637e340186f773b5`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6bb5429219bff94dc75fddb64f0e195934d3e066e0f88e66fe96d07208586c`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11eb3094a926106632c5c6a03439c59a3084027e8c804eabd1e4bcae53ce1baa`  
		Last Modified: Tue, 12 Mar 2024 14:36:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:61209dfc1ea8129540bc8f3f527bd9b0dc092919b4dac88120eecd8b431b066a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b666ad88071ab046dbdc71ce6abf82cc6b5169d9f1ac9812d4a471018b8082`

```dockerfile
```

-	Layers:
	-	`sha256:7a182b0fbf5f71fe0e5d506bc971cdcb07dcf9fc8f00277f98ddd4292d60a1e2`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 4.0 MB (3965094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f0dc84a2fc33f0506821127895c3d1f06d7d963ebad6fb2b9fd0bab6103fc60`  
		Last Modified: Tue, 12 Mar 2024 14:36:20 GMT  
		Size: 31.7 KB (31736 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:b8ff0acf04b78b8fea4b2b2ec74682d93e34f2aa2ca72fbeba02137c899f9a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95572353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce76029afa4c63d7555c64091961d489f80a7f70b966c8681f03d49ce466e090`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
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
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06cb2dd86e1b10e4634199f9c3973046ee081ce2e3b4eab364a1c0607b055f3`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39b71c2ca731395dff6754910b5f0f94dcbe5b1213f3efbc3c79e5e92b94e0d`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 6.0 MB (6042512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f039259cd371a1c4a2aaf5db8aa0329078dd4551a5eaf09db4389dfbf062e99c`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 446.7 KB (446656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc3f03b79aebe627023f165883fa4afb8d27a823bc1a95f87fac188bf29733d`  
		Last Modified: Tue, 12 Mar 2024 19:35:38 GMT  
		Size: 77.8 KB (77841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56f85cfb3cdcfcf570a86091c67c1657e158c68e0b97186ff78c791b16008ce`  
		Last Modified: Tue, 12 Mar 2024 19:35:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805f6eaf9f41b846f9a9a4e112f99e7a5a263583f91ff0f843e19459da572da6`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 53.7 MB (53699764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c688fdd5676f9300b17f0702cdb0b6fb0ba55c6916567d6ba7f87023f1092`  
		Last Modified: Tue, 12 Mar 2024 19:35:39 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00d1425e7f6da85549f5395f27906837a91a6033335c5d5d5062c3319158edd`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972716b5e7985a7a86e83b34383c5949b159078aa8fd71235d0c127f64f6065`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce0a5c75620215e0e6dd9864f3d801a9d3f6eca085b12e8eb92dcbc363a4dd9`  
		Last Modified: Tue, 12 Mar 2024 19:35:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc9bc2208b953947418ae53feb245a1feb061a62345b5eaf876bb963caaf0ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fcf57039d5535a1529d2d686d9c0549dcde375dd1ea402804de5d2f6cb7974`

```dockerfile
```

-	Layers:
	-	`sha256:1de56ac16f12a1eae5b73fed95e5773b6b3f1cfcef1d14a705d4115d67219dd8`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 4.0 MB (3969386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b0841ee6c445fbcd02ca141fa48dc4c47a73bf04588f394a5d5ed926345bc4`  
		Last Modified: Tue, 12 Mar 2024 19:35:37 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:0da3f2c45fe947e70c429ce6a80e489fc7af202bc7890539f81319aaf9e48e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86585706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04498e8701a99b1d9e284225ac887dac0f28b0ac5f2a0257d1c5b3f6708a203a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e121f5164f2335792d17befe564e4a4caf1dec33d5039c8245ce418144782215 in / 
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
	-	`sha256:840335d52e6c781c13aaaed8df36659831a5cb0747048da9bf578dd19a02b30e`  
		Last Modified: Tue, 12 Mar 2024 01:21:45 GMT  
		Size: 29.7 MB (29660245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc29d412a86c9bb1d3f309751aabf00a48127e9881e13951c317e94af85fd9b`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 3.3 KB (3347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a68cfae36a1f9b9177dbaa8e464778bdbfab63131398c63ef4a0120e7f8eaa`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 5.1 MB (5109274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49194257445d97cd95d18dfad61977dbe170d352aac7c9a6ed87faf3dbabdf28`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 357.5 KB (357476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cce9afe5b29ea6e53ec0a17ecd2c9a8d5b41981ceeda4087378a1fd2513adc7`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 77.8 KB (77817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39be4f4afc8fd3f4a0f0231127342c94aefacd8475ab4799a696dc8db62fdd9`  
		Last Modified: Tue, 12 Mar 2024 20:38:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e3bba10728d859dd4104f17048ac9e4b2b0a4e42969eb3e070828048018b2b`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 51.4 MB (51373301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59cc9a209cbe0d8ea4e6a4784bffbebf525d6c7ed1056e15ae9d9f4f51d1dea`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99300506f8cd321549fb6c67be4fc0bbe579bb10c6f1e284ed86d23a6c83dd5d`  
		Last Modified: Tue, 12 Mar 2024 20:38:38 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef61d060418410a198f7929b49f4364b6b52c5daaa090b205911f585c50b0569`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a102a80c253aae9e4afafc94115d5b80a38c15c1dafd012263460940e51725`  
		Last Modified: Tue, 12 Mar 2024 20:38:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc2439ed0b9d225b49e7dcebb1dc57afbd8dad9b3ee1a334baedcb5058f9b639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af20321f5bb71925340f87452348321257292150a0ea4a50303abeaff27bda34`

```dockerfile
```

-	Layers:
	-	`sha256:6ac9c5ca993674968ed8fce38354e553a4ec9f24fe684b3e70223ac147d0bcc1`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 4.0 MB (3964424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e43a90811aeb106a69b953165e1ccbbae90a2a341815a5961edce992d3a1bde`  
		Last Modified: Tue, 12 Mar 2024 20:38:37 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json
