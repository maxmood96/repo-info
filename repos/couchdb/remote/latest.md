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
