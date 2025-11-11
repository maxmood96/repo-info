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
-	[`couchdb:3.5.1`](#couchdb351)
-	[`couchdb:3.5.1-nouveau`](#couchdb351-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

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

### `couchdb:3` - linux; amd64

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

### `couchdb:3` - unknown; unknown

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

### `couchdb:3` - linux; arm64 variant v8

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

### `couchdb:3` - unknown; unknown

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
$ docker pull couchdb@sha256:62892a06582cc1217e9acd9fecfdec72987a0663535b4669eeb6d527c07ea007
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
$ docker pull couchdb@sha256:ba14630b9dad2c142c905ef78d836e2a2b4da23b5111409617461f45f4cfbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f64a3eafb3b15d9df4b97709f73460df419e811a21c8ef8431619fcf11bc1a8`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:28:37 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 00:28:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:28:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:28:58 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:58 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:29:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 00:29:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 00:29:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 00:29:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 00:29:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d04d9845fcfae593ae1808345251e428ef4fb3c8dd5f936e2446654cd2b276`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0506dd93f2a5bc85ebf11a68aeaf5867c2ee4da3388c033286d544826e20ccc3`  
		Last Modified: Tue, 04 Nov 2025 00:29:38 GMT  
		Size: 7.9 MB (7881727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2644b8fa1680ae0db4ec90781ea2109d5e050f351aa461c5cc0cc22132e6407b`  
		Last Modified: Tue, 04 Nov 2025 00:29:45 GMT  
		Size: 77.4 MB (77380720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102078526bd9fb9e43df333c808651969972b027d7eb66c8dd51668ee8a1097b`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 424.1 KB (424085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6a356dbdef6d588ef7a563556455518fdca30553aa2a94c3d9c895ff04ff33`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 99.5 KB (99457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded44638d74930968683be2aae1b76ec4cf3ed2decf48ed338ebe322b2a600d0`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195a0de37f8a6313fe015f14ee4d812e2f3879ad65179950f570e1ffc4dd5d3`  
		Last Modified: Tue, 04 Nov 2025 00:29:43 GMT  
		Size: 42.4 MB (42436290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c48c9f3441b02ccdf5cce0efdff38a15396af514fd4a27d9229f4913f911c2`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:909d65395179abe79e89f3bec366cdf7f4c4efd475bd4c4ccb8cfbf8cb58a2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21c3978ba58ac3b5a46b5e03229658606e1b452f418e98a6c4c568d2cca7b7a`

```dockerfile
```

-	Layers:
	-	`sha256:ddf9955211f3b768c9af16b3d291532c4824ced4fbc85599ea5535c6e722bb3e`  
		Last Modified: Tue, 04 Nov 2025 11:33:32 GMT  
		Size: 3.7 MB (3658053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401aa995221ea5ba3da1571644b255e038ca4ba73a7a873e393aaabe799708d4`  
		Last Modified: Tue, 04 Nov 2025 11:33:33 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9b87ffe96a19f23609df806fe5d59f941aa3ae2718e83b12900b53c9a43dbf4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983a9ddc781a9ce172e99b3bd96a5bee58e893ed58250131b314e1cb6e687007`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:30:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 00:30:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:30:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:30:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:31:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 00:31:06 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 00:31:06 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 00:31:06 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 00:31:06 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d877567f4df604047f2eb226f625f3982f2115bb2483d6d9b54c784180f0fa92`  
		Last Modified: Tue, 04 Nov 2025 00:31:36 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4389d9e835eca1b8a7d6fb5a57c30dfaafa356b6861319e0eab3ee2774f07e7`  
		Last Modified: Tue, 04 Nov 2025 00:31:36 GMT  
		Size: 7.7 MB (7692036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eac257402c7ebe43ddf0fdd7dc6aa64da069f70515ce198c8674a629da30c1f`  
		Last Modified: Tue, 04 Nov 2025 00:31:47 GMT  
		Size: 76.7 MB (76691526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6a872f09b98f342372c3aac87e69ad3985bf34255863d62d313794e5a7a8c0`  
		Last Modified: Tue, 04 Nov 2025 00:31:37 GMT  
		Size: 392.7 KB (392688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621a0a38dc0a23e5f952219453939772d44d91fee2698b97ddadd10e51d9e803`  
		Last Modified: Tue, 04 Nov 2025 00:31:36 GMT  
		Size: 99.4 KB (99412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064dd1e307fee62fe335c8689346442ed37b02b4eace00c7948e7d449ca9c724`  
		Last Modified: Tue, 04 Nov 2025 00:31:36 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d722788c47ca1e7eab00963a5546fe2f9ac6be08a16a51beed0c50b10a85368`  
		Last Modified: Tue, 04 Nov 2025 00:31:42 GMT  
		Size: 42.3 MB (42338491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfaaa9b14c9b02f5bac8c6408e2210c4f8e3fa2f35097de8a33f44a06061754`  
		Last Modified: Tue, 04 Nov 2025 00:31:37 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:68319b39ca1f6a8aeff03f16a32261d92d9b813588f9d89ba56980315b7244ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5767697258fffa5fda2b7790ecec01420248faa53fc27c0cca598875e3354057`

```dockerfile
```

-	Layers:
	-	`sha256:aa4478f273f0982f31978c0f8fe94ca2d1ed57a7fe9c58caee50c37f36cf4064`  
		Last Modified: Tue, 04 Nov 2025 11:33:37 GMT  
		Size: 3.7 MB (3656729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b86d89e8aa3be9f669ace6674a11e46c52bb794e184182dd6113be09aed2971`  
		Last Modified: Tue, 04 Nov 2025 11:33:38 GMT  
		Size: 24.7 KB (24702 bytes)  
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
$ docker pull couchdb@sha256:57aaf1f94039ddae75a3994fc5cef5f06764344fe919ab307acfe522b9ed7995
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
$ docker pull couchdb@sha256:ae92649b1de2af5a30ea16afa0a15662287b1e906887234d1c40962f9bd396e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139013957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc040e8ea83945c4fd839a438c8fad3ee6237c167c82854bacd1143932162fed`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:28:47 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 00:28:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:28:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:29:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:01 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 04 Nov 2025 00:29:01 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:29:14 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 00:29:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 00:29:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c309e0064c83abaec532030cb896235be9913190de769e3856c578805467b1`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af37cbb4228b62b8a25984f56f3f1f6319ca4778a1e53dcadbef7ae9f60a76ca`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 7.9 MB (7881768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8b88432ef4a069404a98fc7da5da7daf4a41a71d6fa95d4e6775d383a87022`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 401.7 KB (401731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb078d567a91f2796daf6f979be6c01b370b303f417e407fdfb4bc2f5bc30c1e`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 76.5 KB (76510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b69adfad93090a275d6c5a6d35ad956857ddd317072a9d11b3c10357b1a0af`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa90b6b09fb165d3e3814d34725623133d8be304b59bbce9f1a15eec4bf55900`  
		Last Modified: Tue, 04 Nov 2025 00:29:48 GMT  
		Size: 102.4 MB (102419951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed773c86bcdb74d35e017d30c3201992f06144929c2d0ccb1dc10247f0d3f2b4`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4665b492d7528f234f5daf4aa405248fe5d6fc4dcb551d648ef67285b73f5121`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cde999ba539c4da994f46b8f03a176ef7cbb5ea82043469c322980720364d53`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a941d5a3854a0c9c1c25c9291b5f3eac8757408e365b0847d958abe30050b6f`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:0feb279ca88f41023331ad038a92457ce8e7be8f0cae73efe99ce6a24bdd648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517b5fcaadb85aaaeae3b6487482cee64014e781c108ff47d7277ac6bfc9f004`

```dockerfile
```

-	Layers:
	-	`sha256:46003e629c9efbaf1be067b184be32150c504a46ecb93b9117ba0805e01c313e`  
		Last Modified: Tue, 04 Nov 2025 11:33:42 GMT  
		Size: 4.1 MB (4125385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee11a78b0c7bfe5d99115d2cf9017a3a5cfaabf8ec850f49a897635c355b286b`  
		Last Modified: Tue, 04 Nov 2025 11:33:43 GMT  
		Size: 31.1 KB (31147 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2a7b27021eb330482389d6d0a458365aa3abbf33c95966970dfe473d829362bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138415822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293400da04488d1b9895e016d8aaa255135634d83a12262f02a317bb1df93392`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:30:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 00:31:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:31:07 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:31:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:13 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 04 Nov 2025 00:31:13 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:31:26 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 00:31:26 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 00:31:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa07e0ad136c2d81f08031cacea7cf53591018e635b98792dc196aa25f5ff817`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8530c6a682a670efa2dad1306e54ae7243dde03c298fd4d2314afbe526be8d74`  
		Last Modified: Tue, 04 Nov 2025 00:31:50 GMT  
		Size: 7.7 MB (7692062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbed46138490a32cdc42261c9cc74dbd61554773d5cd1ea6d6a1196313d7633`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 370.5 KB (370474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c6fd493d8273440f4a33bf48cba5e709cecb7890bf493442f3d30c7995927c`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 76.5 KB (76489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5700557c00ad6a97d945d95742339bd0231e8c04c7d53803c425a8ff77a8da64`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82205562d09d1353723fe9dfb290fb140071a479eab8ec17a6a771854f8bdfde`  
		Last Modified: Tue, 04 Nov 2025 00:32:01 GMT  
		Size: 102.2 MB (102169002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075bed437a0f95b0246c5fa38e3ce914b7b19bf0bae1e60b986dfcfaf9ed671e`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50813a568ad5d80449de58f1fa88f33e93d11792b55ab28e527bfa3b1bc9316c`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4b101f7877358209b006590c3cc4c5a30c0a488bf327fd4e8c3d4fc37ee949`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 2.2 KB (2223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba32e7e70af1d2f79e667a87423713201376e2369b85b0f97e7d3fe88c23a30`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:7cb7ee766ece8539a85b77062ae8649036c413e1d2a70493d24ff4fc115e5bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83d91f94a47bb0c4365f76ae4fef42d2e35f877379d22b9962bffea082f1704`

```dockerfile
```

-	Layers:
	-	`sha256:c36180c73e9391c022c084e45caf238e6a8589878bd467fdc26ce5256f33fca7`  
		Last Modified: Tue, 04 Nov 2025 11:33:48 GMT  
		Size: 4.1 MB (4125654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6417cc064e6e4c8735cf98e62c84aae8f155dab00e1888c9f77336417513d71f`  
		Last Modified: Tue, 04 Nov 2025 11:33:49 GMT  
		Size: 31.3 KB (31318 bytes)  
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
$ docker pull couchdb@sha256:73cec3233025fca7771de3c210356bb503cb8a4c33a83ad61ec68fa1bfd92003
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
$ docker pull couchdb@sha256:e89c1ca28509ef58d06eb69437b051ba82525209ef897d97ebd0f9538bad6d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07014dc088587ea17b296479e2301b20674dd791e8d144dac636d676017b1ff4`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:28:51 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 00:28:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:29:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:29:12 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:12 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:29:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 00:29:17 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 00:29:17 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 00:29:17 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 00:29:17 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1baa3f34f1f0b416fc635d8528859a4ace4a710155adb7bab7162be3d9c01ef`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc47a29a3aeceec28033eefdeef21ec52824e831c80a0b2082afb8dfcd1b143`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 7.9 MB (7881827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e654e32c73e5f166e000959eb66293ca86d969a50765309ae2577d2e199ce`  
		Last Modified: Tue, 04 Nov 2025 00:29:46 GMT  
		Size: 77.4 MB (77380777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2baca22c5b5dcb16d7d8b9090aef401fea173970ac366fc29058a0bd7ec82417`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 424.1 KB (424100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e38882bf6bf9d5eab34d9b24fc53c80b9f2f36381de70a135f97248d8add`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 99.5 KB (99509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec31032200367531e6dc5f66facb9b3f12f89c141af119373f883b866126a3d`  
		Last Modified: Tue, 04 Nov 2025 00:29:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3534afae21db3a85bdf3c2b158c1d794313c431cf94e5048291aca218dae7fbc`  
		Last Modified: Tue, 04 Nov 2025 00:29:46 GMT  
		Size: 42.4 MB (42436072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc445fc3dd6d577af95062e01bc783f112dbcc379c8dac4c52acfa983b5880c`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5e6190d3030c7e418be905a3d2918ccd4f2b335e3792f7e3f2965bb4f5a55043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821a21457ebebe2398298513512b18dc25e8d3bc87e89902e97ff42338fbd7f1`

```dockerfile
```

-	Layers:
	-	`sha256:3df563e514f63d880a008e1aa29d70ceeb0c130054aba118d127778031cd5531`  
		Last Modified: Tue, 04 Nov 2025 11:33:53 GMT  
		Size: 3.7 MB (3657747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b349c809c80936be658fef724eff8631b4e18eb7401d78066fcab5855c852541`  
		Last Modified: Tue, 04 Nov 2025 11:33:54 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6c9cf3dca020d2f49a7756fe8f8105f86d339d18a18e458d843d93acef026407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f6b5cce950c92e5012360057858e0a99cb68bb8213d701e15825f94bf1a849`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:30:58 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 00:31:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:31:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:31:16 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:16 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:31:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 00:31:21 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 00:31:21 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 00:31:21 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 00:31:21 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edcdf1865838daf6de13d2f54e6059b2ae577054f1243c900c51d96eff25016`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0fff095ff52d0d31ad80dcf98768cff07a53dcdc9e52780584470950235995`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 7.7 MB (7692016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829eaec023c87572eb2d4c890b8c5dc90b1779a07ef7e5b523e2bfa236a0fe3`  
		Last Modified: Tue, 04 Nov 2025 00:31:52 GMT  
		Size: 76.7 MB (76691605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce943843a58567bbdca0d02287165f7ce43c55558b3abd3f67630307fc46f5a`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 392.7 KB (392681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f3f6041487d038917d0260cd126c1e043a39d02c9551a19bd8e652909341d4`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 99.4 KB (99425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018defa4077bcb7effc54eb96363849f037e87acf35482b85943d11d814bbfd`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9066acdcf3de579f128c379ccf334603a47dc20a1a17ae720791ccd7bb4bf255`  
		Last Modified: Tue, 04 Nov 2025 00:31:51 GMT  
		Size: 42.3 MB (42338058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dc773705b3ce38bd572ebe6d6e4160480535d7e8f949f0908fac21ba0a7a6f`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c7dbc1f55361fca496f65603d9749809a1ae3f4743a0f0e089492b9b48c6006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9456edb0f9f0c90e8106370e9782aa17a893fbe04183aac243ab250d51d1d6`

```dockerfile
```

-	Layers:
	-	`sha256:cf84fcc0ed95c4f83de2383072e0a58e4c25b30d1a1686999406e013d4026fac`  
		Last Modified: Tue, 04 Nov 2025 11:33:58 GMT  
		Size: 3.7 MB (3656411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbbf19db69c0dd013c389362a7c08bd6befd9a121255d8b11287230a16f693b5`  
		Last Modified: Tue, 04 Nov 2025 11:33:59 GMT  
		Size: 24.4 KB (24384 bytes)  
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
$ docker pull couchdb@sha256:57aaf1f94039ddae75a3994fc5cef5f06764344fe919ab307acfe522b9ed7995
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
$ docker pull couchdb@sha256:ae92649b1de2af5a30ea16afa0a15662287b1e906887234d1c40962f9bd396e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139013957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc040e8ea83945c4fd839a438c8fad3ee6237c167c82854bacd1143932162fed`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:28:47 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 00:28:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:28:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:29:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:01 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 04 Nov 2025 00:29:01 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:29:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:29:14 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 00:29:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 00:29:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c309e0064c83abaec532030cb896235be9913190de769e3856c578805467b1`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af37cbb4228b62b8a25984f56f3f1f6319ca4778a1e53dcadbef7ae9f60a76ca`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 7.9 MB (7881768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8b88432ef4a069404a98fc7da5da7daf4a41a71d6fa95d4e6775d383a87022`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 401.7 KB (401731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb078d567a91f2796daf6f979be6c01b370b303f417e407fdfb4bc2f5bc30c1e`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 76.5 KB (76510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b69adfad93090a275d6c5a6d35ad956857ddd317072a9d11b3c10357b1a0af`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa90b6b09fb165d3e3814d34725623133d8be304b59bbce9f1a15eec4bf55900`  
		Last Modified: Tue, 04 Nov 2025 00:29:48 GMT  
		Size: 102.4 MB (102419951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed773c86bcdb74d35e017d30c3201992f06144929c2d0ccb1dc10247f0d3f2b4`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4665b492d7528f234f5daf4aa405248fe5d6fc4dcb551d648ef67285b73f5121`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cde999ba539c4da994f46b8f03a176ef7cbb5ea82043469c322980720364d53`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a941d5a3854a0c9c1c25c9291b5f3eac8757408e365b0847d958abe30050b6f`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:0feb279ca88f41023331ad038a92457ce8e7be8f0cae73efe99ce6a24bdd648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517b5fcaadb85aaaeae3b6487482cee64014e781c108ff47d7277ac6bfc9f004`

```dockerfile
```

-	Layers:
	-	`sha256:46003e629c9efbaf1be067b184be32150c504a46ecb93b9117ba0805e01c313e`  
		Last Modified: Tue, 04 Nov 2025 11:33:42 GMT  
		Size: 4.1 MB (4125385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee11a78b0c7bfe5d99115d2cf9017a3a5cfaabf8ec850f49a897635c355b286b`  
		Last Modified: Tue, 04 Nov 2025 11:33:43 GMT  
		Size: 31.1 KB (31147 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2a7b27021eb330482389d6d0a458365aa3abbf33c95966970dfe473d829362bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138415822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293400da04488d1b9895e016d8aaa255135634d83a12262f02a317bb1df93392`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:30:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 04 Nov 2025 00:31:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:31:07 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:31:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:13 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 04 Nov 2025 00:31:13 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:31:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:31:26 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Nov 2025 00:31:26 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 04 Nov 2025 00:31:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa07e0ad136c2d81f08031cacea7cf53591018e635b98792dc196aa25f5ff817`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8530c6a682a670efa2dad1306e54ae7243dde03c298fd4d2314afbe526be8d74`  
		Last Modified: Tue, 04 Nov 2025 00:31:50 GMT  
		Size: 7.7 MB (7692062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbed46138490a32cdc42261c9cc74dbd61554773d5cd1ea6d6a1196313d7633`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 370.5 KB (370474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c6fd493d8273440f4a33bf48cba5e709cecb7890bf493442f3d30c7995927c`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 76.5 KB (76489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5700557c00ad6a97d945d95742339bd0231e8c04c7d53803c425a8ff77a8da64`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82205562d09d1353723fe9dfb290fb140071a479eab8ec17a6a771854f8bdfde`  
		Last Modified: Tue, 04 Nov 2025 00:32:01 GMT  
		Size: 102.2 MB (102169002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075bed437a0f95b0246c5fa38e3ce914b7b19bf0bae1e60b986dfcfaf9ed671e`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50813a568ad5d80449de58f1fa88f33e93d11792b55ab28e527bfa3b1bc9316c`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4b101f7877358209b006590c3cc4c5a30c0a488bf327fd4e8c3d4fc37ee949`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 2.2 KB (2223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba32e7e70af1d2f79e667a87423713201376e2369b85b0f97e7d3fe88c23a30`  
		Last Modified: Tue, 04 Nov 2025 00:31:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:7cb7ee766ece8539a85b77062ae8649036c413e1d2a70493d24ff4fc115e5bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83d91f94a47bb0c4365f76ae4fef42d2e35f877379d22b9962bffea082f1704`

```dockerfile
```

-	Layers:
	-	`sha256:c36180c73e9391c022c084e45caf238e6a8589878bd467fdc26ce5256f33fca7`  
		Last Modified: Tue, 04 Nov 2025 11:33:48 GMT  
		Size: 4.1 MB (4125654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6417cc064e6e4c8735cf98e62c84aae8f155dab00e1888c9f77336417513d71f`  
		Last Modified: Tue, 04 Nov 2025 11:33:49 GMT  
		Size: 31.3 KB (31318 bytes)  
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
$ docker pull couchdb@sha256:73cec3233025fca7771de3c210356bb503cb8a4c33a83ad61ec68fa1bfd92003
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
$ docker pull couchdb@sha256:e89c1ca28509ef58d06eb69437b051ba82525209ef897d97ebd0f9538bad6d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07014dc088587ea17b296479e2301b20674dd791e8d144dac636d676017b1ff4`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:28:51 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 00:28:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:29:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:29:12 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:12 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:29:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 00:29:17 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 00:29:17 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 00:29:17 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 00:29:17 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1baa3f34f1f0b416fc635d8528859a4ace4a710155adb7bab7162be3d9c01ef`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc47a29a3aeceec28033eefdeef21ec52824e831c80a0b2082afb8dfcd1b143`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 7.9 MB (7881827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e654e32c73e5f166e000959eb66293ca86d969a50765309ae2577d2e199ce`  
		Last Modified: Tue, 04 Nov 2025 00:29:46 GMT  
		Size: 77.4 MB (77380777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2baca22c5b5dcb16d7d8b9090aef401fea173970ac366fc29058a0bd7ec82417`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 424.1 KB (424100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e38882bf6bf9d5eab34d9b24fc53c80b9f2f36381de70a135f97248d8add`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 99.5 KB (99509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec31032200367531e6dc5f66facb9b3f12f89c141af119373f883b866126a3d`  
		Last Modified: Tue, 04 Nov 2025 00:29:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3534afae21db3a85bdf3c2b158c1d794313c431cf94e5048291aca218dae7fbc`  
		Last Modified: Tue, 04 Nov 2025 00:29:46 GMT  
		Size: 42.4 MB (42436072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc445fc3dd6d577af95062e01bc783f112dbcc379c8dac4c52acfa983b5880c`  
		Last Modified: Tue, 04 Nov 2025 00:29:41 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5e6190d3030c7e418be905a3d2918ccd4f2b335e3792f7e3f2965bb4f5a55043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821a21457ebebe2398298513512b18dc25e8d3bc87e89902e97ff42338fbd7f1`

```dockerfile
```

-	Layers:
	-	`sha256:3df563e514f63d880a008e1aa29d70ceeb0c130054aba118d127778031cd5531`  
		Last Modified: Tue, 04 Nov 2025 11:33:53 GMT  
		Size: 3.7 MB (3657747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b349c809c80936be658fef724eff8631b4e18eb7401d78066fcab5855c852541`  
		Last Modified: Tue, 04 Nov 2025 11:33:54 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6c9cf3dca020d2f49a7756fe8f8105f86d339d18a18e458d843d93acef026407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f6b5cce950c92e5012360057858e0a99cb68bb8213d701e15825f94bf1a849`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:30:58 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 00:31:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:31:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:31:16 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:16 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:31:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 00:31:21 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 00:31:21 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 00:31:21 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 00:31:21 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edcdf1865838daf6de13d2f54e6059b2ae577054f1243c900c51d96eff25016`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0fff095ff52d0d31ad80dcf98768cff07a53dcdc9e52780584470950235995`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 7.7 MB (7692016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829eaec023c87572eb2d4c890b8c5dc90b1779a07ef7e5b523e2bfa236a0fe3`  
		Last Modified: Tue, 04 Nov 2025 00:31:52 GMT  
		Size: 76.7 MB (76691605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce943843a58567bbdca0d02287165f7ce43c55558b3abd3f67630307fc46f5a`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 392.7 KB (392681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f3f6041487d038917d0260cd126c1e043a39d02c9551a19bd8e652909341d4`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 99.4 KB (99425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018defa4077bcb7effc54eb96363849f037e87acf35482b85943d11d814bbfd`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9066acdcf3de579f128c379ccf334603a47dc20a1a17ae720791ccd7bb4bf255`  
		Last Modified: Tue, 04 Nov 2025 00:31:51 GMT  
		Size: 42.3 MB (42338058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dc773705b3ce38bd572ebe6d6e4160480535d7e8f949f0908fac21ba0a7a6f`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c7dbc1f55361fca496f65603d9749809a1ae3f4743a0f0e089492b9b48c6006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9456edb0f9f0c90e8106370e9782aa17a893fbe04183aac243ab250d51d1d6`

```dockerfile
```

-	Layers:
	-	`sha256:cf84fcc0ed95c4f83de2383072e0a58e4c25b30d1a1686999406e013d4026fac`  
		Last Modified: Tue, 04 Nov 2025 11:33:58 GMT  
		Size: 3.7 MB (3656411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbbf19db69c0dd013c389362a7c08bd6befd9a121255d8b11287230a16f693b5`  
		Last Modified: Tue, 04 Nov 2025 11:33:59 GMT  
		Size: 24.4 KB (24384 bytes)  
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

### `couchdb:3.5` - linux; amd64

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

### `couchdb:3.5` - unknown; unknown

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

### `couchdb:3.5` - linux; arm64 variant v8

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

### `couchdb:3.5` - unknown; unknown

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
$ docker pull couchdb@sha256:62892a06582cc1217e9acd9fecfdec72987a0663535b4669eeb6d527c07ea007
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
$ docker pull couchdb@sha256:ba14630b9dad2c142c905ef78d836e2a2b4da23b5111409617461f45f4cfbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f64a3eafb3b15d9df4b97709f73460df419e811a21c8ef8431619fcf11bc1a8`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:28:37 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 00:28:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:28:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:28:58 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:58 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:29:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 00:29:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 00:29:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 00:29:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 00:29:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d04d9845fcfae593ae1808345251e428ef4fb3c8dd5f936e2446654cd2b276`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0506dd93f2a5bc85ebf11a68aeaf5867c2ee4da3388c033286d544826e20ccc3`  
		Last Modified: Tue, 04 Nov 2025 00:29:38 GMT  
		Size: 7.9 MB (7881727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2644b8fa1680ae0db4ec90781ea2109d5e050f351aa461c5cc0cc22132e6407b`  
		Last Modified: Tue, 04 Nov 2025 00:29:45 GMT  
		Size: 77.4 MB (77380720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102078526bd9fb9e43df333c808651969972b027d7eb66c8dd51668ee8a1097b`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 424.1 KB (424085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6a356dbdef6d588ef7a563556455518fdca30553aa2a94c3d9c895ff04ff33`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 99.5 KB (99457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded44638d74930968683be2aae1b76ec4cf3ed2decf48ed338ebe322b2a600d0`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195a0de37f8a6313fe015f14ee4d812e2f3879ad65179950f570e1ffc4dd5d3`  
		Last Modified: Tue, 04 Nov 2025 00:29:43 GMT  
		Size: 42.4 MB (42436290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c48c9f3441b02ccdf5cce0efdff38a15396af514fd4a27d9229f4913f911c2`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:909d65395179abe79e89f3bec366cdf7f4c4efd475bd4c4ccb8cfbf8cb58a2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21c3978ba58ac3b5a46b5e03229658606e1b452f418e98a6c4c568d2cca7b7a`

```dockerfile
```

-	Layers:
	-	`sha256:ddf9955211f3b768c9af16b3d291532c4824ced4fbc85599ea5535c6e722bb3e`  
		Last Modified: Tue, 04 Nov 2025 11:33:32 GMT  
		Size: 3.7 MB (3658053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401aa995221ea5ba3da1571644b255e038ca4ba73a7a873e393aaabe799708d4`  
		Last Modified: Tue, 04 Nov 2025 11:33:33 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9b87ffe96a19f23609df806fe5d59f941aa3ae2718e83b12900b53c9a43dbf4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983a9ddc781a9ce172e99b3bd96a5bee58e893ed58250131b314e1cb6e687007`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:30:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 00:30:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:30:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:30:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:31:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 00:31:06 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 00:31:06 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 00:31:06 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 00:31:06 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d877567f4df604047f2eb226f625f3982f2115bb2483d6d9b54c784180f0fa92`  
		Last Modified: Tue, 04 Nov 2025 00:31:36 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4389d9e835eca1b8a7d6fb5a57c30dfaafa356b6861319e0eab3ee2774f07e7`  
		Last Modified: Tue, 04 Nov 2025 00:31:36 GMT  
		Size: 7.7 MB (7692036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eac257402c7ebe43ddf0fdd7dc6aa64da069f70515ce198c8674a629da30c1f`  
		Last Modified: Tue, 04 Nov 2025 00:31:47 GMT  
		Size: 76.7 MB (76691526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6a872f09b98f342372c3aac87e69ad3985bf34255863d62d313794e5a7a8c0`  
		Last Modified: Tue, 04 Nov 2025 00:31:37 GMT  
		Size: 392.7 KB (392688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621a0a38dc0a23e5f952219453939772d44d91fee2698b97ddadd10e51d9e803`  
		Last Modified: Tue, 04 Nov 2025 00:31:36 GMT  
		Size: 99.4 KB (99412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064dd1e307fee62fe335c8689346442ed37b02b4eace00c7948e7d449ca9c724`  
		Last Modified: Tue, 04 Nov 2025 00:31:36 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d722788c47ca1e7eab00963a5546fe2f9ac6be08a16a51beed0c50b10a85368`  
		Last Modified: Tue, 04 Nov 2025 00:31:42 GMT  
		Size: 42.3 MB (42338491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfaaa9b14c9b02f5bac8c6408e2210c4f8e3fa2f35097de8a33f44a06061754`  
		Last Modified: Tue, 04 Nov 2025 00:31:37 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:68319b39ca1f6a8aeff03f16a32261d92d9b813588f9d89ba56980315b7244ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5767697258fffa5fda2b7790ecec01420248faa53fc27c0cca598875e3354057`

```dockerfile
```

-	Layers:
	-	`sha256:aa4478f273f0982f31978c0f8fe94ca2d1ed57a7fe9c58caee50c37f36cf4064`  
		Last Modified: Tue, 04 Nov 2025 11:33:37 GMT  
		Size: 3.7 MB (3656729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b86d89e8aa3be9f669ace6674a11e46c52bb794e184182dd6113be09aed2971`  
		Last Modified: Tue, 04 Nov 2025 11:33:38 GMT  
		Size: 24.7 KB (24702 bytes)  
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

## `couchdb:3.5.1`

```console
$ docker pull couchdb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `couchdb:3.5.1-nouveau`

```console
$ docker pull couchdb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

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
