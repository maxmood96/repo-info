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
$ docker pull couchdb@sha256:6e379b69ef063497b69ba661ccde4cf4b3a34a91590bd61e2f99ff224f8831d3
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
$ docker pull couchdb@sha256:54ea64f59140ac48e51ea0e4ad05f90fb25b4e1470813f6c2208749c6a1a6e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139837266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9d8ea0e34c17fbd7aa046bdd1e8ea8ce75b6416398d878d65716ba04906bf4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3418cd4354df70cbc3f38602bedf118bebf6f2c30eb20c8a1cff75e0aa68234`  
		Last Modified: Tue, 30 Sep 2025 00:12:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5391005848fcd8ff2646a5a5900b64ba4d7d0cfe038dc9f89a0d8e0cbcefe4`  
		Last Modified: Tue, 30 Sep 2025 00:12:22 GMT  
		Size: 7.9 MB (7881663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9db32416ea5b5afea586586f054427523267746b536cb29e2dbe9669ccb745`  
		Last Modified: Tue, 30 Sep 2025 00:12:20 GMT  
		Size: 401.7 KB (401728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2492e3d890071ea1e33b4a4207ce5b3d52b44fbcac60410da7c674a5064d9e03`  
		Last Modified: Tue, 30 Sep 2025 00:12:20 GMT  
		Size: 76.5 KB (76468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb89227f4334afe7e19fe773486ab061e31e1f377c2bf9fa5753928f89a4f750`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7085367bff1ed93af408f57da1c83d990c6a0ae30fd9ced462b24f875a20897b`  
		Last Modified: Tue, 30 Sep 2025 00:12:28 GMT  
		Size: 103.2 MB (103243645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f174ee6aee209409c8114bc72ad1758c501d95a81dc83aa084b6bdf19d416aa`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bce87f2ba00b097391b3c985f6e113e81ef897c07fc2dfc4d2e6a93be431f4f`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455a775b2896e1fd5a17e5b3fbd4e16ed4a542e62d18c10b15294ccf81ab72ae`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e55b231d664464cbed5e20983876ea36a77c03c2723f34562a8ffa80e8c900`  
		Last Modified: Tue, 30 Sep 2025 00:12:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d387798cc84de1a6a28dd67f1e0e867265a04d82ed33795502bc650cdc9b0ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c895b95d0b921282c241d5ea5ae1109d0520ed897feb0476002f18d3339068a`

```dockerfile
```

-	Layers:
	-	`sha256:b3c80834976cbe1a5b7c5225136abf4f695dd7da7f376f5d7d1b736b8b742443`  
		Last Modified: Wed, 01 Oct 2025 16:33:21 GMT  
		Size: 4.1 MB (4141252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58b99101a235b0a2e76591518d0a7b330f09b80b2a85cc30d87c259d089a03c`  
		Last Modified: Wed, 01 Oct 2025 16:33:22 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a5f50ef9185473caa7a8fb95bf13598080fc5f539ef293cd15ff2f577064019b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139156041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee3fbea99b66ccb49029e5fb94cb5780c99c90adb4c73ec0401c7567340b05b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b33cd8814a56bab74ff410b4b56ffbad6a20b281c4ccb06f104f1d7f547770`  
		Last Modified: Tue, 30 Sep 2025 00:15:24 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3602b49f923cadda7d2f38ca0128f279f6d1379a17255bfb4b723bc843c8ff6a`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 7.7 MB (7692013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c331624f091aa071757c2d474c4822c9d9272c541695e3469e273e1e38d13e15`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 370.5 KB (370482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ba805bd02d8f4eec7398e75afc0cf96d7aa4b75545233ab492a9fa18490b47`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 76.5 KB (76459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da439f569038fb1d6e0ef84bf99f7280dc6bc8f4447bd9e5e5bdf629684fc33`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a98295683d6e2d14d6acdfa40b2da8b19d989613acd5a9ee5be01c837d8970`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 102.9 MB (102909517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe36b689fece14435f6d7d3ee56e0e34ea97bad7c1e090f5a5b54c0d3c09d40`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119729afb3b66cf3cf9fc0fda3e9f8416d7bf7babafd2eb49458e55a9daf3914`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da64966d7ebb577c3a46ec8aa8105f2f30ceb8bc05eca7096c4e80bca6d4f84e`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82627e16d8266ef108b2050801e2c6f89046be99ee6c4b2419068e6288397d7`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:0f84646931e0e4f79e3e8484567f43e1a673e45a2a4f03161dd7f43472c67a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d57d8a1b66730c1d974cba58707e96dbda9d74e7feb4149c348f81ff53b325`

```dockerfile
```

-	Layers:
	-	`sha256:af6523121382afb86bfe9a78e5673b198a200a6b40f5810c9b7fc944b2209545`  
		Last Modified: Wed, 01 Oct 2025 13:33:43 GMT  
		Size: 4.1 MB (4141545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec563fe8deb456936f04f9c6259e7caa7faace44cdfba2f10500208bd32793e9`  
		Last Modified: Wed, 01 Oct 2025 13:33:44 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:49bd43791b2a8e90981f81cc3df862a2e78c98a0839a7adebad718b0fab80a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136535368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7cd1181fa41367e88cffce0088ddf91c8158c2ae6f1e7c4965d9c12cca0154`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc974b68a96cb9613948be41d48c95b11256922ec30ed86ff522d7ed43538893`  
		Last Modified: Tue, 09 Sep 2025 01:15:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cdcab67f7535323419e032c49994a3856a03aa211325df57144390a3d9d585`  
		Last Modified: Tue, 09 Sep 2025 07:29:38 GMT  
		Size: 7.4 MB (7398124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a1e5f2d33d1a152a120b4dccfbb324269caf8fb32a5043c35809e100ca760b`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 372.1 KB (372092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a872688d6492057aac594611cfc5b625c0e1e1a7ff940617f997704169e9995`  
		Last Modified: Tue, 09 Sep 2025 01:15:02 GMT  
		Size: 76.5 KB (76474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a3f6b7373136c1cb2d1298a2d2f73413c7b8f547d35ffb8b50ca04a1addd1b`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2cbab153673e0482891bf1c9bd2ae59af2229ffdba923fd4789ad884a290d4`  
		Last Modified: Tue, 09 Sep 2025 07:29:53 GMT  
		Size: 101.8 MB (101798944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff04489a55fe042596b0d31824144d0eb4e70e1140495a620275221c5395e3d8`  
		Last Modified: Tue, 09 Sep 2025 01:15:07 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d0a12528ee99fe8d84804d62582d8440c541959f08c04052ec6684c99cfdaf`  
		Last Modified: Tue, 09 Sep 2025 01:15:02 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655b820b4aa315ce76b890ac016a6099ad5c702d6cd2f58293d9e15235f02c84`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df33dbb0f88bbbc18112e2a368427ae82f1cb89828735d1cd23fc406b2382a9`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:0d542ff2e1e509d8aefffabaab664ce35e73ca259f0f4a7706c1b9cc33dac89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c97c25ab13bfd1feb8017ad6f5bcc4f2073a7ff0adfc8c09a051c69e559ad49`

```dockerfile
```

-	Layers:
	-	`sha256:7aafde54b4d5a7fde65f62567e3ddc218904048738582917347f388ab9b55de9`  
		Last Modified: Tue, 09 Sep 2025 01:33:25 GMT  
		Size: 4.1 MB (4137448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05d2f4c4ba9d7760c0f1710ce711c32bc1d2652360873595fc7f48a5aa8af43`  
		Last Modified: Tue, 09 Sep 2025 01:33:26 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:3d0bf6e5ed7eec87a0c49bd007cf0c44ea0baa4e89f1a91e54365688839d4ad9
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
$ docker pull couchdb@sha256:715fb9dce1716897b071b86d6653c62b72bdc024668ac53f4d5a883e2f0fd284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135fc9b4d69ecc10e0ae388cdf0ef9565967ac625932a7d92152b2da726ac25e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb50c07b2ef11a8ec1f0607bf6c9513aab386bcf59ac8797c85a56990b51de8`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672f458973f11333cea934aa85e060219715efc84aea49c2f600ff572614332f`  
		Last Modified: Tue, 30 Sep 2025 00:12:33 GMT  
		Size: 7.9 MB (7881684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f63af8926750c43e6aedbe6c076b618771816c759507186d67a8bb8bea03bc`  
		Last Modified: Tue, 30 Sep 2025 00:12:39 GMT  
		Size: 77.3 MB (77326979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f45fb8f7ea6edb0bada78e12142ff68a4638979af8d64a7a9fc421ac551222`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 424.1 KB (424065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f04a4c53df1a57663873195756adc16ab07078bed90ce0bc2dbd11a10aebb`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 99.5 KB (99492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b52fa3e91ddd7e8e960ea90ed0b34b4338656ab877b706a2f01b3e71e035b7`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cda19eab3e8a24e603dba796758b4de017fcdd4cd3c8316ad2ec1e4c6148ed`  
		Last Modified: Tue, 30 Sep 2025 00:12:36 GMT  
		Size: 42.4 MB (42436193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7bf39ca98400552895af79ee20571e2ce575080e996cdb7fad59ce118075e`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc1c0619a8d6b9adf17be170ea3977b599528321798edfbb2e9e94074acea196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1820c22fef622289211a17c279495101ed3a6ed988edf0ee919e7b075b459f71`

```dockerfile
```

-	Layers:
	-	`sha256:4940a7adacc757e5d4fa22bfab225fbbf79da6db12c33158d4ff21c39b41cd69`  
		Last Modified: Wed, 01 Oct 2025 16:33:27 GMT  
		Size: 3.7 MB (3658049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74a75fce6a7f3411ed1381c11e952821ff85cdd27bd48779b00a661242e1731b`  
		Last Modified: Wed, 01 Oct 2025 16:33:29 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8542f71de8d3fb3656fc658237d00cd3326b672be16aa511faa72cd73349e9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155279477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fea46598ff3c12fbb18a93356fb4e11002376dac93fcd7b8c482348e2326d19`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489eed97204181f5e217407f1a76b144c156604dc67a6dfc83772858b681909d`  
		Last Modified: Tue, 30 Sep 2025 00:16:17 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398f5c46545ac256be1c07670b8511b33ec736953a1ee232d54e45c97517e989`  
		Last Modified: Tue, 30 Sep 2025 00:16:18 GMT  
		Size: 7.7 MB (7692022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a36a56fa00a8b81c6f5174c1e2bcaf2c271b89d0db2b702deb25d0a540e74b9`  
		Last Modified: Tue, 30 Sep 2025 00:16:36 GMT  
		Size: 76.7 MB (76652777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242ca2e029ce153691a4ed49f49b5c6a42c7bd24f855b741b54d050c3bef6c64`  
		Last Modified: Tue, 30 Sep 2025 00:16:16 GMT  
		Size: 392.7 KB (392709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f12c3da0de9727bf448a75a923636574adebeda03e50b2de7487632148e9fb`  
		Last Modified: Tue, 30 Sep 2025 00:16:16 GMT  
		Size: 99.5 KB (99460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40de999fb52303ca5bb3d6a21b74101d81982b90ea093bc72b9e31f26dd1f9d4`  
		Last Modified: Tue, 30 Sep 2025 00:16:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d147f495a50a75ae53283b9ae24a72b9b0ae1e7f2f1a615e8b858734b16d27`  
		Last Modified: Tue, 30 Sep 2025 00:16:19 GMT  
		Size: 42.3 MB (42338490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d91e04c7ac1fe428bba250821315ee73121fdc2c85a866364555bb8e5b87ce3`  
		Last Modified: Tue, 30 Sep 2025 00:16:16 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:ca56e281523d5438b66575e9f17af770c9067e4622b4f582955013f4e6b7bfa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97a40531d51b5ff3255ee4e9c2d6ed3c52b621fbca7762b93b4d6834eacb0b0`

```dockerfile
```

-	Layers:
	-	`sha256:dd59bc16a77dc54d6e331c00eee168bd496feff198737389aefb35732081fe6c`  
		Last Modified: Wed, 01 Oct 2025 13:33:22 GMT  
		Size: 3.7 MB (3656725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0237fa1d440e21dd89dd1db0e1118579d70afa8f4d19569bad1b81bca09bcd`  
		Last Modified: Wed, 01 Oct 2025 13:33:23 GMT  
		Size: 24.7 KB (24744 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:e4d95a8569f0563080c1d34e55235699562145f94dbb121588bf81e8c02e7cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150040910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d4fbe2bdd8a68b87cb0e856db9a6509bf54e915f3a49022c73dedc224eff11`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6660c0849f31015adaa92ce7a5301c2e4989720f60b06c3a3337bb458626ee5b`  
		Last Modified: Tue, 09 Sep 2025 01:15:00 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a2c699e296fd038b13d9ebc990c2c25f01034c23f71945a946512c166006d1`  
		Last Modified: Tue, 09 Sep 2025 01:22:29 GMT  
		Size: 7.4 MB (7398150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0141fc5fd220a0e8342d747d29d994c7da8eec8b3ba9ed10e7865fca70bca801`  
		Last Modified: Tue, 09 Sep 2025 01:22:24 GMT  
		Size: 73.1 MB (73099278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e154f3d3148c1109f04cd74f222cf566b1f7655c15f091471bc3c43519ea46`  
		Last Modified: Tue, 09 Sep 2025 01:14:59 GMT  
		Size: 394.4 KB (394399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1e4fc22f332be1a66c12c5045cba6ef0ccf5802ebc43cf79a99f0e94976c63`  
		Last Modified: Tue, 09 Sep 2025 01:15:00 GMT  
		Size: 99.6 KB (99601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a6c6b7a5b02bb21d0f41b4fb3c7beeec1b6343876dff2c10c8644f45fd7ed7`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddeb7ded7819c3dc9e616172a7d225fa689c613ed6e7d3a527dc8d5b9cff035`  
		Last Modified: Tue, 09 Sep 2025 19:03:45 GMT  
		Size: 42.2 MB (42163302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e61ca25d28292bbb2d871373142dd9ba5430a8f3605cae2b310f1c11fdc3aea`  
		Last Modified: Tue, 09 Sep 2025 01:14:59 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f803328ecad04363b00ec2e59440b5d8688e40835d58996f9cc7adda3b96eb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd548e5f239560e2a07fae13608afd965209f67cf8fe0ecff5616fee6c6d98bb`

```dockerfile
```

-	Layers:
	-	`sha256:3f5c205a784e5f94f3d57a81b1d70b835ab4bfd32578c13a8dfea8e5d784c59a`  
		Last Modified: Tue, 09 Sep 2025 01:33:30 GMT  
		Size: 3.6 MB (3648578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49bc1fd01154ed011d1bb4588847d645f16a941f5ff24b8e2e2929b7f90e362c`  
		Last Modified: Tue, 09 Sep 2025 01:33:31 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:5eabecb58b3e312cec8286055d18f81431a38ac9ee379c13ac7cc5f35b2c0743
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
$ docker pull couchdb@sha256:d818821ea1a59821b7aae88c2249438400bc35869442457ad05cc868d86eed38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139014593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739ede85f41005213569149c16fbaaa4dd28844b201cef997df2376932ff6bd6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b98c0c00f0a1060b4198ac7a418d55f630d5c7268cc8a64930b523752d6cd2`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f20d4423551f7c8aa4c26ebb8976b9f6d047388e277d3318126b4e1cdafb47`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 7.9 MB (7881732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f074d0e991ec0b7340663f1adb85da86580810846a29fa91293ffda1c67c7b`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 401.7 KB (401715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0de04b92b75bcf8fc18b8199735a8c7220064c1cd76f5bd997e974ed15a9009`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 76.5 KB (76477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026b0513493b8732a3feff3890ee8e77a6c3ddb4b915679c87e6b57ce2af062e`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792a419a0fa60eace7af64d500ca3f0e8f6a6236207696a5d2f08e5e6c47912d`  
		Last Modified: Tue, 30 Sep 2025 00:12:40 GMT  
		Size: 102.4 MB (102420900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986d3b4c7c3ec410a91de6e27c5ea40d0c44463431d5469013a9550744b1e35c`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2544c6098f7071c44b1a98a08255652653b93d5da51d3513d026c4718f6e3e`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5176ccaec1817f8cf00c77f17ce637836e3202812982bbd691af054aae72ac`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9edbc96a2c5ba4e9cce6e86ee2948f4f0bf809144dd81dd29d040551599ec1`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:ef92616adbfbfc6be351e56db9f6a2d3e128fb938842ede2224051db50bc02a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd9eb8661597073da5d6b4de259f9beac6cdafe809199666a3283412306265a`

```dockerfile
```

-	Layers:
	-	`sha256:dc687b5d8a6285266f88f84c79cd921f6fd9aedce02134ce0b1bff9dfac67cd1`  
		Last Modified: Wed, 01 Oct 2025 16:33:32 GMT  
		Size: 4.1 MB (4125385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29230abcaa308cc75b2bf53dac18169c7ccc97045075411e3acb8803d071f483`  
		Last Modified: Wed, 01 Oct 2025 16:33:32 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e7a929414ebe11923d3e30ee3cc77451ad03f141841dbe65d70e8a35ebaeed8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138415567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1122fba6710ec88442253c75d5d688d92a1a945b0cc5aec876995353aed78337`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e681e76652650947dc6636dd1083467fd6cec192fde42436dee56b826b62587`  
		Last Modified: Mon, 08 Sep 2025 22:08:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bd0682b96f54a508d2cbecd22fb38e255292a9fafd6cf0966dc478351b4054`  
		Last Modified: Mon, 08 Sep 2025 23:54:46 GMT  
		Size: 7.7 MB (7692034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f387444f2640f17b78a1c1df2b6d3859e666a3d360a69c6d65918891c2221f63`  
		Last Modified: Mon, 08 Sep 2025 22:08:09 GMT  
		Size: 370.5 KB (370475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b17371b9447ff820de8fd6fd6693ddbd5367a564db29ca89dabc2cd2396cc05`  
		Last Modified: Mon, 08 Sep 2025 22:08:13 GMT  
		Size: 76.5 KB (76486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f89150d0dc57657fb1a33b2994866117d69d8186b93f485773c070170f307c`  
		Last Modified: Mon, 08 Sep 2025 22:08:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f08adfe279c16807d2c089c0f5c3e54400d986a20983d62f5d528251d60e1`  
		Last Modified: Mon, 08 Sep 2025 23:54:55 GMT  
		Size: 102.2 MB (102169053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beef007f03abc6287b8101fe9f5e4bad48c67be33f09a08dbe7f3c035491fa2d`  
		Last Modified: Mon, 08 Sep 2025 22:08:19 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ade1ffa2c8c4f4cc2573b469e9d84ba6ceaa3cdf350b4116b58fcb303f5fff1`  
		Last Modified: Mon, 08 Sep 2025 22:08:23 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fcc82e1cc737dcf13a886254145e6a133512c24c90f7ea0cf1043b8bd3b3ff`  
		Last Modified: Mon, 08 Sep 2025 22:08:27 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fb16cbf1e6dc1b964638489f1cce3527a07103f36add49319d6b85efa31fe5`  
		Last Modified: Mon, 08 Sep 2025 22:08:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:be5c9d823dec75d99a4a3bfd8906de5a87ff98cf7dee562545b61da23bb7965f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e9067ed12180e7773451ae04b7ac9ec299f31a324a6381854065ef8a3982bb`

```dockerfile
```

-	Layers:
	-	`sha256:82c51fdac884ce31b1210d38c792c7224ff142e416b56c6ffb83196d2032ab74`  
		Last Modified: Mon, 08 Sep 2025 22:33:47 GMT  
		Size: 4.1 MB (4125654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dec1fefee7902db14a0fdbdbded49b4cd2a8cbdd4c3df22dd2581b4eee76226`  
		Last Modified: Mon, 08 Sep 2025 22:33:48 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:e4bacebc79c22dedcf60457622664e44dd267109bf1df3efe034de98cccea103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135792704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f094599e44ad6c6b247c0bbc09dc4f99e42f648344f0244c2fe7dfcded574047`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc974b68a96cb9613948be41d48c95b11256922ec30ed86ff522d7ed43538893`  
		Last Modified: Tue, 09 Sep 2025 01:15:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cdcab67f7535323419e032c49994a3856a03aa211325df57144390a3d9d585`  
		Last Modified: Tue, 09 Sep 2025 07:29:38 GMT  
		Size: 7.4 MB (7398124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a1e5f2d33d1a152a120b4dccfbb324269caf8fb32a5043c35809e100ca760b`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 372.1 KB (372092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a872688d6492057aac594611cfc5b625c0e1e1a7ff940617f997704169e9995`  
		Last Modified: Tue, 09 Sep 2025 01:15:02 GMT  
		Size: 76.5 KB (76474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f29cfec10ed6860568166256c08c200b1f295424ab2d050c8af5633b2927888`  
		Last Modified: Tue, 09 Sep 2025 01:17:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45710fa6cc0aede8d29111fe36b799cd46ed394aeafd554a760bbcf5ea64f548`  
		Last Modified: Wed, 10 Sep 2025 10:25:58 GMT  
		Size: 101.1 MB (101056287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3a274d6df1748d6d76ceaaf659889ce9f62d78542b84cdc1242c53bfdd94c6`  
		Last Modified: Tue, 09 Sep 2025 01:17:38 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ca416d30eb2e5f16492285f385742ac7025083ff27fb7cf32fd78cfb39a65`  
		Last Modified: Tue, 09 Sep 2025 01:17:41 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8562823a9ea056ad34cb775718860340ee67d3f6d6383d9167768ada81c791a`  
		Last Modified: Tue, 09 Sep 2025 01:17:44 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705543bcea624f858e3d9083333ceb97329e19c529e5bc0ca9b97d35892dabdb`  
		Last Modified: Tue, 09 Sep 2025 01:17:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:abdbb0c74d45b24ce58798c16671acca14fc0ce26a593c6273ca8454ee792c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57750011fd468beddc797e9e55613db91ff5ef94902558b07a795acc17d94cb`

```dockerfile
```

-	Layers:
	-	`sha256:bed0a93041da23423f26e4cf9ee20b6e7a0c367476fd4486cf59c7d9ed268aeb`  
		Last Modified: Tue, 09 Sep 2025 01:33:38 GMT  
		Size: 4.1 MB (4121581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6373190c09b950a931a22529d7fb7fe27cd381663dde7a73eef46911e25aad1`  
		Last Modified: Tue, 09 Sep 2025 01:33:40 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:cbcba1660f79cc709947f0613e04a2157a17ef88b504f953bbcea7f45f4765ed
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
$ docker pull couchdb@sha256:4aafb6d158b7acac0f3235bbff7049960fa3b16036346db8d71f07414671f7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7c139e388392f34b2092ac3ae483c2c3fc3155357df27638bdafbad8897293`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea7ac9d82cd9f0ff2d527237df18204fc88c48e5d938752697e386c7b3e0de4`  
		Last Modified: Tue, 30 Sep 2025 00:12:36 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567f53fe966743c3ceb69b6788dfff47bfc8a772ca818c55e9e20b27aabe2b3b`  
		Last Modified: Tue, 30 Sep 2025 00:12:39 GMT  
		Size: 7.9 MB (7881688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73903c84e483f8f44c8453668197c85a6aafd1a3e3db68f9a9a6333f9b4d46ab`  
		Last Modified: Tue, 30 Sep 2025 00:12:45 GMT  
		Size: 77.3 MB (77326920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a64f9afe598d165381a8bce28dbc989456b87b7d40e134158c6c6b62d819a8`  
		Last Modified: Tue, 30 Sep 2025 00:12:39 GMT  
		Size: 424.1 KB (424077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb55c3b6a56854fe32123c27006b70d6ed6d8268f5e677704708a56668fd2ab`  
		Last Modified: Tue, 30 Sep 2025 00:12:39 GMT  
		Size: 99.5 KB (99492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04c770023f89e5185b0c77716d8faca0e0203807e1988b159667392dcd4d609`  
		Last Modified: Tue, 30 Sep 2025 00:12:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf51266099e2d36b45136037ce88bf7e88b687ef82a8d3d6ed07ab11e64afc14`  
		Last Modified: Tue, 30 Sep 2025 00:12:45 GMT  
		Size: 42.4 MB (42435992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d058e2fdc753529aac469614cc3f97b4b750b568951381b2f0553df30c30eaf`  
		Last Modified: Tue, 30 Sep 2025 00:12:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:fce4d19b56b3983d784267d1a49066ca947b18f966e55379941f07128ba75942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92949cf40dfb1275624357f562cf8342a0d5ce341030917ec852dfaeec2f82b8`

```dockerfile
```

-	Layers:
	-	`sha256:d98d379475cf0fa1c2c752652c8348657e50065abd3a6b69dddc1cb9c19d2b89`  
		Last Modified: Wed, 01 Oct 2025 16:33:42 GMT  
		Size: 3.7 MB (3657743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40039a836122d13dcbf5da6de47e1c44f3253aa20ce55c56cbf21c2cff998be5`  
		Last Modified: Wed, 01 Oct 2025 16:33:43 GMT  
		Size: 24.3 KB (24257 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:872f74a4ad321c4093c83c5456464619ba20a6b27986eb25181bc9dd1d0665dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155278867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4651dc71462f40ee4390e3a3395c8b1e3f27e7eaad4b4b7fab4cb44fbce2d75`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482bd44b4f4187bcf8730a04e6fb3959048bebefa44d548dcf7b606b275acd51`  
		Last Modified: Tue, 30 Sep 2025 00:16:24 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4881f269405b8c4499a62ca468333e347ef9fffe077e0f795d9273c9d745111f`  
		Last Modified: Tue, 30 Sep 2025 00:16:28 GMT  
		Size: 7.7 MB (7691958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de77d0139936cd1d9e6352dc14c6c0af38108573e6f12eafbed1bac97236851c`  
		Last Modified: Tue, 30 Sep 2025 00:16:51 GMT  
		Size: 76.7 MB (76652737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4542805c16f4a83a13ecba8e3aa410e0a64136e542f5721df3d84a90f9d66b3c`  
		Last Modified: Tue, 30 Sep 2025 00:16:24 GMT  
		Size: 392.7 KB (392690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2a616b65292ab74d2f1b8295e950c7d17e9336f8a49aa47ef1af4731f3f7c`  
		Last Modified: Tue, 30 Sep 2025 00:16:25 GMT  
		Size: 99.4 KB (99442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a241368c4be77d144064e430f3947ce99bbbdebe8745dc47e7689f460598d5e`  
		Last Modified: Tue, 30 Sep 2025 00:16:25 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa031d107652e0b7655997675f2f9170cbf9060992195a20aabd0bf8f86589e`  
		Last Modified: Tue, 30 Sep 2025 00:16:27 GMT  
		Size: 42.3 MB (42338022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d49ea83005436c32868106479aa2fb30c432ab05ae2e443c6efd1c8bb46648`  
		Last Modified: Tue, 30 Sep 2025 00:16:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:4caf2d49d72163b397bdf15d4abf3106f4b0f2f17b1bd1ea365efcc3bda50804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9cf08ea9faffc213b5e887b441454522c35fb39cc293ff209b28213bd7cc4b4`

```dockerfile
```

-	Layers:
	-	`sha256:895f067ba433e1875b15731c9d6f2109324d65b8f4376f82b5ab99f24d164f6a`  
		Last Modified: Wed, 01 Oct 2025 13:33:29 GMT  
		Size: 3.7 MB (3656407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb6952131e64a4250e965937752bd408b94c149aa2ead61dca413bdfb8186eba`  
		Last Modified: Wed, 01 Oct 2025 13:33:30 GMT  
		Size: 24.4 KB (24428 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:09f23e6d75404823da8b9dcfb79fc12b7b140121724a081d075ca5ab0bf19ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150040583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936212f001204d780eeab9f0c04bac9dfdb72f019f487587745e2406ac787513`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6660c0849f31015adaa92ce7a5301c2e4989720f60b06c3a3337bb458626ee5b`  
		Last Modified: Tue, 09 Sep 2025 01:15:00 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a2c699e296fd038b13d9ebc990c2c25f01034c23f71945a946512c166006d1`  
		Last Modified: Tue, 09 Sep 2025 01:22:29 GMT  
		Size: 7.4 MB (7398150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0141fc5fd220a0e8342d747d29d994c7da8eec8b3ba9ed10e7865fca70bca801`  
		Last Modified: Tue, 09 Sep 2025 01:22:24 GMT  
		Size: 73.1 MB (73099278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e154f3d3148c1109f04cd74f222cf566b1f7655c15f091471bc3c43519ea46`  
		Last Modified: Tue, 09 Sep 2025 01:14:59 GMT  
		Size: 394.4 KB (394399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1e4fc22f332be1a66c12c5045cba6ef0ccf5802ebc43cf79a99f0e94976c63`  
		Last Modified: Tue, 09 Sep 2025 01:15:00 GMT  
		Size: 99.6 KB (99601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a6c6b7a5b02bb21d0f41b4fb3c7beeec1b6343876dff2c10c8644f45fd7ed7`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7176a933c215f6f17587c905de26bc59d2f5180409436fce5450b4ebfb1c2e`  
		Last Modified: Tue, 09 Sep 2025 01:22:41 GMT  
		Size: 42.2 MB (42162975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3abac53ffac62f63f56ab09b5e92b0c2e41161e910aca49535c4fca44eca175`  
		Last Modified: Tue, 09 Sep 2025 01:19:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:3d894ee1c0283585d1b64b37fb48ecdf1022799f1b4e5944c38c2ebc02ba1c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c604b583dba83cfe4f26b9ff066aaa4e6c20dec1730648cd33adbdce3ba17e82`

```dockerfile
```

-	Layers:
	-	`sha256:2e80bdfbe65ad20629d67fb2b63684d4194a080ddd69715f89831e0951dfec93`  
		Last Modified: Tue, 09 Sep 2025 01:33:41 GMT  
		Size: 3.6 MB (3648272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87e3c22012be7b015f22534e916168a47b8292b2547a707477cd808ba247287`  
		Last Modified: Tue, 09 Sep 2025 01:33:43 GMT  
		Size: 24.3 KB (24258 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:5eabecb58b3e312cec8286055d18f81431a38ac9ee379c13ac7cc5f35b2c0743
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
$ docker pull couchdb@sha256:d818821ea1a59821b7aae88c2249438400bc35869442457ad05cc868d86eed38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139014593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739ede85f41005213569149c16fbaaa4dd28844b201cef997df2376932ff6bd6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b98c0c00f0a1060b4198ac7a418d55f630d5c7268cc8a64930b523752d6cd2`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f20d4423551f7c8aa4c26ebb8976b9f6d047388e277d3318126b4e1cdafb47`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 7.9 MB (7881732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f074d0e991ec0b7340663f1adb85da86580810846a29fa91293ffda1c67c7b`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 401.7 KB (401715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0de04b92b75bcf8fc18b8199735a8c7220064c1cd76f5bd997e974ed15a9009`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 76.5 KB (76477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026b0513493b8732a3feff3890ee8e77a6c3ddb4b915679c87e6b57ce2af062e`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792a419a0fa60eace7af64d500ca3f0e8f6a6236207696a5d2f08e5e6c47912d`  
		Last Modified: Tue, 30 Sep 2025 00:12:40 GMT  
		Size: 102.4 MB (102420900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986d3b4c7c3ec410a91de6e27c5ea40d0c44463431d5469013a9550744b1e35c`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2544c6098f7071c44b1a98a08255652653b93d5da51d3513d026c4718f6e3e`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5176ccaec1817f8cf00c77f17ce637836e3202812982bbd691af054aae72ac`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9edbc96a2c5ba4e9cce6e86ee2948f4f0bf809144dd81dd29d040551599ec1`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ef92616adbfbfc6be351e56db9f6a2d3e128fb938842ede2224051db50bc02a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd9eb8661597073da5d6b4de259f9beac6cdafe809199666a3283412306265a`

```dockerfile
```

-	Layers:
	-	`sha256:dc687b5d8a6285266f88f84c79cd921f6fd9aedce02134ce0b1bff9dfac67cd1`  
		Last Modified: Wed, 01 Oct 2025 16:33:32 GMT  
		Size: 4.1 MB (4125385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29230abcaa308cc75b2bf53dac18169c7ccc97045075411e3acb8803d071f483`  
		Last Modified: Wed, 01 Oct 2025 16:33:32 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e7a929414ebe11923d3e30ee3cc77451ad03f141841dbe65d70e8a35ebaeed8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138415567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1122fba6710ec88442253c75d5d688d92a1a945b0cc5aec876995353aed78337`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e681e76652650947dc6636dd1083467fd6cec192fde42436dee56b826b62587`  
		Last Modified: Mon, 08 Sep 2025 22:08:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bd0682b96f54a508d2cbecd22fb38e255292a9fafd6cf0966dc478351b4054`  
		Last Modified: Mon, 08 Sep 2025 23:54:46 GMT  
		Size: 7.7 MB (7692034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f387444f2640f17b78a1c1df2b6d3859e666a3d360a69c6d65918891c2221f63`  
		Last Modified: Mon, 08 Sep 2025 22:08:09 GMT  
		Size: 370.5 KB (370475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b17371b9447ff820de8fd6fd6693ddbd5367a564db29ca89dabc2cd2396cc05`  
		Last Modified: Mon, 08 Sep 2025 22:08:13 GMT  
		Size: 76.5 KB (76486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f89150d0dc57657fb1a33b2994866117d69d8186b93f485773c070170f307c`  
		Last Modified: Mon, 08 Sep 2025 22:08:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f08adfe279c16807d2c089c0f5c3e54400d986a20983d62f5d528251d60e1`  
		Last Modified: Mon, 08 Sep 2025 23:54:55 GMT  
		Size: 102.2 MB (102169053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beef007f03abc6287b8101fe9f5e4bad48c67be33f09a08dbe7f3c035491fa2d`  
		Last Modified: Mon, 08 Sep 2025 22:08:19 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ade1ffa2c8c4f4cc2573b469e9d84ba6ceaa3cdf350b4116b58fcb303f5fff1`  
		Last Modified: Mon, 08 Sep 2025 22:08:23 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fcc82e1cc737dcf13a886254145e6a133512c24c90f7ea0cf1043b8bd3b3ff`  
		Last Modified: Mon, 08 Sep 2025 22:08:27 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fb16cbf1e6dc1b964638489f1cce3527a07103f36add49319d6b85efa31fe5`  
		Last Modified: Mon, 08 Sep 2025 22:08:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:be5c9d823dec75d99a4a3bfd8906de5a87ff98cf7dee562545b61da23bb7965f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e9067ed12180e7773451ae04b7ac9ec299f31a324a6381854065ef8a3982bb`

```dockerfile
```

-	Layers:
	-	`sha256:82c51fdac884ce31b1210d38c792c7224ff142e416b56c6ffb83196d2032ab74`  
		Last Modified: Mon, 08 Sep 2025 22:33:47 GMT  
		Size: 4.1 MB (4125654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dec1fefee7902db14a0fdbdbded49b4cd2a8cbdd4c3df22dd2581b4eee76226`  
		Last Modified: Mon, 08 Sep 2025 22:33:48 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:e4bacebc79c22dedcf60457622664e44dd267109bf1df3efe034de98cccea103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135792704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f094599e44ad6c6b247c0bbc09dc4f99e42f648344f0244c2fe7dfcded574047`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc974b68a96cb9613948be41d48c95b11256922ec30ed86ff522d7ed43538893`  
		Last Modified: Tue, 09 Sep 2025 01:15:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cdcab67f7535323419e032c49994a3856a03aa211325df57144390a3d9d585`  
		Last Modified: Tue, 09 Sep 2025 07:29:38 GMT  
		Size: 7.4 MB (7398124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a1e5f2d33d1a152a120b4dccfbb324269caf8fb32a5043c35809e100ca760b`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 372.1 KB (372092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a872688d6492057aac594611cfc5b625c0e1e1a7ff940617f997704169e9995`  
		Last Modified: Tue, 09 Sep 2025 01:15:02 GMT  
		Size: 76.5 KB (76474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f29cfec10ed6860568166256c08c200b1f295424ab2d050c8af5633b2927888`  
		Last Modified: Tue, 09 Sep 2025 01:17:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45710fa6cc0aede8d29111fe36b799cd46ed394aeafd554a760bbcf5ea64f548`  
		Last Modified: Wed, 10 Sep 2025 10:25:58 GMT  
		Size: 101.1 MB (101056287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3a274d6df1748d6d76ceaaf659889ce9f62d78542b84cdc1242c53bfdd94c6`  
		Last Modified: Tue, 09 Sep 2025 01:17:38 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ca416d30eb2e5f16492285f385742ac7025083ff27fb7cf32fd78cfb39a65`  
		Last Modified: Tue, 09 Sep 2025 01:17:41 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8562823a9ea056ad34cb775718860340ee67d3f6d6383d9167768ada81c791a`  
		Last Modified: Tue, 09 Sep 2025 01:17:44 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705543bcea624f858e3d9083333ceb97329e19c529e5bc0ca9b97d35892dabdb`  
		Last Modified: Tue, 09 Sep 2025 01:17:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:abdbb0c74d45b24ce58798c16671acca14fc0ce26a593c6273ca8454ee792c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57750011fd468beddc797e9e55613db91ff5ef94902558b07a795acc17d94cb`

```dockerfile
```

-	Layers:
	-	`sha256:bed0a93041da23423f26e4cf9ee20b6e7a0c367476fd4486cf59c7d9ed268aeb`  
		Last Modified: Tue, 09 Sep 2025 01:33:38 GMT  
		Size: 4.1 MB (4121581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6373190c09b950a931a22529d7fb7fe27cd381663dde7a73eef46911e25aad1`  
		Last Modified: Tue, 09 Sep 2025 01:33:40 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:313b7e8fc5e2a7a59d0f8642c655e69515f8d0c20f663de24272313ded73cf8e
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
$ docker pull couchdb@sha256:4aafb6d158b7acac0f3235bbff7049960fa3b16036346db8d71f07414671f7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7c139e388392f34b2092ac3ae483c2c3fc3155357df27638bdafbad8897293`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea7ac9d82cd9f0ff2d527237df18204fc88c48e5d938752697e386c7b3e0de4`  
		Last Modified: Tue, 30 Sep 2025 00:12:36 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567f53fe966743c3ceb69b6788dfff47bfc8a772ca818c55e9e20b27aabe2b3b`  
		Last Modified: Tue, 30 Sep 2025 00:12:39 GMT  
		Size: 7.9 MB (7881688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73903c84e483f8f44c8453668197c85a6aafd1a3e3db68f9a9a6333f9b4d46ab`  
		Last Modified: Tue, 30 Sep 2025 00:12:45 GMT  
		Size: 77.3 MB (77326920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a64f9afe598d165381a8bce28dbc989456b87b7d40e134158c6c6b62d819a8`  
		Last Modified: Tue, 30 Sep 2025 00:12:39 GMT  
		Size: 424.1 KB (424077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb55c3b6a56854fe32123c27006b70d6ed6d8268f5e677704708a56668fd2ab`  
		Last Modified: Tue, 30 Sep 2025 00:12:39 GMT  
		Size: 99.5 KB (99492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04c770023f89e5185b0c77716d8faca0e0203807e1988b159667392dcd4d609`  
		Last Modified: Tue, 30 Sep 2025 00:12:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf51266099e2d36b45136037ce88bf7e88b687ef82a8d3d6ed07ab11e64afc14`  
		Last Modified: Tue, 30 Sep 2025 00:12:45 GMT  
		Size: 42.4 MB (42435992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d058e2fdc753529aac469614cc3f97b4b750b568951381b2f0553df30c30eaf`  
		Last Modified: Tue, 30 Sep 2025 00:12:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:fce4d19b56b3983d784267d1a49066ca947b18f966e55379941f07128ba75942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92949cf40dfb1275624357f562cf8342a0d5ce341030917ec852dfaeec2f82b8`

```dockerfile
```

-	Layers:
	-	`sha256:d98d379475cf0fa1c2c752652c8348657e50065abd3a6b69dddc1cb9c19d2b89`  
		Last Modified: Wed, 01 Oct 2025 16:33:42 GMT  
		Size: 3.7 MB (3657743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40039a836122d13dcbf5da6de47e1c44f3253aa20ce55c56cbf21c2cff998be5`  
		Last Modified: Wed, 01 Oct 2025 16:33:43 GMT  
		Size: 24.3 KB (24257 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:872f74a4ad321c4093c83c5456464619ba20a6b27986eb25181bc9dd1d0665dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155278867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4651dc71462f40ee4390e3a3395c8b1e3f27e7eaad4b4b7fab4cb44fbce2d75`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482bd44b4f4187bcf8730a04e6fb3959048bebefa44d548dcf7b606b275acd51`  
		Last Modified: Tue, 30 Sep 2025 00:16:24 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4881f269405b8c4499a62ca468333e347ef9fffe077e0f795d9273c9d745111f`  
		Last Modified: Tue, 30 Sep 2025 00:16:28 GMT  
		Size: 7.7 MB (7691958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de77d0139936cd1d9e6352dc14c6c0af38108573e6f12eafbed1bac97236851c`  
		Last Modified: Tue, 30 Sep 2025 00:16:51 GMT  
		Size: 76.7 MB (76652737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4542805c16f4a83a13ecba8e3aa410e0a64136e542f5721df3d84a90f9d66b3c`  
		Last Modified: Tue, 30 Sep 2025 00:16:24 GMT  
		Size: 392.7 KB (392690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2a616b65292ab74d2f1b8295e950c7d17e9336f8a49aa47ef1af4731f3f7c`  
		Last Modified: Tue, 30 Sep 2025 00:16:25 GMT  
		Size: 99.4 KB (99442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a241368c4be77d144064e430f3947ce99bbbdebe8745dc47e7689f460598d5e`  
		Last Modified: Tue, 30 Sep 2025 00:16:25 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa031d107652e0b7655997675f2f9170cbf9060992195a20aabd0bf8f86589e`  
		Last Modified: Tue, 30 Sep 2025 00:16:27 GMT  
		Size: 42.3 MB (42338022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d49ea83005436c32868106479aa2fb30c432ab05ae2e443c6efd1c8bb46648`  
		Last Modified: Tue, 30 Sep 2025 00:16:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:4caf2d49d72163b397bdf15d4abf3106f4b0f2f17b1bd1ea365efcc3bda50804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9cf08ea9faffc213b5e887b441454522c35fb39cc293ff209b28213bd7cc4b4`

```dockerfile
```

-	Layers:
	-	`sha256:895f067ba433e1875b15731c9d6f2109324d65b8f4376f82b5ab99f24d164f6a`  
		Last Modified: Wed, 01 Oct 2025 13:33:29 GMT  
		Size: 3.7 MB (3656407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb6952131e64a4250e965937752bd408b94c149aa2ead61dca413bdfb8186eba`  
		Last Modified: Wed, 01 Oct 2025 13:33:30 GMT  
		Size: 24.4 KB (24428 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:ac7dc6881138202386a0cbc3dd333dd2ff60b8b5ab768608717ed8b0ef9faf25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150040261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb8c6e8d8948f79efb8b196ec87f85d9827b7c8764bcb0aa7c3b2c019ee1abd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
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
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94868e75909782299d08034927b5d7be970e4c3ae160126ae4054926baa376c`  
		Last Modified: Tue, 30 Sep 2025 03:25:24 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b03903a57cdf7e6571bc2a49d71614c593988fca8339c5a43e26defb6d22df`  
		Last Modified: Wed, 01 Oct 2025 19:31:43 GMT  
		Size: 7.4 MB (7398078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53dfcd51ee6f606562c8a43a2a8af9c897ad6a190524606db5acc7932b6a47d`  
		Last Modified: Wed, 01 Oct 2025 19:31:49 GMT  
		Size: 73.1 MB (73099094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f5a64e8fabc952082ff93407d79b7fe9ca3b505faef585625917252c0c33ba`  
		Last Modified: Tue, 30 Sep 2025 03:25:27 GMT  
		Size: 394.4 KB (394421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba42706b5e741834633eddc844c753f1bf122c9a18919c6175dd1c9abf2461e8`  
		Last Modified: Tue, 30 Sep 2025 03:25:31 GMT  
		Size: 99.6 KB (99577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef7c8a8e671b9c7b0a3ca3f16c6e8166d7f835fce806fa6b3a6104b42c17783`  
		Last Modified: Tue, 30 Sep 2025 03:25:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cad458d0694cc2c45627794d5ddd913e7d9e00b30815dc8aace350703530907`  
		Last Modified: Tue, 30 Sep 2025 03:17:29 GMT  
		Size: 42.2 MB (42162896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e8b1dff7393f8116c28fd712283cc0e5f7d4a93c42504a5b631ecd61340690`  
		Last Modified: Tue, 30 Sep 2025 03:17:26 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d016775bb5aad0804241fbaa7360291579bc1d248c128be8d2c6de0e4a980850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d571c4a7733b46fae98bd1dda4aa7fc1c9e075b3b41d858782de6efd329001fe`

```dockerfile
```

-	Layers:
	-	`sha256:f4836b319f88a86cc7e12cec9012202b0e3ca04d63ae5f0ad6597894feaaa1d7`  
		Last Modified: Wed, 01 Oct 2025 19:33:29 GMT  
		Size: 3.6 MB (3648272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bcdc3a360234cecfefb2762e130b659a98493582a0a9670d3b2525a3dd489c5`  
		Last Modified: Wed, 01 Oct 2025 19:33:29 GMT  
		Size: 24.3 KB (24256 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:6e379b69ef063497b69ba661ccde4cf4b3a34a91590bd61e2f99ff224f8831d3
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
$ docker pull couchdb@sha256:54ea64f59140ac48e51ea0e4ad05f90fb25b4e1470813f6c2208749c6a1a6e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139837266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9d8ea0e34c17fbd7aa046bdd1e8ea8ce75b6416398d878d65716ba04906bf4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3418cd4354df70cbc3f38602bedf118bebf6f2c30eb20c8a1cff75e0aa68234`  
		Last Modified: Tue, 30 Sep 2025 00:12:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5391005848fcd8ff2646a5a5900b64ba4d7d0cfe038dc9f89a0d8e0cbcefe4`  
		Last Modified: Tue, 30 Sep 2025 00:12:22 GMT  
		Size: 7.9 MB (7881663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9db32416ea5b5afea586586f054427523267746b536cb29e2dbe9669ccb745`  
		Last Modified: Tue, 30 Sep 2025 00:12:20 GMT  
		Size: 401.7 KB (401728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2492e3d890071ea1e33b4a4207ce5b3d52b44fbcac60410da7c674a5064d9e03`  
		Last Modified: Tue, 30 Sep 2025 00:12:20 GMT  
		Size: 76.5 KB (76468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb89227f4334afe7e19fe773486ab061e31e1f377c2bf9fa5753928f89a4f750`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7085367bff1ed93af408f57da1c83d990c6a0ae30fd9ced462b24f875a20897b`  
		Last Modified: Tue, 30 Sep 2025 00:12:28 GMT  
		Size: 103.2 MB (103243645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f174ee6aee209409c8114bc72ad1758c501d95a81dc83aa084b6bdf19d416aa`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bce87f2ba00b097391b3c985f6e113e81ef897c07fc2dfc4d2e6a93be431f4f`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455a775b2896e1fd5a17e5b3fbd4e16ed4a542e62d18c10b15294ccf81ab72ae`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e55b231d664464cbed5e20983876ea36a77c03c2723f34562a8ffa80e8c900`  
		Last Modified: Tue, 30 Sep 2025 00:12:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:d387798cc84de1a6a28dd67f1e0e867265a04d82ed33795502bc650cdc9b0ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c895b95d0b921282c241d5ea5ae1109d0520ed897feb0476002f18d3339068a`

```dockerfile
```

-	Layers:
	-	`sha256:b3c80834976cbe1a5b7c5225136abf4f695dd7da7f376f5d7d1b736b8b742443`  
		Last Modified: Wed, 01 Oct 2025 16:33:21 GMT  
		Size: 4.1 MB (4141252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58b99101a235b0a2e76591518d0a7b330f09b80b2a85cc30d87c259d089a03c`  
		Last Modified: Wed, 01 Oct 2025 16:33:22 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a5f50ef9185473caa7a8fb95bf13598080fc5f539ef293cd15ff2f577064019b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139156041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee3fbea99b66ccb49029e5fb94cb5780c99c90adb4c73ec0401c7567340b05b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b33cd8814a56bab74ff410b4b56ffbad6a20b281c4ccb06f104f1d7f547770`  
		Last Modified: Tue, 30 Sep 2025 00:15:24 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3602b49f923cadda7d2f38ca0128f279f6d1379a17255bfb4b723bc843c8ff6a`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 7.7 MB (7692013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c331624f091aa071757c2d474c4822c9d9272c541695e3469e273e1e38d13e15`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 370.5 KB (370482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ba805bd02d8f4eec7398e75afc0cf96d7aa4b75545233ab492a9fa18490b47`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 76.5 KB (76459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da439f569038fb1d6e0ef84bf99f7280dc6bc8f4447bd9e5e5bdf629684fc33`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a98295683d6e2d14d6acdfa40b2da8b19d989613acd5a9ee5be01c837d8970`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 102.9 MB (102909517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe36b689fece14435f6d7d3ee56e0e34ea97bad7c1e090f5a5b54c0d3c09d40`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119729afb3b66cf3cf9fc0fda3e9f8416d7bf7babafd2eb49458e55a9daf3914`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da64966d7ebb577c3a46ec8aa8105f2f30ceb8bc05eca7096c4e80bca6d4f84e`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82627e16d8266ef108b2050801e2c6f89046be99ee6c4b2419068e6288397d7`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:0f84646931e0e4f79e3e8484567f43e1a673e45a2a4f03161dd7f43472c67a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d57d8a1b66730c1d974cba58707e96dbda9d74e7feb4149c348f81ff53b325`

```dockerfile
```

-	Layers:
	-	`sha256:af6523121382afb86bfe9a78e5673b198a200a6b40f5810c9b7fc944b2209545`  
		Last Modified: Wed, 01 Oct 2025 13:33:43 GMT  
		Size: 4.1 MB (4141545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec563fe8deb456936f04f9c6259e7caa7faace44cdfba2f10500208bd32793e9`  
		Last Modified: Wed, 01 Oct 2025 13:33:44 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:49bd43791b2a8e90981f81cc3df862a2e78c98a0839a7adebad718b0fab80a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136535368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7cd1181fa41367e88cffce0088ddf91c8158c2ae6f1e7c4965d9c12cca0154`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc974b68a96cb9613948be41d48c95b11256922ec30ed86ff522d7ed43538893`  
		Last Modified: Tue, 09 Sep 2025 01:15:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cdcab67f7535323419e032c49994a3856a03aa211325df57144390a3d9d585`  
		Last Modified: Tue, 09 Sep 2025 07:29:38 GMT  
		Size: 7.4 MB (7398124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a1e5f2d33d1a152a120b4dccfbb324269caf8fb32a5043c35809e100ca760b`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 372.1 KB (372092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a872688d6492057aac594611cfc5b625c0e1e1a7ff940617f997704169e9995`  
		Last Modified: Tue, 09 Sep 2025 01:15:02 GMT  
		Size: 76.5 KB (76474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a3f6b7373136c1cb2d1298a2d2f73413c7b8f547d35ffb8b50ca04a1addd1b`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2cbab153673e0482891bf1c9bd2ae59af2229ffdba923fd4789ad884a290d4`  
		Last Modified: Tue, 09 Sep 2025 07:29:53 GMT  
		Size: 101.8 MB (101798944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff04489a55fe042596b0d31824144d0eb4e70e1140495a620275221c5395e3d8`  
		Last Modified: Tue, 09 Sep 2025 01:15:07 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d0a12528ee99fe8d84804d62582d8440c541959f08c04052ec6684c99cfdaf`  
		Last Modified: Tue, 09 Sep 2025 01:15:02 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655b820b4aa315ce76b890ac016a6099ad5c702d6cd2f58293d9e15235f02c84`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df33dbb0f88bbbc18112e2a368427ae82f1cb89828735d1cd23fc406b2382a9`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:0d542ff2e1e509d8aefffabaab664ce35e73ca259f0f4a7706c1b9cc33dac89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c97c25ab13bfd1feb8017ad6f5bcc4f2073a7ff0adfc8c09a051c69e559ad49`

```dockerfile
```

-	Layers:
	-	`sha256:7aafde54b4d5a7fde65f62567e3ddc218904048738582917347f388ab9b55de9`  
		Last Modified: Tue, 09 Sep 2025 01:33:25 GMT  
		Size: 4.1 MB (4137448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05d2f4c4ba9d7760c0f1710ce711c32bc1d2652360873595fc7f48a5aa8af43`  
		Last Modified: Tue, 09 Sep 2025 01:33:26 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:3d0bf6e5ed7eec87a0c49bd007cf0c44ea0baa4e89f1a91e54365688839d4ad9
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
$ docker pull couchdb@sha256:715fb9dce1716897b071b86d6653c62b72bdc024668ac53f4d5a883e2f0fd284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135fc9b4d69ecc10e0ae388cdf0ef9565967ac625932a7d92152b2da726ac25e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb50c07b2ef11a8ec1f0607bf6c9513aab386bcf59ac8797c85a56990b51de8`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672f458973f11333cea934aa85e060219715efc84aea49c2f600ff572614332f`  
		Last Modified: Tue, 30 Sep 2025 00:12:33 GMT  
		Size: 7.9 MB (7881684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f63af8926750c43e6aedbe6c076b618771816c759507186d67a8bb8bea03bc`  
		Last Modified: Tue, 30 Sep 2025 00:12:39 GMT  
		Size: 77.3 MB (77326979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f45fb8f7ea6edb0bada78e12142ff68a4638979af8d64a7a9fc421ac551222`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 424.1 KB (424065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f04a4c53df1a57663873195756adc16ab07078bed90ce0bc2dbd11a10aebb`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 99.5 KB (99492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b52fa3e91ddd7e8e960ea90ed0b34b4338656ab877b706a2f01b3e71e035b7`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cda19eab3e8a24e603dba796758b4de017fcdd4cd3c8316ad2ec1e4c6148ed`  
		Last Modified: Tue, 30 Sep 2025 00:12:36 GMT  
		Size: 42.4 MB (42436193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7bf39ca98400552895af79ee20571e2ce575080e996cdb7fad59ce118075e`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc1c0619a8d6b9adf17be170ea3977b599528321798edfbb2e9e94074acea196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1820c22fef622289211a17c279495101ed3a6ed988edf0ee919e7b075b459f71`

```dockerfile
```

-	Layers:
	-	`sha256:4940a7adacc757e5d4fa22bfab225fbbf79da6db12c33158d4ff21c39b41cd69`  
		Last Modified: Wed, 01 Oct 2025 16:33:27 GMT  
		Size: 3.7 MB (3658049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74a75fce6a7f3411ed1381c11e952821ff85cdd27bd48779b00a661242e1731b`  
		Last Modified: Wed, 01 Oct 2025 16:33:29 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8542f71de8d3fb3656fc658237d00cd3326b672be16aa511faa72cd73349e9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155279477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fea46598ff3c12fbb18a93356fb4e11002376dac93fcd7b8c482348e2326d19`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489eed97204181f5e217407f1a76b144c156604dc67a6dfc83772858b681909d`  
		Last Modified: Tue, 30 Sep 2025 00:16:17 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398f5c46545ac256be1c07670b8511b33ec736953a1ee232d54e45c97517e989`  
		Last Modified: Tue, 30 Sep 2025 00:16:18 GMT  
		Size: 7.7 MB (7692022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a36a56fa00a8b81c6f5174c1e2bcaf2c271b89d0db2b702deb25d0a540e74b9`  
		Last Modified: Tue, 30 Sep 2025 00:16:36 GMT  
		Size: 76.7 MB (76652777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242ca2e029ce153691a4ed49f49b5c6a42c7bd24f855b741b54d050c3bef6c64`  
		Last Modified: Tue, 30 Sep 2025 00:16:16 GMT  
		Size: 392.7 KB (392709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f12c3da0de9727bf448a75a923636574adebeda03e50b2de7487632148e9fb`  
		Last Modified: Tue, 30 Sep 2025 00:16:16 GMT  
		Size: 99.5 KB (99460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40de999fb52303ca5bb3d6a21b74101d81982b90ea093bc72b9e31f26dd1f9d4`  
		Last Modified: Tue, 30 Sep 2025 00:16:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d147f495a50a75ae53283b9ae24a72b9b0ae1e7f2f1a615e8b858734b16d27`  
		Last Modified: Tue, 30 Sep 2025 00:16:19 GMT  
		Size: 42.3 MB (42338490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d91e04c7ac1fe428bba250821315ee73121fdc2c85a866364555bb8e5b87ce3`  
		Last Modified: Tue, 30 Sep 2025 00:16:16 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:ca56e281523d5438b66575e9f17af770c9067e4622b4f582955013f4e6b7bfa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97a40531d51b5ff3255ee4e9c2d6ed3c52b621fbca7762b93b4d6834eacb0b0`

```dockerfile
```

-	Layers:
	-	`sha256:dd59bc16a77dc54d6e331c00eee168bd496feff198737389aefb35732081fe6c`  
		Last Modified: Wed, 01 Oct 2025 13:33:22 GMT  
		Size: 3.7 MB (3656725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0237fa1d440e21dd89dd1db0e1118579d70afa8f4d19569bad1b81bca09bcd`  
		Last Modified: Wed, 01 Oct 2025 13:33:23 GMT  
		Size: 24.7 KB (24744 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:e4d95a8569f0563080c1d34e55235699562145f94dbb121588bf81e8c02e7cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150040910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d4fbe2bdd8a68b87cb0e856db9a6509bf54e915f3a49022c73dedc224eff11`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6660c0849f31015adaa92ce7a5301c2e4989720f60b06c3a3337bb458626ee5b`  
		Last Modified: Tue, 09 Sep 2025 01:15:00 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a2c699e296fd038b13d9ebc990c2c25f01034c23f71945a946512c166006d1`  
		Last Modified: Tue, 09 Sep 2025 01:22:29 GMT  
		Size: 7.4 MB (7398150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0141fc5fd220a0e8342d747d29d994c7da8eec8b3ba9ed10e7865fca70bca801`  
		Last Modified: Tue, 09 Sep 2025 01:22:24 GMT  
		Size: 73.1 MB (73099278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e154f3d3148c1109f04cd74f222cf566b1f7655c15f091471bc3c43519ea46`  
		Last Modified: Tue, 09 Sep 2025 01:14:59 GMT  
		Size: 394.4 KB (394399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1e4fc22f332be1a66c12c5045cba6ef0ccf5802ebc43cf79a99f0e94976c63`  
		Last Modified: Tue, 09 Sep 2025 01:15:00 GMT  
		Size: 99.6 KB (99601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a6c6b7a5b02bb21d0f41b4fb3c7beeec1b6343876dff2c10c8644f45fd7ed7`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddeb7ded7819c3dc9e616172a7d225fa689c613ed6e7d3a527dc8d5b9cff035`  
		Last Modified: Tue, 09 Sep 2025 19:03:45 GMT  
		Size: 42.2 MB (42163302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e61ca25d28292bbb2d871373142dd9ba5430a8f3605cae2b310f1c11fdc3aea`  
		Last Modified: Tue, 09 Sep 2025 01:14:59 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f803328ecad04363b00ec2e59440b5d8688e40835d58996f9cc7adda3b96eb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd548e5f239560e2a07fae13608afd965209f67cf8fe0ecff5616fee6c6d98bb`

```dockerfile
```

-	Layers:
	-	`sha256:3f5c205a784e5f94f3d57a81b1d70b835ab4bfd32578c13a8dfea8e5d784c59a`  
		Last Modified: Tue, 09 Sep 2025 01:33:30 GMT  
		Size: 3.6 MB (3648578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49bc1fd01154ed011d1bb4588847d645f16a941f5ff24b8e2e2929b7f90e362c`  
		Last Modified: Tue, 09 Sep 2025 01:33:31 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0`

```console
$ docker pull couchdb@sha256:6e379b69ef063497b69ba661ccde4cf4b3a34a91590bd61e2f99ff224f8831d3
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
$ docker pull couchdb@sha256:54ea64f59140ac48e51ea0e4ad05f90fb25b4e1470813f6c2208749c6a1a6e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139837266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9d8ea0e34c17fbd7aa046bdd1e8ea8ce75b6416398d878d65716ba04906bf4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3418cd4354df70cbc3f38602bedf118bebf6f2c30eb20c8a1cff75e0aa68234`  
		Last Modified: Tue, 30 Sep 2025 00:12:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5391005848fcd8ff2646a5a5900b64ba4d7d0cfe038dc9f89a0d8e0cbcefe4`  
		Last Modified: Tue, 30 Sep 2025 00:12:22 GMT  
		Size: 7.9 MB (7881663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9db32416ea5b5afea586586f054427523267746b536cb29e2dbe9669ccb745`  
		Last Modified: Tue, 30 Sep 2025 00:12:20 GMT  
		Size: 401.7 KB (401728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2492e3d890071ea1e33b4a4207ce5b3d52b44fbcac60410da7c674a5064d9e03`  
		Last Modified: Tue, 30 Sep 2025 00:12:20 GMT  
		Size: 76.5 KB (76468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb89227f4334afe7e19fe773486ab061e31e1f377c2bf9fa5753928f89a4f750`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7085367bff1ed93af408f57da1c83d990c6a0ae30fd9ced462b24f875a20897b`  
		Last Modified: Tue, 30 Sep 2025 00:12:28 GMT  
		Size: 103.2 MB (103243645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f174ee6aee209409c8114bc72ad1758c501d95a81dc83aa084b6bdf19d416aa`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bce87f2ba00b097391b3c985f6e113e81ef897c07fc2dfc4d2e6a93be431f4f`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455a775b2896e1fd5a17e5b3fbd4e16ed4a542e62d18c10b15294ccf81ab72ae`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e55b231d664464cbed5e20983876ea36a77c03c2723f34562a8ffa80e8c900`  
		Last Modified: Tue, 30 Sep 2025 00:12:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:d387798cc84de1a6a28dd67f1e0e867265a04d82ed33795502bc650cdc9b0ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c895b95d0b921282c241d5ea5ae1109d0520ed897feb0476002f18d3339068a`

```dockerfile
```

-	Layers:
	-	`sha256:b3c80834976cbe1a5b7c5225136abf4f695dd7da7f376f5d7d1b736b8b742443`  
		Last Modified: Wed, 01 Oct 2025 16:33:21 GMT  
		Size: 4.1 MB (4141252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58b99101a235b0a2e76591518d0a7b330f09b80b2a85cc30d87c259d089a03c`  
		Last Modified: Wed, 01 Oct 2025 16:33:22 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a5f50ef9185473caa7a8fb95bf13598080fc5f539ef293cd15ff2f577064019b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139156041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee3fbea99b66ccb49029e5fb94cb5780c99c90adb4c73ec0401c7567340b05b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b33cd8814a56bab74ff410b4b56ffbad6a20b281c4ccb06f104f1d7f547770`  
		Last Modified: Tue, 30 Sep 2025 00:15:24 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3602b49f923cadda7d2f38ca0128f279f6d1379a17255bfb4b723bc843c8ff6a`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 7.7 MB (7692013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c331624f091aa071757c2d474c4822c9d9272c541695e3469e273e1e38d13e15`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 370.5 KB (370482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ba805bd02d8f4eec7398e75afc0cf96d7aa4b75545233ab492a9fa18490b47`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 76.5 KB (76459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da439f569038fb1d6e0ef84bf99f7280dc6bc8f4447bd9e5e5bdf629684fc33`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a98295683d6e2d14d6acdfa40b2da8b19d989613acd5a9ee5be01c837d8970`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 102.9 MB (102909517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe36b689fece14435f6d7d3ee56e0e34ea97bad7c1e090f5a5b54c0d3c09d40`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119729afb3b66cf3cf9fc0fda3e9f8416d7bf7babafd2eb49458e55a9daf3914`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da64966d7ebb577c3a46ec8aa8105f2f30ceb8bc05eca7096c4e80bca6d4f84e`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82627e16d8266ef108b2050801e2c6f89046be99ee6c4b2419068e6288397d7`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:0f84646931e0e4f79e3e8484567f43e1a673e45a2a4f03161dd7f43472c67a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d57d8a1b66730c1d974cba58707e96dbda9d74e7feb4149c348f81ff53b325`

```dockerfile
```

-	Layers:
	-	`sha256:af6523121382afb86bfe9a78e5673b198a200a6b40f5810c9b7fc944b2209545`  
		Last Modified: Wed, 01 Oct 2025 13:33:43 GMT  
		Size: 4.1 MB (4141545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec563fe8deb456936f04f9c6259e7caa7faace44cdfba2f10500208bd32793e9`  
		Last Modified: Wed, 01 Oct 2025 13:33:44 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; s390x

```console
$ docker pull couchdb@sha256:49bd43791b2a8e90981f81cc3df862a2e78c98a0839a7adebad718b0fab80a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136535368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7cd1181fa41367e88cffce0088ddf91c8158c2ae6f1e7c4965d9c12cca0154`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc974b68a96cb9613948be41d48c95b11256922ec30ed86ff522d7ed43538893`  
		Last Modified: Tue, 09 Sep 2025 01:15:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cdcab67f7535323419e032c49994a3856a03aa211325df57144390a3d9d585`  
		Last Modified: Tue, 09 Sep 2025 07:29:38 GMT  
		Size: 7.4 MB (7398124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a1e5f2d33d1a152a120b4dccfbb324269caf8fb32a5043c35809e100ca760b`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 372.1 KB (372092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a872688d6492057aac594611cfc5b625c0e1e1a7ff940617f997704169e9995`  
		Last Modified: Tue, 09 Sep 2025 01:15:02 GMT  
		Size: 76.5 KB (76474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a3f6b7373136c1cb2d1298a2d2f73413c7b8f547d35ffb8b50ca04a1addd1b`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2cbab153673e0482891bf1c9bd2ae59af2229ffdba923fd4789ad884a290d4`  
		Last Modified: Tue, 09 Sep 2025 07:29:53 GMT  
		Size: 101.8 MB (101798944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff04489a55fe042596b0d31824144d0eb4e70e1140495a620275221c5395e3d8`  
		Last Modified: Tue, 09 Sep 2025 01:15:07 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d0a12528ee99fe8d84804d62582d8440c541959f08c04052ec6684c99cfdaf`  
		Last Modified: Tue, 09 Sep 2025 01:15:02 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655b820b4aa315ce76b890ac016a6099ad5c702d6cd2f58293d9e15235f02c84`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df33dbb0f88bbbc18112e2a368427ae82f1cb89828735d1cd23fc406b2382a9`  
		Last Modified: Tue, 09 Sep 2025 01:15:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:0d542ff2e1e509d8aefffabaab664ce35e73ca259f0f4a7706c1b9cc33dac89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c97c25ab13bfd1feb8017ad6f5bcc4f2073a7ff0adfc8c09a051c69e559ad49`

```dockerfile
```

-	Layers:
	-	`sha256:7aafde54b4d5a7fde65f62567e3ddc218904048738582917347f388ab9b55de9`  
		Last Modified: Tue, 09 Sep 2025 01:33:25 GMT  
		Size: 4.1 MB (4137448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05d2f4c4ba9d7760c0f1710ce711c32bc1d2652360873595fc7f48a5aa8af43`  
		Last Modified: Tue, 09 Sep 2025 01:33:26 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0-nouveau`

```console
$ docker pull couchdb@sha256:e4357508e8e99f53799492dd734d39b517a2433e3ef29f94529d933e3a9deb04
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
$ docker pull couchdb@sha256:715fb9dce1716897b071b86d6653c62b72bdc024668ac53f4d5a883e2f0fd284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135fc9b4d69ecc10e0ae388cdf0ef9565967ac625932a7d92152b2da726ac25e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb50c07b2ef11a8ec1f0607bf6c9513aab386bcf59ac8797c85a56990b51de8`  
		Last Modified: Tue, 30 Sep 2025 00:12:31 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672f458973f11333cea934aa85e060219715efc84aea49c2f600ff572614332f`  
		Last Modified: Tue, 30 Sep 2025 00:12:33 GMT  
		Size: 7.9 MB (7881684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f63af8926750c43e6aedbe6c076b618771816c759507186d67a8bb8bea03bc`  
		Last Modified: Tue, 30 Sep 2025 00:12:39 GMT  
		Size: 77.3 MB (77326979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f45fb8f7ea6edb0bada78e12142ff68a4638979af8d64a7a9fc421ac551222`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 424.1 KB (424065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f04a4c53df1a57663873195756adc16ab07078bed90ce0bc2dbd11a10aebb`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 99.5 KB (99492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b52fa3e91ddd7e8e960ea90ed0b34b4338656ab877b706a2f01b3e71e035b7`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cda19eab3e8a24e603dba796758b4de017fcdd4cd3c8316ad2ec1e4c6148ed`  
		Last Modified: Tue, 30 Sep 2025 00:12:36 GMT  
		Size: 42.4 MB (42436193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7bf39ca98400552895af79ee20571e2ce575080e996cdb7fad59ce118075e`  
		Last Modified: Tue, 30 Sep 2025 00:12:32 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc1c0619a8d6b9adf17be170ea3977b599528321798edfbb2e9e94074acea196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1820c22fef622289211a17c279495101ed3a6ed988edf0ee919e7b075b459f71`

```dockerfile
```

-	Layers:
	-	`sha256:4940a7adacc757e5d4fa22bfab225fbbf79da6db12c33158d4ff21c39b41cd69`  
		Last Modified: Wed, 01 Oct 2025 16:33:27 GMT  
		Size: 3.7 MB (3658049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74a75fce6a7f3411ed1381c11e952821ff85cdd27bd48779b00a661242e1731b`  
		Last Modified: Wed, 01 Oct 2025 16:33:29 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8542f71de8d3fb3656fc658237d00cd3326b672be16aa511faa72cd73349e9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155279477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fea46598ff3c12fbb18a93356fb4e11002376dac93fcd7b8c482348e2326d19`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489eed97204181f5e217407f1a76b144c156604dc67a6dfc83772858b681909d`  
		Last Modified: Tue, 30 Sep 2025 00:16:17 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398f5c46545ac256be1c07670b8511b33ec736953a1ee232d54e45c97517e989`  
		Last Modified: Tue, 30 Sep 2025 00:16:18 GMT  
		Size: 7.7 MB (7692022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a36a56fa00a8b81c6f5174c1e2bcaf2c271b89d0db2b702deb25d0a540e74b9`  
		Last Modified: Tue, 30 Sep 2025 00:16:36 GMT  
		Size: 76.7 MB (76652777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242ca2e029ce153691a4ed49f49b5c6a42c7bd24f855b741b54d050c3bef6c64`  
		Last Modified: Tue, 30 Sep 2025 00:16:16 GMT  
		Size: 392.7 KB (392709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f12c3da0de9727bf448a75a923636574adebeda03e50b2de7487632148e9fb`  
		Last Modified: Tue, 30 Sep 2025 00:16:16 GMT  
		Size: 99.5 KB (99460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40de999fb52303ca5bb3d6a21b74101d81982b90ea093bc72b9e31f26dd1f9d4`  
		Last Modified: Tue, 30 Sep 2025 00:16:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d147f495a50a75ae53283b9ae24a72b9b0ae1e7f2f1a615e8b858734b16d27`  
		Last Modified: Tue, 30 Sep 2025 00:16:19 GMT  
		Size: 42.3 MB (42338490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d91e04c7ac1fe428bba250821315ee73121fdc2c85a866364555bb8e5b87ce3`  
		Last Modified: Tue, 30 Sep 2025 00:16:16 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:ca56e281523d5438b66575e9f17af770c9067e4622b4f582955013f4e6b7bfa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97a40531d51b5ff3255ee4e9c2d6ed3c52b621fbca7762b93b4d6834eacb0b0`

```dockerfile
```

-	Layers:
	-	`sha256:dd59bc16a77dc54d6e331c00eee168bd496feff198737389aefb35732081fe6c`  
		Last Modified: Wed, 01 Oct 2025 13:33:22 GMT  
		Size: 3.7 MB (3656725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0237fa1d440e21dd89dd1db0e1118579d70afa8f4d19569bad1b81bca09bcd`  
		Last Modified: Wed, 01 Oct 2025 13:33:23 GMT  
		Size: 24.7 KB (24744 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:db27a4bad6aeb41d10540c5f62c971d325f90101be6ce32c6ddf40939107ae40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150040648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918c8866b02ac09241cbd4e09c50198bcbf49ea16cb27c0e024580a7f24f6063`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
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
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94868e75909782299d08034927b5d7be970e4c3ae160126ae4054926baa376c`  
		Last Modified: Tue, 30 Sep 2025 03:25:24 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b03903a57cdf7e6571bc2a49d71614c593988fca8339c5a43e26defb6d22df`  
		Last Modified: Wed, 01 Oct 2025 19:31:43 GMT  
		Size: 7.4 MB (7398078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53dfcd51ee6f606562c8a43a2a8af9c897ad6a190524606db5acc7932b6a47d`  
		Last Modified: Wed, 01 Oct 2025 19:31:49 GMT  
		Size: 73.1 MB (73099094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f5a64e8fabc952082ff93407d79b7fe9ca3b505faef585625917252c0c33ba`  
		Last Modified: Tue, 30 Sep 2025 03:25:27 GMT  
		Size: 394.4 KB (394421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba42706b5e741834633eddc844c753f1bf122c9a18919c6175dd1c9abf2461e8`  
		Last Modified: Tue, 30 Sep 2025 03:25:31 GMT  
		Size: 99.6 KB (99577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef7c8a8e671b9c7b0a3ca3f16c6e8166d7f835fce806fa6b3a6104b42c17783`  
		Last Modified: Tue, 30 Sep 2025 03:25:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1474f9ab44eebafde1742c3b828eda8881289a9c8772479bfd9753a14e78b1cf`  
		Last Modified: Tue, 30 Sep 2025 03:15:31 GMT  
		Size: 42.2 MB (42163281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d36768817145df1c187b944da0559774675a3983ddb4ea1ef61bee09375c8c7`  
		Last Modified: Tue, 30 Sep 2025 03:25:37 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:6c47e9209e468e75b167ffd611946c2d90555027933d32d356df687c0e518406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baace8e51383f7d2019bc27191247529c37a54601303ac804997d4ff53bd77ec`

```dockerfile
```

-	Layers:
	-	`sha256:150f471cb52f9ddc6abc4b140d269cc05f594096337cc77c27da95483ad0c538`  
		Last Modified: Wed, 01 Oct 2025 19:33:44 GMT  
		Size: 3.6 MB (3648578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1826214e31aeadcf20427d05aea81f1c43f67448d8bf52b557172abe939ab86`  
		Last Modified: Wed, 01 Oct 2025 19:33:44 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:9d57dc1482bf1006149f8cdce91499a0b0754fdc75332f149b8109323a2ef347
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
$ docker pull couchdb@sha256:54ea64f59140ac48e51ea0e4ad05f90fb25b4e1470813f6c2208749c6a1a6e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139837266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9d8ea0e34c17fbd7aa046bdd1e8ea8ce75b6416398d878d65716ba04906bf4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3418cd4354df70cbc3f38602bedf118bebf6f2c30eb20c8a1cff75e0aa68234`  
		Last Modified: Tue, 30 Sep 2025 00:12:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5391005848fcd8ff2646a5a5900b64ba4d7d0cfe038dc9f89a0d8e0cbcefe4`  
		Last Modified: Tue, 30 Sep 2025 00:12:22 GMT  
		Size: 7.9 MB (7881663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9db32416ea5b5afea586586f054427523267746b536cb29e2dbe9669ccb745`  
		Last Modified: Tue, 30 Sep 2025 00:12:20 GMT  
		Size: 401.7 KB (401728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2492e3d890071ea1e33b4a4207ce5b3d52b44fbcac60410da7c674a5064d9e03`  
		Last Modified: Tue, 30 Sep 2025 00:12:20 GMT  
		Size: 76.5 KB (76468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb89227f4334afe7e19fe773486ab061e31e1f377c2bf9fa5753928f89a4f750`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7085367bff1ed93af408f57da1c83d990c6a0ae30fd9ced462b24f875a20897b`  
		Last Modified: Tue, 30 Sep 2025 00:12:28 GMT  
		Size: 103.2 MB (103243645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f174ee6aee209409c8114bc72ad1758c501d95a81dc83aa084b6bdf19d416aa`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bce87f2ba00b097391b3c985f6e113e81ef897c07fc2dfc4d2e6a93be431f4f`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455a775b2896e1fd5a17e5b3fbd4e16ed4a542e62d18c10b15294ccf81ab72ae`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e55b231d664464cbed5e20983876ea36a77c03c2723f34562a8ffa80e8c900`  
		Last Modified: Tue, 30 Sep 2025 00:12:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:d387798cc84de1a6a28dd67f1e0e867265a04d82ed33795502bc650cdc9b0ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c895b95d0b921282c241d5ea5ae1109d0520ed897feb0476002f18d3339068a`

```dockerfile
```

-	Layers:
	-	`sha256:b3c80834976cbe1a5b7c5225136abf4f695dd7da7f376f5d7d1b736b8b742443`  
		Last Modified: Wed, 01 Oct 2025 16:33:21 GMT  
		Size: 4.1 MB (4141252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58b99101a235b0a2e76591518d0a7b330f09b80b2a85cc30d87c259d089a03c`  
		Last Modified: Wed, 01 Oct 2025 16:33:22 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a5f50ef9185473caa7a8fb95bf13598080fc5f539ef293cd15ff2f577064019b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139156041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee3fbea99b66ccb49029e5fb94cb5780c99c90adb4c73ec0401c7567340b05b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b33cd8814a56bab74ff410b4b56ffbad6a20b281c4ccb06f104f1d7f547770`  
		Last Modified: Tue, 30 Sep 2025 00:15:24 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3602b49f923cadda7d2f38ca0128f279f6d1379a17255bfb4b723bc843c8ff6a`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 7.7 MB (7692013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c331624f091aa071757c2d474c4822c9d9272c541695e3469e273e1e38d13e15`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 370.5 KB (370482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ba805bd02d8f4eec7398e75afc0cf96d7aa4b75545233ab492a9fa18490b47`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 76.5 KB (76459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da439f569038fb1d6e0ef84bf99f7280dc6bc8f4447bd9e5e5bdf629684fc33`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a98295683d6e2d14d6acdfa40b2da8b19d989613acd5a9ee5be01c837d8970`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 102.9 MB (102909517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe36b689fece14435f6d7d3ee56e0e34ea97bad7c1e090f5a5b54c0d3c09d40`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119729afb3b66cf3cf9fc0fda3e9f8416d7bf7babafd2eb49458e55a9daf3914`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da64966d7ebb577c3a46ec8aa8105f2f30ceb8bc05eca7096c4e80bca6d4f84e`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82627e16d8266ef108b2050801e2c6f89046be99ee6c4b2419068e6288397d7`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:0f84646931e0e4f79e3e8484567f43e1a673e45a2a4f03161dd7f43472c67a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d57d8a1b66730c1d974cba58707e96dbda9d74e7feb4149c348f81ff53b325`

```dockerfile
```

-	Layers:
	-	`sha256:af6523121382afb86bfe9a78e5673b198a200a6b40f5810c9b7fc944b2209545`  
		Last Modified: Wed, 01 Oct 2025 13:33:43 GMT  
		Size: 4.1 MB (4141545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec563fe8deb456936f04f9c6259e7caa7faace44cdfba2f10500208bd32793e9`  
		Last Modified: Wed, 01 Oct 2025 13:33:44 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:cedb6620efe93101ce130b736d629ff634be4575ce5cd9071f5ee17a8367cf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136534891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbade65256379b4d5ccc0311c6ca04d8c10d7404fbe2b7d3811c2e27b6117756`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
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
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8707ca73f47713fa87c126a9c016b13592ece4d94d1fd6b59a9493eb551f01`  
		Last Modified: Tue, 30 Sep 2025 03:12:35 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6540f4d5aa9f0c9cb21c6c4df7b694e7979be3fe7c6519ed05163f1da6f4b2`  
		Last Modified: Tue, 30 Sep 2025 03:12:36 GMT  
		Size: 7.4 MB (7398094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89aafca33e34e92fe2e66fe6f55cf4726a4dfb65ed32809c848b03532394827`  
		Last Modified: Tue, 30 Sep 2025 03:12:35 GMT  
		Size: 372.1 KB (372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d00c12ea8d16255757afdcc9527d38774f6ee8f0fee1274be828fb7c7296dbf`  
		Last Modified: Tue, 30 Sep 2025 03:12:36 GMT  
		Size: 76.5 KB (76483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ebbba8e6b09814d1e9f5116686ca3d44794dae35a27ebbeac1c263f4af8eff`  
		Last Modified: Tue, 30 Sep 2025 03:12:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd025166892031dae2175c592517894e5c02e3297dcb5b20cfbe1c2a1ac0cac`  
		Last Modified: Tue, 30 Sep 2025 03:12:37 GMT  
		Size: 101.8 MB (101798461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d30c6a71b9fa6e825d45388ff2e01e094cc5b1a2a4719f4df91630fee734bc0`  
		Last Modified: Tue, 30 Sep 2025 03:12:25 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9535fd8ca7e17228f69ba889fd55463481daf6b87b3b7b84fe55e5aff29b53c0`  
		Last Modified: Tue, 30 Sep 2025 03:12:25 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6739f71805e48c2734f133edd62e30186bc95d0d77766482c82af6b22b71995e`  
		Last Modified: Tue, 30 Sep 2025 03:12:25 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6f179427339dbf14a757c1eea8ae05eee0751dadfe6ba6eadfdb981a49182e`  
		Last Modified: Tue, 30 Sep 2025 03:12:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:9fb55912ad7e5c692f5aec6eb4fa19bf27a8f9f8eae231fd7d4baf8aedec5b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38a5ac74974af604f08bcf1c00d5ee6032dc4d0b3a736f4e3a79017103094d5`

```dockerfile
```

-	Layers:
	-	`sha256:59e0fbf1e9840799f6a633f1544e7bb2a68a850c3e77f548940d50e99135ca9c`  
		Last Modified: Wed, 01 Oct 2025 19:33:51 GMT  
		Size: 4.1 MB (4137448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c57d814c765c51b9f4968db70f5a139bde6175543354c5bbf003d07fa936156`  
		Last Modified: Wed, 01 Oct 2025 19:33:52 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json
