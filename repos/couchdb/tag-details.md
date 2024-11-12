<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3-nouveau`](#couchdb3-nouveau)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.3`](#couchdb333)
-	[`couchdb:3.4`](#couchdb34)
-	[`couchdb:3.4-nouveau`](#couchdb34-nouveau)
-	[`couchdb:3.4.2`](#couchdb342)
-	[`couchdb:3.4.2-nouveau`](#couchdb342-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:dd206b5c289dbe7ba3ff342e39eccebc74f8afac7ee2ec0567a7a4a131b9cb5b
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
$ docker pull couchdb@sha256:735194fe77a88d69ece21773709de5e22ca7f28c8468f71da05e659ff86951d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134139677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312a55065e927c2cd676e805ae872a95e9c1fa0fbf4bf655d8f003f3c7ae852a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81cd93b18f135ee83d01825f7fecacb7acae18cf0d229e41220d3d49e28f692`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2aa1fb55da0c568713a1a0b85fe7539f2aa956a0bedbe284613ea5234dc445`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 7.9 MB (7874852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff34e1414bc986bde3827be21e31cede390993e86aa8ef856e3194767f3577c0`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 392.1 KB (392111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562d6125a85f0529c429ac34462074bb35b2f00733461bdadf11301b8d648cc`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 76.2 KB (76250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda7a7f53d0e57963e34090515de7e93e6151bb506b2da694e47150c7cfae384`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d512b93b61e418f09435b41ccf4612603c67e4f5c28376fa3a9bf8034e4fbba`  
		Last Modified: Tue, 12 Nov 2024 02:39:13 GMT  
		Size: 96.7 MB (96663033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cde1e5d5956ad76d0d22369ceb1503c3131d9ff104426eb3eb4652945d309e9`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48486363b9474121ca8e42d62b0561bbd47ac5abb83b56c03c5e296ae74238ec`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec83637f971083de2400a03e5d9eff95716ec4b1d0af0f47e619452ec48a395d`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82a9780025224aa7cb7ffa559df8831056735aa215867045cab4e3ce0dcbe6a`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f20b0e2adfd17adc82aa26af449f1177143837be66e45839ca55314b1af560c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7e559b9ad69bd91a0ace8d1e2989c2097fdfa799bdc87c735f295f292aa6a2`

```dockerfile
```

-	Layers:
	-	`sha256:1064d94b48b9794c4a9887de837a799ab1231f6637f838215965a040f745164e`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 3.9 MB (3947737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26a2e846657e24c19a12b74cef4d37fde9d8d68660e1720e05c16700bfa17c82`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b2995ca89617544e541a332918fdd5243da4b5e54d9b77fb594dedae30f6a2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133638613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13e25a8bdd5774de422c04b98fc3ac1b69be888f1ef1fc1a47345ae8551698c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
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
	-	`sha256:15ffe618b033b4cd957befd97c090e2ece69ba792eb50e7a710734587d3141ea`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 76.3 KB (76262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f91c9c6b0683e3a96e4228c48d706874dffa44389ae94c2b6679aaef55b85f`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62cce859844c9a8fe1704dc59e7539523fefd202b2cacdec2bd757df0eea342`  
		Last Modified: Tue, 22 Oct 2024 22:55:57 GMT  
		Size: 96.4 MB (96398076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67993a95c4192b1274b87d5f130e9826a50023a7ba60c78474bb7dcefce3d126`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91773508b70d1f9fd2cdb934a74173bf644abfa96a26ea5d7de35fa12c4090a`  
		Last Modified: Tue, 22 Oct 2024 22:55:55 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a66bdc41b21c8d8ae45d87f56ec64849164a3337c5b54cc0855e812cb7001b`  
		Last Modified: Tue, 22 Oct 2024 22:55:55 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d1ba095cb793f07ef398d83f3308c03d7846cb8e8c97d0f57e42c23d9b0f51`  
		Last Modified: Tue, 22 Oct 2024 22:55:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:904718ac7d1fca26ea2dd54906b9f636224116cbeaa42b6229af8e7a6560ae34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134564f44d44ede2ce6aa419fb3aa433137281031166eca45c4eef6e87572236`

```dockerfile
```

-	Layers:
	-	`sha256:4895539c4b106ad364b2786dd58436e5316426e2af8d577a7078549fdd0029c9`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 3.9 MB (3947993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e99a926b4b8b5d5d3c4e80bf549231a7f707d38e2b6e534605fcab3241a098ab`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 31.8 KB (31834 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:f9f0636806ae88dc461f067ecfe5d9ee77295559d8c1f9de1644bfec50a3178c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130606174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d64d01efd9a70e0060875698773c915ddc73aafd3a9b488292280e753255a4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe50171c1e31dfa26718c51ddcc5872c8fdab4d3263ebd9f04aef953259ac1d`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500762f13f114e2db6d2c1643551a4df71892f0535589340d8757b5647d5437`  
		Last Modified: Tue, 12 Nov 2024 09:05:27 GMT  
		Size: 7.4 MB (7387904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107b3a2fc5342d18016e7023ebbe69d83faccb03f367cde58071a39b4e1a229f`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 355.6 KB (355612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0b142e1a4e2d652182cdf84958d2c3c82429d95b995c64ec640d8bc34e95fc`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 76.3 KB (76339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e221b4ae713d7a5761e67086113cad325056288809b57598a9ff4cf39c158b8`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2e146630a045cba2bbc843466807f9c849e6f44231f6acacb38ba6925319c`  
		Last Modified: Tue, 12 Nov 2024 09:05:29 GMT  
		Size: 95.3 MB (95289258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db302f5ed06c1cfb54f257e31faf97cbf108f9a78f92bdc76044c0fb91772feb`  
		Last Modified: Tue, 12 Nov 2024 09:05:27 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096c7c90e014802ac9db88baaf9ce1ef8840260977fac85f7b9efc7ef5026321`  
		Last Modified: Tue, 12 Nov 2024 09:05:27 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b0ac698ab8ca1a5afcdc3b6fae173f1765b7eccdb2125872093794446d5e45`  
		Last Modified: Tue, 12 Nov 2024 09:05:28 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40d4bfb167e02369452f7feabdefaaed473eaef02032b619af5298af66605f6`  
		Last Modified: Tue, 12 Nov 2024 09:05:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:23ef435a855c10ead0b1a5d7dd8beef8513b8dd96e2644e7af0953541af17556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3978601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de44b5754f2faafcb5b2ede6b0565797eae9644f96b93a4918baa03cf135589b`

```dockerfile
```

-	Layers:
	-	`sha256:0d3cea293c10382b0d64d7aaaf87d4e5f4a56d04424c5ec656117caec2dc486b`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 3.9 MB (3946825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58c6043f6b03387395ea500ef9e988915eb99335cb71a7b2da7ad9bf50adbe9`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:b3a58a740869d3428cdd85c9da5b7c4dd8e7bdd3e6a47fb800ce1a03013a37f7
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
$ docker pull couchdb@sha256:7d73dd1c6b22690398fd72ff27a25874164de7d806fd9772c4c137cdb2d7980c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156433595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b23780d2087cf211c268ccd827028c5c107a9278082704c4cd701de05ad3248`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3e36b499d69fac410ec13e0e90b60065a5b483078f5d3e2536254423e5222f`  
		Last Modified: Tue, 12 Nov 2024 02:38:58 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a763829d6bfcab12c49dcd6b99fedaee601a9530fdef21eb74787cd2d7bb51`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 7.9 MB (7874861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f566daf2fdaf3790e6e330ee6247a9905d27094c64f025b74bf822ecc1fd00`  
		Last Modified: Tue, 12 Nov 2024 02:39:02 GMT  
		Size: 77.3 MB (77283799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07e481c7742184cdcb01de441e4178ae91c88aa40f42a7f18b94c4c1783c60`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 415.0 KB (414956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0aff5ca936036838c76a8d98fc6b07c79f42bf78110b37f28a3ba34bf970b5`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 99.3 KB (99285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04889d990fb1ce0f1ca9e4b6e4f74f4b76af37331fe91a4e11300b33a6dca558`  
		Last Modified: Tue, 12 Nov 2024 02:39:00 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ee84f15d3c696930742e848143b57371c46d7abfef5b603f149daa53cdac08`  
		Last Modified: Tue, 12 Nov 2024 02:39:02 GMT  
		Size: 41.6 MB (41630822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba664c1772d53c31b6a9bd5cb04686013b55788ee8e6c84c8b3662d9afa76033`  
		Last Modified: Tue, 12 Nov 2024 02:39:01 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5fa80ed1bb4a2513c114fedad9b26e6ded2360a2792c6a566f0574aee8c3068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3499647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a25a7ac49f8a425785a8beda80ee4155187481585517753a83409d9924ed016`

```dockerfile
```

-	Layers:
	-	`sha256:ffa03f762479765e205bfad5e8dd0fbbb0e09ab401ecc2b1ddcd19c70335fdf0`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 3.5 MB (3475085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff075489e5b49cb272d18000416cbb85dad3443e7f28df20fb6e7c5a6a6b4ac4`  
		Last Modified: Tue, 12 Nov 2024 02:38:58 GMT  
		Size: 24.6 KB (24562 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b87d41d8a4dc850c9df23b5e490b0eaf7534cfe9a81c549507cda07de713114a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155393649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1603b44f6c46c1b5e9aec253ff61d9d9f108720c3a74cd92ba52f643eb92595`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
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
	-	`sha256:84a2f199b083cc236d74acc480bc9abac691d493b1b8e8369c9b0d711304a0d0`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 7.7 MB (7653607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8459eb8b4c9964bd391e5d65122d9a6b51597679a46b26371df1aa25c7981230`  
		Last Modified: Tue, 22 Oct 2024 22:57:02 GMT  
		Size: 76.6 MB (76584069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d986d3cb2299ff5e9dcb002b84ed876ae4e141113c44029975f6e0285da4e5`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 371.7 KB (371687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658ba1a93b3f07ccb268aeee3cb247fd401728815cc696750fe4aa47e142d86`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 99.2 KB (99196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa093cddfcef74b5ea9feb12e196ed0de5282e3862fdfbe9388a13a8c3eba4f`  
		Last Modified: Tue, 22 Oct 2024 22:57:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c7071f8700c62ae031ca50097a10bcd1c1e8a1b663bb00a6de3432fd5f37d4`  
		Last Modified: Tue, 22 Oct 2024 22:57:02 GMT  
		Size: 41.5 MB (41526874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d704fde3024b8d5493329ea84940158034a267430e68c3b5fc6aa9b0ac28709b`  
		Last Modified: Tue, 22 Oct 2024 22:57:01 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:8c740bc74395f333b71bbaba633ce42a1d82c5d44247db9146df72b187582fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3498284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b511829792aaf6014b3919f785f3fd3597e0bbd618669e654196b9ef11d97bf8`

```dockerfile
```

-	Layers:
	-	`sha256:4bca8295be7075aaf79068a58523545f2b3f747f8d1182985c8834b17445ba74`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 3.5 MB (3473686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca52556d4416346ade61f88b44b846655e00138f989397d40478b0dc89035e1f`  
		Last Modified: Tue, 22 Oct 2024 22:56:59 GMT  
		Size: 24.6 KB (24598 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2cf915e89a9e7ed739113d095a8950b73929607949cabf2eff1ef4b7803c6866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149773483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879569e9e9cc1c272419476640029f25521bb00c2ba380b5958c1dc029be1e81`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c523130e4b9afa3f91f91c908ce7bc4f919818bc40d287191b5a3a48008e3fb`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2416975d6d48cc012c07fcfbd5d51f3af39ca9368af1cc038631b6e2a62ddac`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 7.4 MB (7387955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e7f35fec5d35bb10e1db7844516ad24ef8c9456d45497b4ea4f2a239ff10c8`  
		Last Modified: Tue, 12 Nov 2024 09:07:06 GMT  
		Size: 73.1 MB (73064505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10eda5ab7a8048646c86d3a8db41209ade88ee1d23079c43f5e5d91d49ab998`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 378.1 KB (378060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea45ee187eaa87421edbca0ee7055ab419db019e9606defb81b285952f0ed3b`  
		Last Modified: Tue, 12 Nov 2024 09:07:05 GMT  
		Size: 99.4 KB (99388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12accd577d35774ab5f9af2f75ceeb8e3f9ad2af5e0e7701ef024fc2e72635`  
		Last Modified: Tue, 12 Nov 2024 09:07:05 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db905cb94dc3cbfa90ea8e0f7851aebccced11b2bd23d61ff9790987b463b84a`  
		Last Modified: Tue, 12 Nov 2024 09:07:06 GMT  
		Size: 41.4 MB (41350067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83197dd55986f200b224d19273beade21655652c6a3d4abb012c7d473e63c80`  
		Last Modified: Tue, 12 Nov 2024 09:07:06 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f1eb394d72eb6e720820031c0904ea5717139e896b9b42facec8e06ce44bc144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc50f5f76af03030c6469294c8cd93184907bccad6e4b6de5d7d5a56f272791`

```dockerfile
```

-	Layers:
	-	`sha256:4de89241136a06eab37c23e3419dcaaf5ac4b40e4ac5c482409665f4e13bb32c`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 3.5 MB (3468498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca29ecebdf667ae3d12fff343bc5f7c661d59455e74a0e728bc967c8c03be581`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:ac2b0e6bd7d0fbaf9e71564c5f0c3b319c8f180020c5020fbc190528853f7f65
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
$ docker pull couchdb@sha256:12b0937e8fa63c0ae232dc9738321f718bdc30b8ce39b123762a3de71a346744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97626440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de771175ec17b2278cd6067afeb8ee2882f957dfaa39111abc68286819313bb3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bae2d3eacccbffc9a3e072c6f7a18d7f4e6621d1156928da18b3d00f0ab17e`  
		Last Modified: Tue, 12 Nov 2024 02:38:55 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950145677ac4761da093349cfda3639bef638985bd755b09aa39967de792187e`  
		Last Modified: Tue, 12 Nov 2024 02:38:56 GMT  
		Size: 7.9 MB (7874876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2954202d7a9fb78588ae681a4fbc7055d6c3ebc0a9a78c0fd98eafd69adbd8ad`  
		Last Modified: Tue, 12 Nov 2024 02:38:55 GMT  
		Size: 392.1 KB (392097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d578d06b2e3ab373b2c3dc46e0f6478b3634cc6e8506c2dc52b74d929fd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:55 GMT  
		Size: 76.2 KB (76245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315f7cf481d0e36a0251e65d13e7b15c80d0fd03be5ef0ccf6c89d45fbd05c7f`  
		Last Modified: Tue, 12 Nov 2024 02:38:56 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12aa09dbb7e966e2fea0fb93a74736e9284c428f3dc488715b37f83d2740e49`  
		Last Modified: Tue, 12 Nov 2024 02:38:58 GMT  
		Size: 60.1 MB (60149800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9651afba4bf16fd09fe0d66ec327cde394c7d8ed9dad5fad7349328e1f4d09a`  
		Last Modified: Tue, 12 Nov 2024 02:38:56 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88e2986cb01320cf67fd33f3c68c3e071b2eb49e48cb126221638d4111d9013`  
		Last Modified: Tue, 12 Nov 2024 02:38:57 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825ce35640c2337f9be7d03c4c8aeafec29c56feee9223801f3470559b8bf699`  
		Last Modified: Tue, 12 Nov 2024 02:38:57 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf1d9e6ebc2613284da866d346d5ed2a4fb99f3d37608e72a7a287db8f0da4e`  
		Last Modified: Tue, 12 Nov 2024 02:38:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d5d9cd6e96a0b08b6302fe5d038b84f1a17cf8ed2fb593a3d56c8183e3cdbb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3771151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc156d4083232872d4f7558591b66484d6c9c698e1084ba0209743c323a44d3b`

```dockerfile
```

-	Layers:
	-	`sha256:6d30df5988b9169b8dbaf1c876d7faab04a1430e95e275c836a11cc57ca860bb`  
		Last Modified: Tue, 12 Nov 2024 02:38:55 GMT  
		Size: 3.7 MB (3739959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52e1d8d5147beb57fef6a0fc41dbe60adf9a6af8e00f33b3bc67ec6a480c44f2`  
		Last Modified: Tue, 12 Nov 2024 02:38:55 GMT  
		Size: 31.2 KB (31192 bytes)  
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
$ docker pull couchdb@sha256:566ad00a547f8cf73ee34234b2e496d3a1963973e487e416ba594b2431d51aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103917264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b853565bb2b3b4ecaeb7acbce0d4e64140783444d7298127aa388110fe94d56e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bb2d0d6a96e0df1e64c6768058ba160ece9975ff41e747051744754a6602ac`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78490fd3e69ce38a495f7047ae8ed194959ec3f187a1ebfc990078722eae4362`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 8.9 MB (8890074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce01cb959b4fd862b60ae9837737c8ae2a0a17ad33e6c5971ac58b7e8068b1fc`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 444.7 KB (444666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c581212b5869c39bf5e3ecfba5232c2e6bd76f5314b89bee947fab2fb08535f`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 76.3 KB (76288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68175198b4e73d464d85218d95d1eb1f61316be8f306012d91e6674ef178c8b6`  
		Last Modified: Tue, 12 Nov 2024 08:32:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b778ca3ac5159edb66416242074844e33086e769010222e9ae5bdbdb8efe66`  
		Last Modified: Tue, 12 Nov 2024 08:32:37 GMT  
		Size: 61.4 MB (61375448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4748275adde2dd6d571701074dee9d145b1826b47736443a7cda4aec44feafe8`  
		Last Modified: Tue, 12 Nov 2024 08:32:35 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb300b001a0b8870a23250ca36ad63779ea1d7680fe6f3e194278916f85a2ca`  
		Last Modified: Tue, 12 Nov 2024 08:32:35 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf6ae42c56873bcbb40d3d2a1a133c74dc5620616b14e4c81ab1e760651ceac`  
		Last Modified: Tue, 12 Nov 2024 08:32:36 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c50f6b7552bd2cfec853bf4223af75fa9da30bab35ce5eab4ea0bcc9bf30393`  
		Last Modified: Tue, 12 Nov 2024 08:32:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ca42a705b9a242c3dc3df7d360d738a6f72b0c876655b2790b0dacd158d6e064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c28cf2c0195d25a74c4a91196a397496dbc660faa89953159ada59907f6c34`

```dockerfile
```

-	Layers:
	-	`sha256:95e9d15956bddda1858f37d80eb7c1da71110ad01af698fdca041f76596c5ffa`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 3.7 MB (3744462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c729809f0ae8c11a05e787e501746039c4f11b2995e85e66e1a94919a87b38c3`  
		Last Modified: Tue, 12 Nov 2024 08:32:33 GMT  
		Size: 31.2 KB (31236 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:bf5b362a5066c3c64f1db3a38f43c828a4aa637dcb9ec4e1c8525623cbbd8e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94057367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a6dc24123b9855a4fae0de010e0613867e6a8dbf37638a6d13890026c809f0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe50171c1e31dfa26718c51ddcc5872c8fdab4d3263ebd9f04aef953259ac1d`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500762f13f114e2db6d2c1643551a4df71892f0535589340d8757b5647d5437`  
		Last Modified: Tue, 12 Nov 2024 09:05:27 GMT  
		Size: 7.4 MB (7387904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107b3a2fc5342d18016e7023ebbe69d83faccb03f367cde58071a39b4e1a229f`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 355.6 KB (355612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0b142e1a4e2d652182cdf84958d2c3c82429d95b995c64ec640d8bc34e95fc`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 76.3 KB (76339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e9e48ad844b84fe43f6a57e37a8c53e3d8c34d917afa03e3b86528f0532ce1`  
		Last Modified: Tue, 12 Nov 2024 09:08:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff424fa0018abe9d7918c3a71437dc38f7dcbe6bed153552e9e32fdcafa108a2`  
		Last Modified: Tue, 12 Nov 2024 09:08:14 GMT  
		Size: 58.7 MB (58740447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4c54f3536f38288f34149dc70062b6306124ba3492537723781404ba20a062`  
		Last Modified: Tue, 12 Nov 2024 09:08:13 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a09211ec3e93b6cd50b47c79da51a21d685211f654c414237de6c205697014`  
		Last Modified: Tue, 12 Nov 2024 09:08:13 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd206433d01baf5a6532f56caf68f688fadc1df7cd3d78e49c7e8bff141e0964`  
		Last Modified: Tue, 12 Nov 2024 09:08:13 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af639272897c6d328a1177edb697f0161b845915f5a2b4e300a8a5fe425122fd`  
		Last Modified: Tue, 12 Nov 2024 09:08:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a4039531e9e3c58dbfb59d4e3039741742db8364f9e99f6259ad5f3c10e6090c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3770239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f558bc6b501ba1b2abdaa1b61e08b7347e532eb265e3524ac6b98e1bb16270`

```dockerfile
```

-	Layers:
	-	`sha256:bd6d7c77b90211a70b5b0f7416b171ddb0a6e4249be269b03d89046d2bbdc5c8`  
		Last Modified: Tue, 12 Nov 2024 09:08:13 GMT  
		Size: 3.7 MB (3739047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675213844c86e53ea37fd1780d87bcdccd176aa8ff1b2aac3d248139b9931b86`  
		Last Modified: Tue, 12 Nov 2024 09:08:12 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:ac2b0e6bd7d0fbaf9e71564c5f0c3b319c8f180020c5020fbc190528853f7f65
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
$ docker pull couchdb@sha256:12b0937e8fa63c0ae232dc9738321f718bdc30b8ce39b123762a3de71a346744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97626440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de771175ec17b2278cd6067afeb8ee2882f957dfaa39111abc68286819313bb3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bae2d3eacccbffc9a3e072c6f7a18d7f4e6621d1156928da18b3d00f0ab17e`  
		Last Modified: Tue, 12 Nov 2024 02:38:55 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950145677ac4761da093349cfda3639bef638985bd755b09aa39967de792187e`  
		Last Modified: Tue, 12 Nov 2024 02:38:56 GMT  
		Size: 7.9 MB (7874876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2954202d7a9fb78588ae681a4fbc7055d6c3ebc0a9a78c0fd98eafd69adbd8ad`  
		Last Modified: Tue, 12 Nov 2024 02:38:55 GMT  
		Size: 392.1 KB (392097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d578d06b2e3ab373b2c3dc46e0f6478b3634cc6e8506c2dc52b74d929fd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:55 GMT  
		Size: 76.2 KB (76245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315f7cf481d0e36a0251e65d13e7b15c80d0fd03be5ef0ccf6c89d45fbd05c7f`  
		Last Modified: Tue, 12 Nov 2024 02:38:56 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12aa09dbb7e966e2fea0fb93a74736e9284c428f3dc488715b37f83d2740e49`  
		Last Modified: Tue, 12 Nov 2024 02:38:58 GMT  
		Size: 60.1 MB (60149800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9651afba4bf16fd09fe0d66ec327cde394c7d8ed9dad5fad7349328e1f4d09a`  
		Last Modified: Tue, 12 Nov 2024 02:38:56 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88e2986cb01320cf67fd33f3c68c3e071b2eb49e48cb126221638d4111d9013`  
		Last Modified: Tue, 12 Nov 2024 02:38:57 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825ce35640c2337f9be7d03c4c8aeafec29c56feee9223801f3470559b8bf699`  
		Last Modified: Tue, 12 Nov 2024 02:38:57 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf1d9e6ebc2613284da866d346d5ed2a4fb99f3d37608e72a7a287db8f0da4e`  
		Last Modified: Tue, 12 Nov 2024 02:38:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d5d9cd6e96a0b08b6302fe5d038b84f1a17cf8ed2fb593a3d56c8183e3cdbb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3771151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc156d4083232872d4f7558591b66484d6c9c698e1084ba0209743c323a44d3b`

```dockerfile
```

-	Layers:
	-	`sha256:6d30df5988b9169b8dbaf1c876d7faab04a1430e95e275c836a11cc57ca860bb`  
		Last Modified: Tue, 12 Nov 2024 02:38:55 GMT  
		Size: 3.7 MB (3739959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52e1d8d5147beb57fef6a0fc41dbe60adf9a6af8e00f33b3bc67ec6a480c44f2`  
		Last Modified: Tue, 12 Nov 2024 02:38:55 GMT  
		Size: 31.2 KB (31192 bytes)  
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
$ docker pull couchdb@sha256:566ad00a547f8cf73ee34234b2e496d3a1963973e487e416ba594b2431d51aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103917264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b853565bb2b3b4ecaeb7acbce0d4e64140783444d7298127aa388110fe94d56e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bb2d0d6a96e0df1e64c6768058ba160ece9975ff41e747051744754a6602ac`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78490fd3e69ce38a495f7047ae8ed194959ec3f187a1ebfc990078722eae4362`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 8.9 MB (8890074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce01cb959b4fd862b60ae9837737c8ae2a0a17ad33e6c5971ac58b7e8068b1fc`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 444.7 KB (444666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c581212b5869c39bf5e3ecfba5232c2e6bd76f5314b89bee947fab2fb08535f`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 76.3 KB (76288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68175198b4e73d464d85218d95d1eb1f61316be8f306012d91e6674ef178c8b6`  
		Last Modified: Tue, 12 Nov 2024 08:32:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b778ca3ac5159edb66416242074844e33086e769010222e9ae5bdbdb8efe66`  
		Last Modified: Tue, 12 Nov 2024 08:32:37 GMT  
		Size: 61.4 MB (61375448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4748275adde2dd6d571701074dee9d145b1826b47736443a7cda4aec44feafe8`  
		Last Modified: Tue, 12 Nov 2024 08:32:35 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb300b001a0b8870a23250ca36ad63779ea1d7680fe6f3e194278916f85a2ca`  
		Last Modified: Tue, 12 Nov 2024 08:32:35 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf6ae42c56873bcbb40d3d2a1a133c74dc5620616b14e4c81ab1e760651ceac`  
		Last Modified: Tue, 12 Nov 2024 08:32:36 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c50f6b7552bd2cfec853bf4223af75fa9da30bab35ce5eab4ea0bcc9bf30393`  
		Last Modified: Tue, 12 Nov 2024 08:32:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ca42a705b9a242c3dc3df7d360d738a6f72b0c876655b2790b0dacd158d6e064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c28cf2c0195d25a74c4a91196a397496dbc660faa89953159ada59907f6c34`

```dockerfile
```

-	Layers:
	-	`sha256:95e9d15956bddda1858f37d80eb7c1da71110ad01af698fdca041f76596c5ffa`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 3.7 MB (3744462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c729809f0ae8c11a05e787e501746039c4f11b2995e85e66e1a94919a87b38c3`  
		Last Modified: Tue, 12 Nov 2024 08:32:33 GMT  
		Size: 31.2 KB (31236 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:bf5b362a5066c3c64f1db3a38f43c828a4aa637dcb9ec4e1c8525623cbbd8e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94057367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a6dc24123b9855a4fae0de010e0613867e6a8dbf37638a6d13890026c809f0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe50171c1e31dfa26718c51ddcc5872c8fdab4d3263ebd9f04aef953259ac1d`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500762f13f114e2db6d2c1643551a4df71892f0535589340d8757b5647d5437`  
		Last Modified: Tue, 12 Nov 2024 09:05:27 GMT  
		Size: 7.4 MB (7387904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107b3a2fc5342d18016e7023ebbe69d83faccb03f367cde58071a39b4e1a229f`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 355.6 KB (355612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0b142e1a4e2d652182cdf84958d2c3c82429d95b995c64ec640d8bc34e95fc`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 76.3 KB (76339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e9e48ad844b84fe43f6a57e37a8c53e3d8c34d917afa03e3b86528f0532ce1`  
		Last Modified: Tue, 12 Nov 2024 09:08:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff424fa0018abe9d7918c3a71437dc38f7dcbe6bed153552e9e32fdcafa108a2`  
		Last Modified: Tue, 12 Nov 2024 09:08:14 GMT  
		Size: 58.7 MB (58740447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4c54f3536f38288f34149dc70062b6306124ba3492537723781404ba20a062`  
		Last Modified: Tue, 12 Nov 2024 09:08:13 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a09211ec3e93b6cd50b47c79da51a21d685211f654c414237de6c205697014`  
		Last Modified: Tue, 12 Nov 2024 09:08:13 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd206433d01baf5a6532f56caf68f688fadc1df7cd3d78e49c7e8bff141e0964`  
		Last Modified: Tue, 12 Nov 2024 09:08:13 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af639272897c6d328a1177edb697f0161b845915f5a2b4e300a8a5fe425122fd`  
		Last Modified: Tue, 12 Nov 2024 09:08:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a4039531e9e3c58dbfb59d4e3039741742db8364f9e99f6259ad5f3c10e6090c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3770239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f558bc6b501ba1b2abdaa1b61e08b7347e532eb265e3524ac6b98e1bb16270`

```dockerfile
```

-	Layers:
	-	`sha256:bd6d7c77b90211a70b5b0f7416b171ddb0a6e4249be269b03d89046d2bbdc5c8`  
		Last Modified: Tue, 12 Nov 2024 09:08:13 GMT  
		Size: 3.7 MB (3739047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675213844c86e53ea37fd1780d87bcdccd176aa8ff1b2aac3d248139b9931b86`  
		Last Modified: Tue, 12 Nov 2024 09:08:12 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:dd206b5c289dbe7ba3ff342e39eccebc74f8afac7ee2ec0567a7a4a131b9cb5b
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
$ docker pull couchdb@sha256:735194fe77a88d69ece21773709de5e22ca7f28c8468f71da05e659ff86951d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134139677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312a55065e927c2cd676e805ae872a95e9c1fa0fbf4bf655d8f003f3c7ae852a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81cd93b18f135ee83d01825f7fecacb7acae18cf0d229e41220d3d49e28f692`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2aa1fb55da0c568713a1a0b85fe7539f2aa956a0bedbe284613ea5234dc445`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 7.9 MB (7874852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff34e1414bc986bde3827be21e31cede390993e86aa8ef856e3194767f3577c0`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 392.1 KB (392111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562d6125a85f0529c429ac34462074bb35b2f00733461bdadf11301b8d648cc`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 76.2 KB (76250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda7a7f53d0e57963e34090515de7e93e6151bb506b2da694e47150c7cfae384`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d512b93b61e418f09435b41ccf4612603c67e4f5c28376fa3a9bf8034e4fbba`  
		Last Modified: Tue, 12 Nov 2024 02:39:13 GMT  
		Size: 96.7 MB (96663033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cde1e5d5956ad76d0d22369ceb1503c3131d9ff104426eb3eb4652945d309e9`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48486363b9474121ca8e42d62b0561bbd47ac5abb83b56c03c5e296ae74238ec`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec83637f971083de2400a03e5d9eff95716ec4b1d0af0f47e619452ec48a395d`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82a9780025224aa7cb7ffa559df8831056735aa215867045cab4e3ce0dcbe6a`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:f20b0e2adfd17adc82aa26af449f1177143837be66e45839ca55314b1af560c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7e559b9ad69bd91a0ace8d1e2989c2097fdfa799bdc87c735f295f292aa6a2`

```dockerfile
```

-	Layers:
	-	`sha256:1064d94b48b9794c4a9887de837a799ab1231f6637f838215965a040f745164e`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 3.9 MB (3947737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26a2e846657e24c19a12b74cef4d37fde9d8d68660e1720e05c16700bfa17c82`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b2995ca89617544e541a332918fdd5243da4b5e54d9b77fb594dedae30f6a2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133638613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13e25a8bdd5774de422c04b98fc3ac1b69be888f1ef1fc1a47345ae8551698c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
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
	-	`sha256:15ffe618b033b4cd957befd97c090e2ece69ba792eb50e7a710734587d3141ea`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 76.3 KB (76262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f91c9c6b0683e3a96e4228c48d706874dffa44389ae94c2b6679aaef55b85f`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62cce859844c9a8fe1704dc59e7539523fefd202b2cacdec2bd757df0eea342`  
		Last Modified: Tue, 22 Oct 2024 22:55:57 GMT  
		Size: 96.4 MB (96398076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67993a95c4192b1274b87d5f130e9826a50023a7ba60c78474bb7dcefce3d126`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91773508b70d1f9fd2cdb934a74173bf644abfa96a26ea5d7de35fa12c4090a`  
		Last Modified: Tue, 22 Oct 2024 22:55:55 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a66bdc41b21c8d8ae45d87f56ec64849164a3337c5b54cc0855e812cb7001b`  
		Last Modified: Tue, 22 Oct 2024 22:55:55 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d1ba095cb793f07ef398d83f3308c03d7846cb8e8c97d0f57e42c23d9b0f51`  
		Last Modified: Tue, 22 Oct 2024 22:55:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:904718ac7d1fca26ea2dd54906b9f636224116cbeaa42b6229af8e7a6560ae34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134564f44d44ede2ce6aa419fb3aa433137281031166eca45c4eef6e87572236`

```dockerfile
```

-	Layers:
	-	`sha256:4895539c4b106ad364b2786dd58436e5316426e2af8d577a7078549fdd0029c9`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 3.9 MB (3947993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e99a926b4b8b5d5d3c4e80bf549231a7f707d38e2b6e534605fcab3241a098ab`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 31.8 KB (31834 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:f9f0636806ae88dc461f067ecfe5d9ee77295559d8c1f9de1644bfec50a3178c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130606174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d64d01efd9a70e0060875698773c915ddc73aafd3a9b488292280e753255a4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe50171c1e31dfa26718c51ddcc5872c8fdab4d3263ebd9f04aef953259ac1d`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500762f13f114e2db6d2c1643551a4df71892f0535589340d8757b5647d5437`  
		Last Modified: Tue, 12 Nov 2024 09:05:27 GMT  
		Size: 7.4 MB (7387904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107b3a2fc5342d18016e7023ebbe69d83faccb03f367cde58071a39b4e1a229f`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 355.6 KB (355612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0b142e1a4e2d652182cdf84958d2c3c82429d95b995c64ec640d8bc34e95fc`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 76.3 KB (76339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e221b4ae713d7a5761e67086113cad325056288809b57598a9ff4cf39c158b8`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2e146630a045cba2bbc843466807f9c849e6f44231f6acacb38ba6925319c`  
		Last Modified: Tue, 12 Nov 2024 09:05:29 GMT  
		Size: 95.3 MB (95289258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db302f5ed06c1cfb54f257e31faf97cbf108f9a78f92bdc76044c0fb91772feb`  
		Last Modified: Tue, 12 Nov 2024 09:05:27 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096c7c90e014802ac9db88baaf9ce1ef8840260977fac85f7b9efc7ef5026321`  
		Last Modified: Tue, 12 Nov 2024 09:05:27 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b0ac698ab8ca1a5afcdc3b6fae173f1765b7eccdb2125872093794446d5e45`  
		Last Modified: Tue, 12 Nov 2024 09:05:28 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40d4bfb167e02369452f7feabdefaaed473eaef02032b619af5298af66605f6`  
		Last Modified: Tue, 12 Nov 2024 09:05:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:23ef435a855c10ead0b1a5d7dd8beef8513b8dd96e2644e7af0953541af17556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3978601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de44b5754f2faafcb5b2ede6b0565797eae9644f96b93a4918baa03cf135589b`

```dockerfile
```

-	Layers:
	-	`sha256:0d3cea293c10382b0d64d7aaaf87d4e5f4a56d04424c5ec656117caec2dc486b`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 3.9 MB (3946825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58c6043f6b03387395ea500ef9e988915eb99335cb71a7b2da7ad9bf50adbe9`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:b3a58a740869d3428cdd85c9da5b7c4dd8e7bdd3e6a47fb800ce1a03013a37f7
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
$ docker pull couchdb@sha256:7d73dd1c6b22690398fd72ff27a25874164de7d806fd9772c4c137cdb2d7980c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156433595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b23780d2087cf211c268ccd827028c5c107a9278082704c4cd701de05ad3248`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3e36b499d69fac410ec13e0e90b60065a5b483078f5d3e2536254423e5222f`  
		Last Modified: Tue, 12 Nov 2024 02:38:58 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a763829d6bfcab12c49dcd6b99fedaee601a9530fdef21eb74787cd2d7bb51`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 7.9 MB (7874861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f566daf2fdaf3790e6e330ee6247a9905d27094c64f025b74bf822ecc1fd00`  
		Last Modified: Tue, 12 Nov 2024 02:39:02 GMT  
		Size: 77.3 MB (77283799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07e481c7742184cdcb01de441e4178ae91c88aa40f42a7f18b94c4c1783c60`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 415.0 KB (414956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0aff5ca936036838c76a8d98fc6b07c79f42bf78110b37f28a3ba34bf970b5`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 99.3 KB (99285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04889d990fb1ce0f1ca9e4b6e4f74f4b76af37331fe91a4e11300b33a6dca558`  
		Last Modified: Tue, 12 Nov 2024 02:39:00 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ee84f15d3c696930742e848143b57371c46d7abfef5b603f149daa53cdac08`  
		Last Modified: Tue, 12 Nov 2024 02:39:02 GMT  
		Size: 41.6 MB (41630822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba664c1772d53c31b6a9bd5cb04686013b55788ee8e6c84c8b3662d9afa76033`  
		Last Modified: Tue, 12 Nov 2024 02:39:01 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5fa80ed1bb4a2513c114fedad9b26e6ded2360a2792c6a566f0574aee8c3068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3499647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a25a7ac49f8a425785a8beda80ee4155187481585517753a83409d9924ed016`

```dockerfile
```

-	Layers:
	-	`sha256:ffa03f762479765e205bfad5e8dd0fbbb0e09ab401ecc2b1ddcd19c70335fdf0`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 3.5 MB (3475085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff075489e5b49cb272d18000416cbb85dad3443e7f28df20fb6e7c5a6a6b4ac4`  
		Last Modified: Tue, 12 Nov 2024 02:38:58 GMT  
		Size: 24.6 KB (24562 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b87d41d8a4dc850c9df23b5e490b0eaf7534cfe9a81c549507cda07de713114a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155393649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1603b44f6c46c1b5e9aec253ff61d9d9f108720c3a74cd92ba52f643eb92595`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
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
	-	`sha256:84a2f199b083cc236d74acc480bc9abac691d493b1b8e8369c9b0d711304a0d0`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 7.7 MB (7653607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8459eb8b4c9964bd391e5d65122d9a6b51597679a46b26371df1aa25c7981230`  
		Last Modified: Tue, 22 Oct 2024 22:57:02 GMT  
		Size: 76.6 MB (76584069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d986d3cb2299ff5e9dcb002b84ed876ae4e141113c44029975f6e0285da4e5`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 371.7 KB (371687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658ba1a93b3f07ccb268aeee3cb247fd401728815cc696750fe4aa47e142d86`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 99.2 KB (99196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa093cddfcef74b5ea9feb12e196ed0de5282e3862fdfbe9388a13a8c3eba4f`  
		Last Modified: Tue, 22 Oct 2024 22:57:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c7071f8700c62ae031ca50097a10bcd1c1e8a1b663bb00a6de3432fd5f37d4`  
		Last Modified: Tue, 22 Oct 2024 22:57:02 GMT  
		Size: 41.5 MB (41526874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d704fde3024b8d5493329ea84940158034a267430e68c3b5fc6aa9b0ac28709b`  
		Last Modified: Tue, 22 Oct 2024 22:57:01 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:8c740bc74395f333b71bbaba633ce42a1d82c5d44247db9146df72b187582fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3498284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b511829792aaf6014b3919f785f3fd3597e0bbd618669e654196b9ef11d97bf8`

```dockerfile
```

-	Layers:
	-	`sha256:4bca8295be7075aaf79068a58523545f2b3f747f8d1182985c8834b17445ba74`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 3.5 MB (3473686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca52556d4416346ade61f88b44b846655e00138f989397d40478b0dc89035e1f`  
		Last Modified: Tue, 22 Oct 2024 22:56:59 GMT  
		Size: 24.6 KB (24598 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2cf915e89a9e7ed739113d095a8950b73929607949cabf2eff1ef4b7803c6866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149773483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879569e9e9cc1c272419476640029f25521bb00c2ba380b5958c1dc029be1e81`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c523130e4b9afa3f91f91c908ce7bc4f919818bc40d287191b5a3a48008e3fb`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2416975d6d48cc012c07fcfbd5d51f3af39ca9368af1cc038631b6e2a62ddac`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 7.4 MB (7387955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e7f35fec5d35bb10e1db7844516ad24ef8c9456d45497b4ea4f2a239ff10c8`  
		Last Modified: Tue, 12 Nov 2024 09:07:06 GMT  
		Size: 73.1 MB (73064505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10eda5ab7a8048646c86d3a8db41209ade88ee1d23079c43f5e5d91d49ab998`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 378.1 KB (378060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea45ee187eaa87421edbca0ee7055ab419db019e9606defb81b285952f0ed3b`  
		Last Modified: Tue, 12 Nov 2024 09:07:05 GMT  
		Size: 99.4 KB (99388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12accd577d35774ab5f9af2f75ceeb8e3f9ad2af5e0e7701ef024fc2e72635`  
		Last Modified: Tue, 12 Nov 2024 09:07:05 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db905cb94dc3cbfa90ea8e0f7851aebccced11b2bd23d61ff9790987b463b84a`  
		Last Modified: Tue, 12 Nov 2024 09:07:06 GMT  
		Size: 41.4 MB (41350067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83197dd55986f200b224d19273beade21655652c6a3d4abb012c7d473e63c80`  
		Last Modified: Tue, 12 Nov 2024 09:07:06 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f1eb394d72eb6e720820031c0904ea5717139e896b9b42facec8e06ce44bc144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc50f5f76af03030c6469294c8cd93184907bccad6e4b6de5d7d5a56f272791`

```dockerfile
```

-	Layers:
	-	`sha256:4de89241136a06eab37c23e3419dcaaf5ac4b40e4ac5c482409665f4e13bb32c`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 3.5 MB (3468498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca29ecebdf667ae3d12fff343bc5f7c661d59455e74a0e728bc967c8c03be581`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.2`

```console
$ docker pull couchdb@sha256:dd206b5c289dbe7ba3ff342e39eccebc74f8afac7ee2ec0567a7a4a131b9cb5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.2` - linux; amd64

```console
$ docker pull couchdb@sha256:735194fe77a88d69ece21773709de5e22ca7f28c8468f71da05e659ff86951d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134139677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312a55065e927c2cd676e805ae872a95e9c1fa0fbf4bf655d8f003f3c7ae852a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81cd93b18f135ee83d01825f7fecacb7acae18cf0d229e41220d3d49e28f692`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2aa1fb55da0c568713a1a0b85fe7539f2aa956a0bedbe284613ea5234dc445`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 7.9 MB (7874852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff34e1414bc986bde3827be21e31cede390993e86aa8ef856e3194767f3577c0`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 392.1 KB (392111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562d6125a85f0529c429ac34462074bb35b2f00733461bdadf11301b8d648cc`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 76.2 KB (76250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda7a7f53d0e57963e34090515de7e93e6151bb506b2da694e47150c7cfae384`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d512b93b61e418f09435b41ccf4612603c67e4f5c28376fa3a9bf8034e4fbba`  
		Last Modified: Tue, 12 Nov 2024 02:39:13 GMT  
		Size: 96.7 MB (96663033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cde1e5d5956ad76d0d22369ceb1503c3131d9ff104426eb3eb4652945d309e9`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48486363b9474121ca8e42d62b0561bbd47ac5abb83b56c03c5e296ae74238ec`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec83637f971083de2400a03e5d9eff95716ec4b1d0af0f47e619452ec48a395d`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82a9780025224aa7cb7ffa559df8831056735aa215867045cab4e3ce0dcbe6a`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:f20b0e2adfd17adc82aa26af449f1177143837be66e45839ca55314b1af560c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7e559b9ad69bd91a0ace8d1e2989c2097fdfa799bdc87c735f295f292aa6a2`

```dockerfile
```

-	Layers:
	-	`sha256:1064d94b48b9794c4a9887de837a799ab1231f6637f838215965a040f745164e`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 3.9 MB (3947737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26a2e846657e24c19a12b74cef4d37fde9d8d68660e1720e05c16700bfa17c82`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b2995ca89617544e541a332918fdd5243da4b5e54d9b77fb594dedae30f6a2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133638613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13e25a8bdd5774de422c04b98fc3ac1b69be888f1ef1fc1a47345ae8551698c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
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
	-	`sha256:15ffe618b033b4cd957befd97c090e2ece69ba792eb50e7a710734587d3141ea`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 76.3 KB (76262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f91c9c6b0683e3a96e4228c48d706874dffa44389ae94c2b6679aaef55b85f`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62cce859844c9a8fe1704dc59e7539523fefd202b2cacdec2bd757df0eea342`  
		Last Modified: Tue, 22 Oct 2024 22:55:57 GMT  
		Size: 96.4 MB (96398076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67993a95c4192b1274b87d5f130e9826a50023a7ba60c78474bb7dcefce3d126`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91773508b70d1f9fd2cdb934a74173bf644abfa96a26ea5d7de35fa12c4090a`  
		Last Modified: Tue, 22 Oct 2024 22:55:55 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a66bdc41b21c8d8ae45d87f56ec64849164a3337c5b54cc0855e812cb7001b`  
		Last Modified: Tue, 22 Oct 2024 22:55:55 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d1ba095cb793f07ef398d83f3308c03d7846cb8e8c97d0f57e42c23d9b0f51`  
		Last Modified: Tue, 22 Oct 2024 22:55:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:904718ac7d1fca26ea2dd54906b9f636224116cbeaa42b6229af8e7a6560ae34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134564f44d44ede2ce6aa419fb3aa433137281031166eca45c4eef6e87572236`

```dockerfile
```

-	Layers:
	-	`sha256:4895539c4b106ad364b2786dd58436e5316426e2af8d577a7078549fdd0029c9`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 3.9 MB (3947993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e99a926b4b8b5d5d3c4e80bf549231a7f707d38e2b6e534605fcab3241a098ab`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 31.8 KB (31834 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2` - linux; s390x

```console
$ docker pull couchdb@sha256:f9f0636806ae88dc461f067ecfe5d9ee77295559d8c1f9de1644bfec50a3178c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130606174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d64d01efd9a70e0060875698773c915ddc73aafd3a9b488292280e753255a4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe50171c1e31dfa26718c51ddcc5872c8fdab4d3263ebd9f04aef953259ac1d`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500762f13f114e2db6d2c1643551a4df71892f0535589340d8757b5647d5437`  
		Last Modified: Tue, 12 Nov 2024 09:05:27 GMT  
		Size: 7.4 MB (7387904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107b3a2fc5342d18016e7023ebbe69d83faccb03f367cde58071a39b4e1a229f`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 355.6 KB (355612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0b142e1a4e2d652182cdf84958d2c3c82429d95b995c64ec640d8bc34e95fc`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 76.3 KB (76339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e221b4ae713d7a5761e67086113cad325056288809b57598a9ff4cf39c158b8`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2e146630a045cba2bbc843466807f9c849e6f44231f6acacb38ba6925319c`  
		Last Modified: Tue, 12 Nov 2024 09:05:29 GMT  
		Size: 95.3 MB (95289258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db302f5ed06c1cfb54f257e31faf97cbf108f9a78f92bdc76044c0fb91772feb`  
		Last Modified: Tue, 12 Nov 2024 09:05:27 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096c7c90e014802ac9db88baaf9ce1ef8840260977fac85f7b9efc7ef5026321`  
		Last Modified: Tue, 12 Nov 2024 09:05:27 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b0ac698ab8ca1a5afcdc3b6fae173f1765b7eccdb2125872093794446d5e45`  
		Last Modified: Tue, 12 Nov 2024 09:05:28 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40d4bfb167e02369452f7feabdefaaed473eaef02032b619af5298af66605f6`  
		Last Modified: Tue, 12 Nov 2024 09:05:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:23ef435a855c10ead0b1a5d7dd8beef8513b8dd96e2644e7af0953541af17556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3978601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de44b5754f2faafcb5b2ede6b0565797eae9644f96b93a4918baa03cf135589b`

```dockerfile
```

-	Layers:
	-	`sha256:0d3cea293c10382b0d64d7aaaf87d4e5f4a56d04424c5ec656117caec2dc486b`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 3.9 MB (3946825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58c6043f6b03387395ea500ef9e988915eb99335cb71a7b2da7ad9bf50adbe9`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.2-nouveau`

```console
$ docker pull couchdb@sha256:b3a58a740869d3428cdd85c9da5b7c4dd8e7bdd3e6a47fb800ce1a03013a37f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.2-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:7d73dd1c6b22690398fd72ff27a25874164de7d806fd9772c4c137cdb2d7980c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156433595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b23780d2087cf211c268ccd827028c5c107a9278082704c4cd701de05ad3248`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3e36b499d69fac410ec13e0e90b60065a5b483078f5d3e2536254423e5222f`  
		Last Modified: Tue, 12 Nov 2024 02:38:58 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a763829d6bfcab12c49dcd6b99fedaee601a9530fdef21eb74787cd2d7bb51`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 7.9 MB (7874861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f566daf2fdaf3790e6e330ee6247a9905d27094c64f025b74bf822ecc1fd00`  
		Last Modified: Tue, 12 Nov 2024 02:39:02 GMT  
		Size: 77.3 MB (77283799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07e481c7742184cdcb01de441e4178ae91c88aa40f42a7f18b94c4c1783c60`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 415.0 KB (414956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0aff5ca936036838c76a8d98fc6b07c79f42bf78110b37f28a3ba34bf970b5`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 99.3 KB (99285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04889d990fb1ce0f1ca9e4b6e4f74f4b76af37331fe91a4e11300b33a6dca558`  
		Last Modified: Tue, 12 Nov 2024 02:39:00 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ee84f15d3c696930742e848143b57371c46d7abfef5b603f149daa53cdac08`  
		Last Modified: Tue, 12 Nov 2024 02:39:02 GMT  
		Size: 41.6 MB (41630822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba664c1772d53c31b6a9bd5cb04686013b55788ee8e6c84c8b3662d9afa76033`  
		Last Modified: Tue, 12 Nov 2024 02:39:01 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5fa80ed1bb4a2513c114fedad9b26e6ded2360a2792c6a566f0574aee8c3068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3499647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a25a7ac49f8a425785a8beda80ee4155187481585517753a83409d9924ed016`

```dockerfile
```

-	Layers:
	-	`sha256:ffa03f762479765e205bfad5e8dd0fbbb0e09ab401ecc2b1ddcd19c70335fdf0`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 3.5 MB (3475085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff075489e5b49cb272d18000416cbb85dad3443e7f28df20fb6e7c5a6a6b4ac4`  
		Last Modified: Tue, 12 Nov 2024 02:38:58 GMT  
		Size: 24.6 KB (24562 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b87d41d8a4dc850c9df23b5e490b0eaf7534cfe9a81c549507cda07de713114a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155393649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1603b44f6c46c1b5e9aec253ff61d9d9f108720c3a74cd92ba52f643eb92595`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
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
	-	`sha256:84a2f199b083cc236d74acc480bc9abac691d493b1b8e8369c9b0d711304a0d0`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 7.7 MB (7653607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8459eb8b4c9964bd391e5d65122d9a6b51597679a46b26371df1aa25c7981230`  
		Last Modified: Tue, 22 Oct 2024 22:57:02 GMT  
		Size: 76.6 MB (76584069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d986d3cb2299ff5e9dcb002b84ed876ae4e141113c44029975f6e0285da4e5`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 371.7 KB (371687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658ba1a93b3f07ccb268aeee3cb247fd401728815cc696750fe4aa47e142d86`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 99.2 KB (99196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa093cddfcef74b5ea9feb12e196ed0de5282e3862fdfbe9388a13a8c3eba4f`  
		Last Modified: Tue, 22 Oct 2024 22:57:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c7071f8700c62ae031ca50097a10bcd1c1e8a1b663bb00a6de3432fd5f37d4`  
		Last Modified: Tue, 22 Oct 2024 22:57:02 GMT  
		Size: 41.5 MB (41526874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d704fde3024b8d5493329ea84940158034a267430e68c3b5fc6aa9b0ac28709b`  
		Last Modified: Tue, 22 Oct 2024 22:57:01 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:8c740bc74395f333b71bbaba633ce42a1d82c5d44247db9146df72b187582fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3498284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b511829792aaf6014b3919f785f3fd3597e0bbd618669e654196b9ef11d97bf8`

```dockerfile
```

-	Layers:
	-	`sha256:4bca8295be7075aaf79068a58523545f2b3f747f8d1182985c8834b17445ba74`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 3.5 MB (3473686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca52556d4416346ade61f88b44b846655e00138f989397d40478b0dc89035e1f`  
		Last Modified: Tue, 22 Oct 2024 22:56:59 GMT  
		Size: 24.6 KB (24598 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2cf915e89a9e7ed739113d095a8950b73929607949cabf2eff1ef4b7803c6866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149773483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879569e9e9cc1c272419476640029f25521bb00c2ba380b5958c1dc029be1e81`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c523130e4b9afa3f91f91c908ce7bc4f919818bc40d287191b5a3a48008e3fb`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2416975d6d48cc012c07fcfbd5d51f3af39ca9368af1cc038631b6e2a62ddac`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 7.4 MB (7387955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e7f35fec5d35bb10e1db7844516ad24ef8c9456d45497b4ea4f2a239ff10c8`  
		Last Modified: Tue, 12 Nov 2024 09:07:06 GMT  
		Size: 73.1 MB (73064505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10eda5ab7a8048646c86d3a8db41209ade88ee1d23079c43f5e5d91d49ab998`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 378.1 KB (378060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea45ee187eaa87421edbca0ee7055ab419db019e9606defb81b285952f0ed3b`  
		Last Modified: Tue, 12 Nov 2024 09:07:05 GMT  
		Size: 99.4 KB (99388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12accd577d35774ab5f9af2f75ceeb8e3f9ad2af5e0e7701ef024fc2e72635`  
		Last Modified: Tue, 12 Nov 2024 09:07:05 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db905cb94dc3cbfa90ea8e0f7851aebccced11b2bd23d61ff9790987b463b84a`  
		Last Modified: Tue, 12 Nov 2024 09:07:06 GMT  
		Size: 41.4 MB (41350067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83197dd55986f200b224d19273beade21655652c6a3d4abb012c7d473e63c80`  
		Last Modified: Tue, 12 Nov 2024 09:07:06 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f1eb394d72eb6e720820031c0904ea5717139e896b9b42facec8e06ce44bc144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc50f5f76af03030c6469294c8cd93184907bccad6e4b6de5d7d5a56f272791`

```dockerfile
```

-	Layers:
	-	`sha256:4de89241136a06eab37c23e3419dcaaf5ac4b40e4ac5c482409665f4e13bb32c`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 3.5 MB (3468498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca29ecebdf667ae3d12fff343bc5f7c661d59455e74a0e728bc967c8c03be581`  
		Last Modified: Tue, 12 Nov 2024 09:07:04 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:dd206b5c289dbe7ba3ff342e39eccebc74f8afac7ee2ec0567a7a4a131b9cb5b
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
$ docker pull couchdb@sha256:735194fe77a88d69ece21773709de5e22ca7f28c8468f71da05e659ff86951d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134139677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312a55065e927c2cd676e805ae872a95e9c1fa0fbf4bf655d8f003f3c7ae852a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81cd93b18f135ee83d01825f7fecacb7acae18cf0d229e41220d3d49e28f692`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2aa1fb55da0c568713a1a0b85fe7539f2aa956a0bedbe284613ea5234dc445`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 7.9 MB (7874852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff34e1414bc986bde3827be21e31cede390993e86aa8ef856e3194767f3577c0`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 392.1 KB (392111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562d6125a85f0529c429ac34462074bb35b2f00733461bdadf11301b8d648cc`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 76.2 KB (76250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda7a7f53d0e57963e34090515de7e93e6151bb506b2da694e47150c7cfae384`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d512b93b61e418f09435b41ccf4612603c67e4f5c28376fa3a9bf8034e4fbba`  
		Last Modified: Tue, 12 Nov 2024 02:39:13 GMT  
		Size: 96.7 MB (96663033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cde1e5d5956ad76d0d22369ceb1503c3131d9ff104426eb3eb4652945d309e9`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48486363b9474121ca8e42d62b0561bbd47ac5abb83b56c03c5e296ae74238ec`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec83637f971083de2400a03e5d9eff95716ec4b1d0af0f47e619452ec48a395d`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82a9780025224aa7cb7ffa559df8831056735aa215867045cab4e3ce0dcbe6a`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:f20b0e2adfd17adc82aa26af449f1177143837be66e45839ca55314b1af560c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7e559b9ad69bd91a0ace8d1e2989c2097fdfa799bdc87c735f295f292aa6a2`

```dockerfile
```

-	Layers:
	-	`sha256:1064d94b48b9794c4a9887de837a799ab1231f6637f838215965a040f745164e`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 3.9 MB (3947737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26a2e846657e24c19a12b74cef4d37fde9d8d68660e1720e05c16700bfa17c82`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b2995ca89617544e541a332918fdd5243da4b5e54d9b77fb594dedae30f6a2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133638613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13e25a8bdd5774de422c04b98fc3ac1b69be888f1ef1fc1a47345ae8551698c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
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
	-	`sha256:15ffe618b033b4cd957befd97c090e2ece69ba792eb50e7a710734587d3141ea`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 76.3 KB (76262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f91c9c6b0683e3a96e4228c48d706874dffa44389ae94c2b6679aaef55b85f`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62cce859844c9a8fe1704dc59e7539523fefd202b2cacdec2bd757df0eea342`  
		Last Modified: Tue, 22 Oct 2024 22:55:57 GMT  
		Size: 96.4 MB (96398076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67993a95c4192b1274b87d5f130e9826a50023a7ba60c78474bb7dcefce3d126`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91773508b70d1f9fd2cdb934a74173bf644abfa96a26ea5d7de35fa12c4090a`  
		Last Modified: Tue, 22 Oct 2024 22:55:55 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a66bdc41b21c8d8ae45d87f56ec64849164a3337c5b54cc0855e812cb7001b`  
		Last Modified: Tue, 22 Oct 2024 22:55:55 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d1ba095cb793f07ef398d83f3308c03d7846cb8e8c97d0f57e42c23d9b0f51`  
		Last Modified: Tue, 22 Oct 2024 22:55:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:904718ac7d1fca26ea2dd54906b9f636224116cbeaa42b6229af8e7a6560ae34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134564f44d44ede2ce6aa419fb3aa433137281031166eca45c4eef6e87572236`

```dockerfile
```

-	Layers:
	-	`sha256:4895539c4b106ad364b2786dd58436e5316426e2af8d577a7078549fdd0029c9`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 3.9 MB (3947993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e99a926b4b8b5d5d3c4e80bf549231a7f707d38e2b6e534605fcab3241a098ab`  
		Last Modified: Tue, 22 Oct 2024 22:55:54 GMT  
		Size: 31.8 KB (31834 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:f9f0636806ae88dc461f067ecfe5d9ee77295559d8c1f9de1644bfec50a3178c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130606174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d64d01efd9a70e0060875698773c915ddc73aafd3a9b488292280e753255a4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe50171c1e31dfa26718c51ddcc5872c8fdab4d3263ebd9f04aef953259ac1d`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500762f13f114e2db6d2c1643551a4df71892f0535589340d8757b5647d5437`  
		Last Modified: Tue, 12 Nov 2024 09:05:27 GMT  
		Size: 7.4 MB (7387904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107b3a2fc5342d18016e7023ebbe69d83faccb03f367cde58071a39b4e1a229f`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 355.6 KB (355612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0b142e1a4e2d652182cdf84958d2c3c82429d95b995c64ec640d8bc34e95fc`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 76.3 KB (76339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e221b4ae713d7a5761e67086113cad325056288809b57598a9ff4cf39c158b8`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2e146630a045cba2bbc843466807f9c849e6f44231f6acacb38ba6925319c`  
		Last Modified: Tue, 12 Nov 2024 09:05:29 GMT  
		Size: 95.3 MB (95289258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db302f5ed06c1cfb54f257e31faf97cbf108f9a78f92bdc76044c0fb91772feb`  
		Last Modified: Tue, 12 Nov 2024 09:05:27 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096c7c90e014802ac9db88baaf9ce1ef8840260977fac85f7b9efc7ef5026321`  
		Last Modified: Tue, 12 Nov 2024 09:05:27 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b0ac698ab8ca1a5afcdc3b6fae173f1765b7eccdb2125872093794446d5e45`  
		Last Modified: Tue, 12 Nov 2024 09:05:28 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40d4bfb167e02369452f7feabdefaaed473eaef02032b619af5298af66605f6`  
		Last Modified: Tue, 12 Nov 2024 09:05:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:23ef435a855c10ead0b1a5d7dd8beef8513b8dd96e2644e7af0953541af17556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3978601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de44b5754f2faafcb5b2ede6b0565797eae9644f96b93a4918baa03cf135589b`

```dockerfile
```

-	Layers:
	-	`sha256:0d3cea293c10382b0d64d7aaaf87d4e5f4a56d04424c5ec656117caec2dc486b`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 3.9 MB (3946825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58c6043f6b03387395ea500ef9e988915eb99335cb71a7b2da7ad9bf50adbe9`  
		Last Modified: Tue, 12 Nov 2024 09:05:26 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json
