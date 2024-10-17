<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3-nouveau`](#couchdb3-nouveau)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.3`](#couchdb333)
-	[`couchdb:3.4`](#couchdb34)
-	[`couchdb:3.4-nouveau`](#couchdb34-nouveau)
-	[`couchdb:3.4.1`](#couchdb341)
-	[`couchdb:3.4.1-nouveau`](#couchdb341-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:4364560362da99f250e4a8d560bc1806cd8aeb1bbf7e42195de8b2e9d11b53d2
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
$ docker pull couchdb@sha256:029c957c6085831c1b3c871c48a22c0e618696ffe913324d22d9282b0a39b08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134020203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c57cad342da3d09144089b44a33943b580013ac65061b2409edd8821fb7ce3d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.4.1
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e42c379dbed7e01471433a483c15b1d996c5ed3d430105b68689a9c215e800`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32107ac5bd299153711b495ceeff557b8a64aaae2fb9c160d17d05fadb80df3a`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 7.9 MB (7874356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5660ca481d1c336f58d2be80116f5997a9d579d67fc5b555f7f4ba496492b0f`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 392.1 KB (392103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f3e31d4f81d299470bc7f6d7d37028f4b6ad8ace7908f485418f3e8d59295c`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 76.2 KB (76244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dec924dd56ef5930d17c10379cb5267ce7678351ec26f9611ad50dfb9e2143`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a58ade298ff5c2b3c13c00cf8f99be03638408f81549660d5a40b2738f4eed`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 96.5 MB (96545784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a205d842ecb203d13a8861aee1278f11a1d1660310bee6de158831af8cf9893`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dd0d9ec0677277ec17473d6196aa874752c0dbcbd89a42ad52cb4c97fa7158`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e00cd59bccdf60a1b95275cc9dd1339c9bd66e032aa967595a02b02486c20`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd52ab77a219e9f845b3e8f52fa6a39f50281c404945b5e2c4e2af6845b3f0fc`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:61b816fb879f153801f5a0c57aa993509b1ddeb686aeb5fbb95772b4741999a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9d29d794d3d88f48a7d639394be30fbf04023331df77c876d795635af8c0ba`

```dockerfile
```

-	Layers:
	-	`sha256:f4df39bfb7fd657b3ad306503d6702ddc66a7db94de70989483c56cc916466e6`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 3.9 MB (3930860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3385f28de0725f1a6b2ca0be504c7563e084956d3a20dad36f869c51b54a16a`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 31.6 KB (31650 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d532c77f5ac3c2c7675c72630156a513c493e22b8c9bbe9daa3a0539371d94dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133500812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab807e6cce1147b09eb22518b32dfef9270a0f8eb876d6bf35a419d49bfe7db0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.4.1
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158aa9f5c882b5e97fedccc7ae2049826daac1ea4cd80673760c600f66fd25a2`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d0ed31128e494cabd8bf247a75c16916b3384b4ab343f5ca57f7a4a5c953e6`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 7.7 MB (7653591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b763c74cd503a2c115563fbcf3749f7acae5cb7f4747419b2fde045c42d753b`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32407ed42108ffc45dee617bf1da018fce735f15f99b1f7962bf70bc0ca583eb`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 76.2 KB (76229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce8a6203d191d77248cf4554ff76784f28da8ac19de6aae41eff2d3bc095840`  
		Last Modified: Thu, 17 Oct 2024 08:36:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95debc0adb7a8e663736a87a597d945f03b94f5280ee118a162dddf607e45b2c`  
		Last Modified: Thu, 17 Oct 2024 08:36:04 GMT  
		Size: 96.3 MB (96260311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1fdd486e3f558abe65e4b0a5b05fbff273d9926485276b3b9df1dfa01e761b`  
		Last Modified: Thu, 17 Oct 2024 08:36:01 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cde81be4cd034590b1a74c01b8a0f94dfee7a2217d7978d3012614d8a8eb28f`  
		Last Modified: Thu, 17 Oct 2024 08:36:01 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f683798cdb6c2dce7873c45876d80a823f105a215febe6e1c82c5c9fa6c3a88`  
		Last Modified: Thu, 17 Oct 2024 08:36:02 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d986906d69fe681104b8db126b7fd15f16cf51cff824e890f5fccc52b213f06`  
		Last Modified: Thu, 17 Oct 2024 08:36:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d7f4626f764d1b2f2094fb77be6f4894f41a84c53f2ebbd57085bce4368b8f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb6d5a2b4f152a8d857f93528f0f22bbafcc4f75ecd2e59e332023bddb330e8`

```dockerfile
```

-	Layers:
	-	`sha256:97415988cfb8af055a7f756eae5fa6f43d806f969e10ba2d36c980820f9c3d2c`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 3.9 MB (3931152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36aaab4a230db2e84c0718ade07b3dca1336179cc9a3be83c0e732fd44980b3c`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 31.8 KB (31837 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:99de95bf542240cee02bfa5fc60965c31e4a314507d01e18366bdbb610815aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130484580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d98d0c40506661ca51e78c8cae140fec1d459a9e14020ea458d999d88109da`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.4.1
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365969b4631a62e6d7ef499c6b92905c6fa0d70d6a10749efb8e580b5256cfd3`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4ed4afe5f3bbc527fe4b796a3de285fe49d0da533ff237867f3aca6a5968b8`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 7.4 MB (7387059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b12de2ec74a1377b65c5c729ade5d41b78260a3db246c3df9020d2b33010cd`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 355.6 KB (355620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7328de8b8ca2116e01c13afc0eab1a28fb3f64e8a439112d3b20bc4703589bb7`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 76.3 KB (76311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0cf44eaa7e71276c2479f79c743522f24452594342ff154a1755e85865733b`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1512147a7c60623082fa331b1c2b902d9e080d473ee279c2462b34dd7b7712`  
		Last Modified: Thu, 17 Oct 2024 05:22:44 GMT  
		Size: 95.2 MB (95170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b463db19e955485f17688807e3d553f2786b99d74243b5acc59e19d551604246`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab9c80c3a4eabf87a27abb1049f1ddb895c0df87a965c087d4c34b4bbb4bb8`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c2eec10bfc0129f41384dc5144e0ca5630f5392256c2746bdb8d25af26777c`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7248aa17d2b0e8fde84ae6e445ef95b3472fc45975c316fc0a55b3a26a9509`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:4bb4b10c15d697d4356a10857d75b4368a3027b2156fa2861211c365b65d6000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a297875db8cd9f3393bcfcc2fb2684bf3304d003e7a31c25bb1b1f6705d8076`

```dockerfile
```

-	Layers:
	-	`sha256:d684d396e8b38252eed69b47ac07e532144b2fd5c47cade9f13d255436200b71`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 3.9 MB (3930054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598ec2df229033220609d31a9166e652336f64b8b89eb737110ff684b29d78a7`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 31.6 KB (31650 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:c8e6e619045e67b6f614ba41e24923a53b9a87e5b850ee0f0a832afeffb7ca31
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
$ docker pull couchdb@sha256:69201663158ef27cebf3754503b99930fd9fcba11b9ddca4004fb9ebab880526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156247349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c79aa53ba986a9a9f2923dcff657045fbfeba8b0df43c45b018df4c6b7a175`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8341a5170e640ab064934f5a16b9ddda0d977e75c8a35a2c0a21624175ff7d55`  
		Last Modified: Thu, 17 Oct 2024 01:13:58 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d614eb0dffb75053d727b3da4345cc10290bedde0592ab11da569f1303d25e1c`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 7.9 MB (7874325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f47713982a4618c995e645c57ccd25e4bb1a82c7f599781d74ac8beb173c91c`  
		Last Modified: Thu, 17 Oct 2024 01:14:01 GMT  
		Size: 77.2 MB (77212293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b504ad20a2b123b7701b91d47c94fca132bd9b7b0d87a62c98ffe3b0fba7961f`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 414.9 KB (414915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc4abaaed860931f8316e29ccaa1e28fb973cf3465f80a72c6bd229418a1b4`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 99.2 KB (99225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3963ff4981167fb6541aa9d61cf3ca5ceea815cc334f709d7ba28bc35c5664c`  
		Last Modified: Thu, 17 Oct 2024 01:14:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d533960cb845281574aa500cd0664a7af2ff3a0d6f0375b9cec594d6c2dbef`  
		Last Modified: Thu, 17 Oct 2024 01:14:02 GMT  
		Size: 41.5 MB (41518425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25cdd0790b455c2f406f8cc76c546a18ae0c354a7cef553c69bd5e3474d2640`  
		Last Modified: Thu, 17 Oct 2024 01:14:00 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:73f91e3d4325120c083b80a024abe041b6d609fe89dab2f33f1af4ca0acba313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3478701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17bd9c4df629543404caa7974aa89adc67ba197f9468d81ede57cf02ff55e70d`

```dockerfile
```

-	Layers:
	-	`sha256:8db47e984c370964cf9a1fe7f608b95199bacd19bd67b8ac7599931763c3f615`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 3.5 MB (3454275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85194621739adfae301dd10b86700352c70ef6325d11a0fc4591cd7625a2c41`  
		Last Modified: Thu, 17 Oct 2024 01:13:58 GMT  
		Size: 24.4 KB (24426 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8a5b77c7118d220a61071998d224249d041f9f74083eb8f3591fbe9ceef936fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155210795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b353a401f166bb68e575bfd822646a3608e820cc4231fa13464b0683e3e985`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23dade21ddc63b42d2647ee5bd298a2ef267e5acab231c2d6da080d9d71e6e`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfb43d3130dea5b226ee6d3d7a89a1a039708a27401ad55338f9509583bed31`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 7.7 MB (7653601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e5d718c0a45301c947c0bca060f0ef28d7c83043355da9e77a0804f831f46c`  
		Last Modified: Thu, 17 Oct 2024 08:37:10 GMT  
		Size: 76.5 MB (76508581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7eece477d75c7f105fdd604598ed02f5b1068a219cbe58a2229256b9893b5d3`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 371.7 KB (371682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbcc8c872a854268b654cdb819597d6728167612a8a56425d398b2fe641fb`  
		Last Modified: Thu, 17 Oct 2024 08:37:09 GMT  
		Size: 99.2 KB (99198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e6bc749445a8325728ef17a17221250d734e41f3062355d62748a56c7fc33b`  
		Last Modified: Thu, 17 Oct 2024 08:37:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e94d56078b2aa7190091ad8d91efea53f6653876edd7f1f68acc5f36cb423c`  
		Last Modified: Thu, 17 Oct 2024 08:37:10 GMT  
		Size: 41.4 MB (41419520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198e8ef17bfe3703c4efccfe17c5f2e1f4beb2d8e1ca32ea4636edadc5e16b4b`  
		Last Modified: Thu, 17 Oct 2024 08:37:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:655485c5c80e437b211a9b7f0151c0b8459ae590de744b1eab9fc57d195b3ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3477550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d47175e6d8e0f3339c0bef4902b5f78f1161136c89714e9a9f55dc66212e2`

```dockerfile
```

-	Layers:
	-	`sha256:13a60c99d849a0e9a27b5590f5fd975c20c879523ee7a6ca32fed3c2420d6981`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 3.5 MB (3452948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dec208ef53f3f257d00c26a0de0714575dc0ed04a9ee0900349e84366c9cccaf`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 24.6 KB (24602 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:34e4e127c5f9ef485fade28d3f311f0e0c6cbc12a7c2af25afdb08d9c4d4caaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149594813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b07f083ecd69500e12739cee0bfb3d845466964e509d5554f6a5f49be3396e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1da9e475f448a5faef36ac7b6cb60c0ad8ce9821f2cbaa18d4ee80f33bb576e`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca823418cdd443363165feda244a9e4293b99d5a5ac44d9df8a9ca407b4e094a`  
		Last Modified: Thu, 17 Oct 2024 05:24:06 GMT  
		Size: 7.4 MB (7387056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74513d24c6f38678360078dd599c83f6bc450d3c4cc8a46592c568a62d65b05c`  
		Last Modified: Thu, 17 Oct 2024 05:24:07 GMT  
		Size: 73.0 MB (72987699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85ee38c5a5951cf9fc20bccabb755a2a8d30f1b5fac51d652db2480d4a66777`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 378.1 KB (378063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2b747794ac6e71d08c738e803fc7a9e53a96be7f4b2da17fc311c92665edc0`  
		Last Modified: Thu, 17 Oct 2024 05:24:06 GMT  
		Size: 99.3 KB (99349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a453eab34057d928b0e5ff72f73999ad46c3263d20fa80d54147d243cf941591`  
		Last Modified: Thu, 17 Oct 2024 05:24:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344df0ea4b3986556ab2689e47053d6f23aafb0939e455160a615261744c971e`  
		Last Modified: Thu, 17 Oct 2024 05:24:07 GMT  
		Size: 41.3 MB (41250686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077039b4df922fb240063f1a67223bc9406740c5e13ae052c295261ab50c2533`  
		Last Modified: Thu, 17 Oct 2024 05:24:07 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a7c98572f2af51d20a27ac5ecd3d8a1ae45d8bc53fad772fd172b9a519e43393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3472219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbcbfc99f19034f187721f94a407d269357eeb33e8f3b50f38cf08be226de3b`

```dockerfile
```

-	Layers:
	-	`sha256:1357a127db355bdd98ee39a75190cb56b6661faef478e43e331e35c51fb8686e`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 3.4 MB (3447794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85650d43777473290fad1f06db62d0cc4ac3f2ad81e6cdd6f3538051ab7ca92e`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 24.4 KB (24425 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:17e193121beeb266728b300727dff2bc3d53f3aa713bad82639128bb363d2672
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
$ docker pull couchdb@sha256:c9438f4ed2b6e90ba09bbc25b2df038581061bb81a1b11001f17172177869587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97624740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919a18f290f9d7e28ee1726c1e0189dcfe5881144fcc606ca6b274ed6500acdd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.3.3
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6654ee77adc331c6b5225709607dac33faef106908936f749d24c5b2d7cfe168`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8b2949caa483a0e88306272c7c79e1855519537c531e8625daf679508837ef`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 7.9 MB (7874297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b537e0d0281b79906e1a98495dbc00434ba5b90591aafc7dc7e34097e8051cb4`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 392.1 KB (392091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f62067eae2e34072f0be53d33c056d5c3eb0ca47f7b04983ce102ebed8c4bb7`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 76.2 KB (76242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726b7748f3ca349e6cf669943a392700ab037144d7e28ab0a71eb16fa8a54d57`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9434a46b87aee0fb3b62ceb587ecb403ec7402ad160f0fbbe075ed184dd77c21`  
		Last Modified: Thu, 17 Oct 2024 01:13:50 GMT  
		Size: 60.2 MB (60150390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89541654b198f721e3ac4a28792dafb568f4d96d430860989b031635ff31d778`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754f73b7daef8f157a50b73570b7a599b1ceb1c0770d3be1568c8ebe0dc09418`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d144e0eb9d779dec61d887bc7260ba247b888bb07cb0dfc681724085350fad70`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b27765512a01c3ad676fa3493454f9034992c5d4f498a5f52f094c3a49be43`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:93ecac71189d8bd8531f0b690a0214665dc6e0c35eb6fccd539f7c0c9bd0b9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16954654f47336301eaac50a66f52659cbe55e6024dee38d0fe359762fd787cd`

```dockerfile
```

-	Layers:
	-	`sha256:ae0233cac816479735617f56b4852f9bf086d9f2895b203c51e2956bb26142ca`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 3.7 MB (3723082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f461982b986d76f371d02aca16c5704c7d13b32c8892895be7751414434b1c0`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 31.1 KB (31066 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5d59aca2a58e34524dbb29e5cb9ec6bafe596bca1b74137413327db76a22bfa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97174745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af4adcae1460943b9a1f57c86f7a7ce5d544de010662409fc01bd13a97685d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.3.3
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158aa9f5c882b5e97fedccc7ae2049826daac1ea4cd80673760c600f66fd25a2`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d0ed31128e494cabd8bf247a75c16916b3384b4ab343f5ca57f7a4a5c953e6`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 7.7 MB (7653591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b763c74cd503a2c115563fbcf3749f7acae5cb7f4747419b2fde045c42d753b`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32407ed42108ffc45dee617bf1da018fce735f15f99b1f7962bf70bc0ca583eb`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 76.2 KB (76229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c26af2d9658a0ca2cdf2b2679a1eba7967e896906ba83809c730fd44a3ccc8`  
		Last Modified: Thu, 17 Oct 2024 08:37:47 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a18a0fac3014f6394a7365f4ffe40aa6b5621077c9264643f21e06363e1c0c`  
		Last Modified: Thu, 17 Oct 2024 08:37:50 GMT  
		Size: 59.9 MB (59934245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a458d1f4a6910c4a81e9aaf179977a2f7d4af0384d9b2d5c0fcb9e7b561d3e`  
		Last Modified: Thu, 17 Oct 2024 08:37:47 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c46af82ac297a85449065d5b13d947c510d4f3162c751f7619b22b54669ab6f`  
		Last Modified: Thu, 17 Oct 2024 08:37:47 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dc9bdcb0a6c4cce18663178b2319572aa3f709dc3bff2580b2b56eb1ea9140`  
		Last Modified: Thu, 17 Oct 2024 08:37:48 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0103a0371778a651477bdf6b39ceaf9e61ca47e4ced14c6da771fa885b4790cf`  
		Last Modified: Thu, 17 Oct 2024 08:37:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:22878e9d37a607d2806ffbd318f6a0c764783ebdcdc9d85f73a0da93c0ea4816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19f4e00b78bb793f291e8e67a04fd691853aed4181924c170207eab36dd7fbc`

```dockerfile
```

-	Layers:
	-	`sha256:735f678e489445581dcd9b2c1a4ae065d304774de7dc3b0159f296ae2cf881d0`  
		Last Modified: Thu, 17 Oct 2024 08:37:47 GMT  
		Size: 3.7 MB (3723350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c292c925e5353eb45719e002181a51d672996942be08d1467cac4c6dae7f3bc`  
		Last Modified: Thu, 17 Oct 2024 08:37:47 GMT  
		Size: 31.2 KB (31229 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:1f266a9374219c30ec333efc945a6c3c4468a2b8c4d767da3e1dbe1af5e08fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103912861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1453cfd39de378258b757b3cace45e515bda7239b20dfc7030dc03b40a046489`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.3.3
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b256e4f44fe20140a80de607f6b849da29cfc560a25d78539c7e09e10631461d`  
		Last Modified: Thu, 17 Oct 2024 03:33:17 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5161381afb53bbec58a4a880980087f7f4b7ba952f243cd64481922b9fefbcd`  
		Last Modified: Thu, 17 Oct 2024 03:33:18 GMT  
		Size: 8.9 MB (8889196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cba77e35132f41b78f096534b0a2f9736bb22d24bc122cb85ca7aad637b71e`  
		Last Modified: Thu, 17 Oct 2024 03:33:17 GMT  
		Size: 444.7 KB (444672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e791a920179eef0960d40e11d09748f2a3935cd26eca132a818e30e1ac9315`  
		Last Modified: Thu, 17 Oct 2024 03:33:18 GMT  
		Size: 76.3 KB (76310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e219d691e57aeedf093a03be25b85603e6a2c89b900c3a4f57f5e6977b97734`  
		Last Modified: Thu, 17 Oct 2024 03:33:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6e1cf043d952393d4a6a55b6ce5d09537779a98fad37b17586dbaf6ce769af`  
		Last Modified: Thu, 17 Oct 2024 03:33:21 GMT  
		Size: 61.4 MB (61375052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ad94e572c024faa0d605e15b45f2a2eb6260e6159ed15061d6f72c42c9052b`  
		Last Modified: Thu, 17 Oct 2024 03:33:19 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5526fb902381be8726d23a57fe723430a4ab41b8e23f8d9d76f33bbcb63966`  
		Last Modified: Thu, 17 Oct 2024 03:33:19 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9cf77e745b88e466258e3daf5731fa95574a1c8777cd86cba0de405a1b38c9`  
		Last Modified: Thu, 17 Oct 2024 03:33:19 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522ce2ef3612eac5eb9503ce169c07ad6737c1871830cb3e669006a3bead80c3`  
		Last Modified: Thu, 17 Oct 2024 03:33:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:42498d1d8953c47fe414a0f41c9b30d7f16b2fe3782c492170c0c070270aca2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0fc8a2815b21f01768bd88bec0a0b7430dca7398290230fe3875b3eb3ddbdf`

```dockerfile
```

-	Layers:
	-	`sha256:11acd59c7e24494cd94bd148d0f645631d84132bd2c80dc035af66d7af37b109`  
		Last Modified: Thu, 17 Oct 2024 03:33:18 GMT  
		Size: 3.7 MB (3727585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f276ae73e4d5ec11d966c4dc310db680d442208e7b58a3eb4e4ea964bf6dcce`  
		Last Modified: Thu, 17 Oct 2024 03:33:17 GMT  
		Size: 31.1 KB (31104 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:f92a34a27199569c09a1bcae83bb39290f7275dee6702d651d2ec74284fa04a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94054443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fced1e85f58d186423ae842d29273539f60e0696c29dce86aa845bdd9b3b2b44`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.3.3
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365969b4631a62e6d7ef499c6b92905c6fa0d70d6a10749efb8e580b5256cfd3`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4ed4afe5f3bbc527fe4b796a3de285fe49d0da533ff237867f3aca6a5968b8`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 7.4 MB (7387059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b12de2ec74a1377b65c5c729ade5d41b78260a3db246c3df9020d2b33010cd`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 355.6 KB (355620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7328de8b8ca2116e01c13afc0eab1a28fb3f64e8a439112d3b20bc4703589bb7`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 76.3 KB (76311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056eb698e27dedcf8484499047b8b54bd130d4254424509d1e2f73494c9cc04`  
		Last Modified: Thu, 17 Oct 2024 05:25:04 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e2871a83bc097d30e0bd095730beaeddb4f57f2177fc8a549402dd2b29784d`  
		Last Modified: Thu, 17 Oct 2024 05:25:05 GMT  
		Size: 58.7 MB (58739939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3f84e20d6d1b4d06b2ddaf6bf45f5bacbf56275a10860548ab000f58b2a5f1`  
		Last Modified: Thu, 17 Oct 2024 05:25:04 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce65b23513345303b9ae444e9678cc1bfc40781ba610f0e0904145a0d5334c0`  
		Last Modified: Thu, 17 Oct 2024 05:25:04 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bf14d9a2ac02ec6be242145bec878bdc327c81bde65260990597372fa5efab`  
		Last Modified: Thu, 17 Oct 2024 05:25:05 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591cf0357e4cdf59b77e5c82cc3f7fb26e7e73d5274e0d6b9d04513c531f5ede`  
		Last Modified: Thu, 17 Oct 2024 05:25:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:623d6c7f1a908099398a11420d8da9c6b9f9b7d994656678f64fcb20d624aafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3753342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5352b1a0d635c8a03a44ed7834b8dff664e7291f8410cd579aab2ad8cfa7e268`

```dockerfile
```

-	Layers:
	-	`sha256:be6e8b812d82dcd863e270e9e04ca0a3d2bdf38e67c919701242e793ac35fd96`  
		Last Modified: Thu, 17 Oct 2024 05:25:04 GMT  
		Size: 3.7 MB (3722276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a67276daabbed06825876b82e6e1b963ce8bc8ce28421d6b4fa0167deda9c74e`  
		Last Modified: Thu, 17 Oct 2024 05:25:03 GMT  
		Size: 31.1 KB (31066 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:17e193121beeb266728b300727dff2bc3d53f3aa713bad82639128bb363d2672
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
$ docker pull couchdb@sha256:c9438f4ed2b6e90ba09bbc25b2df038581061bb81a1b11001f17172177869587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97624740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919a18f290f9d7e28ee1726c1e0189dcfe5881144fcc606ca6b274ed6500acdd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.3.3
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6654ee77adc331c6b5225709607dac33faef106908936f749d24c5b2d7cfe168`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8b2949caa483a0e88306272c7c79e1855519537c531e8625daf679508837ef`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 7.9 MB (7874297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b537e0d0281b79906e1a98495dbc00434ba5b90591aafc7dc7e34097e8051cb4`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 392.1 KB (392091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f62067eae2e34072f0be53d33c056d5c3eb0ca47f7b04983ce102ebed8c4bb7`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 76.2 KB (76242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726b7748f3ca349e6cf669943a392700ab037144d7e28ab0a71eb16fa8a54d57`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9434a46b87aee0fb3b62ceb587ecb403ec7402ad160f0fbbe075ed184dd77c21`  
		Last Modified: Thu, 17 Oct 2024 01:13:50 GMT  
		Size: 60.2 MB (60150390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89541654b198f721e3ac4a28792dafb568f4d96d430860989b031635ff31d778`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754f73b7daef8f157a50b73570b7a599b1ceb1c0770d3be1568c8ebe0dc09418`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d144e0eb9d779dec61d887bc7260ba247b888bb07cb0dfc681724085350fad70`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b27765512a01c3ad676fa3493454f9034992c5d4f498a5f52f094c3a49be43`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:93ecac71189d8bd8531f0b690a0214665dc6e0c35eb6fccd539f7c0c9bd0b9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16954654f47336301eaac50a66f52659cbe55e6024dee38d0fe359762fd787cd`

```dockerfile
```

-	Layers:
	-	`sha256:ae0233cac816479735617f56b4852f9bf086d9f2895b203c51e2956bb26142ca`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 3.7 MB (3723082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f461982b986d76f371d02aca16c5704c7d13b32c8892895be7751414434b1c0`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 31.1 KB (31066 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5d59aca2a58e34524dbb29e5cb9ec6bafe596bca1b74137413327db76a22bfa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97174745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af4adcae1460943b9a1f57c86f7a7ce5d544de010662409fc01bd13a97685d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.3.3
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158aa9f5c882b5e97fedccc7ae2049826daac1ea4cd80673760c600f66fd25a2`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d0ed31128e494cabd8bf247a75c16916b3384b4ab343f5ca57f7a4a5c953e6`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 7.7 MB (7653591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b763c74cd503a2c115563fbcf3749f7acae5cb7f4747419b2fde045c42d753b`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32407ed42108ffc45dee617bf1da018fce735f15f99b1f7962bf70bc0ca583eb`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 76.2 KB (76229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c26af2d9658a0ca2cdf2b2679a1eba7967e896906ba83809c730fd44a3ccc8`  
		Last Modified: Thu, 17 Oct 2024 08:37:47 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a18a0fac3014f6394a7365f4ffe40aa6b5621077c9264643f21e06363e1c0c`  
		Last Modified: Thu, 17 Oct 2024 08:37:50 GMT  
		Size: 59.9 MB (59934245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a458d1f4a6910c4a81e9aaf179977a2f7d4af0384d9b2d5c0fcb9e7b561d3e`  
		Last Modified: Thu, 17 Oct 2024 08:37:47 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c46af82ac297a85449065d5b13d947c510d4f3162c751f7619b22b54669ab6f`  
		Last Modified: Thu, 17 Oct 2024 08:37:47 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dc9bdcb0a6c4cce18663178b2319572aa3f709dc3bff2580b2b56eb1ea9140`  
		Last Modified: Thu, 17 Oct 2024 08:37:48 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0103a0371778a651477bdf6b39ceaf9e61ca47e4ced14c6da771fa885b4790cf`  
		Last Modified: Thu, 17 Oct 2024 08:37:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:22878e9d37a607d2806ffbd318f6a0c764783ebdcdc9d85f73a0da93c0ea4816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19f4e00b78bb793f291e8e67a04fd691853aed4181924c170207eab36dd7fbc`

```dockerfile
```

-	Layers:
	-	`sha256:735f678e489445581dcd9b2c1a4ae065d304774de7dc3b0159f296ae2cf881d0`  
		Last Modified: Thu, 17 Oct 2024 08:37:47 GMT  
		Size: 3.7 MB (3723350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c292c925e5353eb45719e002181a51d672996942be08d1467cac4c6dae7f3bc`  
		Last Modified: Thu, 17 Oct 2024 08:37:47 GMT  
		Size: 31.2 KB (31229 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:1f266a9374219c30ec333efc945a6c3c4468a2b8c4d767da3e1dbe1af5e08fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103912861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1453cfd39de378258b757b3cace45e515bda7239b20dfc7030dc03b40a046489`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.3.3
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b256e4f44fe20140a80de607f6b849da29cfc560a25d78539c7e09e10631461d`  
		Last Modified: Thu, 17 Oct 2024 03:33:17 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5161381afb53bbec58a4a880980087f7f4b7ba952f243cd64481922b9fefbcd`  
		Last Modified: Thu, 17 Oct 2024 03:33:18 GMT  
		Size: 8.9 MB (8889196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cba77e35132f41b78f096534b0a2f9736bb22d24bc122cb85ca7aad637b71e`  
		Last Modified: Thu, 17 Oct 2024 03:33:17 GMT  
		Size: 444.7 KB (444672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e791a920179eef0960d40e11d09748f2a3935cd26eca132a818e30e1ac9315`  
		Last Modified: Thu, 17 Oct 2024 03:33:18 GMT  
		Size: 76.3 KB (76310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e219d691e57aeedf093a03be25b85603e6a2c89b900c3a4f57f5e6977b97734`  
		Last Modified: Thu, 17 Oct 2024 03:33:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6e1cf043d952393d4a6a55b6ce5d09537779a98fad37b17586dbaf6ce769af`  
		Last Modified: Thu, 17 Oct 2024 03:33:21 GMT  
		Size: 61.4 MB (61375052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ad94e572c024faa0d605e15b45f2a2eb6260e6159ed15061d6f72c42c9052b`  
		Last Modified: Thu, 17 Oct 2024 03:33:19 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5526fb902381be8726d23a57fe723430a4ab41b8e23f8d9d76f33bbcb63966`  
		Last Modified: Thu, 17 Oct 2024 03:33:19 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9cf77e745b88e466258e3daf5731fa95574a1c8777cd86cba0de405a1b38c9`  
		Last Modified: Thu, 17 Oct 2024 03:33:19 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522ce2ef3612eac5eb9503ce169c07ad6737c1871830cb3e669006a3bead80c3`  
		Last Modified: Thu, 17 Oct 2024 03:33:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:42498d1d8953c47fe414a0f41c9b30d7f16b2fe3782c492170c0c070270aca2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0fc8a2815b21f01768bd88bec0a0b7430dca7398290230fe3875b3eb3ddbdf`

```dockerfile
```

-	Layers:
	-	`sha256:11acd59c7e24494cd94bd148d0f645631d84132bd2c80dc035af66d7af37b109`  
		Last Modified: Thu, 17 Oct 2024 03:33:18 GMT  
		Size: 3.7 MB (3727585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f276ae73e4d5ec11d966c4dc310db680d442208e7b58a3eb4e4ea964bf6dcce`  
		Last Modified: Thu, 17 Oct 2024 03:33:17 GMT  
		Size: 31.1 KB (31104 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:f92a34a27199569c09a1bcae83bb39290f7275dee6702d651d2ec74284fa04a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94054443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fced1e85f58d186423ae842d29273539f60e0696c29dce86aa845bdd9b3b2b44`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.3.3
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365969b4631a62e6d7ef499c6b92905c6fa0d70d6a10749efb8e580b5256cfd3`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4ed4afe5f3bbc527fe4b796a3de285fe49d0da533ff237867f3aca6a5968b8`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 7.4 MB (7387059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b12de2ec74a1377b65c5c729ade5d41b78260a3db246c3df9020d2b33010cd`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 355.6 KB (355620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7328de8b8ca2116e01c13afc0eab1a28fb3f64e8a439112d3b20bc4703589bb7`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 76.3 KB (76311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056eb698e27dedcf8484499047b8b54bd130d4254424509d1e2f73494c9cc04`  
		Last Modified: Thu, 17 Oct 2024 05:25:04 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e2871a83bc097d30e0bd095730beaeddb4f57f2177fc8a549402dd2b29784d`  
		Last Modified: Thu, 17 Oct 2024 05:25:05 GMT  
		Size: 58.7 MB (58739939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3f84e20d6d1b4d06b2ddaf6bf45f5bacbf56275a10860548ab000f58b2a5f1`  
		Last Modified: Thu, 17 Oct 2024 05:25:04 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce65b23513345303b9ae444e9678cc1bfc40781ba610f0e0904145a0d5334c0`  
		Last Modified: Thu, 17 Oct 2024 05:25:04 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bf14d9a2ac02ec6be242145bec878bdc327c81bde65260990597372fa5efab`  
		Last Modified: Thu, 17 Oct 2024 05:25:05 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591cf0357e4cdf59b77e5c82cc3f7fb26e7e73d5274e0d6b9d04513c531f5ede`  
		Last Modified: Thu, 17 Oct 2024 05:25:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:623d6c7f1a908099398a11420d8da9c6b9f9b7d994656678f64fcb20d624aafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3753342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5352b1a0d635c8a03a44ed7834b8dff664e7291f8410cd579aab2ad8cfa7e268`

```dockerfile
```

-	Layers:
	-	`sha256:be6e8b812d82dcd863e270e9e04ca0a3d2bdf38e67c919701242e793ac35fd96`  
		Last Modified: Thu, 17 Oct 2024 05:25:04 GMT  
		Size: 3.7 MB (3722276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a67276daabbed06825876b82e6e1b963ce8bc8ce28421d6b4fa0167deda9c74e`  
		Last Modified: Thu, 17 Oct 2024 05:25:03 GMT  
		Size: 31.1 KB (31066 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:4364560362da99f250e4a8d560bc1806cd8aeb1bbf7e42195de8b2e9d11b53d2
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
$ docker pull couchdb@sha256:029c957c6085831c1b3c871c48a22c0e618696ffe913324d22d9282b0a39b08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134020203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c57cad342da3d09144089b44a33943b580013ac65061b2409edd8821fb7ce3d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.4.1
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e42c379dbed7e01471433a483c15b1d996c5ed3d430105b68689a9c215e800`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32107ac5bd299153711b495ceeff557b8a64aaae2fb9c160d17d05fadb80df3a`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 7.9 MB (7874356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5660ca481d1c336f58d2be80116f5997a9d579d67fc5b555f7f4ba496492b0f`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 392.1 KB (392103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f3e31d4f81d299470bc7f6d7d37028f4b6ad8ace7908f485418f3e8d59295c`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 76.2 KB (76244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dec924dd56ef5930d17c10379cb5267ce7678351ec26f9611ad50dfb9e2143`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a58ade298ff5c2b3c13c00cf8f99be03638408f81549660d5a40b2738f4eed`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 96.5 MB (96545784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a205d842ecb203d13a8861aee1278f11a1d1660310bee6de158831af8cf9893`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dd0d9ec0677277ec17473d6196aa874752c0dbcbd89a42ad52cb4c97fa7158`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e00cd59bccdf60a1b95275cc9dd1339c9bd66e032aa967595a02b02486c20`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd52ab77a219e9f845b3e8f52fa6a39f50281c404945b5e2c4e2af6845b3f0fc`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:61b816fb879f153801f5a0c57aa993509b1ddeb686aeb5fbb95772b4741999a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9d29d794d3d88f48a7d639394be30fbf04023331df77c876d795635af8c0ba`

```dockerfile
```

-	Layers:
	-	`sha256:f4df39bfb7fd657b3ad306503d6702ddc66a7db94de70989483c56cc916466e6`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 3.9 MB (3930860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3385f28de0725f1a6b2ca0be504c7563e084956d3a20dad36f869c51b54a16a`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 31.6 KB (31650 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d532c77f5ac3c2c7675c72630156a513c493e22b8c9bbe9daa3a0539371d94dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133500812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab807e6cce1147b09eb22518b32dfef9270a0f8eb876d6bf35a419d49bfe7db0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.4.1
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158aa9f5c882b5e97fedccc7ae2049826daac1ea4cd80673760c600f66fd25a2`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d0ed31128e494cabd8bf247a75c16916b3384b4ab343f5ca57f7a4a5c953e6`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 7.7 MB (7653591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b763c74cd503a2c115563fbcf3749f7acae5cb7f4747419b2fde045c42d753b`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32407ed42108ffc45dee617bf1da018fce735f15f99b1f7962bf70bc0ca583eb`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 76.2 KB (76229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce8a6203d191d77248cf4554ff76784f28da8ac19de6aae41eff2d3bc095840`  
		Last Modified: Thu, 17 Oct 2024 08:36:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95debc0adb7a8e663736a87a597d945f03b94f5280ee118a162dddf607e45b2c`  
		Last Modified: Thu, 17 Oct 2024 08:36:04 GMT  
		Size: 96.3 MB (96260311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1fdd486e3f558abe65e4b0a5b05fbff273d9926485276b3b9df1dfa01e761b`  
		Last Modified: Thu, 17 Oct 2024 08:36:01 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cde81be4cd034590b1a74c01b8a0f94dfee7a2217d7978d3012614d8a8eb28f`  
		Last Modified: Thu, 17 Oct 2024 08:36:01 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f683798cdb6c2dce7873c45876d80a823f105a215febe6e1c82c5c9fa6c3a88`  
		Last Modified: Thu, 17 Oct 2024 08:36:02 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d986906d69fe681104b8db126b7fd15f16cf51cff824e890f5fccc52b213f06`  
		Last Modified: Thu, 17 Oct 2024 08:36:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:d7f4626f764d1b2f2094fb77be6f4894f41a84c53f2ebbd57085bce4368b8f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb6d5a2b4f152a8d857f93528f0f22bbafcc4f75ecd2e59e332023bddb330e8`

```dockerfile
```

-	Layers:
	-	`sha256:97415988cfb8af055a7f756eae5fa6f43d806f969e10ba2d36c980820f9c3d2c`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 3.9 MB (3931152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36aaab4a230db2e84c0718ade07b3dca1336179cc9a3be83c0e732fd44980b3c`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 31.8 KB (31837 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:99de95bf542240cee02bfa5fc60965c31e4a314507d01e18366bdbb610815aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130484580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d98d0c40506661ca51e78c8cae140fec1d459a9e14020ea458d999d88109da`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.4.1
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365969b4631a62e6d7ef499c6b92905c6fa0d70d6a10749efb8e580b5256cfd3`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4ed4afe5f3bbc527fe4b796a3de285fe49d0da533ff237867f3aca6a5968b8`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 7.4 MB (7387059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b12de2ec74a1377b65c5c729ade5d41b78260a3db246c3df9020d2b33010cd`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 355.6 KB (355620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7328de8b8ca2116e01c13afc0eab1a28fb3f64e8a439112d3b20bc4703589bb7`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 76.3 KB (76311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0cf44eaa7e71276c2479f79c743522f24452594342ff154a1755e85865733b`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1512147a7c60623082fa331b1c2b902d9e080d473ee279c2462b34dd7b7712`  
		Last Modified: Thu, 17 Oct 2024 05:22:44 GMT  
		Size: 95.2 MB (95170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b463db19e955485f17688807e3d553f2786b99d74243b5acc59e19d551604246`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab9c80c3a4eabf87a27abb1049f1ddb895c0df87a965c087d4c34b4bbb4bb8`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c2eec10bfc0129f41384dc5144e0ca5630f5392256c2746bdb8d25af26777c`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7248aa17d2b0e8fde84ae6e445ef95b3472fc45975c316fc0a55b3a26a9509`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:4bb4b10c15d697d4356a10857d75b4368a3027b2156fa2861211c365b65d6000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a297875db8cd9f3393bcfcc2fb2684bf3304d003e7a31c25bb1b1f6705d8076`

```dockerfile
```

-	Layers:
	-	`sha256:d684d396e8b38252eed69b47ac07e532144b2fd5c47cade9f13d255436200b71`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 3.9 MB (3930054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598ec2df229033220609d31a9166e652336f64b8b89eb737110ff684b29d78a7`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 31.6 KB (31650 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:c8e6e619045e67b6f614ba41e24923a53b9a87e5b850ee0f0a832afeffb7ca31
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
$ docker pull couchdb@sha256:69201663158ef27cebf3754503b99930fd9fcba11b9ddca4004fb9ebab880526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156247349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c79aa53ba986a9a9f2923dcff657045fbfeba8b0df43c45b018df4c6b7a175`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8341a5170e640ab064934f5a16b9ddda0d977e75c8a35a2c0a21624175ff7d55`  
		Last Modified: Thu, 17 Oct 2024 01:13:58 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d614eb0dffb75053d727b3da4345cc10290bedde0592ab11da569f1303d25e1c`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 7.9 MB (7874325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f47713982a4618c995e645c57ccd25e4bb1a82c7f599781d74ac8beb173c91c`  
		Last Modified: Thu, 17 Oct 2024 01:14:01 GMT  
		Size: 77.2 MB (77212293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b504ad20a2b123b7701b91d47c94fca132bd9b7b0d87a62c98ffe3b0fba7961f`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 414.9 KB (414915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc4abaaed860931f8316e29ccaa1e28fb973cf3465f80a72c6bd229418a1b4`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 99.2 KB (99225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3963ff4981167fb6541aa9d61cf3ca5ceea815cc334f709d7ba28bc35c5664c`  
		Last Modified: Thu, 17 Oct 2024 01:14:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d533960cb845281574aa500cd0664a7af2ff3a0d6f0375b9cec594d6c2dbef`  
		Last Modified: Thu, 17 Oct 2024 01:14:02 GMT  
		Size: 41.5 MB (41518425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25cdd0790b455c2f406f8cc76c546a18ae0c354a7cef553c69bd5e3474d2640`  
		Last Modified: Thu, 17 Oct 2024 01:14:00 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:73f91e3d4325120c083b80a024abe041b6d609fe89dab2f33f1af4ca0acba313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3478701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17bd9c4df629543404caa7974aa89adc67ba197f9468d81ede57cf02ff55e70d`

```dockerfile
```

-	Layers:
	-	`sha256:8db47e984c370964cf9a1fe7f608b95199bacd19bd67b8ac7599931763c3f615`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 3.5 MB (3454275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85194621739adfae301dd10b86700352c70ef6325d11a0fc4591cd7625a2c41`  
		Last Modified: Thu, 17 Oct 2024 01:13:58 GMT  
		Size: 24.4 KB (24426 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8a5b77c7118d220a61071998d224249d041f9f74083eb8f3591fbe9ceef936fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155210795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b353a401f166bb68e575bfd822646a3608e820cc4231fa13464b0683e3e985`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23dade21ddc63b42d2647ee5bd298a2ef267e5acab231c2d6da080d9d71e6e`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfb43d3130dea5b226ee6d3d7a89a1a039708a27401ad55338f9509583bed31`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 7.7 MB (7653601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e5d718c0a45301c947c0bca060f0ef28d7c83043355da9e77a0804f831f46c`  
		Last Modified: Thu, 17 Oct 2024 08:37:10 GMT  
		Size: 76.5 MB (76508581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7eece477d75c7f105fdd604598ed02f5b1068a219cbe58a2229256b9893b5d3`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 371.7 KB (371682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbcc8c872a854268b654cdb819597d6728167612a8a56425d398b2fe641fb`  
		Last Modified: Thu, 17 Oct 2024 08:37:09 GMT  
		Size: 99.2 KB (99198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e6bc749445a8325728ef17a17221250d734e41f3062355d62748a56c7fc33b`  
		Last Modified: Thu, 17 Oct 2024 08:37:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e94d56078b2aa7190091ad8d91efea53f6653876edd7f1f68acc5f36cb423c`  
		Last Modified: Thu, 17 Oct 2024 08:37:10 GMT  
		Size: 41.4 MB (41419520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198e8ef17bfe3703c4efccfe17c5f2e1f4beb2d8e1ca32ea4636edadc5e16b4b`  
		Last Modified: Thu, 17 Oct 2024 08:37:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:655485c5c80e437b211a9b7f0151c0b8459ae590de744b1eab9fc57d195b3ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3477550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d47175e6d8e0f3339c0bef4902b5f78f1161136c89714e9a9f55dc66212e2`

```dockerfile
```

-	Layers:
	-	`sha256:13a60c99d849a0e9a27b5590f5fd975c20c879523ee7a6ca32fed3c2420d6981`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 3.5 MB (3452948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dec208ef53f3f257d00c26a0de0714575dc0ed04a9ee0900349e84366c9cccaf`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 24.6 KB (24602 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:34e4e127c5f9ef485fade28d3f311f0e0c6cbc12a7c2af25afdb08d9c4d4caaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149594813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b07f083ecd69500e12739cee0bfb3d845466964e509d5554f6a5f49be3396e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1da9e475f448a5faef36ac7b6cb60c0ad8ce9821f2cbaa18d4ee80f33bb576e`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca823418cdd443363165feda244a9e4293b99d5a5ac44d9df8a9ca407b4e094a`  
		Last Modified: Thu, 17 Oct 2024 05:24:06 GMT  
		Size: 7.4 MB (7387056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74513d24c6f38678360078dd599c83f6bc450d3c4cc8a46592c568a62d65b05c`  
		Last Modified: Thu, 17 Oct 2024 05:24:07 GMT  
		Size: 73.0 MB (72987699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85ee38c5a5951cf9fc20bccabb755a2a8d30f1b5fac51d652db2480d4a66777`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 378.1 KB (378063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2b747794ac6e71d08c738e803fc7a9e53a96be7f4b2da17fc311c92665edc0`  
		Last Modified: Thu, 17 Oct 2024 05:24:06 GMT  
		Size: 99.3 KB (99349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a453eab34057d928b0e5ff72f73999ad46c3263d20fa80d54147d243cf941591`  
		Last Modified: Thu, 17 Oct 2024 05:24:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344df0ea4b3986556ab2689e47053d6f23aafb0939e455160a615261744c971e`  
		Last Modified: Thu, 17 Oct 2024 05:24:07 GMT  
		Size: 41.3 MB (41250686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077039b4df922fb240063f1a67223bc9406740c5e13ae052c295261ab50c2533`  
		Last Modified: Thu, 17 Oct 2024 05:24:07 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a7c98572f2af51d20a27ac5ecd3d8a1ae45d8bc53fad772fd172b9a519e43393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3472219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbcbfc99f19034f187721f94a407d269357eeb33e8f3b50f38cf08be226de3b`

```dockerfile
```

-	Layers:
	-	`sha256:1357a127db355bdd98ee39a75190cb56b6661faef478e43e331e35c51fb8686e`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 3.4 MB (3447794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85650d43777473290fad1f06db62d0cc4ac3f2ad81e6cdd6f3538051ab7ca92e`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 24.4 KB (24425 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.1`

```console
$ docker pull couchdb@sha256:4364560362da99f250e4a8d560bc1806cd8aeb1bbf7e42195de8b2e9d11b53d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.1` - linux; amd64

```console
$ docker pull couchdb@sha256:029c957c6085831c1b3c871c48a22c0e618696ffe913324d22d9282b0a39b08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134020203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c57cad342da3d09144089b44a33943b580013ac65061b2409edd8821fb7ce3d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.4.1
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e42c379dbed7e01471433a483c15b1d996c5ed3d430105b68689a9c215e800`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32107ac5bd299153711b495ceeff557b8a64aaae2fb9c160d17d05fadb80df3a`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 7.9 MB (7874356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5660ca481d1c336f58d2be80116f5997a9d579d67fc5b555f7f4ba496492b0f`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 392.1 KB (392103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f3e31d4f81d299470bc7f6d7d37028f4b6ad8ace7908f485418f3e8d59295c`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 76.2 KB (76244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dec924dd56ef5930d17c10379cb5267ce7678351ec26f9611ad50dfb9e2143`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a58ade298ff5c2b3c13c00cf8f99be03638408f81549660d5a40b2738f4eed`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 96.5 MB (96545784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a205d842ecb203d13a8861aee1278f11a1d1660310bee6de158831af8cf9893`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dd0d9ec0677277ec17473d6196aa874752c0dbcbd89a42ad52cb4c97fa7158`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e00cd59bccdf60a1b95275cc9dd1339c9bd66e032aa967595a02b02486c20`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd52ab77a219e9f845b3e8f52fa6a39f50281c404945b5e2c4e2af6845b3f0fc`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:61b816fb879f153801f5a0c57aa993509b1ddeb686aeb5fbb95772b4741999a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9d29d794d3d88f48a7d639394be30fbf04023331df77c876d795635af8c0ba`

```dockerfile
```

-	Layers:
	-	`sha256:f4df39bfb7fd657b3ad306503d6702ddc66a7db94de70989483c56cc916466e6`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 3.9 MB (3930860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3385f28de0725f1a6b2ca0be504c7563e084956d3a20dad36f869c51b54a16a`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 31.6 KB (31650 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d532c77f5ac3c2c7675c72630156a513c493e22b8c9bbe9daa3a0539371d94dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133500812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab807e6cce1147b09eb22518b32dfef9270a0f8eb876d6bf35a419d49bfe7db0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.4.1
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158aa9f5c882b5e97fedccc7ae2049826daac1ea4cd80673760c600f66fd25a2`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d0ed31128e494cabd8bf247a75c16916b3384b4ab343f5ca57f7a4a5c953e6`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 7.7 MB (7653591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b763c74cd503a2c115563fbcf3749f7acae5cb7f4747419b2fde045c42d753b`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32407ed42108ffc45dee617bf1da018fce735f15f99b1f7962bf70bc0ca583eb`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 76.2 KB (76229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce8a6203d191d77248cf4554ff76784f28da8ac19de6aae41eff2d3bc095840`  
		Last Modified: Thu, 17 Oct 2024 08:36:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95debc0adb7a8e663736a87a597d945f03b94f5280ee118a162dddf607e45b2c`  
		Last Modified: Thu, 17 Oct 2024 08:36:04 GMT  
		Size: 96.3 MB (96260311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1fdd486e3f558abe65e4b0a5b05fbff273d9926485276b3b9df1dfa01e761b`  
		Last Modified: Thu, 17 Oct 2024 08:36:01 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cde81be4cd034590b1a74c01b8a0f94dfee7a2217d7978d3012614d8a8eb28f`  
		Last Modified: Thu, 17 Oct 2024 08:36:01 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f683798cdb6c2dce7873c45876d80a823f105a215febe6e1c82c5c9fa6c3a88`  
		Last Modified: Thu, 17 Oct 2024 08:36:02 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d986906d69fe681104b8db126b7fd15f16cf51cff824e890f5fccc52b213f06`  
		Last Modified: Thu, 17 Oct 2024 08:36:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:d7f4626f764d1b2f2094fb77be6f4894f41a84c53f2ebbd57085bce4368b8f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb6d5a2b4f152a8d857f93528f0f22bbafcc4f75ecd2e59e332023bddb330e8`

```dockerfile
```

-	Layers:
	-	`sha256:97415988cfb8af055a7f756eae5fa6f43d806f969e10ba2d36c980820f9c3d2c`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 3.9 MB (3931152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36aaab4a230db2e84c0718ade07b3dca1336179cc9a3be83c0e732fd44980b3c`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 31.8 KB (31837 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.1` - linux; s390x

```console
$ docker pull couchdb@sha256:99de95bf542240cee02bfa5fc60965c31e4a314507d01e18366bdbb610815aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130484580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d98d0c40506661ca51e78c8cae140fec1d459a9e14020ea458d999d88109da`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.4.1
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365969b4631a62e6d7ef499c6b92905c6fa0d70d6a10749efb8e580b5256cfd3`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4ed4afe5f3bbc527fe4b796a3de285fe49d0da533ff237867f3aca6a5968b8`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 7.4 MB (7387059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b12de2ec74a1377b65c5c729ade5d41b78260a3db246c3df9020d2b33010cd`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 355.6 KB (355620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7328de8b8ca2116e01c13afc0eab1a28fb3f64e8a439112d3b20bc4703589bb7`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 76.3 KB (76311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0cf44eaa7e71276c2479f79c743522f24452594342ff154a1755e85865733b`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1512147a7c60623082fa331b1c2b902d9e080d473ee279c2462b34dd7b7712`  
		Last Modified: Thu, 17 Oct 2024 05:22:44 GMT  
		Size: 95.2 MB (95170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b463db19e955485f17688807e3d553f2786b99d74243b5acc59e19d551604246`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab9c80c3a4eabf87a27abb1049f1ddb895c0df87a965c087d4c34b4bbb4bb8`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c2eec10bfc0129f41384dc5144e0ca5630f5392256c2746bdb8d25af26777c`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7248aa17d2b0e8fde84ae6e445ef95b3472fc45975c316fc0a55b3a26a9509`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:4bb4b10c15d697d4356a10857d75b4368a3027b2156fa2861211c365b65d6000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a297875db8cd9f3393bcfcc2fb2684bf3304d003e7a31c25bb1b1f6705d8076`

```dockerfile
```

-	Layers:
	-	`sha256:d684d396e8b38252eed69b47ac07e532144b2fd5c47cade9f13d255436200b71`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 3.9 MB (3930054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598ec2df229033220609d31a9166e652336f64b8b89eb737110ff684b29d78a7`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 31.6 KB (31650 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.1-nouveau`

```console
$ docker pull couchdb@sha256:c8e6e619045e67b6f614ba41e24923a53b9a87e5b850ee0f0a832afeffb7ca31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.1-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:69201663158ef27cebf3754503b99930fd9fcba11b9ddca4004fb9ebab880526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156247349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c79aa53ba986a9a9f2923dcff657045fbfeba8b0df43c45b018df4c6b7a175`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8341a5170e640ab064934f5a16b9ddda0d977e75c8a35a2c0a21624175ff7d55`  
		Last Modified: Thu, 17 Oct 2024 01:13:58 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d614eb0dffb75053d727b3da4345cc10290bedde0592ab11da569f1303d25e1c`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 7.9 MB (7874325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f47713982a4618c995e645c57ccd25e4bb1a82c7f599781d74ac8beb173c91c`  
		Last Modified: Thu, 17 Oct 2024 01:14:01 GMT  
		Size: 77.2 MB (77212293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b504ad20a2b123b7701b91d47c94fca132bd9b7b0d87a62c98ffe3b0fba7961f`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 414.9 KB (414915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc4abaaed860931f8316e29ccaa1e28fb973cf3465f80a72c6bd229418a1b4`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 99.2 KB (99225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3963ff4981167fb6541aa9d61cf3ca5ceea815cc334f709d7ba28bc35c5664c`  
		Last Modified: Thu, 17 Oct 2024 01:14:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d533960cb845281574aa500cd0664a7af2ff3a0d6f0375b9cec594d6c2dbef`  
		Last Modified: Thu, 17 Oct 2024 01:14:02 GMT  
		Size: 41.5 MB (41518425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25cdd0790b455c2f406f8cc76c546a18ae0c354a7cef553c69bd5e3474d2640`  
		Last Modified: Thu, 17 Oct 2024 01:14:00 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:73f91e3d4325120c083b80a024abe041b6d609fe89dab2f33f1af4ca0acba313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3478701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17bd9c4df629543404caa7974aa89adc67ba197f9468d81ede57cf02ff55e70d`

```dockerfile
```

-	Layers:
	-	`sha256:8db47e984c370964cf9a1fe7f608b95199bacd19bd67b8ac7599931763c3f615`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 3.5 MB (3454275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85194621739adfae301dd10b86700352c70ef6325d11a0fc4591cd7625a2c41`  
		Last Modified: Thu, 17 Oct 2024 01:13:58 GMT  
		Size: 24.4 KB (24426 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.1-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8a5b77c7118d220a61071998d224249d041f9f74083eb8f3591fbe9ceef936fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155210795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b353a401f166bb68e575bfd822646a3608e820cc4231fa13464b0683e3e985`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23dade21ddc63b42d2647ee5bd298a2ef267e5acab231c2d6da080d9d71e6e`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfb43d3130dea5b226ee6d3d7a89a1a039708a27401ad55338f9509583bed31`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 7.7 MB (7653601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e5d718c0a45301c947c0bca060f0ef28d7c83043355da9e77a0804f831f46c`  
		Last Modified: Thu, 17 Oct 2024 08:37:10 GMT  
		Size: 76.5 MB (76508581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7eece477d75c7f105fdd604598ed02f5b1068a219cbe58a2229256b9893b5d3`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 371.7 KB (371682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbcc8c872a854268b654cdb819597d6728167612a8a56425d398b2fe641fb`  
		Last Modified: Thu, 17 Oct 2024 08:37:09 GMT  
		Size: 99.2 KB (99198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e6bc749445a8325728ef17a17221250d734e41f3062355d62748a56c7fc33b`  
		Last Modified: Thu, 17 Oct 2024 08:37:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e94d56078b2aa7190091ad8d91efea53f6653876edd7f1f68acc5f36cb423c`  
		Last Modified: Thu, 17 Oct 2024 08:37:10 GMT  
		Size: 41.4 MB (41419520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198e8ef17bfe3703c4efccfe17c5f2e1f4beb2d8e1ca32ea4636edadc5e16b4b`  
		Last Modified: Thu, 17 Oct 2024 08:37:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:655485c5c80e437b211a9b7f0151c0b8459ae590de744b1eab9fc57d195b3ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3477550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d47175e6d8e0f3339c0bef4902b5f78f1161136c89714e9a9f55dc66212e2`

```dockerfile
```

-	Layers:
	-	`sha256:13a60c99d849a0e9a27b5590f5fd975c20c879523ee7a6ca32fed3c2420d6981`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 3.5 MB (3452948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dec208ef53f3f257d00c26a0de0714575dc0ed04a9ee0900349e84366c9cccaf`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 24.6 KB (24602 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.1-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:34e4e127c5f9ef485fade28d3f311f0e0c6cbc12a7c2af25afdb08d9c4d4caaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149594813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b07f083ecd69500e12739cee0bfb3d845466964e509d5554f6a5f49be3396e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1da9e475f448a5faef36ac7b6cb60c0ad8ce9821f2cbaa18d4ee80f33bb576e`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca823418cdd443363165feda244a9e4293b99d5a5ac44d9df8a9ca407b4e094a`  
		Last Modified: Thu, 17 Oct 2024 05:24:06 GMT  
		Size: 7.4 MB (7387056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74513d24c6f38678360078dd599c83f6bc450d3c4cc8a46592c568a62d65b05c`  
		Last Modified: Thu, 17 Oct 2024 05:24:07 GMT  
		Size: 73.0 MB (72987699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85ee38c5a5951cf9fc20bccabb755a2a8d30f1b5fac51d652db2480d4a66777`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 378.1 KB (378063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2b747794ac6e71d08c738e803fc7a9e53a96be7f4b2da17fc311c92665edc0`  
		Last Modified: Thu, 17 Oct 2024 05:24:06 GMT  
		Size: 99.3 KB (99349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a453eab34057d928b0e5ff72f73999ad46c3263d20fa80d54147d243cf941591`  
		Last Modified: Thu, 17 Oct 2024 05:24:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344df0ea4b3986556ab2689e47053d6f23aafb0939e455160a615261744c971e`  
		Last Modified: Thu, 17 Oct 2024 05:24:07 GMT  
		Size: 41.3 MB (41250686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077039b4df922fb240063f1a67223bc9406740c5e13ae052c295261ab50c2533`  
		Last Modified: Thu, 17 Oct 2024 05:24:07 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a7c98572f2af51d20a27ac5ecd3d8a1ae45d8bc53fad772fd172b9a519e43393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3472219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbcbfc99f19034f187721f94a407d269357eeb33e8f3b50f38cf08be226de3b`

```dockerfile
```

-	Layers:
	-	`sha256:1357a127db355bdd98ee39a75190cb56b6661faef478e43e331e35c51fb8686e`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 3.4 MB (3447794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85650d43777473290fad1f06db62d0cc4ac3f2ad81e6cdd6f3538051ab7ca92e`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 24.4 KB (24425 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:4364560362da99f250e4a8d560bc1806cd8aeb1bbf7e42195de8b2e9d11b53d2
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
$ docker pull couchdb@sha256:029c957c6085831c1b3c871c48a22c0e618696ffe913324d22d9282b0a39b08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134020203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c57cad342da3d09144089b44a33943b580013ac65061b2409edd8821fb7ce3d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.4.1
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e42c379dbed7e01471433a483c15b1d996c5ed3d430105b68689a9c215e800`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32107ac5bd299153711b495ceeff557b8a64aaae2fb9c160d17d05fadb80df3a`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 7.9 MB (7874356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5660ca481d1c336f58d2be80116f5997a9d579d67fc5b555f7f4ba496492b0f`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 392.1 KB (392103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f3e31d4f81d299470bc7f6d7d37028f4b6ad8ace7908f485418f3e8d59295c`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 76.2 KB (76244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dec924dd56ef5930d17c10379cb5267ce7678351ec26f9611ad50dfb9e2143`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a58ade298ff5c2b3c13c00cf8f99be03638408f81549660d5a40b2738f4eed`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 96.5 MB (96545784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a205d842ecb203d13a8861aee1278f11a1d1660310bee6de158831af8cf9893`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dd0d9ec0677277ec17473d6196aa874752c0dbcbd89a42ad52cb4c97fa7158`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e00cd59bccdf60a1b95275cc9dd1339c9bd66e032aa967595a02b02486c20`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd52ab77a219e9f845b3e8f52fa6a39f50281c404945b5e2c4e2af6845b3f0fc`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:61b816fb879f153801f5a0c57aa993509b1ddeb686aeb5fbb95772b4741999a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9d29d794d3d88f48a7d639394be30fbf04023331df77c876d795635af8c0ba`

```dockerfile
```

-	Layers:
	-	`sha256:f4df39bfb7fd657b3ad306503d6702ddc66a7db94de70989483c56cc916466e6`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 3.9 MB (3930860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3385f28de0725f1a6b2ca0be504c7563e084956d3a20dad36f869c51b54a16a`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 31.6 KB (31650 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d532c77f5ac3c2c7675c72630156a513c493e22b8c9bbe9daa3a0539371d94dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133500812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab807e6cce1147b09eb22518b32dfef9270a0f8eb876d6bf35a419d49bfe7db0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.4.1
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158aa9f5c882b5e97fedccc7ae2049826daac1ea4cd80673760c600f66fd25a2`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d0ed31128e494cabd8bf247a75c16916b3384b4ab343f5ca57f7a4a5c953e6`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 7.7 MB (7653591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b763c74cd503a2c115563fbcf3749f7acae5cb7f4747419b2fde045c42d753b`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32407ed42108ffc45dee617bf1da018fce735f15f99b1f7962bf70bc0ca583eb`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 76.2 KB (76229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce8a6203d191d77248cf4554ff76784f28da8ac19de6aae41eff2d3bc095840`  
		Last Modified: Thu, 17 Oct 2024 08:36:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95debc0adb7a8e663736a87a597d945f03b94f5280ee118a162dddf607e45b2c`  
		Last Modified: Thu, 17 Oct 2024 08:36:04 GMT  
		Size: 96.3 MB (96260311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1fdd486e3f558abe65e4b0a5b05fbff273d9926485276b3b9df1dfa01e761b`  
		Last Modified: Thu, 17 Oct 2024 08:36:01 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cde81be4cd034590b1a74c01b8a0f94dfee7a2217d7978d3012614d8a8eb28f`  
		Last Modified: Thu, 17 Oct 2024 08:36:01 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f683798cdb6c2dce7873c45876d80a823f105a215febe6e1c82c5c9fa6c3a88`  
		Last Modified: Thu, 17 Oct 2024 08:36:02 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d986906d69fe681104b8db126b7fd15f16cf51cff824e890f5fccc52b213f06`  
		Last Modified: Thu, 17 Oct 2024 08:36:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:d7f4626f764d1b2f2094fb77be6f4894f41a84c53f2ebbd57085bce4368b8f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb6d5a2b4f152a8d857f93528f0f22bbafcc4f75ecd2e59e332023bddb330e8`

```dockerfile
```

-	Layers:
	-	`sha256:97415988cfb8af055a7f756eae5fa6f43d806f969e10ba2d36c980820f9c3d2c`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 3.9 MB (3931152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36aaab4a230db2e84c0718ade07b3dca1336179cc9a3be83c0e732fd44980b3c`  
		Last Modified: Thu, 17 Oct 2024 08:36:00 GMT  
		Size: 31.8 KB (31837 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:99de95bf542240cee02bfa5fc60965c31e4a314507d01e18366bdbb610815aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130484580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d98d0c40506661ca51e78c8cae140fec1d459a9e14020ea458d999d88109da`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.4.1
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365969b4631a62e6d7ef499c6b92905c6fa0d70d6a10749efb8e580b5256cfd3`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4ed4afe5f3bbc527fe4b796a3de285fe49d0da533ff237867f3aca6a5968b8`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 7.4 MB (7387059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b12de2ec74a1377b65c5c729ade5d41b78260a3db246c3df9020d2b33010cd`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 355.6 KB (355620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7328de8b8ca2116e01c13afc0eab1a28fb3f64e8a439112d3b20bc4703589bb7`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 76.3 KB (76311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0cf44eaa7e71276c2479f79c743522f24452594342ff154a1755e85865733b`  
		Last Modified: Thu, 17 Oct 2024 05:22:42 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1512147a7c60623082fa331b1c2b902d9e080d473ee279c2462b34dd7b7712`  
		Last Modified: Thu, 17 Oct 2024 05:22:44 GMT  
		Size: 95.2 MB (95170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b463db19e955485f17688807e3d553f2786b99d74243b5acc59e19d551604246`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab9c80c3a4eabf87a27abb1049f1ddb895c0df87a965c087d4c34b4bbb4bb8`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c2eec10bfc0129f41384dc5144e0ca5630f5392256c2746bdb8d25af26777c`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7248aa17d2b0e8fde84ae6e445ef95b3472fc45975c316fc0a55b3a26a9509`  
		Last Modified: Thu, 17 Oct 2024 05:22:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:4bb4b10c15d697d4356a10857d75b4368a3027b2156fa2861211c365b65d6000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a297875db8cd9f3393bcfcc2fb2684bf3304d003e7a31c25bb1b1f6705d8076`

```dockerfile
```

-	Layers:
	-	`sha256:d684d396e8b38252eed69b47ac07e532144b2fd5c47cade9f13d255436200b71`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 3.9 MB (3930054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598ec2df229033220609d31a9166e652336f64b8b89eb737110ff684b29d78a7`  
		Last Modified: Thu, 17 Oct 2024 05:22:41 GMT  
		Size: 31.6 KB (31650 bytes)  
		MIME: application/vnd.in-toto+json
