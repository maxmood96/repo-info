## `couchdb:latest`

```console
$ docker pull couchdb@sha256:1c0a30a54535377bc9ae23f42efb1ca4e92abe796f78ec98b768ac1d5874cc1b
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
$ docker pull couchdb@sha256:4da3945c7a7b798530fa2d8d1a688669e2844499795e39756dfafcfb57ee4937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139837469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79cbaa90bb2c5a628b4b3f44026d0eb3970f6cb2b0ec893df86cdb9c68ed7b1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:28:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 00:28:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:28:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:49 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 04 Nov 2025 00:28:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:29:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 00:29:02 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 00:29:02 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 00:29:02 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 00:29:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:29:02 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:29:02 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 00:29:02 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 00:29:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a88ce690c27e46c06ca70bc34855caa33c6fdeb88e0d351d38ee765cec1064`  
		Last Modified: Tue, 04 Nov 2025 00:29:27 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5956f411eb081fd5e98805a4e179ed6ce37e970dae9f90073f44e3a29846e56c`  
		Last Modified: Tue, 04 Nov 2025 00:29:28 GMT  
		Size: 7.9 MB (7881818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5f0f53a68ee7accfc9a289ee082f475456a30da48c436d7e492e6a51784c02`  
		Last Modified: Tue, 04 Nov 2025 00:29:27 GMT  
		Size: 401.7 KB (401734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1c4301450a190841997ce4d608e8f4fa905c5e05265d6a9dc675a8558b506f`  
		Last Modified: Tue, 04 Nov 2025 00:29:26 GMT  
		Size: 76.5 KB (76503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d028dd9228411efb7d9509493db9441a8c58f4d2da186c2c056fea0f473b50`  
		Last Modified: Tue, 04 Nov 2025 00:29:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65742eda7201276852ec57066565a654f71143c69868528f2b7b00d6ab89ee98`  
		Last Modified: Tue, 04 Nov 2025 00:29:42 GMT  
		Size: 103.2 MB (103243418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768af929a959d8a2bd13618b8bf4110c9cc0f349972095a5b1eca6244ef4d5fa`  
		Last Modified: Tue, 04 Nov 2025 00:29:26 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f30cc7cb486810eba01b0abc11b1be9fa571ec4e88001cef23606995b09289`  
		Last Modified: Tue, 04 Nov 2025 00:29:26 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c728f23e61ab2d3bccb874ac52a32ab78993f7bfff38773f22fa8890baa7fde`  
		Last Modified: Tue, 04 Nov 2025 00:29:26 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21eae8ecc488e1f57057e71d3d85b11a74f7d6ad9edb904b7d0663b1e2128a7`  
		Last Modified: Tue, 04 Nov 2025 00:29:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:5b48d9763be9300a753721795891be39d15de946dec64657203afca463db0e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4172990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d099e4697ea1a873c371dbbc0af6ffb0d4b026f3fc5a555ce09a164c38fb8c2`

```dockerfile
```

-	Layers:
	-	`sha256:a178020c51e58e5a3853b9a970373c515df467ffae1bf66e22d1f509d06f17fc`  
		Last Modified: Tue, 04 Nov 2025 11:33:22 GMT  
		Size: 4.1 MB (4141252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a02fe1ebe3c5ef2d5fc34dff250b21273224531690ce25d34933f41bd2f17e7f`  
		Last Modified: Tue, 04 Nov 2025 11:33:23 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:308ba6c1ce1daa245e4a2565f44f06731d042247d72ac7b076e55d3272f8842a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139156882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8211aa35ff89fdc16f086132cc9df363c6934e4732c39e90f566fae8694fad`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:30:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 00:30:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:30:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:30:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:54 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 04 Nov 2025 00:30:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:31:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 00:31:11 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 00:31:11 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 00:31:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 00:31:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:31:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:31:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 00:31:11 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 00:31:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfe87e999e8e91a0d7594e0d29b0a8879ef1ace3ccf1cdb2ad896a754c38688`  
		Last Modified: Tue, 04 Nov 2025 00:31:40 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91df9dda2f35c75433b041e11089c5f939b69d1c8a5123883405639db6cdb8ff`  
		Last Modified: Tue, 04 Nov 2025 00:31:41 GMT  
		Size: 7.7 MB (7692080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeede8e764e8668384716731ec44077ccc8da940f19681cb1260c06b25ce047a`  
		Last Modified: Tue, 04 Nov 2025 00:31:40 GMT  
		Size: 370.5 KB (370485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7628965715b1dd7230ab318af69b6eb333fec433811383e95bc73de791fba8f`  
		Last Modified: Tue, 04 Nov 2025 00:31:41 GMT  
		Size: 76.5 KB (76500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d5fadb657aeb91653ae7581744d489aada5e2cfde18cec09eeff769e671295`  
		Last Modified: Tue, 04 Nov 2025 00:31:41 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba0d2862cc0e9d815853a4938943ddc675cbfa53e3b8de8630a198d4b87e4ea`  
		Last Modified: Tue, 04 Nov 2025 00:31:53 GMT  
		Size: 102.9 MB (102910007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fae5517d0b327901407da7a8cdfd38a0a5e726abc77a9614047d1c6b3cb18b`  
		Last Modified: Tue, 04 Nov 2025 00:31:41 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fb8515f062ace5d824a363f1bf456b9976027e3e7b8be680121a6b0f216b54`  
		Last Modified: Tue, 04 Nov 2025 00:31:41 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163445bdbbd0cb91ea1bfa96909f2b5f169a0bf26b569832ffda6f612a54f7f`  
		Last Modified: Tue, 04 Nov 2025 00:31:41 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc16b0843a81ff1e6752b7cef2fecd0e6c43a5a98c79e0cde1c2f7e8122c7040`  
		Last Modified: Tue, 04 Nov 2025 00:31:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:308ef846bcc576e7907ce4e75b365f12010ef928d060d5e5cedecd283c7a54d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054e3009250689f23fbb4a380340870fd81dc1b7eacf552aeae47f85670b8c7f`

```dockerfile
```

-	Layers:
	-	`sha256:439955f3774294b268df228cebdbdbfa7433869c5a9cfcc31e04364897c2ea28`  
		Last Modified: Tue, 04 Nov 2025 11:33:27 GMT  
		Size: 4.1 MB (4141545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2926bc3408436e65bbd9808b0fe8123c324f3aa9ec5550e9dee32d0567e0f09`  
		Last Modified: Tue, 04 Nov 2025 11:33:28 GMT  
		Size: 31.9 KB (31931 bytes)  
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
