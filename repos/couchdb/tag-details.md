<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3-nouveau`](#couchdb3-nouveau)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.3`](#couchdb333)
-	[`couchdb:3.4`](#couchdb34)
-	[`couchdb:3.4-nouveau`](#couchdb34-nouveau)
-	[`couchdb:3.4.3`](#couchdb343)
-	[`couchdb:3.4.3-nouveau`](#couchdb343-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:07d39b300e4e9ab9a3212efeb25d855372a914432eb1b1f566255de8943afba9
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
$ docker pull couchdb@sha256:29bda1ef06e431703b2b2ae415afbd8e39cc0bfd5e618aec2ef4afd9b6e8c708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138996025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577f5a2bf8281f310410466f9ff2dbcabfe1473b4e50a8384be08b36ecf99607`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8bb06f1e12481f1734930caaf5aec605aaa24e1a4a714390080ff8d49a9bae`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c643e44c289be880b7e1077b20be39cc8aa46c96dc275d3c274d9f4285b16e89`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 7.9 MB (7874898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139f130bffc490d838a88a0d05accd783a68e9f617fd52025ac774f55bfe8b96`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 392.2 KB (392157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482d9e178fbe5fbe5cfad58aa00c10b65769efe8fb24ae45ec9a43b2389fb87b`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 76.3 KB (76322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662901ec9a4cb6ba009d3607b9ad113b7bdd517130e2eec9112df2d01a05d6cb`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e060d223a8335af42564a119d05c7671db6bf1f629900166eac7b8c0e939a`  
		Last Modified: Mon, 28 Apr 2025 21:56:05 GMT  
		Size: 102.4 MB (102419585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a1370ccd45c896adc8fd7170cfbeb3eeac84209a0219dd34aec6210e1ab02`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1e127bb37e749c471a816e789f4ded13248cb110d7e3f9e4e17c8f7191e9d6`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87be8d54aedb6022da943334261c18e1eed1d602beb1ea3baf8af2a328b975`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133652bc69003427ae7004295dfcdea96aa5a003479ceaa3742c9e0e88528555`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:42c546356d24d3788c955b5d00eb4bcd393a46bc59e6fd076597281b2fe6b7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e2799689e298289b95db4b12008b49d684dc9a4297f34dd80dbfa169f6da0a`

```dockerfile
```

-	Layers:
	-	`sha256:a3f7e3b29115dda76e014b52b775a8dc0168d756776e2e5f0c6569ab4e764c88`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 4.0 MB (3962194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f550c2045c0da081acd88fb3e06f2f1cfe56c8b3010ee2d89946189a639dff5`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

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

### `couchdb:3` - unknown; unknown

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

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:7819b07037fe98ec994ca26a121fbb8c9a601772df54fa0f3af9f7ba85e50a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135766171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220713081441f1810d0218f5900376c97d27ed09c05e86c7476f16287ab5794`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c8a4385111079823034d1e8ed702e9672cd681f79562137fa525d16803eea`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c0f7f5b2751909f18f45844094309abfc54100ace7c37207440666c3dd916`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 7.4 MB (7387937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b6aeef9cd48451c7352e0d027a4ab68782567fd1af8b1aeed4283756407f74`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 355.6 KB (355644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a016c259437b9920b9c085f993abedb656356821d7571071cb17db40433ce23`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf854b3c69326f429e568061da038a651efb11e32516f8571b1eb6c2fa4f676`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63c8fe755b51ffd8fbe51e653149697f4db50ec5f2e547f3cdacddcf23a8cc`  
		Last Modified: Tue, 29 Apr 2025 00:03:42 GMT  
		Size: 101.1 MB (101055957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702504975d7b1931a864c2373bbe22a5a0c200b6689e356d0e589bee6a061932`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c449b40f1681890fb4190af1efe37d7714370d105e051af05596c701a932f57`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094a79dad673e9d7ae35052d26551314238c734e732e0fb16915e7266b6547ad`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1480727e9ec140937813aea1076b6378bf266665e18b0e20314a588367868a3b`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:88af6693555cb508b2d025acdc1cf32ed693329c7425a63e3ca33fcae9d6527d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cd21e53513802102079ed3d78030c64a5a73292fb437f3f01cd3c37abebb08`

```dockerfile
```

-	Layers:
	-	`sha256:899e8cbc1e36d790e687a9f1f9b1b0d69e11609f8e383484c7a552377bdc224b`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 4.0 MB (3961282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5195173997f32afdbc21e62b738eca6b36722bdcbe2527bfd1b80cc09e348e`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:6295bfac943b51087b6175eff9cff56de9f5d9eb94f3910d8c04a62acab74714
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
$ docker pull couchdb@sha256:77ffe59ff29af9d3c5219482f72482fbcb2a0ff2483c083e2d49fb115673bb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156349834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a27220813b744db3146ca8ced46f5cabde9a8fb7793a6c920793d220354a0f6`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a837b37dbc4aaf872f53093cddc1be6d7ef890b0711392143a9af72cef98aa9`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75c714820d9f6c5cbd4bf86389324df57d7541f49cf758a529ba5491022d8f`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 7.9 MB (7874927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe12777043dbe4709756fe502296dc6f6c3bbd613e3ef916bf1734214b192ba7`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 77.3 MB (77297600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78ba57999ae720b3c4071011a08e9999098f55ed42ff9b6ed3f3803132698e6`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 415.0 KB (414976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29364f5cdb32bc05cdd929c02986311ed94c76e959a4e263ba9cf30cd49229ce`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 99.3 KB (99309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bc17ee849dc1a4faaa61126db10e65016ed2a4c2710bd1d2ad98c07f3660bf`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9cc3233d493f6ccb82dbb845f9bf89aedb7a809588f957dff97a8a417b20bd`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 42.4 MB (42433507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fa03def47bdb76fe273a3779236c9b64f6cbba548c826afab19c88bef4e4d`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a6081534b52d88c51815ba521ecff693dea686881b9966a95ee75abfab2e5fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ce8df7d14f7982fb816dce683b26a15fde337ce687af08ea53c0ade53063f9`

```dockerfile
```

-	Layers:
	-	`sha256:a76c0ac78c05527f8220cc9ae241667389856abc3b537b0574c27f99d4400106`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 3.5 MB (3468472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a08d555edab0c60d4bcb148bd4978664d1b20f9aae43f6e9a2097f7d4c7bdf4`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ef86d350be3be5f381e1c1f8c88aa5636d75438d6ed3fbe46de10272dbe71a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155151031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1c6c7c10080658c8b4eadc27e8ce4cd8b1e48f8f847fc4944f24842acf2ab9`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd8f34bf1ac88838e26e0a2aaa5277259abcf731e3be2982f5f7b187a498b7d`  
		Last Modified: Tue, 08 Apr 2025 06:08:34 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfeb2f1090890b2eccec0deb81ace448720d51cf9f6223e04171d01133d6880`  
		Last Modified: Tue, 08 Apr 2025 06:08:35 GMT  
		Size: 7.7 MB (7654526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e8560a11efafc2608b641351699397902ac284b2de13fcc59ad42e88c17ccb`  
		Last Modified: Tue, 08 Apr 2025 06:08:37 GMT  
		Size: 76.6 MB (76624215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05f28575931d496b3ce2fcfaefba1cb4de7c78935d4e869ff9ec4ba910c4ca9`  
		Last Modified: Tue, 08 Apr 2025 06:08:35 GMT  
		Size: 371.8 KB (371752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5e87b04fa9145d9d256ed83fdcab7c6ea18fe09ceffd7f2fbfb4f93a1e3565`  
		Last Modified: Tue, 08 Apr 2025 06:08:36 GMT  
		Size: 99.3 KB (99269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8837079b0c7afc124818e7f34425210f8d93d1079e1a10cb003a7303772886e`  
		Last Modified: Tue, 08 Apr 2025 06:08:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1be7702499648f7eeee1a7c249646f3cfccb0ed6958777e78aa631f83cfc35`  
		Last Modified: Tue, 08 Apr 2025 06:08:37 GMT  
		Size: 42.3 MB (42333067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bbf4a32731c1ff00883e64ac3bfbdd144fb4661295d4fa4cde05f3b8c8c38d`  
		Last Modified: Tue, 08 Apr 2025 06:08:37 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:0a4647b4cf67f83b07b8cedf4dbc451fd13dc6e1131766239a83afa2b38a008f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4849696a300233a5245da38545c5a9c51709e0917fb70396be40cac6b8beece9`

```dockerfile
```

-	Layers:
	-	`sha256:c72e829feccf8ae458a5f9b1e8f1c3939bb3193f2b2b76919fcddd0c9fc1b0d5`  
		Last Modified: Tue, 08 Apr 2025 06:08:35 GMT  
		Size: 3.5 MB (3467148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7df692b8d1cef439ab82454d228b29dd122424de355867e8c1fb75f04acd56cf`  
		Last Modified: Tue, 08 Apr 2025 06:08:34 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:567f3e53824961c5f506118d23c53e6c44333ede5da72ca9fc0453ee8df3559f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149977892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d2af33615aa36bcba2719f0280f43028b632981cf48362c439c8774e5a7e08`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeb9febea926497c6b73a956a66c5ec7705a80ed96a88acd22e023a12bb07b9`  
		Last Modified: Tue, 29 Apr 2025 00:04:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb3720e0f56a097c25a4a4a982b82bafb5b5cd40ac87ffefca40556227f213f`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 7.4 MB (7387952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce679ce7dd142ab1209f6b1e198804851164e290d7c9412f489110386d84a3c4`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 73.1 MB (73065225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ea5e69fb0ac2e8ec68ad79d4ed32a98475e57dec15e01433a7aac1c8d2bcff`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 378.1 KB (378103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8084ad1ebf84dff15753e78e53bdc8cfdccdcb39266f1bf8e231f251d78a64e3`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 99.4 KB (99449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a49819b32ddd9c0fe27e1ed0f760870d4d9170232838540cc48f818ef2606e`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cd8bce374995c6a118e0965c0b2ebf3fa93ae834354a829cc1b3cd0f830219`  
		Last Modified: Tue, 29 Apr 2025 00:04:49 GMT  
		Size: 42.2 MB (42160416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55bbc492280b5c45b056b641e8fec35f5fb54bc50068de783a4c110b4beb376`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:77c04fe246e4b659963c87d866f2678b43426ef3984aac6cc092e602b0dc0ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f22a5e7194519b1d9eff220c23222179736285e22078c6328ae14eda1ca0b0`

```dockerfile
```

-	Layers:
	-	`sha256:e581491861b03880116342ed4b02be1373f61f3ac37d5e781506fac9e30a02d5`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 3.5 MB (3461893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e144eeff7b03258ac15dcb32b9ea1e2ff7892643f844b7df4a7b15118c6c87e3`  
		Last Modified: Tue, 29 Apr 2025 00:04:46 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:73ac8fc24e2af4a6783c8985fe20bfc29f8115d03e078e78aa7b3e9bcaa59567
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
$ docker pull couchdb@sha256:e99f02d9e4742707e405b21443cd0a356c00d04a1bf8cf77577eebd1dc3868b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96727790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca5e1fbe30fdbccb0459c3f10a79d739e0f31c530be14b0557c819d19ab393f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407f5eb39ed8742e057e33cd1b896b81f5b6929d23bce88cb5c17a81840cfcfa`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d7e18ff8a4005a7f5ea9ca6b86b9cf9ab15aad74f4bbddcd638b81960bc3e`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 7.9 MB (7874918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf731d868a24446da372fcb6f05404a7ce5545902bca70f90b2c6c4fe01adaa`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 392.1 KB (392142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55312866b224adebbae017ad55435170d1149844fe1671127cd88aede44274e3`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 76.3 KB (76292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a576df24c6c7e8b0a5e1aac2dfd8597604c94ddf4e52a7d33f34ab766e67cc9b`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce368c5697d630b4246a24b2b7ff45afd37f3cd045c4b44c02b52e25663ce4f6`  
		Last Modified: Mon, 28 Apr 2025 21:56:06 GMT  
		Size: 60.2 MB (60151368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452d939ad465209dfd377643a24569f7b5d7f4b3bea489ac55f68d9fa4b0ff5a`  
		Last Modified: Mon, 28 Apr 2025 21:56:04 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115bf3cdefa316d34f53af2c4589620247c1144983b22cb680d5bf94ce0e05f0`  
		Last Modified: Mon, 28 Apr 2025 21:56:04 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bed53beb22392f56a73cb344cb68487e3da83f60dec8adf055a709d28a5aea`  
		Last Modified: Mon, 28 Apr 2025 21:56:04 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4106aeb26392af5bd9eaa662f9464b7adea8a2fda8399cea3bef5301cb7efc`  
		Last Modified: Mon, 28 Apr 2025 21:56:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:b4e4c2d3260ab92828d8996365e50c56d88d0d43c1a1fb760ae7ea34b92d4e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3767400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5125fcae8f23f87e03de19bd622915ac4dea9351a5ec5bd8defd9ca1572f2aaa`

```dockerfile
```

-	Layers:
	-	`sha256:c8c489da1cc8ad4704d7635333a5193730c24f0b25b995f1bc2437419ff0c802`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 3.7 MB (3736208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f5b842c6900d66e2d973d0a39c6a8fe8d8833659c0e3ab471b23965e9049cbb`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a25dd98a80e3ab96c494e33ad0b7654f226a53380d46bd6e7d693110e4c54d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96085881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3946681c6eb3f7c6fda11d50706a8819f8c0dc5667511b5acb9c9e6a83eb1fe4`
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:3721d73aa9f42df06e8892b2140a77626bae0ee2922bbf56521ba36743fbfb80`  
		Last Modified: Tue, 08 Apr 2025 06:09:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f5705e096789b18090b713891b49fcf66a58a5f934d87c57294de04e40259e`  
		Last Modified: Tue, 08 Apr 2025 06:09:16 GMT  
		Size: 59.9 MB (59934413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaee8a992ebae1e5dff98918fbe092bbcc7fcc1b5b209c94747bb1aef7267f5`  
		Last Modified: Tue, 08 Apr 2025 06:09:14 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fcc951d0131b03b67beccb18d318b9bc4b74675e7a709b662969bcb7dcf922`  
		Last Modified: Tue, 08 Apr 2025 06:09:14 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ff7ae5df43a8d358b1548adabb6b54b179dcf65ea77c4dce2b2d5fbc998d4f`  
		Last Modified: Tue, 08 Apr 2025 06:09:15 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec517fe77d89decfd53c072cb6e44bf62f6d2c37824479e3c004baab8f1c048`  
		Last Modified: Tue, 08 Apr 2025 06:09:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a76a283a9af6aa134cbfc6cfd357778a59e21ce52896469b6ea6e551ff81ec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3767839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f2ea9b9494f0258afe073a3e0e494bc2455803037ae61e65edc9de18eb6a6e`

```dockerfile
```

-	Layers:
	-	`sha256:5093209c13ba8074efb9988ee99a4aa84070058fd33c30764e4d14bc1c5a2ded`  
		Last Modified: Tue, 08 Apr 2025 06:09:14 GMT  
		Size: 3.7 MB (3736477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f5b5c3ce5512fcbdbc32db025c75772ce8da351ad33528fe9aa893e1317968`  
		Last Modified: Tue, 08 Apr 2025 06:09:14 GMT  
		Size: 31.4 KB (31362 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f45396da7cc26743f8e72c872006515047df8d81359252a87e1207c16199e4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102861906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddbcfc4d7be5608ef2fd4acccf6eb20002393936967c187719f4dbdb37851d2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8731030796c12ce9b5d62a2a419d1f71171ca01a4f77173d3b2ba7e8bd33362`  
		Last Modified: Tue, 29 Apr 2025 00:40:26 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15208278f2164f047a2789391c076f61302a28318a44cb9584ed8042b115cb9e`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 8.9 MB (8890023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef32d7d78ee5ac90dfb01f5ffea9e564790ab1fce565caac1107a258b5c3a405`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 444.7 KB (444703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2784d482238c88cb632a8dfc389afdea294c256834519a7748ac07cc2d06f605`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 76.4 KB (76362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd88b39de501bc5bc7b95537db178bb105328de4757f651a3c52b5c52b6defe4`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c053eb35ca156613e1c1e7d5d17c124768083ef0df7752005e19436882fc5262`  
		Last Modified: Tue, 29 Apr 2025 00:40:30 GMT  
		Size: 61.4 MB (61376946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1199e9c940aa8c4136c5f981a8123a0a5e6e56c10c81dd16b6bdd20afff59cb6`  
		Last Modified: Tue, 29 Apr 2025 00:40:28 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3bc3511c87e7b79ae803b28d433431d260ef1ef26cc90f52630cab82892fff`  
		Last Modified: Tue, 29 Apr 2025 00:40:28 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a723ce6d2cecaf0bbe4ff843d6f14a1de1cc278ac4c0e2b7e6ffa8fc9a2c8f46`  
		Last Modified: Tue, 29 Apr 2025 00:40:29 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9490a38aa65df97b8809cb8cf036bc7b6fc393257dcd58c90f3c10a41e4be957`  
		Last Modified: Tue, 29 Apr 2025 00:40:29 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e5af63559e8bbffc038fb0bee9cb097174710b494567524359313fe63d791cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3771948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569f456fdee9d1e1f3c0d862d04a31b91f6a53999e36c450710b0f072d501f8f`

```dockerfile
```

-	Layers:
	-	`sha256:a40ed823df7c76efce63ebc8dd981e6dc3926470fb2e0b146673b6a1aa9d7ea4`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 3.7 MB (3740712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4853a45ed87121c7bafba000562fd2c2f854b5ce3ed4024d99804dad2e327a7b`  
		Last Modified: Tue, 29 Apr 2025 00:40:26 GMT  
		Size: 31.2 KB (31236 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:8da535f283bf6fe9b3c2baa9252a4a13e4794f6f8a779a1180e6f68084cabffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93450974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4819b1906862b3cdf1650526984d06ad927ec281a53c901e0744ce6905c68ce`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c8a4385111079823034d1e8ed702e9672cd681f79562137fa525d16803eea`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c0f7f5b2751909f18f45844094309abfc54100ace7c37207440666c3dd916`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 7.4 MB (7387937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b6aeef9cd48451c7352e0d027a4ab68782567fd1af8b1aeed4283756407f74`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 355.6 KB (355644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a016c259437b9920b9c085f993abedb656356821d7571071cb17db40433ce23`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626eda8b887690797597b86d47fbf9bd887a653d72a8694aae4fad8825b8f4e9`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309ae0ff12be0ccf11ecb17b85e5f7e2d2044a66e84113a33c7d970dc59f9c95`  
		Last Modified: Tue, 29 Apr 2025 00:05:33 GMT  
		Size: 58.7 MB (58740760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d86c95fee04803ae944fbf26c47f3da6214b06c42a1742ea41f22667df8a426`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec1814a99eaa0cf1a6f08a05bfacc74dc65180f4b46838a62e041b4f2db600b`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891160d2d5c6cda656e3a61e2aa974fd98a2ed9a696a1204bda32857619c2e69`  
		Last Modified: Tue, 29 Apr 2025 00:05:33 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97eb0bb15e1241d2f0c8e094baa13bd0b8b6e36eb787478469a9f1f9e7726a4`  
		Last Modified: Tue, 29 Apr 2025 00:05:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:3509830c86e729659945ff2e7eeb172dbd6cc475aaafd1b127300045f690f969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16330a21bc29dfe1d0dfd270b5407b313f177cc1c5fb1b5b644fda5a18cd2719`

```dockerfile
```

-	Layers:
	-	`sha256:80394274165a2b65e8450f5373b03ab197b73b71d3ab927ee89f379f3ff30bfa`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 3.7 MB (3735296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1103b97f0c1b9b9be544d5817b02013cb2a74420389995f13dca8ad7c70f9a2f`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 31.2 KB (31190 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:73ac8fc24e2af4a6783c8985fe20bfc29f8115d03e078e78aa7b3e9bcaa59567
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
$ docker pull couchdb@sha256:e99f02d9e4742707e405b21443cd0a356c00d04a1bf8cf77577eebd1dc3868b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96727790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca5e1fbe30fdbccb0459c3f10a79d739e0f31c530be14b0557c819d19ab393f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407f5eb39ed8742e057e33cd1b896b81f5b6929d23bce88cb5c17a81840cfcfa`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d7e18ff8a4005a7f5ea9ca6b86b9cf9ab15aad74f4bbddcd638b81960bc3e`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 7.9 MB (7874918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf731d868a24446da372fcb6f05404a7ce5545902bca70f90b2c6c4fe01adaa`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 392.1 KB (392142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55312866b224adebbae017ad55435170d1149844fe1671127cd88aede44274e3`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 76.3 KB (76292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a576df24c6c7e8b0a5e1aac2dfd8597604c94ddf4e52a7d33f34ab766e67cc9b`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce368c5697d630b4246a24b2b7ff45afd37f3cd045c4b44c02b52e25663ce4f6`  
		Last Modified: Mon, 28 Apr 2025 21:56:06 GMT  
		Size: 60.2 MB (60151368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452d939ad465209dfd377643a24569f7b5d7f4b3bea489ac55f68d9fa4b0ff5a`  
		Last Modified: Mon, 28 Apr 2025 21:56:04 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115bf3cdefa316d34f53af2c4589620247c1144983b22cb680d5bf94ce0e05f0`  
		Last Modified: Mon, 28 Apr 2025 21:56:04 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bed53beb22392f56a73cb344cb68487e3da83f60dec8adf055a709d28a5aea`  
		Last Modified: Mon, 28 Apr 2025 21:56:04 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4106aeb26392af5bd9eaa662f9464b7adea8a2fda8399cea3bef5301cb7efc`  
		Last Modified: Mon, 28 Apr 2025 21:56:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:b4e4c2d3260ab92828d8996365e50c56d88d0d43c1a1fb760ae7ea34b92d4e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3767400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5125fcae8f23f87e03de19bd622915ac4dea9351a5ec5bd8defd9ca1572f2aaa`

```dockerfile
```

-	Layers:
	-	`sha256:c8c489da1cc8ad4704d7635333a5193730c24f0b25b995f1bc2437419ff0c802`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 3.7 MB (3736208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f5b842c6900d66e2d973d0a39c6a8fe8d8833659c0e3ab471b23965e9049cbb`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a25dd98a80e3ab96c494e33ad0b7654f226a53380d46bd6e7d693110e4c54d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96085881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3946681c6eb3f7c6fda11d50706a8819f8c0dc5667511b5acb9c9e6a83eb1fe4`
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:3721d73aa9f42df06e8892b2140a77626bae0ee2922bbf56521ba36743fbfb80`  
		Last Modified: Tue, 08 Apr 2025 06:09:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f5705e096789b18090b713891b49fcf66a58a5f934d87c57294de04e40259e`  
		Last Modified: Tue, 08 Apr 2025 06:09:16 GMT  
		Size: 59.9 MB (59934413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaee8a992ebae1e5dff98918fbe092bbcc7fcc1b5b209c94747bb1aef7267f5`  
		Last Modified: Tue, 08 Apr 2025 06:09:14 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fcc951d0131b03b67beccb18d318b9bc4b74675e7a709b662969bcb7dcf922`  
		Last Modified: Tue, 08 Apr 2025 06:09:14 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ff7ae5df43a8d358b1548adabb6b54b179dcf65ea77c4dce2b2d5fbc998d4f`  
		Last Modified: Tue, 08 Apr 2025 06:09:15 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec517fe77d89decfd53c072cb6e44bf62f6d2c37824479e3c004baab8f1c048`  
		Last Modified: Tue, 08 Apr 2025 06:09:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a76a283a9af6aa134cbfc6cfd357778a59e21ce52896469b6ea6e551ff81ec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3767839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f2ea9b9494f0258afe073a3e0e494bc2455803037ae61e65edc9de18eb6a6e`

```dockerfile
```

-	Layers:
	-	`sha256:5093209c13ba8074efb9988ee99a4aa84070058fd33c30764e4d14bc1c5a2ded`  
		Last Modified: Tue, 08 Apr 2025 06:09:14 GMT  
		Size: 3.7 MB (3736477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f5b5c3ce5512fcbdbc32db025c75772ce8da351ad33528fe9aa893e1317968`  
		Last Modified: Tue, 08 Apr 2025 06:09:14 GMT  
		Size: 31.4 KB (31362 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f45396da7cc26743f8e72c872006515047df8d81359252a87e1207c16199e4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102861906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddbcfc4d7be5608ef2fd4acccf6eb20002393936967c187719f4dbdb37851d2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8731030796c12ce9b5d62a2a419d1f71171ca01a4f77173d3b2ba7e8bd33362`  
		Last Modified: Tue, 29 Apr 2025 00:40:26 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15208278f2164f047a2789391c076f61302a28318a44cb9584ed8042b115cb9e`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 8.9 MB (8890023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef32d7d78ee5ac90dfb01f5ffea9e564790ab1fce565caac1107a258b5c3a405`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 444.7 KB (444703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2784d482238c88cb632a8dfc389afdea294c256834519a7748ac07cc2d06f605`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 76.4 KB (76362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd88b39de501bc5bc7b95537db178bb105328de4757f651a3c52b5c52b6defe4`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c053eb35ca156613e1c1e7d5d17c124768083ef0df7752005e19436882fc5262`  
		Last Modified: Tue, 29 Apr 2025 00:40:30 GMT  
		Size: 61.4 MB (61376946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1199e9c940aa8c4136c5f981a8123a0a5e6e56c10c81dd16b6bdd20afff59cb6`  
		Last Modified: Tue, 29 Apr 2025 00:40:28 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3bc3511c87e7b79ae803b28d433431d260ef1ef26cc90f52630cab82892fff`  
		Last Modified: Tue, 29 Apr 2025 00:40:28 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a723ce6d2cecaf0bbe4ff843d6f14a1de1cc278ac4c0e2b7e6ffa8fc9a2c8f46`  
		Last Modified: Tue, 29 Apr 2025 00:40:29 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9490a38aa65df97b8809cb8cf036bc7b6fc393257dcd58c90f3c10a41e4be957`  
		Last Modified: Tue, 29 Apr 2025 00:40:29 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e5af63559e8bbffc038fb0bee9cb097174710b494567524359313fe63d791cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3771948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569f456fdee9d1e1f3c0d862d04a31b91f6a53999e36c450710b0f072d501f8f`

```dockerfile
```

-	Layers:
	-	`sha256:a40ed823df7c76efce63ebc8dd981e6dc3926470fb2e0b146673b6a1aa9d7ea4`  
		Last Modified: Tue, 29 Apr 2025 00:40:27 GMT  
		Size: 3.7 MB (3740712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4853a45ed87121c7bafba000562fd2c2f854b5ce3ed4024d99804dad2e327a7b`  
		Last Modified: Tue, 29 Apr 2025 00:40:26 GMT  
		Size: 31.2 KB (31236 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:8da535f283bf6fe9b3c2baa9252a4a13e4794f6f8a779a1180e6f68084cabffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93450974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4819b1906862b3cdf1650526984d06ad927ec281a53c901e0744ce6905c68ce`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c8a4385111079823034d1e8ed702e9672cd681f79562137fa525d16803eea`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c0f7f5b2751909f18f45844094309abfc54100ace7c37207440666c3dd916`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 7.4 MB (7387937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b6aeef9cd48451c7352e0d027a4ab68782567fd1af8b1aeed4283756407f74`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 355.6 KB (355644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a016c259437b9920b9c085f993abedb656356821d7571071cb17db40433ce23`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626eda8b887690797597b86d47fbf9bd887a653d72a8694aae4fad8825b8f4e9`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309ae0ff12be0ccf11ecb17b85e5f7e2d2044a66e84113a33c7d970dc59f9c95`  
		Last Modified: Tue, 29 Apr 2025 00:05:33 GMT  
		Size: 58.7 MB (58740760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d86c95fee04803ae944fbf26c47f3da6214b06c42a1742ea41f22667df8a426`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec1814a99eaa0cf1a6f08a05bfacc74dc65180f4b46838a62e041b4f2db600b`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891160d2d5c6cda656e3a61e2aa974fd98a2ed9a696a1204bda32857619c2e69`  
		Last Modified: Tue, 29 Apr 2025 00:05:33 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97eb0bb15e1241d2f0c8e094baa13bd0b8b6e36eb787478469a9f1f9e7726a4`  
		Last Modified: Tue, 29 Apr 2025 00:05:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:3509830c86e729659945ff2e7eeb172dbd6cc475aaafd1b127300045f690f969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16330a21bc29dfe1d0dfd270b5407b313f177cc1c5fb1b5b644fda5a18cd2719`

```dockerfile
```

-	Layers:
	-	`sha256:80394274165a2b65e8450f5373b03ab197b73b71d3ab927ee89f379f3ff30bfa`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 3.7 MB (3735296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1103b97f0c1b9b9be544d5817b02013cb2a74420389995f13dca8ad7c70f9a2f`  
		Last Modified: Tue, 29 Apr 2025 00:05:32 GMT  
		Size: 31.2 KB (31190 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:07d39b300e4e9ab9a3212efeb25d855372a914432eb1b1f566255de8943afba9
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
$ docker pull couchdb@sha256:29bda1ef06e431703b2b2ae415afbd8e39cc0bfd5e618aec2ef4afd9b6e8c708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138996025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577f5a2bf8281f310410466f9ff2dbcabfe1473b4e50a8384be08b36ecf99607`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8bb06f1e12481f1734930caaf5aec605aaa24e1a4a714390080ff8d49a9bae`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c643e44c289be880b7e1077b20be39cc8aa46c96dc275d3c274d9f4285b16e89`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 7.9 MB (7874898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139f130bffc490d838a88a0d05accd783a68e9f617fd52025ac774f55bfe8b96`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 392.2 KB (392157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482d9e178fbe5fbe5cfad58aa00c10b65769efe8fb24ae45ec9a43b2389fb87b`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 76.3 KB (76322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662901ec9a4cb6ba009d3607b9ad113b7bdd517130e2eec9112df2d01a05d6cb`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e060d223a8335af42564a119d05c7671db6bf1f629900166eac7b8c0e939a`  
		Last Modified: Mon, 28 Apr 2025 21:56:05 GMT  
		Size: 102.4 MB (102419585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a1370ccd45c896adc8fd7170cfbeb3eeac84209a0219dd34aec6210e1ab02`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1e127bb37e749c471a816e789f4ded13248cb110d7e3f9e4e17c8f7191e9d6`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87be8d54aedb6022da943334261c18e1eed1d602beb1ea3baf8af2a328b975`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133652bc69003427ae7004295dfcdea96aa5a003479ceaa3742c9e0e88528555`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:42c546356d24d3788c955b5d00eb4bcd393a46bc59e6fd076597281b2fe6b7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e2799689e298289b95db4b12008b49d684dc9a4297f34dd80dbfa169f6da0a`

```dockerfile
```

-	Layers:
	-	`sha256:a3f7e3b29115dda76e014b52b775a8dc0168d756776e2e5f0c6569ab4e764c88`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 4.0 MB (3962194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f550c2045c0da081acd88fb3e06f2f1cfe56c8b3010ee2d89946189a639dff5`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

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

### `couchdb:3.4` - unknown; unknown

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

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:7819b07037fe98ec994ca26a121fbb8c9a601772df54fa0f3af9f7ba85e50a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135766171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220713081441f1810d0218f5900376c97d27ed09c05e86c7476f16287ab5794`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c8a4385111079823034d1e8ed702e9672cd681f79562137fa525d16803eea`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c0f7f5b2751909f18f45844094309abfc54100ace7c37207440666c3dd916`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 7.4 MB (7387937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b6aeef9cd48451c7352e0d027a4ab68782567fd1af8b1aeed4283756407f74`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 355.6 KB (355644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a016c259437b9920b9c085f993abedb656356821d7571071cb17db40433ce23`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf854b3c69326f429e568061da038a651efb11e32516f8571b1eb6c2fa4f676`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63c8fe755b51ffd8fbe51e653149697f4db50ec5f2e547f3cdacddcf23a8cc`  
		Last Modified: Tue, 29 Apr 2025 00:03:42 GMT  
		Size: 101.1 MB (101055957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702504975d7b1931a864c2373bbe22a5a0c200b6689e356d0e589bee6a061932`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c449b40f1681890fb4190af1efe37d7714370d105e051af05596c701a932f57`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094a79dad673e9d7ae35052d26551314238c734e732e0fb16915e7266b6547ad`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1480727e9ec140937813aea1076b6378bf266665e18b0e20314a588367868a3b`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:88af6693555cb508b2d025acdc1cf32ed693329c7425a63e3ca33fcae9d6527d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cd21e53513802102079ed3d78030c64a5a73292fb437f3f01cd3c37abebb08`

```dockerfile
```

-	Layers:
	-	`sha256:899e8cbc1e36d790e687a9f1f9b1b0d69e11609f8e383484c7a552377bdc224b`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 4.0 MB (3961282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5195173997f32afdbc21e62b738eca6b36722bdcbe2527bfd1b80cc09e348e`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:6295bfac943b51087b6175eff9cff56de9f5d9eb94f3910d8c04a62acab74714
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
$ docker pull couchdb@sha256:77ffe59ff29af9d3c5219482f72482fbcb2a0ff2483c083e2d49fb115673bb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156349834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a27220813b744db3146ca8ced46f5cabde9a8fb7793a6c920793d220354a0f6`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a837b37dbc4aaf872f53093cddc1be6d7ef890b0711392143a9af72cef98aa9`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75c714820d9f6c5cbd4bf86389324df57d7541f49cf758a529ba5491022d8f`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 7.9 MB (7874927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe12777043dbe4709756fe502296dc6f6c3bbd613e3ef916bf1734214b192ba7`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 77.3 MB (77297600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78ba57999ae720b3c4071011a08e9999098f55ed42ff9b6ed3f3803132698e6`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 415.0 KB (414976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29364f5cdb32bc05cdd929c02986311ed94c76e959a4e263ba9cf30cd49229ce`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 99.3 KB (99309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bc17ee849dc1a4faaa61126db10e65016ed2a4c2710bd1d2ad98c07f3660bf`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9cc3233d493f6ccb82dbb845f9bf89aedb7a809588f957dff97a8a417b20bd`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 42.4 MB (42433507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fa03def47bdb76fe273a3779236c9b64f6cbba548c826afab19c88bef4e4d`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a6081534b52d88c51815ba521ecff693dea686881b9966a95ee75abfab2e5fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ce8df7d14f7982fb816dce683b26a15fde337ce687af08ea53c0ade53063f9`

```dockerfile
```

-	Layers:
	-	`sha256:a76c0ac78c05527f8220cc9ae241667389856abc3b537b0574c27f99d4400106`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 3.5 MB (3468472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a08d555edab0c60d4bcb148bd4978664d1b20f9aae43f6e9a2097f7d4c7bdf4`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ef86d350be3be5f381e1c1f8c88aa5636d75438d6ed3fbe46de10272dbe71a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155151031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1c6c7c10080658c8b4eadc27e8ce4cd8b1e48f8f847fc4944f24842acf2ab9`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd8f34bf1ac88838e26e0a2aaa5277259abcf731e3be2982f5f7b187a498b7d`  
		Last Modified: Tue, 08 Apr 2025 06:08:34 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfeb2f1090890b2eccec0deb81ace448720d51cf9f6223e04171d01133d6880`  
		Last Modified: Tue, 08 Apr 2025 06:08:35 GMT  
		Size: 7.7 MB (7654526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e8560a11efafc2608b641351699397902ac284b2de13fcc59ad42e88c17ccb`  
		Last Modified: Tue, 08 Apr 2025 06:08:37 GMT  
		Size: 76.6 MB (76624215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05f28575931d496b3ce2fcfaefba1cb4de7c78935d4e869ff9ec4ba910c4ca9`  
		Last Modified: Tue, 08 Apr 2025 06:08:35 GMT  
		Size: 371.8 KB (371752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5e87b04fa9145d9d256ed83fdcab7c6ea18fe09ceffd7f2fbfb4f93a1e3565`  
		Last Modified: Tue, 08 Apr 2025 06:08:36 GMT  
		Size: 99.3 KB (99269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8837079b0c7afc124818e7f34425210f8d93d1079e1a10cb003a7303772886e`  
		Last Modified: Tue, 08 Apr 2025 06:08:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1be7702499648f7eeee1a7c249646f3cfccb0ed6958777e78aa631f83cfc35`  
		Last Modified: Tue, 08 Apr 2025 06:08:37 GMT  
		Size: 42.3 MB (42333067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bbf4a32731c1ff00883e64ac3bfbdd144fb4661295d4fa4cde05f3b8c8c38d`  
		Last Modified: Tue, 08 Apr 2025 06:08:37 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:0a4647b4cf67f83b07b8cedf4dbc451fd13dc6e1131766239a83afa2b38a008f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4849696a300233a5245da38545c5a9c51709e0917fb70396be40cac6b8beece9`

```dockerfile
```

-	Layers:
	-	`sha256:c72e829feccf8ae458a5f9b1e8f1c3939bb3193f2b2b76919fcddd0c9fc1b0d5`  
		Last Modified: Tue, 08 Apr 2025 06:08:35 GMT  
		Size: 3.5 MB (3467148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7df692b8d1cef439ab82454d228b29dd122424de355867e8c1fb75f04acd56cf`  
		Last Modified: Tue, 08 Apr 2025 06:08:34 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:567f3e53824961c5f506118d23c53e6c44333ede5da72ca9fc0453ee8df3559f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149977892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d2af33615aa36bcba2719f0280f43028b632981cf48362c439c8774e5a7e08`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeb9febea926497c6b73a956a66c5ec7705a80ed96a88acd22e023a12bb07b9`  
		Last Modified: Tue, 29 Apr 2025 00:04:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb3720e0f56a097c25a4a4a982b82bafb5b5cd40ac87ffefca40556227f213f`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 7.4 MB (7387952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce679ce7dd142ab1209f6b1e198804851164e290d7c9412f489110386d84a3c4`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 73.1 MB (73065225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ea5e69fb0ac2e8ec68ad79d4ed32a98475e57dec15e01433a7aac1c8d2bcff`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 378.1 KB (378103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8084ad1ebf84dff15753e78e53bdc8cfdccdcb39266f1bf8e231f251d78a64e3`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 99.4 KB (99449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a49819b32ddd9c0fe27e1ed0f760870d4d9170232838540cc48f818ef2606e`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cd8bce374995c6a118e0965c0b2ebf3fa93ae834354a829cc1b3cd0f830219`  
		Last Modified: Tue, 29 Apr 2025 00:04:49 GMT  
		Size: 42.2 MB (42160416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55bbc492280b5c45b056b641e8fec35f5fb54bc50068de783a4c110b4beb376`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:77c04fe246e4b659963c87d866f2678b43426ef3984aac6cc092e602b0dc0ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f22a5e7194519b1d9eff220c23222179736285e22078c6328ae14eda1ca0b0`

```dockerfile
```

-	Layers:
	-	`sha256:e581491861b03880116342ed4b02be1373f61f3ac37d5e781506fac9e30a02d5`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 3.5 MB (3461893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e144eeff7b03258ac15dcb32b9ea1e2ff7892643f844b7df4a7b15118c6c87e3`  
		Last Modified: Tue, 29 Apr 2025 00:04:46 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:07d39b300e4e9ab9a3212efeb25d855372a914432eb1b1f566255de8943afba9
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
$ docker pull couchdb@sha256:29bda1ef06e431703b2b2ae415afbd8e39cc0bfd5e618aec2ef4afd9b6e8c708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138996025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577f5a2bf8281f310410466f9ff2dbcabfe1473b4e50a8384be08b36ecf99607`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8bb06f1e12481f1734930caaf5aec605aaa24e1a4a714390080ff8d49a9bae`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c643e44c289be880b7e1077b20be39cc8aa46c96dc275d3c274d9f4285b16e89`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 7.9 MB (7874898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139f130bffc490d838a88a0d05accd783a68e9f617fd52025ac774f55bfe8b96`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 392.2 KB (392157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482d9e178fbe5fbe5cfad58aa00c10b65769efe8fb24ae45ec9a43b2389fb87b`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 76.3 KB (76322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662901ec9a4cb6ba009d3607b9ad113b7bdd517130e2eec9112df2d01a05d6cb`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e060d223a8335af42564a119d05c7671db6bf1f629900166eac7b8c0e939a`  
		Last Modified: Mon, 28 Apr 2025 21:56:05 GMT  
		Size: 102.4 MB (102419585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a1370ccd45c896adc8fd7170cfbeb3eeac84209a0219dd34aec6210e1ab02`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1e127bb37e749c471a816e789f4ded13248cb110d7e3f9e4e17c8f7191e9d6`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87be8d54aedb6022da943334261c18e1eed1d602beb1ea3baf8af2a328b975`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133652bc69003427ae7004295dfcdea96aa5a003479ceaa3742c9e0e88528555`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:42c546356d24d3788c955b5d00eb4bcd393a46bc59e6fd076597281b2fe6b7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e2799689e298289b95db4b12008b49d684dc9a4297f34dd80dbfa169f6da0a`

```dockerfile
```

-	Layers:
	-	`sha256:a3f7e3b29115dda76e014b52b775a8dc0168d756776e2e5f0c6569ab4e764c88`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 4.0 MB (3962194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f550c2045c0da081acd88fb3e06f2f1cfe56c8b3010ee2d89946189a639dff5`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

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

### `couchdb:3.4.3` - unknown; unknown

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

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:7819b07037fe98ec994ca26a121fbb8c9a601772df54fa0f3af9f7ba85e50a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135766171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220713081441f1810d0218f5900376c97d27ed09c05e86c7476f16287ab5794`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c8a4385111079823034d1e8ed702e9672cd681f79562137fa525d16803eea`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c0f7f5b2751909f18f45844094309abfc54100ace7c37207440666c3dd916`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 7.4 MB (7387937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b6aeef9cd48451c7352e0d027a4ab68782567fd1af8b1aeed4283756407f74`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 355.6 KB (355644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a016c259437b9920b9c085f993abedb656356821d7571071cb17db40433ce23`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf854b3c69326f429e568061da038a651efb11e32516f8571b1eb6c2fa4f676`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63c8fe755b51ffd8fbe51e653149697f4db50ec5f2e547f3cdacddcf23a8cc`  
		Last Modified: Tue, 29 Apr 2025 00:03:42 GMT  
		Size: 101.1 MB (101055957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702504975d7b1931a864c2373bbe22a5a0c200b6689e356d0e589bee6a061932`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c449b40f1681890fb4190af1efe37d7714370d105e051af05596c701a932f57`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094a79dad673e9d7ae35052d26551314238c734e732e0fb16915e7266b6547ad`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1480727e9ec140937813aea1076b6378bf266665e18b0e20314a588367868a3b`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:88af6693555cb508b2d025acdc1cf32ed693329c7425a63e3ca33fcae9d6527d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cd21e53513802102079ed3d78030c64a5a73292fb437f3f01cd3c37abebb08`

```dockerfile
```

-	Layers:
	-	`sha256:899e8cbc1e36d790e687a9f1f9b1b0d69e11609f8e383484c7a552377bdc224b`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 4.0 MB (3961282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5195173997f32afdbc21e62b738eca6b36722bdcbe2527bfd1b80cc09e348e`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:6295bfac943b51087b6175eff9cff56de9f5d9eb94f3910d8c04a62acab74714
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
$ docker pull couchdb@sha256:77ffe59ff29af9d3c5219482f72482fbcb2a0ff2483c083e2d49fb115673bb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156349834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a27220813b744db3146ca8ced46f5cabde9a8fb7793a6c920793d220354a0f6`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a837b37dbc4aaf872f53093cddc1be6d7ef890b0711392143a9af72cef98aa9`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75c714820d9f6c5cbd4bf86389324df57d7541f49cf758a529ba5491022d8f`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 7.9 MB (7874927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe12777043dbe4709756fe502296dc6f6c3bbd613e3ef916bf1734214b192ba7`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 77.3 MB (77297600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78ba57999ae720b3c4071011a08e9999098f55ed42ff9b6ed3f3803132698e6`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 415.0 KB (414976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29364f5cdb32bc05cdd929c02986311ed94c76e959a4e263ba9cf30cd49229ce`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 99.3 KB (99309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bc17ee849dc1a4faaa61126db10e65016ed2a4c2710bd1d2ad98c07f3660bf`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9cc3233d493f6ccb82dbb845f9bf89aedb7a809588f957dff97a8a417b20bd`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
		Size: 42.4 MB (42433507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fa03def47bdb76fe273a3779236c9b64f6cbba548c826afab19c88bef4e4d`  
		Last Modified: Mon, 28 Apr 2025 21:55:59 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a6081534b52d88c51815ba521ecff693dea686881b9966a95ee75abfab2e5fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ce8df7d14f7982fb816dce683b26a15fde337ce687af08ea53c0ade53063f9`

```dockerfile
```

-	Layers:
	-	`sha256:a76c0ac78c05527f8220cc9ae241667389856abc3b537b0574c27f99d4400106`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 3.5 MB (3468472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a08d555edab0c60d4bcb148bd4978664d1b20f9aae43f6e9a2097f7d4c7bdf4`  
		Last Modified: Mon, 28 Apr 2025 21:55:58 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ef86d350be3be5f381e1c1f8c88aa5636d75438d6ed3fbe46de10272dbe71a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155151031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1c6c7c10080658c8b4eadc27e8ce4cd8b1e48f8f847fc4944f24842acf2ab9`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd8f34bf1ac88838e26e0a2aaa5277259abcf731e3be2982f5f7b187a498b7d`  
		Last Modified: Tue, 08 Apr 2025 06:08:34 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfeb2f1090890b2eccec0deb81ace448720d51cf9f6223e04171d01133d6880`  
		Last Modified: Tue, 08 Apr 2025 06:08:35 GMT  
		Size: 7.7 MB (7654526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e8560a11efafc2608b641351699397902ac284b2de13fcc59ad42e88c17ccb`  
		Last Modified: Tue, 08 Apr 2025 06:08:37 GMT  
		Size: 76.6 MB (76624215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05f28575931d496b3ce2fcfaefba1cb4de7c78935d4e869ff9ec4ba910c4ca9`  
		Last Modified: Tue, 08 Apr 2025 06:08:35 GMT  
		Size: 371.8 KB (371752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5e87b04fa9145d9d256ed83fdcab7c6ea18fe09ceffd7f2fbfb4f93a1e3565`  
		Last Modified: Tue, 08 Apr 2025 06:08:36 GMT  
		Size: 99.3 KB (99269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8837079b0c7afc124818e7f34425210f8d93d1079e1a10cb003a7303772886e`  
		Last Modified: Tue, 08 Apr 2025 06:08:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1be7702499648f7eeee1a7c249646f3cfccb0ed6958777e78aa631f83cfc35`  
		Last Modified: Tue, 08 Apr 2025 06:08:37 GMT  
		Size: 42.3 MB (42333067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bbf4a32731c1ff00883e64ac3bfbdd144fb4661295d4fa4cde05f3b8c8c38d`  
		Last Modified: Tue, 08 Apr 2025 06:08:37 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:0a4647b4cf67f83b07b8cedf4dbc451fd13dc6e1131766239a83afa2b38a008f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4849696a300233a5245da38545c5a9c51709e0917fb70396be40cac6b8beece9`

```dockerfile
```

-	Layers:
	-	`sha256:c72e829feccf8ae458a5f9b1e8f1c3939bb3193f2b2b76919fcddd0c9fc1b0d5`  
		Last Modified: Tue, 08 Apr 2025 06:08:35 GMT  
		Size: 3.5 MB (3467148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7df692b8d1cef439ab82454d228b29dd122424de355867e8c1fb75f04acd56cf`  
		Last Modified: Tue, 08 Apr 2025 06:08:34 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:567f3e53824961c5f506118d23c53e6c44333ede5da72ca9fc0453ee8df3559f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149977892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d2af33615aa36bcba2719f0280f43028b632981cf48362c439c8774e5a7e08`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 18 Mar 2025 04:14:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Mar 2025 04:14:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Mar 2025 04:14:08 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Mar 2025 04:14:08 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Mar 2025 04:14:08 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeb9febea926497c6b73a956a66c5ec7705a80ed96a88acd22e023a12bb07b9`  
		Last Modified: Tue, 29 Apr 2025 00:04:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb3720e0f56a097c25a4a4a982b82bafb5b5cd40ac87ffefca40556227f213f`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 7.4 MB (7387952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce679ce7dd142ab1209f6b1e198804851164e290d7c9412f489110386d84a3c4`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 73.1 MB (73065225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ea5e69fb0ac2e8ec68ad79d4ed32a98475e57dec15e01433a7aac1c8d2bcff`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 378.1 KB (378103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8084ad1ebf84dff15753e78e53bdc8cfdccdcb39266f1bf8e231f251d78a64e3`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 99.4 KB (99449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a49819b32ddd9c0fe27e1ed0f760870d4d9170232838540cc48f818ef2606e`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cd8bce374995c6a118e0965c0b2ebf3fa93ae834354a829cc1b3cd0f830219`  
		Last Modified: Tue, 29 Apr 2025 00:04:49 GMT  
		Size: 42.2 MB (42160416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55bbc492280b5c45b056b641e8fec35f5fb54bc50068de783a4c110b4beb376`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:77c04fe246e4b659963c87d866f2678b43426ef3984aac6cc092e602b0dc0ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f22a5e7194519b1d9eff220c23222179736285e22078c6328ae14eda1ca0b0`

```dockerfile
```

-	Layers:
	-	`sha256:e581491861b03880116342ed4b02be1373f61f3ac37d5e781506fac9e30a02d5`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 3.5 MB (3461893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e144eeff7b03258ac15dcb32b9ea1e2ff7892643f844b7df4a7b15118c6c87e3`  
		Last Modified: Tue, 29 Apr 2025 00:04:46 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:07d39b300e4e9ab9a3212efeb25d855372a914432eb1b1f566255de8943afba9
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
$ docker pull couchdb@sha256:29bda1ef06e431703b2b2ae415afbd8e39cc0bfd5e618aec2ef4afd9b6e8c708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138996025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577f5a2bf8281f310410466f9ff2dbcabfe1473b4e50a8384be08b36ecf99607`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8bb06f1e12481f1734930caaf5aec605aaa24e1a4a714390080ff8d49a9bae`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c643e44c289be880b7e1077b20be39cc8aa46c96dc275d3c274d9f4285b16e89`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 7.9 MB (7874898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139f130bffc490d838a88a0d05accd783a68e9f617fd52025ac774f55bfe8b96`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 392.2 KB (392157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482d9e178fbe5fbe5cfad58aa00c10b65769efe8fb24ae45ec9a43b2389fb87b`  
		Last Modified: Mon, 28 Apr 2025 21:56:01 GMT  
		Size: 76.3 KB (76322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662901ec9a4cb6ba009d3607b9ad113b7bdd517130e2eec9112df2d01a05d6cb`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e060d223a8335af42564a119d05c7671db6bf1f629900166eac7b8c0e939a`  
		Last Modified: Mon, 28 Apr 2025 21:56:05 GMT  
		Size: 102.4 MB (102419585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a1370ccd45c896adc8fd7170cfbeb3eeac84209a0219dd34aec6210e1ab02`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1e127bb37e749c471a816e789f4ded13248cb110d7e3f9e4e17c8f7191e9d6`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87be8d54aedb6022da943334261c18e1eed1d602beb1ea3baf8af2a328b975`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133652bc69003427ae7004295dfcdea96aa5a003479ceaa3742c9e0e88528555`  
		Last Modified: Mon, 28 Apr 2025 21:56:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:42c546356d24d3788c955b5d00eb4bcd393a46bc59e6fd076597281b2fe6b7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e2799689e298289b95db4b12008b49d684dc9a4297f34dd80dbfa169f6da0a`

```dockerfile
```

-	Layers:
	-	`sha256:a3f7e3b29115dda76e014b52b775a8dc0168d756776e2e5f0c6569ab4e764c88`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 4.0 MB (3962194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f550c2045c0da081acd88fb3e06f2f1cfe56c8b3010ee2d89946189a639dff5`  
		Last Modified: Mon, 28 Apr 2025 21:56:00 GMT  
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
$ docker pull couchdb@sha256:7819b07037fe98ec994ca26a121fbb8c9a601772df54fa0f3af9f7ba85e50a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135766171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220713081441f1810d0218f5900376c97d27ed09c05e86c7476f16287ab5794`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 18 Mar 2025 04:14:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c8a4385111079823034d1e8ed702e9672cd681f79562137fa525d16803eea`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c0f7f5b2751909f18f45844094309abfc54100ace7c37207440666c3dd916`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 7.4 MB (7387937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b6aeef9cd48451c7352e0d027a4ab68782567fd1af8b1aeed4283756407f74`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 355.6 KB (355644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a016c259437b9920b9c085f993abedb656356821d7571071cb17db40433ce23`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf854b3c69326f429e568061da038a651efb11e32516f8571b1eb6c2fa4f676`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63c8fe755b51ffd8fbe51e653149697f4db50ec5f2e547f3cdacddcf23a8cc`  
		Last Modified: Tue, 29 Apr 2025 00:03:42 GMT  
		Size: 101.1 MB (101055957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702504975d7b1931a864c2373bbe22a5a0c200b6689e356d0e589bee6a061932`  
		Last Modified: Tue, 29 Apr 2025 00:03:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c449b40f1681890fb4190af1efe37d7714370d105e051af05596c701a932f57`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094a79dad673e9d7ae35052d26551314238c734e732e0fb16915e7266b6547ad`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1480727e9ec140937813aea1076b6378bf266665e18b0e20314a588367868a3b`  
		Last Modified: Tue, 29 Apr 2025 00:03:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:88af6693555cb508b2d025acdc1cf32ed693329c7425a63e3ca33fcae9d6527d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cd21e53513802102079ed3d78030c64a5a73292fb437f3f01cd3c37abebb08`

```dockerfile
```

-	Layers:
	-	`sha256:899e8cbc1e36d790e687a9f1f9b1b0d69e11609f8e383484c7a552377bdc224b`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 4.0 MB (3961282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5195173997f32afdbc21e62b738eca6b36722bdcbe2527bfd1b80cc09e348e`  
		Last Modified: Tue, 29 Apr 2025 00:03:39 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json
