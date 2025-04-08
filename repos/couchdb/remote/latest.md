## `couchdb:latest`

```console
$ docker pull couchdb@sha256:61df6b12ad36146a1ac138e5d9ad31e473a3e622aeccab6664e174e100ec1276
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
$ docker pull couchdb@sha256:2c8cbf9949b4ef6478d591f66530f4ed9954208b0bebf3c8838e0ae3bbfbe56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138995478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6589c872ddf8a0b2d92d7c3e1d53e2eb5731536979e25a985ad163ead766a178`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc794586b3394ed75963cb9ca665c85b9d49eaacde6b4ee620b96f174efc58d`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1564a7be825fe9aeec808391b3160003fae79d5cee48e7b2801f32efe5212ab`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 7.9 MB (7874861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242f120d6bc802a93ad61c1f9710ec01aec6c4dc2d316858413f7bd38b9e8a23`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 392.1 KB (392137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaf08e6d63ef62eae2f65df5668812dc0ce495702cd12ec712c31becaaeb017`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 76.3 KB (76257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846984607b506dc27d2410ae6fb87f73e00f53f203b8930b6555f03ad7445e0f`  
		Last Modified: Tue, 08 Apr 2025 01:25:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081b56385efda4910492641fd010a7869a121d5b9a3da5aae883f12864c6e8ad`  
		Last Modified: Tue, 08 Apr 2025 01:25:08 GMT  
		Size: 102.4 MB (102419533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1fe74a44d4d12cb0e7f31a0010839cb08e874f6f3b7d9694e2e9e557c976ce`  
		Last Modified: Tue, 08 Apr 2025 01:25:07 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c20bb3a5f7956ccc49faa3839e974a9a4c95a85b74e21d6a182d146a046f872`  
		Last Modified: Tue, 08 Apr 2025 01:25:07 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95cd25517214e1a647fe97587456007d3de9d69d9ffe5b6f0fb7743e6c64ce0`  
		Last Modified: Tue, 08 Apr 2025 01:25:07 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1495fea30895c86252acb12c467fbd5e4b79ce013257c8c1b49c59e9d1b213e`  
		Last Modified: Tue, 08 Apr 2025 01:25:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:fe33a56ba8361594a1d4f2baf08d70a535f175cc4fd6d94e0389bd4a8f57fdbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cab12f1b3d52a4585bef3f810cf99813105d0213c1e89ab59d6afcea3ab19db`

```dockerfile
```

-	Layers:
	-	`sha256:67274538e60bb698f357986eb06d0db6e23d8235ad5ed4c49e16db936afa9c27`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 4.0 MB (3962194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f666d6f39efa3777bfd3ce2f185c841efcae85a206f8f13a82d1fceca847f6c`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e4b1ee37e2700f0090cd6d2b1fb0374b77e8cf245362fc17751b793a6c9f5d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138301220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefd1d8d3a1f76ce840fb34b3d2c65b613200ecc3380911fd453d6a3159f8c4c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e65c61d4347dffbff17974d594655364366c20d96108c688ab5d483bc664d37`  
		Last Modified: Tue, 08 Apr 2025 06:07:35 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c90e53df67f2a69dff9d59f4f6a7173fb63dd440e85a327325ebcf55d93af6`  
		Last Modified: Tue, 08 Apr 2025 06:07:36 GMT  
		Size: 7.7 MB (7654484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fce5a4746997d5bb76376354e94fd8a73cbfe19682598de03eddc7c382e780d`  
		Last Modified: Tue, 08 Apr 2025 06:07:36 GMT  
		Size: 348.9 KB (348940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389a1b1e3b4ad06fd97b1fb0765c90e34a491f814684d7ec1c68ef88c536f73b`  
		Last Modified: Tue, 08 Apr 2025 06:07:35 GMT  
		Size: 76.3 KB (76292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290a8c524ca500007122e96e8afb1bc63cfc1a834fd9fe2015aa68723bc020a5`  
		Last Modified: Tue, 08 Apr 2025 06:07:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22868bcabafb0b0443100f0d28d47177d3b068c7934563044b9d1606f76013d9`  
		Last Modified: Tue, 08 Apr 2025 06:07:39 GMT  
		Size: 102.1 MB (102149745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc82c1d9fb51338f9f7e421cdb869bd455f1dc8a4bb2c2e1c0df99f28b82ea8b`  
		Last Modified: Tue, 08 Apr 2025 06:07:37 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6335d62983b244139fac0233de1c31950d82dd3d7f16c96e9a4ed556c9edbd`  
		Last Modified: Tue, 08 Apr 2025 06:07:37 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66c7da0402e65d7425e07be963f75abeec0814b3f5a75886c20d283b72662f8`  
		Last Modified: Tue, 08 Apr 2025 06:07:37 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f16b14704bd96faf9ba04250958590f42f9162cd3401474a9403a22849317e`  
		Last Modified: Tue, 08 Apr 2025 06:07:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:998344ebbca0a60dedea61e8ee872bc414f28b378e57698dbb9d5fca15f81988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d8d7b6fc74d53d8c077b3395cba1acd685fdb7bb41661eca8a48bc78f7348b`

```dockerfile
```

-	Layers:
	-	`sha256:059ea87609356d101c590367766d1cea0b6a06f66fac7739b8a41c736e76fc89`  
		Last Modified: Tue, 08 Apr 2025 06:07:36 GMT  
		Size: 4.0 MB (3962487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4827eb67f556ed5be04bcf3f943487def53e1c904f8d4d80bbef27d0d11956a`  
		Last Modified: Tue, 08 Apr 2025 06:07:35 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:1081cc65f0ce10a987efba9aadaa9b5de2ce60095947983c2359770da4f37e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135765700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d6bf91f193e6828128368202c64186c93634ea274bdf2073aa171e0a4f421b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/couchdb/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a09bd1b0f19b0ec43da3fe696227892eb02db782f5634e4af81c0b11cb58d02`  
		Last Modified: Tue, 08 Apr 2025 03:46:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307c0ac712ea0dee12f8c8452366fbc4747c372ba1c4f5fbc1ee456f75638a06`  
		Last Modified: Tue, 08 Apr 2025 03:46:41 GMT  
		Size: 7.4 MB (7387880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1457362d4640c3c475e27fef878c6ae79988f1ed9e312a6bc0a918e16939c04`  
		Last Modified: Tue, 08 Apr 2025 03:46:41 GMT  
		Size: 355.6 KB (355624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72b413f6516b6abef498a4446842276472d499d916d263771b8cddc3bc053a1`  
		Last Modified: Tue, 08 Apr 2025 03:46:41 GMT  
		Size: 76.3 KB (76329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d482c7b396a850ef08177f60bda35fb19d5d757390344edd8ef6ad0609bbf00`  
		Last Modified: Tue, 08 Apr 2025 03:46:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1900c8794009fc5d0bec5ab5e28e508036ce894fe8b35534e94615b50d0dd6a8`  
		Last Modified: Tue, 08 Apr 2025 03:46:44 GMT  
		Size: 101.1 MB (101055829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5cb5249c32fd301a8cfce8c850e6e8c27d0ddd867bb7dadbf37dc35c6e51fd`  
		Last Modified: Tue, 08 Apr 2025 03:46:42 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51836a4a57295c12b284bafa1665982bad4e57aa0c0fb21ff5cf81a8b04a3c19`  
		Last Modified: Tue, 08 Apr 2025 03:46:42 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c16abc7ebfa5dad3f69632e9674286e5f76eef43e96c6eb8a9412fb3ef0d878`  
		Last Modified: Tue, 08 Apr 2025 03:46:43 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f21188e99a4ce0f20dbeadab73ec787f0a307fe6c6a6b13d208b84dce46dd0c`  
		Last Modified: Tue, 08 Apr 2025 03:46:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:bd80bc7d29b9dbc358fc06f67ad5006aeb8fd378d75ca57cb5c00af7c56fdd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec791241b88c04f77549a6a383f5bb295a13a5bb82089d16971b21bead56c46`

```dockerfile
```

-	Layers:
	-	`sha256:f39ec4762f851782a5d49ecdb59d20e9135ba8a9b9cd5c6c3c46340d3c17de7d`  
		Last Modified: Tue, 08 Apr 2025 03:46:41 GMT  
		Size: 4.0 MB (3961282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab0b856d62d3726186e5161e125a08a3b66beaa32a796b8fa573a625867f10f8`  
		Last Modified: Tue, 08 Apr 2025 03:46:41 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json
