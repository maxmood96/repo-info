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
