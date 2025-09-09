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
$ docker pull couchdb@sha256:c0e8e7b68e1ccba97c98cf2a2e663fd4c9640f87812f4766ca38ffe5738bc249
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
$ docker pull couchdb@sha256:b95bcd53008659d8016dd1bdc95b2952074d86d1d598ed4c61bca8f09724698a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139837150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472995ee8c03c44092cb9a96bad4498e55b5661bf4e108c3bbe89dec9c459134`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02874ef0d17870ffbcb996b7655706cd08883c9761fb16d8d8cb58170190395`  
		Last Modified: Mon, 08 Sep 2025 21:42:40 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abe607827c22fc61dfc9356f346f51fbadf91fe8983d1fe8d1904da0137c999`  
		Last Modified: Mon, 08 Sep 2025 22:33:38 GMT  
		Size: 7.9 MB (7881670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b693851f2e5c0e0cece860bf6060eb71b25e7dd60707ad26ee97e0fd434a6cd`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 401.7 KB (401718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c796a1084c5b9434ed05a243cae9091c6e39d3747a8d62a3528d8e795a0cac3`  
		Last Modified: Mon, 08 Sep 2025 21:42:48 GMT  
		Size: 76.4 KB (76449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2475bda188e32a8bda910ee3b9b98f72aededd6efc8f87b9bc12166917c55f`  
		Last Modified: Mon, 08 Sep 2025 21:42:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47de6950448afb52a0f6e68fe11d621335a0a609b541a68fdf705e7b35717eb`  
		Last Modified: Mon, 08 Sep 2025 22:33:53 GMT  
		Size: 103.2 MB (103243543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04055f063a12e0f2372637d95e6d1b12cea300742189537c833937a0fb76df41`  
		Last Modified: Mon, 08 Sep 2025 21:42:55 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1304422b4ad0a55342291b98914627a02ba192217b8424ba0a095c7e8e3a0c`  
		Last Modified: Mon, 08 Sep 2025 21:42:58 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df01ab1a94c9671c7c37ac8ad2dd9fb74ae08bba12866a771cb2223364f476f0`  
		Last Modified: Mon, 08 Sep 2025 21:43:02 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94da7c605dd357599c4e25cd8f424e4f5ff9bd22d95d14d7a14b344e62625d6`  
		Last Modified: Mon, 08 Sep 2025 22:22:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:383c24ac0aef3b31908f74bbc93cd27a175d083fd5e65ae7ff0ec3d163835569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadec22010348840b46bb003d3a8439c05bf35260008d82f858e63e429d57653`

```dockerfile
```

-	Layers:
	-	`sha256:e31bd3808ef7e9d9fd7a5eec2805a258870c216590bad03bb615a478696dc3b8`  
		Last Modified: Mon, 08 Sep 2025 22:33:23 GMT  
		Size: 4.1 MB (4141252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c126581567a0a912223f1eb5798965b323b9a6406927dfb83ec10d688db0b8b`  
		Last Modified: Mon, 08 Sep 2025 22:33:25 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8c088795e61db62546d957e586d21ee2599d95f33b647bedc7bbcfee70e364ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139156265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98c1cdbc1d67f44bc2446dc03661bc5f6c5fb55e957df155236dcd0e8d056b5`
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dfd0f0a11cfb4475496bf3c0a039952bb67ed261d7c02b753bc546362e7656`  
		Last Modified: Mon, 08 Sep 2025 22:08:09 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3407cf867bd8272881c8e9290b2765c27085903ce5cf2f77728ef0f6afcace`  
		Last Modified: Mon, 08 Sep 2025 22:34:10 GMT  
		Size: 7.7 MB (7692057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fd3164a19a9a5d8f964c095daed3f5aa04f2e6e82a3f3ba0c96d4e671a9b74`  
		Last Modified: Mon, 08 Sep 2025 22:08:15 GMT  
		Size: 370.5 KB (370473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92227dd86433e30e6797478ece5415068675fc85bfc707019f4ddfb9af86c116`  
		Last Modified: Mon, 08 Sep 2025 22:08:18 GMT  
		Size: 76.5 KB (76482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee6cccb20b53b5f199d05a74eb7f58afe60126ad07681ff8feb9274014b2901`  
		Last Modified: Mon, 08 Sep 2025 22:08:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc72cb942d4a8545d3f8a787dd64253b47ac5925a8da45377ab2e99a73fb436`  
		Last Modified: Mon, 08 Sep 2025 22:34:14 GMT  
		Size: 102.9 MB (102909727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00bd8b46de89a47d2f75f054a6e31bf1ca52df8af20d91a26bed085a32f01e6`  
		Last Modified: Mon, 08 Sep 2025 22:08:25 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce9e551c2ff2de57f6fb371cd24208a2623ded29d86477af969096cdfaa7d68`  
		Last Modified: Mon, 08 Sep 2025 22:08:29 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca51f108619cfc4aca73989c988cfa32b51b0e621bc1dcdcfd84f875c526a68d`  
		Last Modified: Mon, 08 Sep 2025 22:08:33 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dd906b025549a4590dbe3b5a06fe67cedbd724d789230614d230e0bf1fb523`  
		Last Modified: Mon, 08 Sep 2025 22:08:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:530176e511b143aae889927ddffed0806dba306d8cc0f4dbd81c42eb4e4bd171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60de6d938c13c3b5b0ef8e8988bfd2b08bd66c834059e37a6dd1d96b285fb77`

```dockerfile
```

-	Layers:
	-	`sha256:37c32034c53bb2875fb6d3b8468a88f14d4776e7dfa47820b11640b4d5dad536`  
		Last Modified: Mon, 08 Sep 2025 22:34:01 GMT  
		Size: 4.1 MB (4141545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeea811cb50722acc3864b0b40add00437f1efce99b5a763eb663f3c0f11f7b5`  
		Last Modified: Mon, 08 Sep 2025 22:34:02 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:e4a4fc9e58539d2868bd15e046780cd8d8b7a71a74c1eb9f555e22fdf9c0c86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136521588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4fca67cecb025b5c09cab9c9549cb681d94892aaf58073a27711545f702b5e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b7acab8e5e7b12089d79275ac325f69e00c57ef109efebab6c70c9cd73a40d`  
		Last Modified: Wed, 13 Aug 2025 15:09:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3abfab6aae8ef4c71d8ee0179a883e31407cdba29d7ec2aedcd6cf479dd3bf`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164187f5523648207c88c10beecff4fa873224418908ed2042111b9008220445`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 355.6 KB (355650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1ea234d9128aa5cf95bed7f6b642ed39541c3ce0421026891a6ae6c3a62cf6`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 76.3 KB (76347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d507f15e04c67e6c028ebaf9b70be03905c6b099f3280dc1ee5b6c61e54fb9`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32a62c011f37d07095a847adb6849fc8b49b594312b80901dd3fa8730a8f14`  
		Last Modified: Wed, 13 Aug 2025 16:38:43 GMT  
		Size: 101.8 MB (101798492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c7a0c08391ce264a34acc839e0c22ef3ae30cd5170382d429de2fd535dd89`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8e63f7118f360ea233b6a4b5bfe85601905a9f58ccd1f8e5bd49122797016e`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c223e87672740895458e8f91f45b4a146badb15e846fc58f8860c7318a8ff3ab`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317e7af7e41277224e9cbb8f9c30c37a3271c0df880f6cf92e4bb22db5ecefe2`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:37f51edaf047cdf5f5111855683e13ea3c6672c8a15c2251ae5e354aae7a84a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4166926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36fa1cbb03efdd840bd2a162de1c1575a3bbbdb97b9d101b488ed2ce25e1f89`

```dockerfile
```

-	Layers:
	-	`sha256:66a48a697a343af104ea7f47a48904fb5b1d220938d9142743643f1b94344055`  
		Last Modified: Wed, 13 Aug 2025 16:33:26 GMT  
		Size: 4.1 MB (4135145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f50372cd52cb3fa8e4baf039bb58aa2c00bbb482d234fe623bfcf97bd2ac1f1`  
		Last Modified: Wed, 13 Aug 2025 16:33:27 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:5a7e8dcf6a0a809f66f4fbff64171add0025dc4a74a11cfab030fd1a938fc5ea
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
$ docker pull couchdb@sha256:b1000e0728337dd3d84ebaaae6f0606aad5ed40783ec43e8d8eae080c47e4a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6174913c1edbe4abb6a5192b5da3e2cc2dbe98d474fd5f9f6c40197d55370b3`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b469ac2ee0e3de167e6a242a02c54780f46832a46adec0e2628b370dbe788460`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fbb2b8000b0f5224acce7d7e6b32b1b7f09b18dad205f60e215c2be97e01c6`  
		Last Modified: Mon, 08 Sep 2025 21:26:37 GMT  
		Size: 7.9 MB (7881706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0749606934f02d9c67481cdbce2383a1640ca962b8cdac1604926200040c6527`  
		Last Modified: Mon, 08 Sep 2025 21:26:39 GMT  
		Size: 77.3 MB (77326942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03e0c5ab13c309e483acd4dfac0bf2b4c9aa576e4e6f3099d74d6541c034e58`  
		Last Modified: Mon, 08 Sep 2025 21:42:49 GMT  
		Size: 424.1 KB (424053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62402c800df2aa69907248395af9a5444d6a518020da5c12bebaab7099fcc568`  
		Last Modified: Mon, 08 Sep 2025 21:42:54 GMT  
		Size: 99.5 KB (99458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379f4397e125183cdc9f6d9571026b7169da02ad39535616952ac5a5d0a03c9c`  
		Last Modified: Mon, 08 Sep 2025 21:42:57 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fd4a6c9a29fa6e9b997588eab01076f7d198804b90a422eb3984f4385f4d7e`  
		Last Modified: Mon, 08 Sep 2025 21:26:39 GMT  
		Size: 42.4 MB (42436150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b15fda7ea7094e694a9a26531dfe009c5b54591693bae26a2b348450daa0ef4`  
		Last Modified: Mon, 08 Sep 2025 21:43:01 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7cc7a922043a6a666bd63c85c204ba3fa27d932abd3ad8f12da97f22e55cfe62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e946331eff4f4a89498788d67dc707c84838fe29094a841106fffb9ddf0896e7`

```dockerfile
```

-	Layers:
	-	`sha256:456497be36d6dcbc4c20f2d97e31ce2a8054a70f4983bcb7d8d87eb57b856228`  
		Last Modified: Mon, 08 Sep 2025 22:34:00 GMT  
		Size: 3.7 MB (3658049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ac7b8fc9547dd403d45a11bc4af17a55f0e91d3737e7ac76d80dd8e44beb2c4`  
		Last Modified: Mon, 08 Sep 2025 22:34:01 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3c320412252cc51ad905a90f27314d2129bba036c3bad6e5e46e101951c2b814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155275817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa90d3a33c69e39a9b9ad1c6e4a1b85b4cf931531022771a51fb9674f9d8d922`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a413f0c733a3548b814f6d4a97fa0cddfddd52c06c883ec019e117d9c0b8f13`  
		Last Modified: Mon, 08 Sep 2025 22:08:07 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfa68e0ff0a2dd479b0b952e0d65bbd4dde57a1e73fe41f1713299ff30e1657`  
		Last Modified: Mon, 08 Sep 2025 22:33:28 GMT  
		Size: 7.7 MB (7691952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0cb2c245fa0d0ad988fea8289bf5b8d21c15588014c883cf5d724c7c70a586`  
		Last Modified: Mon, 08 Sep 2025 22:33:24 GMT  
		Size: 76.6 MB (76649232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f9064bd3c9558602ff908a34e094b3bb24f7c2b64b15e7fddb548496dd894f`  
		Last Modified: Mon, 08 Sep 2025 22:08:11 GMT  
		Size: 392.7 KB (392701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc201e9fe34a3aacbe4402ec0e076dbcb194b57971ed1a60f9a4db5627f37cf`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 99.5 KB (99461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6415e00a72e7cfa1467fa9cd048405a2fdacea142010c08fe37de5e06ed57c`  
		Last Modified: Mon, 08 Sep 2025 22:08:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35c8a5032090877150fd0f9bde65f05f188e355e7f6cb504ae91da2e96669af`  
		Last Modified: Mon, 08 Sep 2025 22:33:36 GMT  
		Size: 42.3 MB (42338496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab590219771a92c971baa49eded2f0146d5929ce2fba90bd5ad2f72b80a4d631`  
		Last Modified: Mon, 08 Sep 2025 22:08:23 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:48dd97b02ce0cdc1804326b19f6668837df92b7c620be9019754487f47b35c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac76c4a5cdffbfaefe425e20949e9ee4cef4986e00481a145a4d875896f03d8`

```dockerfile
```

-	Layers:
	-	`sha256:355963e5ee37c7e5941686c4aaa45632b9ca237edb3dda0123cc5ddf8ab7b5a8`  
		Last Modified: Mon, 08 Sep 2025 22:34:14 GMT  
		Size: 3.7 MB (3656725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2ae5fe0da96d9954608c0dbfc11c77cdb7efa5335814b985e377c2f31455b58`  
		Last Modified: Mon, 08 Sep 2025 22:34:15 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:73824f0155e246b84dea55564307bb35e5f8c148c20955998c2141c0b530aaaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150023195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05f9dc355961a03f42bc99f2f59d7ec43cc26298525416313408f7c14cf92e1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3477dad2db3c13f403c9d3623e6dfb36742c6965d5f54e5dc14e6cdde7a66a`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86997ea5cef151b0f22463c8db32b22377a36a2731a2463041c00e51c38e300a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 7.4 MB (7397796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b144c470493ab37c0bb7e68831cbd7adcb46418984ff5c2e15bc9294f2bbf8`  
		Last Modified: Wed, 13 Aug 2025 15:11:09 GMT  
		Size: 73.1 MB (73095781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00131fd1a5e3b4e5c4d46a08db3d5872c0188af95bf15854a2dbf3905f33f8bf`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 378.1 KB (378144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f80705c9664868350b03281eb24469f3aceb54869ffc9f657263080c30ea5a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 99.5 KB (99457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ffc778b9acc33d5910aea83aa62f4b55cdb80c97d48981b56efa84efafa3`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fee0e258dfab558556571f6bbf5be945aba0594c7d94ded0b2534a3e561ff0`  
		Last Modified: Wed, 13 Aug 2025 15:11:02 GMT  
		Size: 42.2 MB (42162304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3262828dcf86d709adeba6a2659dbcb199cb7c93304d7598634ace98064db058`  
		Last Modified: Wed, 13 Aug 2025 15:10:47 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:01e73baa3ddf3cc18244596980d9dbcd0715dd0f702b80e3442ad77f92b26036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c061cd234b8d24d411d7c378a6431d7b93c84e003406baf7937afd63b9eb74`

```dockerfile
```

-	Layers:
	-	`sha256:38077c4ca8e780d7f9c82c3324c4faef42cfd6c9bfa6bb634844fafe940de982`  
		Last Modified: Wed, 13 Aug 2025 16:33:34 GMT  
		Size: 3.6 MB (3646275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f6c362c5aa68c17e5335c7507046ee6ac7c287bfa8c411dd4e163c833835dd`  
		Last Modified: Wed, 13 Aug 2025 16:33:35 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:bcb7a898d001c83c779bafbbd21fc57debce5886dabb30692044c4d340cdc810
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
$ docker pull couchdb@sha256:ef4ab623af1624c13ea67ecd9475ca2116fc877c85e48e5fa88b9d90f323fa66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139013583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f6894d9bf86c984051e8194effca96bac608dd1ed32d24ec7767d01628cfef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadd5196727acc47bd8397cf721b14237399c925d1258e8ee6ae652075c1772a`  
		Last Modified: Mon, 08 Sep 2025 22:08:04 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e3b3f8f776382533f5888c683708273e5f72b6e24c209377500ac6a44ce111`  
		Last Modified: Mon, 08 Sep 2025 22:09:54 GMT  
		Size: 7.9 MB (7881670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb92244e71ae359073947922b27a989ab5fd8d2b14234f71008c2acd7d42ca6d`  
		Last Modified: Mon, 08 Sep 2025 22:08:05 GMT  
		Size: 401.7 KB (401707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7c0fbb80a2ac6fc93b3712a0386d4ca6329c4da3b9f53bbe68e9c498092ce`  
		Last Modified: Mon, 08 Sep 2025 22:08:05 GMT  
		Size: 76.5 KB (76477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d2620568f0afc5c672e596845afd63b765af6dd78e261aeb7d356bbc20ec2c`  
		Last Modified: Mon, 08 Sep 2025 22:08:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55a9d7805672ae43a0459c204f3695ade45c7e861efd901ce7c94670034c685`  
		Last Modified: Mon, 08 Sep 2025 22:10:13 GMT  
		Size: 102.4 MB (102419944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904bbccd069375a42fd4f274743539ed880e2b2c46ce521a3e6e24c67c1b6b63`  
		Last Modified: Mon, 08 Sep 2025 22:08:06 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e94fe13ebbfbdcff0f01cb769b28b9bb74011ce29ac7266e591a1a2a3a75f`  
		Last Modified: Mon, 08 Sep 2025 22:08:06 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553fa98518e939e05372c6bda4f4337f167c760d1d4d1430a0a7ff20c118256c`  
		Last Modified: Mon, 08 Sep 2025 22:08:04 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a66a955eb564fcc8db561594d49643315b302a5e842d811ea0f853c75ccdcae`  
		Last Modified: Mon, 08 Sep 2025 22:08:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:e11a9ec548b5e4cdc20b1c0b3bdd28f34c3d82d5db4977129923d5656efaf5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc1853b6951312fd33fdaaafe03ae640f6761bf1e4ba95dee1c3f0d0943afd8`

```dockerfile
```

-	Layers:
	-	`sha256:303be3ad4e9bfa2a526aa17feca6e209dd5e3b34aaeacf8e49b2bf62fa6de558`  
		Last Modified: Mon, 08 Sep 2025 22:33:42 GMT  
		Size: 4.1 MB (4125385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36bf1c8c852f15f4c87f11cc6f3cb5939c81b5e08f7d1754b0fa8198e72d959b`  
		Last Modified: Mon, 08 Sep 2025 22:33:43 GMT  
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
		Last Modified: Mon, 08 Sep 2025 21:41:42 GMT  
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
		Last Modified: Mon, 08 Sep 2025 21:41:46 GMT  
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
$ docker pull couchdb@sha256:475a31cbc44a2fb61db8f40f68d2a43a7df6203ab8541c60a04f00e75d23e9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135779239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76feea0d35e5f28c68026e61d63cbeb55bb86c2d0648537d7ef91a50a675a6e5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b7acab8e5e7b12089d79275ac325f69e00c57ef109efebab6c70c9cd73a40d`  
		Last Modified: Wed, 13 Aug 2025 15:09:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3abfab6aae8ef4c71d8ee0179a883e31407cdba29d7ec2aedcd6cf479dd3bf`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164187f5523648207c88c10beecff4fa873224418908ed2042111b9008220445`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 355.6 KB (355650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1ea234d9128aa5cf95bed7f6b642ed39541c3ce0421026891a6ae6c3a62cf6`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 76.3 KB (76347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31eafa29c931a560e6b3825d4cf7578551d10bac09d97f79640154888a5267d9`  
		Last Modified: Wed, 13 Aug 2025 15:11:41 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bbebb2451e44f221410bb99fc16c68d6227619ea1d40e46f1c322fa6be8261`  
		Last Modified: Wed, 13 Aug 2025 17:22:56 GMT  
		Size: 101.1 MB (101056146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40a1e5db618c6db55c67aa7470d25b6ff665bf2eee0850c6b4a2434a6cc675f`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d3a7c3c0f081c9aa325de28e5b1a88ce117e6e97089467714ef4323f8ff89d`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13c04d1d7a1610a81b44627a0729e8ba8f83564f7bd9d8795d524445398c22b`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31267d069eb208d9c0505bb4499401969fb3e2a1e110e98384699875ae34e7a4`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:0702144fbd51bc0883bda128b39914edbe0b5411395774d5ddea3ed2ac41e3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4150469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf7d8ae3a1b05777fc68c846391b7efa5169afc93e352141483d064edeaa51f`

```dockerfile
```

-	Layers:
	-	`sha256:b8f331a35f1260a06b663f45696307c75875b555c396b2c05247c107c0307a32`  
		Last Modified: Wed, 13 Aug 2025 16:33:38 GMT  
		Size: 4.1 MB (4119278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fafd3d357f9aa58405db89a43e13ea3fcc657daf32211a0a9105be43ee526d31`  
		Last Modified: Wed, 13 Aug 2025 16:33:39 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:3b5ccf824a5173f983307e0693daf3ea878e82b8ab3d9bb02b8fb0b416befb31
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
$ docker pull couchdb@sha256:fc156951f207beda56de104f9965b189e62e1078c445a8766092a5bbca92fea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854326454e38deab2dcd5275285b4bd8fafacbb210822d3563e0c36a3c67523c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac5fd24b088e695cfa5e583a8de36e34d198777bd912385973a58c4f4dcfd85`  
		Last Modified: Mon, 08 Sep 2025 22:14:40 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f6aa8434d654502e5e21451179c2fe05b15b0d82593b4dd843295b7cd4391a`  
		Last Modified: Mon, 08 Sep 2025 21:27:07 GMT  
		Size: 7.9 MB (7881695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ad7a4d42c79fb866c72d1fb68a4adfba9130eb471f828998ad14daae0723a2`  
		Last Modified: Mon, 08 Sep 2025 21:27:09 GMT  
		Size: 77.3 MB (77326959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2765bfc3b301187afbb88a4ce3bc9352be96fe266ab2c6281af4ca62d4ca92`  
		Last Modified: Mon, 08 Sep 2025 22:14:40 GMT  
		Size: 424.1 KB (424054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b17d9f624a75b9397d81b9b80c7fe652d6d025265f8427319672c300d2dced9`  
		Last Modified: Mon, 08 Sep 2025 22:14:40 GMT  
		Size: 99.5 KB (99463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3754f7ab58c64d4ff9029fde11339c0e8ab24a4a61307efbfc3def436d449024`  
		Last Modified: Mon, 08 Sep 2025 22:14:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8aeaac1cb958b871708f3c20194ee235e85a5492375c886c47067f32ef947f`  
		Last Modified: Mon, 08 Sep 2025 21:27:10 GMT  
		Size: 42.4 MB (42435998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd97f546b5988bf1498727c88645852b41d1fada2143a2ecc837bb37b581949`  
		Last Modified: Mon, 08 Sep 2025 22:14:40 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:cb168635cace2619715a96e07e71bc0f2c59bbbae96e9334b94d3eea3c893fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4421c57461a5e87a964328cae69bc3766b9707e214f39232396392dfabc88f57`

```dockerfile
```

-	Layers:
	-	`sha256:30841f25f10e6d5485a67a27c96005e89f5cf0a04fbe67aa0c8db84a8174ec48`  
		Last Modified: Mon, 08 Sep 2025 22:33:53 GMT  
		Size: 3.7 MB (3657743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1ae5b866196718b61a92c7607e885c9687b5770db928444968863d003b92249`  
		Last Modified: Mon, 08 Sep 2025 22:33:54 GMT  
		Size: 24.3 KB (24258 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:85108b7ef7c30b2b2ac1ea61017ae24ab871147f0228608c994a0efa8494bed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155275457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f732316eff3c69c663650542022bb8ebf33ce1bcebd939b241d3d37a3712e03`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f3aea18dc2c74e3bf2604c590b82d69ec17c8f30fadab9f68708ccc6d58e52`  
		Last Modified: Mon, 08 Sep 2025 22:08:12 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5f4919b40f0d6ec492fffebfcb1a81122eef6792283434b365539a45fae3f4`  
		Last Modified: Mon, 08 Sep 2025 21:41:45 GMT  
		Size: 7.7 MB (7691984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50833f270f863061e2167dc3a969cb7a4ebd7f2708f533f75169303ea2cff933`  
		Last Modified: Mon, 08 Sep 2025 21:41:47 GMT  
		Size: 76.6 MB (76649296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8c26cbe5662cf3743fbc580fa2addad24223369fd6c28e455b0362bac52312`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 392.7 KB (392684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3313b7ba41d03a66a87fc653285efe17639537e395fc524dcf8bd351d3fb9573`  
		Last Modified: Mon, 08 Sep 2025 22:08:21 GMT  
		Size: 99.5 KB (99458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7af0c1b857d42e65c4a88604dc7451d981235e39e13e44e07f540258fbad06`  
		Last Modified: Mon, 08 Sep 2025 22:08:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9910d259b5fc98b39dda5eb475cbaeb7b53d5e4459095424a22f19e87d565597`  
		Last Modified: Mon, 08 Sep 2025 21:41:47 GMT  
		Size: 42.3 MB (42338063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf86a48e935c57426db35a928aaf034797947d6b16ef5224fc691f0cfb765ac0`  
		Last Modified: Mon, 08 Sep 2025 22:08:28 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:0cddfa2334cf6886ff2aa2af554854b0b7556a5bea78b7a6b99159f1f469d230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c781c211f756ea6923fdb00845c369372b45f62231f2f0c8165268f986fc407b`

```dockerfile
```

-	Layers:
	-	`sha256:0c9fea88205c45b0ec4e689333bf90a772a7430ffdf94d50e56b3cdddae33bdf`  
		Last Modified: Mon, 08 Sep 2025 22:33:59 GMT  
		Size: 3.7 MB (3656407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9078381c8f8b54235bd210e177c44fe59eaf908c8c2bc709a5d7125d9f6bd59`  
		Last Modified: Mon, 08 Sep 2025 22:34:00 GMT  
		Size: 24.4 KB (24428 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:eb802fc992e4559ff4a4d86931e8abacee7477e8bd7d9081a539d1b8e8cbe10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150022545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7eeefa47cf18467fbc3c8b1d80b71d0c9b760dfcd35e335d0ff8f8b59e4457`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3477dad2db3c13f403c9d3623e6dfb36742c6965d5f54e5dc14e6cdde7a66a`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86997ea5cef151b0f22463c8db32b22377a36a2731a2463041c00e51c38e300a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 7.4 MB (7397796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b144c470493ab37c0bb7e68831cbd7adcb46418984ff5c2e15bc9294f2bbf8`  
		Last Modified: Wed, 13 Aug 2025 15:11:09 GMT  
		Size: 73.1 MB (73095781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00131fd1a5e3b4e5c4d46a08db3d5872c0188af95bf15854a2dbf3905f33f8bf`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 378.1 KB (378144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f80705c9664868350b03281eb24469f3aceb54869ffc9f657263080c30ea5a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 99.5 KB (99457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ffc778b9acc33d5910aea83aa62f4b55cdb80c97d48981b56efa84efafa3`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1e32bb5da08beecc59e3adfebac462d3735e0c1082b7aae9755aa546f19001`  
		Last Modified: Wed, 13 Aug 2025 15:11:47 GMT  
		Size: 42.2 MB (42161653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501d0bffdbbae076b8f7cf4c1e24462af05b6ee1ddd9d44f78b85acd0956579f`  
		Last Modified: Wed, 13 Aug 2025 16:11:52 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c38b501e412cf53d89d7668f6ff5916acc23a521a495ec1e244d147125605c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bf5b34db72d35433d90174d76b734fb1614dad3fdf0a5e17074ba96d3b858d`

```dockerfile
```

-	Layers:
	-	`sha256:6915d2adee7ad51bfb4d7c2bcc413e3c69a1e56f0befc34b51949dd445909dc1`  
		Last Modified: Wed, 13 Aug 2025 16:33:43 GMT  
		Size: 3.6 MB (3645969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b56d87596fc78b875c9be2053cd7dab18a060d82a70e52fc91dea42767b1636`  
		Last Modified: Wed, 13 Aug 2025 16:33:43 GMT  
		Size: 24.3 KB (24257 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:bcb7a898d001c83c779bafbbd21fc57debce5886dabb30692044c4d340cdc810
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
$ docker pull couchdb@sha256:ef4ab623af1624c13ea67ecd9475ca2116fc877c85e48e5fa88b9d90f323fa66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139013583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f6894d9bf86c984051e8194effca96bac608dd1ed32d24ec7767d01628cfef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadd5196727acc47bd8397cf721b14237399c925d1258e8ee6ae652075c1772a`  
		Last Modified: Mon, 08 Sep 2025 22:08:04 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e3b3f8f776382533f5888c683708273e5f72b6e24c209377500ac6a44ce111`  
		Last Modified: Mon, 08 Sep 2025 22:09:54 GMT  
		Size: 7.9 MB (7881670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb92244e71ae359073947922b27a989ab5fd8d2b14234f71008c2acd7d42ca6d`  
		Last Modified: Mon, 08 Sep 2025 22:08:05 GMT  
		Size: 401.7 KB (401707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7c0fbb80a2ac6fc93b3712a0386d4ca6329c4da3b9f53bbe68e9c498092ce`  
		Last Modified: Mon, 08 Sep 2025 22:08:05 GMT  
		Size: 76.5 KB (76477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d2620568f0afc5c672e596845afd63b765af6dd78e261aeb7d356bbc20ec2c`  
		Last Modified: Mon, 08 Sep 2025 22:08:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55a9d7805672ae43a0459c204f3695ade45c7e861efd901ce7c94670034c685`  
		Last Modified: Mon, 08 Sep 2025 22:10:13 GMT  
		Size: 102.4 MB (102419944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904bbccd069375a42fd4f274743539ed880e2b2c46ce521a3e6e24c67c1b6b63`  
		Last Modified: Mon, 08 Sep 2025 22:08:06 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e94fe13ebbfbdcff0f01cb769b28b9bb74011ce29ac7266e591a1a2a3a75f`  
		Last Modified: Mon, 08 Sep 2025 22:08:06 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553fa98518e939e05372c6bda4f4337f167c760d1d4d1430a0a7ff20c118256c`  
		Last Modified: Mon, 08 Sep 2025 22:08:04 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a66a955eb564fcc8db561594d49643315b302a5e842d811ea0f853c75ccdcae`  
		Last Modified: Mon, 08 Sep 2025 22:08:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e11a9ec548b5e4cdc20b1c0b3bdd28f34c3d82d5db4977129923d5656efaf5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc1853b6951312fd33fdaaafe03ae640f6761bf1e4ba95dee1c3f0d0943afd8`

```dockerfile
```

-	Layers:
	-	`sha256:303be3ad4e9bfa2a526aa17feca6e209dd5e3b34aaeacf8e49b2bf62fa6de558`  
		Last Modified: Mon, 08 Sep 2025 22:33:42 GMT  
		Size: 4.1 MB (4125385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36bf1c8c852f15f4c87f11cc6f3cb5939c81b5e08f7d1754b0fa8198e72d959b`  
		Last Modified: Mon, 08 Sep 2025 22:33:43 GMT  
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
		Last Modified: Mon, 08 Sep 2025 21:41:42 GMT  
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
		Last Modified: Mon, 08 Sep 2025 21:41:46 GMT  
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
$ docker pull couchdb@sha256:475a31cbc44a2fb61db8f40f68d2a43a7df6203ab8541c60a04f00e75d23e9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135779239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76feea0d35e5f28c68026e61d63cbeb55bb86c2d0648537d7ef91a50a675a6e5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b7acab8e5e7b12089d79275ac325f69e00c57ef109efebab6c70c9cd73a40d`  
		Last Modified: Wed, 13 Aug 2025 15:09:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3abfab6aae8ef4c71d8ee0179a883e31407cdba29d7ec2aedcd6cf479dd3bf`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164187f5523648207c88c10beecff4fa873224418908ed2042111b9008220445`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 355.6 KB (355650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1ea234d9128aa5cf95bed7f6b642ed39541c3ce0421026891a6ae6c3a62cf6`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 76.3 KB (76347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31eafa29c931a560e6b3825d4cf7578551d10bac09d97f79640154888a5267d9`  
		Last Modified: Wed, 13 Aug 2025 15:11:41 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bbebb2451e44f221410bb99fc16c68d6227619ea1d40e46f1c322fa6be8261`  
		Last Modified: Wed, 13 Aug 2025 17:22:56 GMT  
		Size: 101.1 MB (101056146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40a1e5db618c6db55c67aa7470d25b6ff665bf2eee0850c6b4a2434a6cc675f`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d3a7c3c0f081c9aa325de28e5b1a88ce117e6e97089467714ef4323f8ff89d`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13c04d1d7a1610a81b44627a0729e8ba8f83564f7bd9d8795d524445398c22b`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31267d069eb208d9c0505bb4499401969fb3e2a1e110e98384699875ae34e7a4`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:0702144fbd51bc0883bda128b39914edbe0b5411395774d5ddea3ed2ac41e3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4150469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf7d8ae3a1b05777fc68c846391b7efa5169afc93e352141483d064edeaa51f`

```dockerfile
```

-	Layers:
	-	`sha256:b8f331a35f1260a06b663f45696307c75875b555c396b2c05247c107c0307a32`  
		Last Modified: Wed, 13 Aug 2025 16:33:38 GMT  
		Size: 4.1 MB (4119278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fafd3d357f9aa58405db89a43e13ea3fcc657daf32211a0a9105be43ee526d31`  
		Last Modified: Wed, 13 Aug 2025 16:33:39 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:3b5ccf824a5173f983307e0693daf3ea878e82b8ab3d9bb02b8fb0b416befb31
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
$ docker pull couchdb@sha256:fc156951f207beda56de104f9965b189e62e1078c445a8766092a5bbca92fea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854326454e38deab2dcd5275285b4bd8fafacbb210822d3563e0c36a3c67523c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac5fd24b088e695cfa5e583a8de36e34d198777bd912385973a58c4f4dcfd85`  
		Last Modified: Mon, 08 Sep 2025 22:14:40 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f6aa8434d654502e5e21451179c2fe05b15b0d82593b4dd843295b7cd4391a`  
		Last Modified: Mon, 08 Sep 2025 21:27:07 GMT  
		Size: 7.9 MB (7881695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ad7a4d42c79fb866c72d1fb68a4adfba9130eb471f828998ad14daae0723a2`  
		Last Modified: Mon, 08 Sep 2025 21:27:09 GMT  
		Size: 77.3 MB (77326959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2765bfc3b301187afbb88a4ce3bc9352be96fe266ab2c6281af4ca62d4ca92`  
		Last Modified: Mon, 08 Sep 2025 22:14:40 GMT  
		Size: 424.1 KB (424054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b17d9f624a75b9397d81b9b80c7fe652d6d025265f8427319672c300d2dced9`  
		Last Modified: Mon, 08 Sep 2025 22:14:40 GMT  
		Size: 99.5 KB (99463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3754f7ab58c64d4ff9029fde11339c0e8ab24a4a61307efbfc3def436d449024`  
		Last Modified: Mon, 08 Sep 2025 22:14:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8aeaac1cb958b871708f3c20194ee235e85a5492375c886c47067f32ef947f`  
		Last Modified: Mon, 08 Sep 2025 21:27:10 GMT  
		Size: 42.4 MB (42435998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd97f546b5988bf1498727c88645852b41d1fada2143a2ecc837bb37b581949`  
		Last Modified: Mon, 08 Sep 2025 22:14:40 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:cb168635cace2619715a96e07e71bc0f2c59bbbae96e9334b94d3eea3c893fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4421c57461a5e87a964328cae69bc3766b9707e214f39232396392dfabc88f57`

```dockerfile
```

-	Layers:
	-	`sha256:30841f25f10e6d5485a67a27c96005e89f5cf0a04fbe67aa0c8db84a8174ec48`  
		Last Modified: Mon, 08 Sep 2025 22:33:53 GMT  
		Size: 3.7 MB (3657743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1ae5b866196718b61a92c7607e885c9687b5770db928444968863d003b92249`  
		Last Modified: Mon, 08 Sep 2025 22:33:54 GMT  
		Size: 24.3 KB (24258 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:85108b7ef7c30b2b2ac1ea61017ae24ab871147f0228608c994a0efa8494bed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155275457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f732316eff3c69c663650542022bb8ebf33ce1bcebd939b241d3d37a3712e03`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f3aea18dc2c74e3bf2604c590b82d69ec17c8f30fadab9f68708ccc6d58e52`  
		Last Modified: Mon, 08 Sep 2025 22:08:12 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5f4919b40f0d6ec492fffebfcb1a81122eef6792283434b365539a45fae3f4`  
		Last Modified: Mon, 08 Sep 2025 21:41:45 GMT  
		Size: 7.7 MB (7691984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50833f270f863061e2167dc3a969cb7a4ebd7f2708f533f75169303ea2cff933`  
		Last Modified: Mon, 08 Sep 2025 21:41:47 GMT  
		Size: 76.6 MB (76649296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8c26cbe5662cf3743fbc580fa2addad24223369fd6c28e455b0362bac52312`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 392.7 KB (392684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3313b7ba41d03a66a87fc653285efe17639537e395fc524dcf8bd351d3fb9573`  
		Last Modified: Mon, 08 Sep 2025 22:08:21 GMT  
		Size: 99.5 KB (99458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7af0c1b857d42e65c4a88604dc7451d981235e39e13e44e07f540258fbad06`  
		Last Modified: Mon, 08 Sep 2025 22:08:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9910d259b5fc98b39dda5eb475cbaeb7b53d5e4459095424a22f19e87d565597`  
		Last Modified: Mon, 08 Sep 2025 21:41:47 GMT  
		Size: 42.3 MB (42338063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf86a48e935c57426db35a928aaf034797947d6b16ef5224fc691f0cfb765ac0`  
		Last Modified: Mon, 08 Sep 2025 22:08:28 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:0cddfa2334cf6886ff2aa2af554854b0b7556a5bea78b7a6b99159f1f469d230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c781c211f756ea6923fdb00845c369372b45f62231f2f0c8165268f986fc407b`

```dockerfile
```

-	Layers:
	-	`sha256:0c9fea88205c45b0ec4e689333bf90a772a7430ffdf94d50e56b3cdddae33bdf`  
		Last Modified: Mon, 08 Sep 2025 22:33:59 GMT  
		Size: 3.7 MB (3656407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9078381c8f8b54235bd210e177c44fe59eaf908c8c2bc709a5d7125d9f6bd59`  
		Last Modified: Mon, 08 Sep 2025 22:34:00 GMT  
		Size: 24.4 KB (24428 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:eb802fc992e4559ff4a4d86931e8abacee7477e8bd7d9081a539d1b8e8cbe10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150022545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7eeefa47cf18467fbc3c8b1d80b71d0c9b760dfcd35e335d0ff8f8b59e4457`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3477dad2db3c13f403c9d3623e6dfb36742c6965d5f54e5dc14e6cdde7a66a`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86997ea5cef151b0f22463c8db32b22377a36a2731a2463041c00e51c38e300a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 7.4 MB (7397796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b144c470493ab37c0bb7e68831cbd7adcb46418984ff5c2e15bc9294f2bbf8`  
		Last Modified: Wed, 13 Aug 2025 15:11:09 GMT  
		Size: 73.1 MB (73095781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00131fd1a5e3b4e5c4d46a08db3d5872c0188af95bf15854a2dbf3905f33f8bf`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 378.1 KB (378144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f80705c9664868350b03281eb24469f3aceb54869ffc9f657263080c30ea5a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 99.5 KB (99457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ffc778b9acc33d5910aea83aa62f4b55cdb80c97d48981b56efa84efafa3`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1e32bb5da08beecc59e3adfebac462d3735e0c1082b7aae9755aa546f19001`  
		Last Modified: Wed, 13 Aug 2025 15:11:47 GMT  
		Size: 42.2 MB (42161653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501d0bffdbbae076b8f7cf4c1e24462af05b6ee1ddd9d44f78b85acd0956579f`  
		Last Modified: Wed, 13 Aug 2025 16:11:52 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c38b501e412cf53d89d7668f6ff5916acc23a521a495ec1e244d147125605c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bf5b34db72d35433d90174d76b734fb1614dad3fdf0a5e17074ba96d3b858d`

```dockerfile
```

-	Layers:
	-	`sha256:6915d2adee7ad51bfb4d7c2bcc413e3c69a1e56f0befc34b51949dd445909dc1`  
		Last Modified: Wed, 13 Aug 2025 16:33:43 GMT  
		Size: 3.6 MB (3645969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b56d87596fc78b875c9be2053cd7dab18a060d82a70e52fc91dea42767b1636`  
		Last Modified: Wed, 13 Aug 2025 16:33:43 GMT  
		Size: 24.3 KB (24257 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:c0e8e7b68e1ccba97c98cf2a2e663fd4c9640f87812f4766ca38ffe5738bc249
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
$ docker pull couchdb@sha256:b95bcd53008659d8016dd1bdc95b2952074d86d1d598ed4c61bca8f09724698a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139837150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472995ee8c03c44092cb9a96bad4498e55b5661bf4e108c3bbe89dec9c459134`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02874ef0d17870ffbcb996b7655706cd08883c9761fb16d8d8cb58170190395`  
		Last Modified: Mon, 08 Sep 2025 21:42:40 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abe607827c22fc61dfc9356f346f51fbadf91fe8983d1fe8d1904da0137c999`  
		Last Modified: Mon, 08 Sep 2025 22:33:38 GMT  
		Size: 7.9 MB (7881670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b693851f2e5c0e0cece860bf6060eb71b25e7dd60707ad26ee97e0fd434a6cd`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 401.7 KB (401718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c796a1084c5b9434ed05a243cae9091c6e39d3747a8d62a3528d8e795a0cac3`  
		Last Modified: Mon, 08 Sep 2025 21:42:48 GMT  
		Size: 76.4 KB (76449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2475bda188e32a8bda910ee3b9b98f72aededd6efc8f87b9bc12166917c55f`  
		Last Modified: Mon, 08 Sep 2025 21:42:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47de6950448afb52a0f6e68fe11d621335a0a609b541a68fdf705e7b35717eb`  
		Last Modified: Mon, 08 Sep 2025 22:33:53 GMT  
		Size: 103.2 MB (103243543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04055f063a12e0f2372637d95e6d1b12cea300742189537c833937a0fb76df41`  
		Last Modified: Mon, 08 Sep 2025 21:42:55 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1304422b4ad0a55342291b98914627a02ba192217b8424ba0a095c7e8e3a0c`  
		Last Modified: Mon, 08 Sep 2025 21:42:58 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df01ab1a94c9671c7c37ac8ad2dd9fb74ae08bba12866a771cb2223364f476f0`  
		Last Modified: Mon, 08 Sep 2025 21:43:02 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94da7c605dd357599c4e25cd8f424e4f5ff9bd22d95d14d7a14b344e62625d6`  
		Last Modified: Mon, 08 Sep 2025 22:22:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:383c24ac0aef3b31908f74bbc93cd27a175d083fd5e65ae7ff0ec3d163835569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadec22010348840b46bb003d3a8439c05bf35260008d82f858e63e429d57653`

```dockerfile
```

-	Layers:
	-	`sha256:e31bd3808ef7e9d9fd7a5eec2805a258870c216590bad03bb615a478696dc3b8`  
		Last Modified: Mon, 08 Sep 2025 22:33:23 GMT  
		Size: 4.1 MB (4141252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c126581567a0a912223f1eb5798965b323b9a6406927dfb83ec10d688db0b8b`  
		Last Modified: Mon, 08 Sep 2025 22:33:25 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8c088795e61db62546d957e586d21ee2599d95f33b647bedc7bbcfee70e364ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139156265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98c1cdbc1d67f44bc2446dc03661bc5f6c5fb55e957df155236dcd0e8d056b5`
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dfd0f0a11cfb4475496bf3c0a039952bb67ed261d7c02b753bc546362e7656`  
		Last Modified: Mon, 08 Sep 2025 22:08:09 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3407cf867bd8272881c8e9290b2765c27085903ce5cf2f77728ef0f6afcace`  
		Last Modified: Mon, 08 Sep 2025 22:34:10 GMT  
		Size: 7.7 MB (7692057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fd3164a19a9a5d8f964c095daed3f5aa04f2e6e82a3f3ba0c96d4e671a9b74`  
		Last Modified: Mon, 08 Sep 2025 22:08:15 GMT  
		Size: 370.5 KB (370473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92227dd86433e30e6797478ece5415068675fc85bfc707019f4ddfb9af86c116`  
		Last Modified: Mon, 08 Sep 2025 22:08:18 GMT  
		Size: 76.5 KB (76482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee6cccb20b53b5f199d05a74eb7f58afe60126ad07681ff8feb9274014b2901`  
		Last Modified: Mon, 08 Sep 2025 22:08:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc72cb942d4a8545d3f8a787dd64253b47ac5925a8da45377ab2e99a73fb436`  
		Last Modified: Mon, 08 Sep 2025 22:34:14 GMT  
		Size: 102.9 MB (102909727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00bd8b46de89a47d2f75f054a6e31bf1ca52df8af20d91a26bed085a32f01e6`  
		Last Modified: Mon, 08 Sep 2025 22:08:25 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce9e551c2ff2de57f6fb371cd24208a2623ded29d86477af969096cdfaa7d68`  
		Last Modified: Mon, 08 Sep 2025 22:08:29 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca51f108619cfc4aca73989c988cfa32b51b0e621bc1dcdcfd84f875c526a68d`  
		Last Modified: Mon, 08 Sep 2025 22:08:33 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dd906b025549a4590dbe3b5a06fe67cedbd724d789230614d230e0bf1fb523`  
		Last Modified: Mon, 08 Sep 2025 22:08:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:530176e511b143aae889927ddffed0806dba306d8cc0f4dbd81c42eb4e4bd171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60de6d938c13c3b5b0ef8e8988bfd2b08bd66c834059e37a6dd1d96b285fb77`

```dockerfile
```

-	Layers:
	-	`sha256:37c32034c53bb2875fb6d3b8468a88f14d4776e7dfa47820b11640b4d5dad536`  
		Last Modified: Mon, 08 Sep 2025 22:34:01 GMT  
		Size: 4.1 MB (4141545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeea811cb50722acc3864b0b40add00437f1efce99b5a763eb663f3c0f11f7b5`  
		Last Modified: Mon, 08 Sep 2025 22:34:02 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:e4a4fc9e58539d2868bd15e046780cd8d8b7a71a74c1eb9f555e22fdf9c0c86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136521588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4fca67cecb025b5c09cab9c9549cb681d94892aaf58073a27711545f702b5e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b7acab8e5e7b12089d79275ac325f69e00c57ef109efebab6c70c9cd73a40d`  
		Last Modified: Wed, 13 Aug 2025 15:09:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3abfab6aae8ef4c71d8ee0179a883e31407cdba29d7ec2aedcd6cf479dd3bf`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164187f5523648207c88c10beecff4fa873224418908ed2042111b9008220445`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 355.6 KB (355650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1ea234d9128aa5cf95bed7f6b642ed39541c3ce0421026891a6ae6c3a62cf6`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 76.3 KB (76347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d507f15e04c67e6c028ebaf9b70be03905c6b099f3280dc1ee5b6c61e54fb9`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32a62c011f37d07095a847adb6849fc8b49b594312b80901dd3fa8730a8f14`  
		Last Modified: Wed, 13 Aug 2025 16:38:43 GMT  
		Size: 101.8 MB (101798492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c7a0c08391ce264a34acc839e0c22ef3ae30cd5170382d429de2fd535dd89`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8e63f7118f360ea233b6a4b5bfe85601905a9f58ccd1f8e5bd49122797016e`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c223e87672740895458e8f91f45b4a146badb15e846fc58f8860c7318a8ff3ab`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317e7af7e41277224e9cbb8f9c30c37a3271c0df880f6cf92e4bb22db5ecefe2`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:37f51edaf047cdf5f5111855683e13ea3c6672c8a15c2251ae5e354aae7a84a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4166926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36fa1cbb03efdd840bd2a162de1c1575a3bbbdb97b9d101b488ed2ce25e1f89`

```dockerfile
```

-	Layers:
	-	`sha256:66a48a697a343af104ea7f47a48904fb5b1d220938d9142743643f1b94344055`  
		Last Modified: Wed, 13 Aug 2025 16:33:26 GMT  
		Size: 4.1 MB (4135145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f50372cd52cb3fa8e4baf039bb58aa2c00bbb482d234fe623bfcf97bd2ac1f1`  
		Last Modified: Wed, 13 Aug 2025 16:33:27 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:5a7e8dcf6a0a809f66f4fbff64171add0025dc4a74a11cfab030fd1a938fc5ea
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
$ docker pull couchdb@sha256:b1000e0728337dd3d84ebaaae6f0606aad5ed40783ec43e8d8eae080c47e4a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6174913c1edbe4abb6a5192b5da3e2cc2dbe98d474fd5f9f6c40197d55370b3`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b469ac2ee0e3de167e6a242a02c54780f46832a46adec0e2628b370dbe788460`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fbb2b8000b0f5224acce7d7e6b32b1b7f09b18dad205f60e215c2be97e01c6`  
		Last Modified: Mon, 08 Sep 2025 21:26:37 GMT  
		Size: 7.9 MB (7881706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0749606934f02d9c67481cdbce2383a1640ca962b8cdac1604926200040c6527`  
		Last Modified: Mon, 08 Sep 2025 21:26:39 GMT  
		Size: 77.3 MB (77326942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03e0c5ab13c309e483acd4dfac0bf2b4c9aa576e4e6f3099d74d6541c034e58`  
		Last Modified: Mon, 08 Sep 2025 21:42:49 GMT  
		Size: 424.1 KB (424053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62402c800df2aa69907248395af9a5444d6a518020da5c12bebaab7099fcc568`  
		Last Modified: Mon, 08 Sep 2025 21:42:54 GMT  
		Size: 99.5 KB (99458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379f4397e125183cdc9f6d9571026b7169da02ad39535616952ac5a5d0a03c9c`  
		Last Modified: Mon, 08 Sep 2025 21:42:57 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fd4a6c9a29fa6e9b997588eab01076f7d198804b90a422eb3984f4385f4d7e`  
		Last Modified: Mon, 08 Sep 2025 21:26:39 GMT  
		Size: 42.4 MB (42436150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b15fda7ea7094e694a9a26531dfe009c5b54591693bae26a2b348450daa0ef4`  
		Last Modified: Mon, 08 Sep 2025 21:43:01 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7cc7a922043a6a666bd63c85c204ba3fa27d932abd3ad8f12da97f22e55cfe62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e946331eff4f4a89498788d67dc707c84838fe29094a841106fffb9ddf0896e7`

```dockerfile
```

-	Layers:
	-	`sha256:456497be36d6dcbc4c20f2d97e31ce2a8054a70f4983bcb7d8d87eb57b856228`  
		Last Modified: Mon, 08 Sep 2025 22:34:00 GMT  
		Size: 3.7 MB (3658049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ac7b8fc9547dd403d45a11bc4af17a55f0e91d3737e7ac76d80dd8e44beb2c4`  
		Last Modified: Mon, 08 Sep 2025 22:34:01 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3c320412252cc51ad905a90f27314d2129bba036c3bad6e5e46e101951c2b814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155275817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa90d3a33c69e39a9b9ad1c6e4a1b85b4cf931531022771a51fb9674f9d8d922`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a413f0c733a3548b814f6d4a97fa0cddfddd52c06c883ec019e117d9c0b8f13`  
		Last Modified: Mon, 08 Sep 2025 22:08:07 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfa68e0ff0a2dd479b0b952e0d65bbd4dde57a1e73fe41f1713299ff30e1657`  
		Last Modified: Mon, 08 Sep 2025 22:33:28 GMT  
		Size: 7.7 MB (7691952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0cb2c245fa0d0ad988fea8289bf5b8d21c15588014c883cf5d724c7c70a586`  
		Last Modified: Mon, 08 Sep 2025 22:33:24 GMT  
		Size: 76.6 MB (76649232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f9064bd3c9558602ff908a34e094b3bb24f7c2b64b15e7fddb548496dd894f`  
		Last Modified: Mon, 08 Sep 2025 22:08:11 GMT  
		Size: 392.7 KB (392701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc201e9fe34a3aacbe4402ec0e076dbcb194b57971ed1a60f9a4db5627f37cf`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 99.5 KB (99461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6415e00a72e7cfa1467fa9cd048405a2fdacea142010c08fe37de5e06ed57c`  
		Last Modified: Mon, 08 Sep 2025 22:08:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35c8a5032090877150fd0f9bde65f05f188e355e7f6cb504ae91da2e96669af`  
		Last Modified: Mon, 08 Sep 2025 22:33:36 GMT  
		Size: 42.3 MB (42338496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab590219771a92c971baa49eded2f0146d5929ce2fba90bd5ad2f72b80a4d631`  
		Last Modified: Mon, 08 Sep 2025 22:08:23 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:48dd97b02ce0cdc1804326b19f6668837df92b7c620be9019754487f47b35c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac76c4a5cdffbfaefe425e20949e9ee4cef4986e00481a145a4d875896f03d8`

```dockerfile
```

-	Layers:
	-	`sha256:355963e5ee37c7e5941686c4aaa45632b9ca237edb3dda0123cc5ddf8ab7b5a8`  
		Last Modified: Mon, 08 Sep 2025 22:34:14 GMT  
		Size: 3.7 MB (3656725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2ae5fe0da96d9954608c0dbfc11c77cdb7efa5335814b985e377c2f31455b58`  
		Last Modified: Mon, 08 Sep 2025 22:34:15 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:73824f0155e246b84dea55564307bb35e5f8c148c20955998c2141c0b530aaaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150023195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05f9dc355961a03f42bc99f2f59d7ec43cc26298525416313408f7c14cf92e1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3477dad2db3c13f403c9d3623e6dfb36742c6965d5f54e5dc14e6cdde7a66a`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86997ea5cef151b0f22463c8db32b22377a36a2731a2463041c00e51c38e300a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 7.4 MB (7397796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b144c470493ab37c0bb7e68831cbd7adcb46418984ff5c2e15bc9294f2bbf8`  
		Last Modified: Wed, 13 Aug 2025 15:11:09 GMT  
		Size: 73.1 MB (73095781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00131fd1a5e3b4e5c4d46a08db3d5872c0188af95bf15854a2dbf3905f33f8bf`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 378.1 KB (378144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f80705c9664868350b03281eb24469f3aceb54869ffc9f657263080c30ea5a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 99.5 KB (99457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ffc778b9acc33d5910aea83aa62f4b55cdb80c97d48981b56efa84efafa3`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fee0e258dfab558556571f6bbf5be945aba0594c7d94ded0b2534a3e561ff0`  
		Last Modified: Wed, 13 Aug 2025 15:11:02 GMT  
		Size: 42.2 MB (42162304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3262828dcf86d709adeba6a2659dbcb199cb7c93304d7598634ace98064db058`  
		Last Modified: Wed, 13 Aug 2025 15:10:47 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:01e73baa3ddf3cc18244596980d9dbcd0715dd0f702b80e3442ad77f92b26036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c061cd234b8d24d411d7c378a6431d7b93c84e003406baf7937afd63b9eb74`

```dockerfile
```

-	Layers:
	-	`sha256:38077c4ca8e780d7f9c82c3324c4faef42cfd6c9bfa6bb634844fafe940de982`  
		Last Modified: Wed, 13 Aug 2025 16:33:34 GMT  
		Size: 3.6 MB (3646275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f6c362c5aa68c17e5335c7507046ee6ac7c287bfa8c411dd4e163c833835dd`  
		Last Modified: Wed, 13 Aug 2025 16:33:35 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0`

```console
$ docker pull couchdb@sha256:c0e8e7b68e1ccba97c98cf2a2e663fd4c9640f87812f4766ca38ffe5738bc249
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
$ docker pull couchdb@sha256:b95bcd53008659d8016dd1bdc95b2952074d86d1d598ed4c61bca8f09724698a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139837150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472995ee8c03c44092cb9a96bad4498e55b5661bf4e108c3bbe89dec9c459134`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02874ef0d17870ffbcb996b7655706cd08883c9761fb16d8d8cb58170190395`  
		Last Modified: Mon, 08 Sep 2025 21:42:40 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abe607827c22fc61dfc9356f346f51fbadf91fe8983d1fe8d1904da0137c999`  
		Last Modified: Mon, 08 Sep 2025 22:33:38 GMT  
		Size: 7.9 MB (7881670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b693851f2e5c0e0cece860bf6060eb71b25e7dd60707ad26ee97e0fd434a6cd`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 401.7 KB (401718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c796a1084c5b9434ed05a243cae9091c6e39d3747a8d62a3528d8e795a0cac3`  
		Last Modified: Mon, 08 Sep 2025 21:42:48 GMT  
		Size: 76.4 KB (76449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2475bda188e32a8bda910ee3b9b98f72aededd6efc8f87b9bc12166917c55f`  
		Last Modified: Mon, 08 Sep 2025 21:42:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47de6950448afb52a0f6e68fe11d621335a0a609b541a68fdf705e7b35717eb`  
		Last Modified: Mon, 08 Sep 2025 22:33:53 GMT  
		Size: 103.2 MB (103243543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04055f063a12e0f2372637d95e6d1b12cea300742189537c833937a0fb76df41`  
		Last Modified: Mon, 08 Sep 2025 21:42:55 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1304422b4ad0a55342291b98914627a02ba192217b8424ba0a095c7e8e3a0c`  
		Last Modified: Mon, 08 Sep 2025 21:42:58 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df01ab1a94c9671c7c37ac8ad2dd9fb74ae08bba12866a771cb2223364f476f0`  
		Last Modified: Mon, 08 Sep 2025 21:43:02 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94da7c605dd357599c4e25cd8f424e4f5ff9bd22d95d14d7a14b344e62625d6`  
		Last Modified: Mon, 08 Sep 2025 22:22:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:383c24ac0aef3b31908f74bbc93cd27a175d083fd5e65ae7ff0ec3d163835569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadec22010348840b46bb003d3a8439c05bf35260008d82f858e63e429d57653`

```dockerfile
```

-	Layers:
	-	`sha256:e31bd3808ef7e9d9fd7a5eec2805a258870c216590bad03bb615a478696dc3b8`  
		Last Modified: Mon, 08 Sep 2025 22:33:23 GMT  
		Size: 4.1 MB (4141252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c126581567a0a912223f1eb5798965b323b9a6406927dfb83ec10d688db0b8b`  
		Last Modified: Mon, 08 Sep 2025 22:33:25 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8c088795e61db62546d957e586d21ee2599d95f33b647bedc7bbcfee70e364ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139156265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98c1cdbc1d67f44bc2446dc03661bc5f6c5fb55e957df155236dcd0e8d056b5`
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dfd0f0a11cfb4475496bf3c0a039952bb67ed261d7c02b753bc546362e7656`  
		Last Modified: Mon, 08 Sep 2025 22:08:09 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3407cf867bd8272881c8e9290b2765c27085903ce5cf2f77728ef0f6afcace`  
		Last Modified: Mon, 08 Sep 2025 22:34:10 GMT  
		Size: 7.7 MB (7692057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fd3164a19a9a5d8f964c095daed3f5aa04f2e6e82a3f3ba0c96d4e671a9b74`  
		Last Modified: Mon, 08 Sep 2025 22:08:15 GMT  
		Size: 370.5 KB (370473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92227dd86433e30e6797478ece5415068675fc85bfc707019f4ddfb9af86c116`  
		Last Modified: Mon, 08 Sep 2025 22:08:18 GMT  
		Size: 76.5 KB (76482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee6cccb20b53b5f199d05a74eb7f58afe60126ad07681ff8feb9274014b2901`  
		Last Modified: Mon, 08 Sep 2025 22:08:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc72cb942d4a8545d3f8a787dd64253b47ac5925a8da45377ab2e99a73fb436`  
		Last Modified: Mon, 08 Sep 2025 22:34:14 GMT  
		Size: 102.9 MB (102909727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00bd8b46de89a47d2f75f054a6e31bf1ca52df8af20d91a26bed085a32f01e6`  
		Last Modified: Mon, 08 Sep 2025 22:08:25 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce9e551c2ff2de57f6fb371cd24208a2623ded29d86477af969096cdfaa7d68`  
		Last Modified: Mon, 08 Sep 2025 22:08:29 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca51f108619cfc4aca73989c988cfa32b51b0e621bc1dcdcfd84f875c526a68d`  
		Last Modified: Mon, 08 Sep 2025 22:08:33 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dd906b025549a4590dbe3b5a06fe67cedbd724d789230614d230e0bf1fb523`  
		Last Modified: Mon, 08 Sep 2025 22:08:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:530176e511b143aae889927ddffed0806dba306d8cc0f4dbd81c42eb4e4bd171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60de6d938c13c3b5b0ef8e8988bfd2b08bd66c834059e37a6dd1d96b285fb77`

```dockerfile
```

-	Layers:
	-	`sha256:37c32034c53bb2875fb6d3b8468a88f14d4776e7dfa47820b11640b4d5dad536`  
		Last Modified: Mon, 08 Sep 2025 22:34:01 GMT  
		Size: 4.1 MB (4141545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeea811cb50722acc3864b0b40add00437f1efce99b5a763eb663f3c0f11f7b5`  
		Last Modified: Mon, 08 Sep 2025 22:34:02 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; s390x

```console
$ docker pull couchdb@sha256:e4a4fc9e58539d2868bd15e046780cd8d8b7a71a74c1eb9f555e22fdf9c0c86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136521588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4fca67cecb025b5c09cab9c9549cb681d94892aaf58073a27711545f702b5e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b7acab8e5e7b12089d79275ac325f69e00c57ef109efebab6c70c9cd73a40d`  
		Last Modified: Wed, 13 Aug 2025 15:09:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3abfab6aae8ef4c71d8ee0179a883e31407cdba29d7ec2aedcd6cf479dd3bf`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164187f5523648207c88c10beecff4fa873224418908ed2042111b9008220445`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 355.6 KB (355650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1ea234d9128aa5cf95bed7f6b642ed39541c3ce0421026891a6ae6c3a62cf6`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 76.3 KB (76347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d507f15e04c67e6c028ebaf9b70be03905c6b099f3280dc1ee5b6c61e54fb9`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32a62c011f37d07095a847adb6849fc8b49b594312b80901dd3fa8730a8f14`  
		Last Modified: Wed, 13 Aug 2025 16:38:43 GMT  
		Size: 101.8 MB (101798492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c7a0c08391ce264a34acc839e0c22ef3ae30cd5170382d429de2fd535dd89`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8e63f7118f360ea233b6a4b5bfe85601905a9f58ccd1f8e5bd49122797016e`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c223e87672740895458e8f91f45b4a146badb15e846fc58f8860c7318a8ff3ab`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317e7af7e41277224e9cbb8f9c30c37a3271c0df880f6cf92e4bb22db5ecefe2`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:37f51edaf047cdf5f5111855683e13ea3c6672c8a15c2251ae5e354aae7a84a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4166926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36fa1cbb03efdd840bd2a162de1c1575a3bbbdb97b9d101b488ed2ce25e1f89`

```dockerfile
```

-	Layers:
	-	`sha256:66a48a697a343af104ea7f47a48904fb5b1d220938d9142743643f1b94344055`  
		Last Modified: Wed, 13 Aug 2025 16:33:26 GMT  
		Size: 4.1 MB (4135145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f50372cd52cb3fa8e4baf039bb58aa2c00bbb482d234fe623bfcf97bd2ac1f1`  
		Last Modified: Wed, 13 Aug 2025 16:33:27 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0-nouveau`

```console
$ docker pull couchdb@sha256:5a7e8dcf6a0a809f66f4fbff64171add0025dc4a74a11cfab030fd1a938fc5ea
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
$ docker pull couchdb@sha256:b1000e0728337dd3d84ebaaae6f0606aad5ed40783ec43e8d8eae080c47e4a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6174913c1edbe4abb6a5192b5da3e2cc2dbe98d474fd5f9f6c40197d55370b3`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b469ac2ee0e3de167e6a242a02c54780f46832a46adec0e2628b370dbe788460`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fbb2b8000b0f5224acce7d7e6b32b1b7f09b18dad205f60e215c2be97e01c6`  
		Last Modified: Mon, 08 Sep 2025 21:26:37 GMT  
		Size: 7.9 MB (7881706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0749606934f02d9c67481cdbce2383a1640ca962b8cdac1604926200040c6527`  
		Last Modified: Mon, 08 Sep 2025 21:26:39 GMT  
		Size: 77.3 MB (77326942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03e0c5ab13c309e483acd4dfac0bf2b4c9aa576e4e6f3099d74d6541c034e58`  
		Last Modified: Mon, 08 Sep 2025 21:42:49 GMT  
		Size: 424.1 KB (424053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62402c800df2aa69907248395af9a5444d6a518020da5c12bebaab7099fcc568`  
		Last Modified: Mon, 08 Sep 2025 21:42:54 GMT  
		Size: 99.5 KB (99458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379f4397e125183cdc9f6d9571026b7169da02ad39535616952ac5a5d0a03c9c`  
		Last Modified: Mon, 08 Sep 2025 21:42:57 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fd4a6c9a29fa6e9b997588eab01076f7d198804b90a422eb3984f4385f4d7e`  
		Last Modified: Mon, 08 Sep 2025 21:26:39 GMT  
		Size: 42.4 MB (42436150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b15fda7ea7094e694a9a26531dfe009c5b54591693bae26a2b348450daa0ef4`  
		Last Modified: Mon, 08 Sep 2025 21:43:01 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7cc7a922043a6a666bd63c85c204ba3fa27d932abd3ad8f12da97f22e55cfe62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e946331eff4f4a89498788d67dc707c84838fe29094a841106fffb9ddf0896e7`

```dockerfile
```

-	Layers:
	-	`sha256:456497be36d6dcbc4c20f2d97e31ce2a8054a70f4983bcb7d8d87eb57b856228`  
		Last Modified: Mon, 08 Sep 2025 22:34:00 GMT  
		Size: 3.7 MB (3658049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ac7b8fc9547dd403d45a11bc4af17a55f0e91d3737e7ac76d80dd8e44beb2c4`  
		Last Modified: Mon, 08 Sep 2025 22:34:01 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3c320412252cc51ad905a90f27314d2129bba036c3bad6e5e46e101951c2b814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155275817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa90d3a33c69e39a9b9ad1c6e4a1b85b4cf931531022771a51fb9674f9d8d922`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a413f0c733a3548b814f6d4a97fa0cddfddd52c06c883ec019e117d9c0b8f13`  
		Last Modified: Mon, 08 Sep 2025 22:08:07 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfa68e0ff0a2dd479b0b952e0d65bbd4dde57a1e73fe41f1713299ff30e1657`  
		Last Modified: Mon, 08 Sep 2025 22:33:28 GMT  
		Size: 7.7 MB (7691952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0cb2c245fa0d0ad988fea8289bf5b8d21c15588014c883cf5d724c7c70a586`  
		Last Modified: Mon, 08 Sep 2025 22:33:24 GMT  
		Size: 76.6 MB (76649232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f9064bd3c9558602ff908a34e094b3bb24f7c2b64b15e7fddb548496dd894f`  
		Last Modified: Mon, 08 Sep 2025 22:08:11 GMT  
		Size: 392.7 KB (392701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc201e9fe34a3aacbe4402ec0e076dbcb194b57971ed1a60f9a4db5627f37cf`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 99.5 KB (99461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6415e00a72e7cfa1467fa9cd048405a2fdacea142010c08fe37de5e06ed57c`  
		Last Modified: Mon, 08 Sep 2025 22:08:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35c8a5032090877150fd0f9bde65f05f188e355e7f6cb504ae91da2e96669af`  
		Last Modified: Mon, 08 Sep 2025 22:33:36 GMT  
		Size: 42.3 MB (42338496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab590219771a92c971baa49eded2f0146d5929ce2fba90bd5ad2f72b80a4d631`  
		Last Modified: Mon, 08 Sep 2025 22:08:23 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:48dd97b02ce0cdc1804326b19f6668837df92b7c620be9019754487f47b35c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac76c4a5cdffbfaefe425e20949e9ee4cef4986e00481a145a4d875896f03d8`

```dockerfile
```

-	Layers:
	-	`sha256:355963e5ee37c7e5941686c4aaa45632b9ca237edb3dda0123cc5ddf8ab7b5a8`  
		Last Modified: Mon, 08 Sep 2025 22:34:14 GMT  
		Size: 3.7 MB (3656725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2ae5fe0da96d9954608c0dbfc11c77cdb7efa5335814b985e377c2f31455b58`  
		Last Modified: Mon, 08 Sep 2025 22:34:15 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:73824f0155e246b84dea55564307bb35e5f8c148c20955998c2141c0b530aaaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150023195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05f9dc355961a03f42bc99f2f59d7ec43cc26298525416313408f7c14cf92e1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3477dad2db3c13f403c9d3623e6dfb36742c6965d5f54e5dc14e6cdde7a66a`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86997ea5cef151b0f22463c8db32b22377a36a2731a2463041c00e51c38e300a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 7.4 MB (7397796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b144c470493ab37c0bb7e68831cbd7adcb46418984ff5c2e15bc9294f2bbf8`  
		Last Modified: Wed, 13 Aug 2025 15:11:09 GMT  
		Size: 73.1 MB (73095781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00131fd1a5e3b4e5c4d46a08db3d5872c0188af95bf15854a2dbf3905f33f8bf`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 378.1 KB (378144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f80705c9664868350b03281eb24469f3aceb54869ffc9f657263080c30ea5a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 99.5 KB (99457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ffc778b9acc33d5910aea83aa62f4b55cdb80c97d48981b56efa84efafa3`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fee0e258dfab558556571f6bbf5be945aba0594c7d94ded0b2534a3e561ff0`  
		Last Modified: Wed, 13 Aug 2025 15:11:02 GMT  
		Size: 42.2 MB (42162304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3262828dcf86d709adeba6a2659dbcb199cb7c93304d7598634ace98064db058`  
		Last Modified: Wed, 13 Aug 2025 15:10:47 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:01e73baa3ddf3cc18244596980d9dbcd0715dd0f702b80e3442ad77f92b26036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c061cd234b8d24d411d7c378a6431d7b93c84e003406baf7937afd63b9eb74`

```dockerfile
```

-	Layers:
	-	`sha256:38077c4ca8e780d7f9c82c3324c4faef42cfd6c9bfa6bb634844fafe940de982`  
		Last Modified: Wed, 13 Aug 2025 16:33:34 GMT  
		Size: 3.6 MB (3646275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f6c362c5aa68c17e5335c7507046ee6ac7c287bfa8c411dd4e163c833835dd`  
		Last Modified: Wed, 13 Aug 2025 16:33:35 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:c0e8e7b68e1ccba97c98cf2a2e663fd4c9640f87812f4766ca38ffe5738bc249
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
$ docker pull couchdb@sha256:b95bcd53008659d8016dd1bdc95b2952074d86d1d598ed4c61bca8f09724698a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139837150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472995ee8c03c44092cb9a96bad4498e55b5661bf4e108c3bbe89dec9c459134`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02874ef0d17870ffbcb996b7655706cd08883c9761fb16d8d8cb58170190395`  
		Last Modified: Mon, 08 Sep 2025 21:42:40 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abe607827c22fc61dfc9356f346f51fbadf91fe8983d1fe8d1904da0137c999`  
		Last Modified: Mon, 08 Sep 2025 22:33:38 GMT  
		Size: 7.9 MB (7881670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b693851f2e5c0e0cece860bf6060eb71b25e7dd60707ad26ee97e0fd434a6cd`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 401.7 KB (401718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c796a1084c5b9434ed05a243cae9091c6e39d3747a8d62a3528d8e795a0cac3`  
		Last Modified: Mon, 08 Sep 2025 21:42:48 GMT  
		Size: 76.4 KB (76449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2475bda188e32a8bda910ee3b9b98f72aededd6efc8f87b9bc12166917c55f`  
		Last Modified: Mon, 08 Sep 2025 21:42:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47de6950448afb52a0f6e68fe11d621335a0a609b541a68fdf705e7b35717eb`  
		Last Modified: Mon, 08 Sep 2025 22:33:53 GMT  
		Size: 103.2 MB (103243543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04055f063a12e0f2372637d95e6d1b12cea300742189537c833937a0fb76df41`  
		Last Modified: Mon, 08 Sep 2025 21:42:55 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1304422b4ad0a55342291b98914627a02ba192217b8424ba0a095c7e8e3a0c`  
		Last Modified: Mon, 08 Sep 2025 21:42:58 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df01ab1a94c9671c7c37ac8ad2dd9fb74ae08bba12866a771cb2223364f476f0`  
		Last Modified: Mon, 08 Sep 2025 21:43:02 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94da7c605dd357599c4e25cd8f424e4f5ff9bd22d95d14d7a14b344e62625d6`  
		Last Modified: Mon, 08 Sep 2025 22:22:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:383c24ac0aef3b31908f74bbc93cd27a175d083fd5e65ae7ff0ec3d163835569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadec22010348840b46bb003d3a8439c05bf35260008d82f858e63e429d57653`

```dockerfile
```

-	Layers:
	-	`sha256:e31bd3808ef7e9d9fd7a5eec2805a258870c216590bad03bb615a478696dc3b8`  
		Last Modified: Mon, 08 Sep 2025 22:33:23 GMT  
		Size: 4.1 MB (4141252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c126581567a0a912223f1eb5798965b323b9a6406927dfb83ec10d688db0b8b`  
		Last Modified: Mon, 08 Sep 2025 22:33:25 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8c088795e61db62546d957e586d21ee2599d95f33b647bedc7bbcfee70e364ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139156265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98c1cdbc1d67f44bc2446dc03661bc5f6c5fb55e957df155236dcd0e8d056b5`
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dfd0f0a11cfb4475496bf3c0a039952bb67ed261d7c02b753bc546362e7656`  
		Last Modified: Mon, 08 Sep 2025 22:08:09 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3407cf867bd8272881c8e9290b2765c27085903ce5cf2f77728ef0f6afcace`  
		Last Modified: Mon, 08 Sep 2025 22:34:10 GMT  
		Size: 7.7 MB (7692057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fd3164a19a9a5d8f964c095daed3f5aa04f2e6e82a3f3ba0c96d4e671a9b74`  
		Last Modified: Mon, 08 Sep 2025 22:08:15 GMT  
		Size: 370.5 KB (370473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92227dd86433e30e6797478ece5415068675fc85bfc707019f4ddfb9af86c116`  
		Last Modified: Mon, 08 Sep 2025 22:08:18 GMT  
		Size: 76.5 KB (76482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee6cccb20b53b5f199d05a74eb7f58afe60126ad07681ff8feb9274014b2901`  
		Last Modified: Mon, 08 Sep 2025 22:08:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc72cb942d4a8545d3f8a787dd64253b47ac5925a8da45377ab2e99a73fb436`  
		Last Modified: Mon, 08 Sep 2025 22:34:14 GMT  
		Size: 102.9 MB (102909727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00bd8b46de89a47d2f75f054a6e31bf1ca52df8af20d91a26bed085a32f01e6`  
		Last Modified: Mon, 08 Sep 2025 22:08:25 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce9e551c2ff2de57f6fb371cd24208a2623ded29d86477af969096cdfaa7d68`  
		Last Modified: Mon, 08 Sep 2025 22:08:29 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca51f108619cfc4aca73989c988cfa32b51b0e621bc1dcdcfd84f875c526a68d`  
		Last Modified: Mon, 08 Sep 2025 22:08:33 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dd906b025549a4590dbe3b5a06fe67cedbd724d789230614d230e0bf1fb523`  
		Last Modified: Mon, 08 Sep 2025 22:08:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:530176e511b143aae889927ddffed0806dba306d8cc0f4dbd81c42eb4e4bd171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60de6d938c13c3b5b0ef8e8988bfd2b08bd66c834059e37a6dd1d96b285fb77`

```dockerfile
```

-	Layers:
	-	`sha256:37c32034c53bb2875fb6d3b8468a88f14d4776e7dfa47820b11640b4d5dad536`  
		Last Modified: Mon, 08 Sep 2025 22:34:01 GMT  
		Size: 4.1 MB (4141545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeea811cb50722acc3864b0b40add00437f1efce99b5a763eb663f3c0f11f7b5`  
		Last Modified: Mon, 08 Sep 2025 22:34:02 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:e4a4fc9e58539d2868bd15e046780cd8d8b7a71a74c1eb9f555e22fdf9c0c86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136521588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4fca67cecb025b5c09cab9c9549cb681d94892aaf58073a27711545f702b5e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b7acab8e5e7b12089d79275ac325f69e00c57ef109efebab6c70c9cd73a40d`  
		Last Modified: Wed, 13 Aug 2025 15:09:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3abfab6aae8ef4c71d8ee0179a883e31407cdba29d7ec2aedcd6cf479dd3bf`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164187f5523648207c88c10beecff4fa873224418908ed2042111b9008220445`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 355.6 KB (355650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1ea234d9128aa5cf95bed7f6b642ed39541c3ce0421026891a6ae6c3a62cf6`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 76.3 KB (76347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d507f15e04c67e6c028ebaf9b70be03905c6b099f3280dc1ee5b6c61e54fb9`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32a62c011f37d07095a847adb6849fc8b49b594312b80901dd3fa8730a8f14`  
		Last Modified: Wed, 13 Aug 2025 16:38:43 GMT  
		Size: 101.8 MB (101798492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c7a0c08391ce264a34acc839e0c22ef3ae30cd5170382d429de2fd535dd89`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8e63f7118f360ea233b6a4b5bfe85601905a9f58ccd1f8e5bd49122797016e`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c223e87672740895458e8f91f45b4a146badb15e846fc58f8860c7318a8ff3ab`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317e7af7e41277224e9cbb8f9c30c37a3271c0df880f6cf92e4bb22db5ecefe2`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:37f51edaf047cdf5f5111855683e13ea3c6672c8a15c2251ae5e354aae7a84a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4166926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36fa1cbb03efdd840bd2a162de1c1575a3bbbdb97b9d101b488ed2ce25e1f89`

```dockerfile
```

-	Layers:
	-	`sha256:66a48a697a343af104ea7f47a48904fb5b1d220938d9142743643f1b94344055`  
		Last Modified: Wed, 13 Aug 2025 16:33:26 GMT  
		Size: 4.1 MB (4135145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f50372cd52cb3fa8e4baf039bb58aa2c00bbb482d234fe623bfcf97bd2ac1f1`  
		Last Modified: Wed, 13 Aug 2025 16:33:27 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json
