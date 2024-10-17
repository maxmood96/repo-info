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
$ docker pull couchdb@sha256:92910f259df692ace51ac69d8a11e4c6fe37009c36e675fe3b3673adbb7dd589
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
$ docker pull couchdb@sha256:6f7304af9afc8cf0f0bee740d867584e2534bcd365aaba854f6a85d746ce695b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133500332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212fb806a99dd40948d6bbbd4a823fb5cf3329b47232a91cf38d126dfb028eff`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9442d790d6635e0b482db9e87cfb0cac90976dba8b8c97587193528324018d86`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdc3f69418039c0518a92ae7aba5811a85e436c9a6eb5122c28aae5b5f11c2e`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 7.7 MB (7653622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae297c75ee602d28290f293b626460f25e418eee654ce55b3832094ed3b8ad01`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 348.9 KB (348918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4250e6935cc5320d6b60fcb18f04d395f7da1124ffcf71b4e45e039776e94553`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 76.2 KB (76249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c412911b39adbd44f52383546496c2af710b6ccca5c9989e0ba373bc50b80e90`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd475490e141a14ac69667f3c350fcb6d140936cef9cd3007aa305d77e4cc5f6`  
		Last Modified: Mon, 07 Oct 2024 17:59:16 GMT  
		Size: 96.3 MB (96259732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5baaeef047eea69480cf0707d9e80c07f9a3d1b48f91eaa2ab40c01b1154d6`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374a0dd7ca701907840fe7937240a0ef12b8cb0daaf89a1cb2840a377272b8ec`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f09a5ca8e0ba7b12c4986347521af7a048b284dfb4bbad8c7f7bcbbc00118e`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8552ede7fbb1fb7d79984a5d6f3b386b0e261ad872026f1379e57881d893d42f`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:7b455ba696ae595140ce2d3688b57a4598a900bcc9ae90f74ee05e42d9eddc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9186f946aa7677ff5ce63c3755037aa75a3aaae00792b50fc00810fa16c96d23`

```dockerfile
```

-	Layers:
	-	`sha256:801a118eeb4f2f9e15b2a6fc955a4ffb05cf4f24a93952313e4299fea8503d19`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 3.9 MB (3931152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2a446b8215c1076b2dbea9b42b9b660a0c1f2effda481e563ed7da921101ed`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 31.8 KB (31805 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:7c01108575f86bd4a58fb4339c622c656c573688ec5097740ddef31855118609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130484414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c467056de202277fe0f85cd31f0db9c565e7419d0bd380a8bac0d954d2d74c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:25 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Fri, 27 Sep 2024 02:43:26 GMT
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2001248de490d09e03580d82567df39a6377d1b7bc6438b80f045348802020`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e5c3868b3ab8d295a312e2627b5eb5aae4d26fe22fa4c8732f03dbc5e5256b`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 7.4 MB (7387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b190bf09204a63267db1b7c1910be8bd0a7c6961ce6299a95ac8bed3920d397e`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 355.7 KB (355665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a36fe4ec66e9bf52c1c64efcdee3d6f8eab451846c24ee867524f0767071a8`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 76.4 KB (76430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65c70f2bb55367e98e72296838eff96f1ade898641d684c30f6774d5beffbd8`  
		Last Modified: Mon, 07 Oct 2024 18:00:50 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dda488e868e46e2aae9e22b7ed97f6b41842fc63fe9a427338ea2aabba9298`  
		Last Modified: Mon, 07 Oct 2024 18:00:52 GMT  
		Size: 95.2 MB (95169632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bfdd9b127b6c65f5e53539c6efcb481130d1aa56901341b6b2b5568d78555e`  
		Last Modified: Mon, 07 Oct 2024 18:00:50 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c9cf06d126bbba924308104e73165d5c3002527357b26fe6d0741771714530`  
		Last Modified: Mon, 07 Oct 2024 18:00:50 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4ead5c81ad58a81ed283dade2b03c5098d40700352417cdb27d76046490aab`  
		Last Modified: Mon, 07 Oct 2024 18:00:51 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64f37e57a06d60981346ed1ec7cdabbfed4707a89ea6ef646f57eb466be0fd6`  
		Last Modified: Mon, 07 Oct 2024 18:00:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:624ce0dfd11046ffec42a75bf12328cf355188371cc41a0ad3f64b25b37f1cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498a97d04d7643704d491e91c6d50be39e65bf67ebd38c752df182304d0b2789`

```dockerfile
```

-	Layers:
	-	`sha256:f98ff86261737a399d3f3ce5e0bbea20360b7434be910a91936b35c71b0448e8`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 3.9 MB (3930054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5414a7b7baf8e81541f56911a98eb1042d18a02697efa0f4550963887ace6b7b`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 31.6 KB (31615 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:a2d5d17f69db3fd25b5ee6f6e6cabaaabb37d90cd3e3fa4b418b50cca601d1ff
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
$ docker pull couchdb@sha256:6cb6aa93c071a1f3d35eddad7dd50bde831a6b69f0e0b3eb25b855da2c5795ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155211011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6720b48cd575172fe484da0a28d6e560e005e57eaedf0d66422fa1f685c424a0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dd4e3ec72ebd08003da9bae2a4f91d7054c7f219464df5c99dff6b44357474`  
		Last Modified: Mon, 07 Oct 2024 18:00:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b137a87f378e3c4b496ef8aee954623363575617dc3a5c7483f8c3ad1e6d2f`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 7.7 MB (7653599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438ad86fea8079ebaffc58a077adcfe370c3ebf5fdcc586a3a436f3fe702b64d`  
		Last Modified: Mon, 07 Oct 2024 18:00:24 GMT  
		Size: 76.5 MB (76508600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3de680e3bb5f4da4aa8fb277abfa4e3f9c789f961838de4afe48155fb5703f`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 371.7 KB (371699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c47625cd46d9f532742c73d6953d6f24d949e77ca64418792b5f53b862d254`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 99.2 KB (99217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d1f9143bb84d6b7c608ee25f6afea8af5874e2ae35e88d5c30d0da7ffe310`  
		Last Modified: Mon, 07 Oct 2024 18:00:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d508b85b561fba7d2e644cd77f5b8a05aed8f90a778f04fddd00ffa7253bcd2`  
		Last Modified: Mon, 07 Oct 2024 18:00:25 GMT  
		Size: 41.4 MB (41419645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b28d630547bae5f947878ebecabba5ef9b005b5f9fc3048b4edd72f28b51e9`  
		Last Modified: Mon, 07 Oct 2024 18:00:23 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f017d58d202848d8c80f74a5bcab5b6764f4e0c5c5051b4ce573865abdc4e42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3477517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3d3c9e59015ec1d1b521062e7c828ab3abcb3628a8738b55effe9f47eaa5dd`

```dockerfile
```

-	Layers:
	-	`sha256:3a582c389a53f22cadcb0f1e17a3270ec996f89250ca740ea9dd3572660cf229`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 3.5 MB (3452948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ab1f52acee1d1347095589a024c76cdb40a50b698e950c8dd8d1cd4a966ebb`  
		Last Modified: Mon, 07 Oct 2024 18:00:21 GMT  
		Size: 24.6 KB (24569 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:a769a37fa918495b7b9b4d6507ca0d845f438ea9fec4c8a92669465c6585666a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149595951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459e06e7a4838283c6ad7127f3ea08a349130672bbabb29c65ce5a81445032c9`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:25 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Fri, 27 Sep 2024 02:43:26 GMT
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cdd8ece04acd2127415e13f8bec0227eb84f82d8c1084c908d6660ea0a1fb2`  
		Last Modified: Mon, 07 Oct 2024 18:03:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a6697c4dda07211a6fe83879e5371efb32a06f9108171fa7c01a9beb8930c`  
		Last Modified: Mon, 07 Oct 2024 18:03:56 GMT  
		Size: 7.4 MB (7387297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9308f390eede38eeba97ddf2aae327974fe41a32a9c9adce6fc2b1dc369f062c`  
		Last Modified: Mon, 07 Oct 2024 18:03:57 GMT  
		Size: 73.0 MB (72988074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec8e46df547a8e2dfffb0951bad8e1ba159f114823579b772d4da45be50686`  
		Last Modified: Mon, 07 Oct 2024 18:03:55 GMT  
		Size: 378.2 KB (378168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f6ae7c1a5fb4a8048ba668ff13896a99ee959b58956d5601dc4c0cb905c6a3`  
		Last Modified: Mon, 07 Oct 2024 18:03:56 GMT  
		Size: 99.6 KB (99558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c97dd50ac3b237728d0973ecdebc18615d542963f377f2400c5dbba8ba08b3d`  
		Last Modified: Mon, 07 Oct 2024 18:03:56 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5477fdaef2dcad89941d20a4fbed9eb177641739f37f7c08ccf8ca015a22e489`  
		Last Modified: Mon, 07 Oct 2024 18:03:58 GMT  
		Size: 41.3 MB (41250948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9097da2b45c386dcbc78bfa352e23bab39155aa34aba43b0bdfa5796857302`  
		Last Modified: Mon, 07 Oct 2024 18:03:57 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:9f1139ae96caf97f1fc0738b5558bd23e20ce0b46f6a7b0d4369c402b91851ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3472186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3390060b4240d5b09ec2424441b839043844b748371bbf08b059cd10bf311311`

```dockerfile
```

-	Layers:
	-	`sha256:298aeec794eba0490e889885e1758cfb76a700f527aaaec4a4d4f8d572b784ed`  
		Last Modified: Mon, 07 Oct 2024 18:03:55 GMT  
		Size: 3.4 MB (3447794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc4fc686d3e2892bd2e501a3d3506ddb951ce2fd4858fcedd71fc428ab3f0984`  
		Last Modified: Mon, 07 Oct 2024 18:03:55 GMT  
		Size: 24.4 KB (24392 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:0a8702b57018992a532731203e5a2f0141539562be56f1cb15fee42489f0f855
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
$ docker pull couchdb@sha256:bfba3256d6594ae3decef473b0d0e7e25496980c3a6cbf49bb6201da039f9da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97174904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2834df946e286bac5bb3e61c8471ad3282188d54935c94e9129a7831124e141`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9442d790d6635e0b482db9e87cfb0cac90976dba8b8c97587193528324018d86`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdc3f69418039c0518a92ae7aba5811a85e436c9a6eb5122c28aae5b5f11c2e`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 7.7 MB (7653622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae297c75ee602d28290f293b626460f25e418eee654ce55b3832094ed3b8ad01`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 348.9 KB (348918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4250e6935cc5320d6b60fcb18f04d395f7da1124ffcf71b4e45e039776e94553`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 76.2 KB (76249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f035e84dc1280869bf96e6d56d1b44c820b292ea52e02edb891390a01159b0c`  
		Last Modified: Mon, 07 Oct 2024 18:01:13 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dbaf5123802bd20022593c0a411ca5cc49aaa292ea10fb492d4004dc51a89d`  
		Last Modified: Mon, 07 Oct 2024 18:01:14 GMT  
		Size: 59.9 MB (59934303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9235d516056e5c801c36bc82cf4f764231b499a835357b7b6baba89185324bd1`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38d2de30a2b11e03b7863ee0c8d989c844b05ed193688af7a5a4f35c0a8558f`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca735c111823e0dc69173ce4a264440acadd3c94a15f16657ee5fd01dae2f22`  
		Last Modified: Mon, 07 Oct 2024 18:01:13 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efdd3b9c1edd642c3cfbb48875d8c17d0c7f3552ae5e897fb41455138d974a4`  
		Last Modified: Mon, 07 Oct 2024 18:01:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a30ef4cbc9c696c26b7db3263e230f3c1a5a5080f3b82aeb12369c85c9c22c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17c79f5ef930a6655202539e34ad785d1e9f7f67fc74fe21972547d15b53e11`

```dockerfile
```

-	Layers:
	-	`sha256:eefac6e18d06e1e3a897f337366bfd3167e5a6ac50c43afae7ec9dd3a8382eba`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 3.7 MB (3723350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:905f9b4ba2b5c7b97bedf399ab54e99ecbf7e3ee5966e38d918f41c6c895686d`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 31.2 KB (31197 bytes)  
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
$ docker pull couchdb@sha256:0f782abb20f8538f0737a03ccf9c8763bbd0ca927345ce4b9eb4aa983486ba18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94055017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36070957d0133d63cda991ce0d5c386e90524ba1f43b9d6cb2114c0adff29dfa`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:25 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Fri, 27 Sep 2024 02:43:26 GMT
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2001248de490d09e03580d82567df39a6377d1b7bc6438b80f045348802020`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e5c3868b3ab8d295a312e2627b5eb5aae4d26fe22fa4c8732f03dbc5e5256b`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 7.4 MB (7387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b190bf09204a63267db1b7c1910be8bd0a7c6961ce6299a95ac8bed3920d397e`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 355.7 KB (355665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a36fe4ec66e9bf52c1c64efcdee3d6f8eab451846c24ee867524f0767071a8`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 76.4 KB (76430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bc289711a202f3e5706c78e5563294d7c47783ebd0a4f12861465a25ccbfb5`  
		Last Modified: Mon, 07 Oct 2024 18:05:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9721e986bb5ef4de6222fcff2a10961d32f5575df568685613977e47c9803a`  
		Last Modified: Mon, 07 Oct 2024 18:05:47 GMT  
		Size: 58.7 MB (58740233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf12e352ef273a44902be561aed5f9de83a6fea3c07e6c3592e5044a881660c`  
		Last Modified: Mon, 07 Oct 2024 18:05:45 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef71ec8be35d0903ab820bbc215bfce407f54b75ce96fbee6b201817cab3c8f`  
		Last Modified: Mon, 07 Oct 2024 18:05:45 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e06f8c396526cf0d9a8c68076edaf85d550e6e8cf493b8ad159ea047b3819`  
		Last Modified: Mon, 07 Oct 2024 18:05:46 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c03e022273ff6f3a58bb477f3fd09dff5aa2accebac6314440e55175b3b712`  
		Last Modified: Mon, 07 Oct 2024 18:05:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:8a6a211b5136e604bf30feab4ff42c48a564f45a335b0fe836ecb942d6874fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3753309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34d0ee4340e7c4c62639fcc845898d4d17579eab68857082cf92f962c0a1adc`

```dockerfile
```

-	Layers:
	-	`sha256:ea7c0e1d1b4ae4e84ea98af36ac6812f805790af82fe8823efaacf079a7ac826`  
		Last Modified: Mon, 07 Oct 2024 18:05:45 GMT  
		Size: 3.7 MB (3722276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a61e16bd446d7d268447470261d66609c12adacb4c65a7c32201e3c8753dd1`  
		Last Modified: Mon, 07 Oct 2024 18:05:45 GMT  
		Size: 31.0 KB (31033 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:0a8702b57018992a532731203e5a2f0141539562be56f1cb15fee42489f0f855
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
$ docker pull couchdb@sha256:bfba3256d6594ae3decef473b0d0e7e25496980c3a6cbf49bb6201da039f9da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97174904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2834df946e286bac5bb3e61c8471ad3282188d54935c94e9129a7831124e141`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9442d790d6635e0b482db9e87cfb0cac90976dba8b8c97587193528324018d86`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdc3f69418039c0518a92ae7aba5811a85e436c9a6eb5122c28aae5b5f11c2e`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 7.7 MB (7653622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae297c75ee602d28290f293b626460f25e418eee654ce55b3832094ed3b8ad01`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 348.9 KB (348918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4250e6935cc5320d6b60fcb18f04d395f7da1124ffcf71b4e45e039776e94553`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 76.2 KB (76249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f035e84dc1280869bf96e6d56d1b44c820b292ea52e02edb891390a01159b0c`  
		Last Modified: Mon, 07 Oct 2024 18:01:13 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dbaf5123802bd20022593c0a411ca5cc49aaa292ea10fb492d4004dc51a89d`  
		Last Modified: Mon, 07 Oct 2024 18:01:14 GMT  
		Size: 59.9 MB (59934303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9235d516056e5c801c36bc82cf4f764231b499a835357b7b6baba89185324bd1`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38d2de30a2b11e03b7863ee0c8d989c844b05ed193688af7a5a4f35c0a8558f`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca735c111823e0dc69173ce4a264440acadd3c94a15f16657ee5fd01dae2f22`  
		Last Modified: Mon, 07 Oct 2024 18:01:13 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efdd3b9c1edd642c3cfbb48875d8c17d0c7f3552ae5e897fb41455138d974a4`  
		Last Modified: Mon, 07 Oct 2024 18:01:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a30ef4cbc9c696c26b7db3263e230f3c1a5a5080f3b82aeb12369c85c9c22c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17c79f5ef930a6655202539e34ad785d1e9f7f67fc74fe21972547d15b53e11`

```dockerfile
```

-	Layers:
	-	`sha256:eefac6e18d06e1e3a897f337366bfd3167e5a6ac50c43afae7ec9dd3a8382eba`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 3.7 MB (3723350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:905f9b4ba2b5c7b97bedf399ab54e99ecbf7e3ee5966e38d918f41c6c895686d`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 31.2 KB (31197 bytes)  
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
$ docker pull couchdb@sha256:0f782abb20f8538f0737a03ccf9c8763bbd0ca927345ce4b9eb4aa983486ba18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94055017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36070957d0133d63cda991ce0d5c386e90524ba1f43b9d6cb2114c0adff29dfa`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:25 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Fri, 27 Sep 2024 02:43:26 GMT
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2001248de490d09e03580d82567df39a6377d1b7bc6438b80f045348802020`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e5c3868b3ab8d295a312e2627b5eb5aae4d26fe22fa4c8732f03dbc5e5256b`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 7.4 MB (7387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b190bf09204a63267db1b7c1910be8bd0a7c6961ce6299a95ac8bed3920d397e`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 355.7 KB (355665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a36fe4ec66e9bf52c1c64efcdee3d6f8eab451846c24ee867524f0767071a8`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 76.4 KB (76430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bc289711a202f3e5706c78e5563294d7c47783ebd0a4f12861465a25ccbfb5`  
		Last Modified: Mon, 07 Oct 2024 18:05:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9721e986bb5ef4de6222fcff2a10961d32f5575df568685613977e47c9803a`  
		Last Modified: Mon, 07 Oct 2024 18:05:47 GMT  
		Size: 58.7 MB (58740233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf12e352ef273a44902be561aed5f9de83a6fea3c07e6c3592e5044a881660c`  
		Last Modified: Mon, 07 Oct 2024 18:05:45 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef71ec8be35d0903ab820bbc215bfce407f54b75ce96fbee6b201817cab3c8f`  
		Last Modified: Mon, 07 Oct 2024 18:05:45 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e06f8c396526cf0d9a8c68076edaf85d550e6e8cf493b8ad159ea047b3819`  
		Last Modified: Mon, 07 Oct 2024 18:05:46 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c03e022273ff6f3a58bb477f3fd09dff5aa2accebac6314440e55175b3b712`  
		Last Modified: Mon, 07 Oct 2024 18:05:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:8a6a211b5136e604bf30feab4ff42c48a564f45a335b0fe836ecb942d6874fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3753309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34d0ee4340e7c4c62639fcc845898d4d17579eab68857082cf92f962c0a1adc`

```dockerfile
```

-	Layers:
	-	`sha256:ea7c0e1d1b4ae4e84ea98af36ac6812f805790af82fe8823efaacf079a7ac826`  
		Last Modified: Mon, 07 Oct 2024 18:05:45 GMT  
		Size: 3.7 MB (3722276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a61e16bd446d7d268447470261d66609c12adacb4c65a7c32201e3c8753dd1`  
		Last Modified: Mon, 07 Oct 2024 18:05:45 GMT  
		Size: 31.0 KB (31033 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:92910f259df692ace51ac69d8a11e4c6fe37009c36e675fe3b3673adbb7dd589
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
$ docker pull couchdb@sha256:6f7304af9afc8cf0f0bee740d867584e2534bcd365aaba854f6a85d746ce695b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133500332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212fb806a99dd40948d6bbbd4a823fb5cf3329b47232a91cf38d126dfb028eff`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9442d790d6635e0b482db9e87cfb0cac90976dba8b8c97587193528324018d86`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdc3f69418039c0518a92ae7aba5811a85e436c9a6eb5122c28aae5b5f11c2e`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 7.7 MB (7653622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae297c75ee602d28290f293b626460f25e418eee654ce55b3832094ed3b8ad01`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 348.9 KB (348918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4250e6935cc5320d6b60fcb18f04d395f7da1124ffcf71b4e45e039776e94553`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 76.2 KB (76249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c412911b39adbd44f52383546496c2af710b6ccca5c9989e0ba373bc50b80e90`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd475490e141a14ac69667f3c350fcb6d140936cef9cd3007aa305d77e4cc5f6`  
		Last Modified: Mon, 07 Oct 2024 17:59:16 GMT  
		Size: 96.3 MB (96259732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5baaeef047eea69480cf0707d9e80c07f9a3d1b48f91eaa2ab40c01b1154d6`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374a0dd7ca701907840fe7937240a0ef12b8cb0daaf89a1cb2840a377272b8ec`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f09a5ca8e0ba7b12c4986347521af7a048b284dfb4bbad8c7f7bcbbc00118e`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8552ede7fbb1fb7d79984a5d6f3b386b0e261ad872026f1379e57881d893d42f`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:7b455ba696ae595140ce2d3688b57a4598a900bcc9ae90f74ee05e42d9eddc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9186f946aa7677ff5ce63c3755037aa75a3aaae00792b50fc00810fa16c96d23`

```dockerfile
```

-	Layers:
	-	`sha256:801a118eeb4f2f9e15b2a6fc955a4ffb05cf4f24a93952313e4299fea8503d19`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 3.9 MB (3931152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2a446b8215c1076b2dbea9b42b9b660a0c1f2effda481e563ed7da921101ed`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 31.8 KB (31805 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:7c01108575f86bd4a58fb4339c622c656c573688ec5097740ddef31855118609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130484414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c467056de202277fe0f85cd31f0db9c565e7419d0bd380a8bac0d954d2d74c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:25 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Fri, 27 Sep 2024 02:43:26 GMT
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2001248de490d09e03580d82567df39a6377d1b7bc6438b80f045348802020`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e5c3868b3ab8d295a312e2627b5eb5aae4d26fe22fa4c8732f03dbc5e5256b`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 7.4 MB (7387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b190bf09204a63267db1b7c1910be8bd0a7c6961ce6299a95ac8bed3920d397e`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 355.7 KB (355665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a36fe4ec66e9bf52c1c64efcdee3d6f8eab451846c24ee867524f0767071a8`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 76.4 KB (76430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65c70f2bb55367e98e72296838eff96f1ade898641d684c30f6774d5beffbd8`  
		Last Modified: Mon, 07 Oct 2024 18:00:50 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dda488e868e46e2aae9e22b7ed97f6b41842fc63fe9a427338ea2aabba9298`  
		Last Modified: Mon, 07 Oct 2024 18:00:52 GMT  
		Size: 95.2 MB (95169632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bfdd9b127b6c65f5e53539c6efcb481130d1aa56901341b6b2b5568d78555e`  
		Last Modified: Mon, 07 Oct 2024 18:00:50 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c9cf06d126bbba924308104e73165d5c3002527357b26fe6d0741771714530`  
		Last Modified: Mon, 07 Oct 2024 18:00:50 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4ead5c81ad58a81ed283dade2b03c5098d40700352417cdb27d76046490aab`  
		Last Modified: Mon, 07 Oct 2024 18:00:51 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64f37e57a06d60981346ed1ec7cdabbfed4707a89ea6ef646f57eb466be0fd6`  
		Last Modified: Mon, 07 Oct 2024 18:00:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:624ce0dfd11046ffec42a75bf12328cf355188371cc41a0ad3f64b25b37f1cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498a97d04d7643704d491e91c6d50be39e65bf67ebd38c752df182304d0b2789`

```dockerfile
```

-	Layers:
	-	`sha256:f98ff86261737a399d3f3ce5e0bbea20360b7434be910a91936b35c71b0448e8`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 3.9 MB (3930054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5414a7b7baf8e81541f56911a98eb1042d18a02697efa0f4550963887ace6b7b`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 31.6 KB (31615 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:a2d5d17f69db3fd25b5ee6f6e6cabaaabb37d90cd3e3fa4b418b50cca601d1ff
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
$ docker pull couchdb@sha256:6cb6aa93c071a1f3d35eddad7dd50bde831a6b69f0e0b3eb25b855da2c5795ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155211011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6720b48cd575172fe484da0a28d6e560e005e57eaedf0d66422fa1f685c424a0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dd4e3ec72ebd08003da9bae2a4f91d7054c7f219464df5c99dff6b44357474`  
		Last Modified: Mon, 07 Oct 2024 18:00:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b137a87f378e3c4b496ef8aee954623363575617dc3a5c7483f8c3ad1e6d2f`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 7.7 MB (7653599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438ad86fea8079ebaffc58a077adcfe370c3ebf5fdcc586a3a436f3fe702b64d`  
		Last Modified: Mon, 07 Oct 2024 18:00:24 GMT  
		Size: 76.5 MB (76508600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3de680e3bb5f4da4aa8fb277abfa4e3f9c789f961838de4afe48155fb5703f`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 371.7 KB (371699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c47625cd46d9f532742c73d6953d6f24d949e77ca64418792b5f53b862d254`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 99.2 KB (99217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d1f9143bb84d6b7c608ee25f6afea8af5874e2ae35e88d5c30d0da7ffe310`  
		Last Modified: Mon, 07 Oct 2024 18:00:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d508b85b561fba7d2e644cd77f5b8a05aed8f90a778f04fddd00ffa7253bcd2`  
		Last Modified: Mon, 07 Oct 2024 18:00:25 GMT  
		Size: 41.4 MB (41419645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b28d630547bae5f947878ebecabba5ef9b005b5f9fc3048b4edd72f28b51e9`  
		Last Modified: Mon, 07 Oct 2024 18:00:23 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f017d58d202848d8c80f74a5bcab5b6764f4e0c5c5051b4ce573865abdc4e42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3477517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3d3c9e59015ec1d1b521062e7c828ab3abcb3628a8738b55effe9f47eaa5dd`

```dockerfile
```

-	Layers:
	-	`sha256:3a582c389a53f22cadcb0f1e17a3270ec996f89250ca740ea9dd3572660cf229`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 3.5 MB (3452948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ab1f52acee1d1347095589a024c76cdb40a50b698e950c8dd8d1cd4a966ebb`  
		Last Modified: Mon, 07 Oct 2024 18:00:21 GMT  
		Size: 24.6 KB (24569 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:a769a37fa918495b7b9b4d6507ca0d845f438ea9fec4c8a92669465c6585666a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149595951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459e06e7a4838283c6ad7127f3ea08a349130672bbabb29c65ce5a81445032c9`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:25 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Fri, 27 Sep 2024 02:43:26 GMT
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cdd8ece04acd2127415e13f8bec0227eb84f82d8c1084c908d6660ea0a1fb2`  
		Last Modified: Mon, 07 Oct 2024 18:03:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a6697c4dda07211a6fe83879e5371efb32a06f9108171fa7c01a9beb8930c`  
		Last Modified: Mon, 07 Oct 2024 18:03:56 GMT  
		Size: 7.4 MB (7387297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9308f390eede38eeba97ddf2aae327974fe41a32a9c9adce6fc2b1dc369f062c`  
		Last Modified: Mon, 07 Oct 2024 18:03:57 GMT  
		Size: 73.0 MB (72988074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec8e46df547a8e2dfffb0951bad8e1ba159f114823579b772d4da45be50686`  
		Last Modified: Mon, 07 Oct 2024 18:03:55 GMT  
		Size: 378.2 KB (378168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f6ae7c1a5fb4a8048ba668ff13896a99ee959b58956d5601dc4c0cb905c6a3`  
		Last Modified: Mon, 07 Oct 2024 18:03:56 GMT  
		Size: 99.6 KB (99558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c97dd50ac3b237728d0973ecdebc18615d542963f377f2400c5dbba8ba08b3d`  
		Last Modified: Mon, 07 Oct 2024 18:03:56 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5477fdaef2dcad89941d20a4fbed9eb177641739f37f7c08ccf8ca015a22e489`  
		Last Modified: Mon, 07 Oct 2024 18:03:58 GMT  
		Size: 41.3 MB (41250948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9097da2b45c386dcbc78bfa352e23bab39155aa34aba43b0bdfa5796857302`  
		Last Modified: Mon, 07 Oct 2024 18:03:57 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:9f1139ae96caf97f1fc0738b5558bd23e20ce0b46f6a7b0d4369c402b91851ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3472186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3390060b4240d5b09ec2424441b839043844b748371bbf08b059cd10bf311311`

```dockerfile
```

-	Layers:
	-	`sha256:298aeec794eba0490e889885e1758cfb76a700f527aaaec4a4d4f8d572b784ed`  
		Last Modified: Mon, 07 Oct 2024 18:03:55 GMT  
		Size: 3.4 MB (3447794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc4fc686d3e2892bd2e501a3d3506ddb951ce2fd4858fcedd71fc428ab3f0984`  
		Last Modified: Mon, 07 Oct 2024 18:03:55 GMT  
		Size: 24.4 KB (24392 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.1`

```console
$ docker pull couchdb@sha256:92910f259df692ace51ac69d8a11e4c6fe37009c36e675fe3b3673adbb7dd589
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
$ docker pull couchdb@sha256:6f7304af9afc8cf0f0bee740d867584e2534bcd365aaba854f6a85d746ce695b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133500332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212fb806a99dd40948d6bbbd4a823fb5cf3329b47232a91cf38d126dfb028eff`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9442d790d6635e0b482db9e87cfb0cac90976dba8b8c97587193528324018d86`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdc3f69418039c0518a92ae7aba5811a85e436c9a6eb5122c28aae5b5f11c2e`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 7.7 MB (7653622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae297c75ee602d28290f293b626460f25e418eee654ce55b3832094ed3b8ad01`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 348.9 KB (348918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4250e6935cc5320d6b60fcb18f04d395f7da1124ffcf71b4e45e039776e94553`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 76.2 KB (76249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c412911b39adbd44f52383546496c2af710b6ccca5c9989e0ba373bc50b80e90`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd475490e141a14ac69667f3c350fcb6d140936cef9cd3007aa305d77e4cc5f6`  
		Last Modified: Mon, 07 Oct 2024 17:59:16 GMT  
		Size: 96.3 MB (96259732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5baaeef047eea69480cf0707d9e80c07f9a3d1b48f91eaa2ab40c01b1154d6`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374a0dd7ca701907840fe7937240a0ef12b8cb0daaf89a1cb2840a377272b8ec`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f09a5ca8e0ba7b12c4986347521af7a048b284dfb4bbad8c7f7bcbbc00118e`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8552ede7fbb1fb7d79984a5d6f3b386b0e261ad872026f1379e57881d893d42f`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:7b455ba696ae595140ce2d3688b57a4598a900bcc9ae90f74ee05e42d9eddc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9186f946aa7677ff5ce63c3755037aa75a3aaae00792b50fc00810fa16c96d23`

```dockerfile
```

-	Layers:
	-	`sha256:801a118eeb4f2f9e15b2a6fc955a4ffb05cf4f24a93952313e4299fea8503d19`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 3.9 MB (3931152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2a446b8215c1076b2dbea9b42b9b660a0c1f2effda481e563ed7da921101ed`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 31.8 KB (31805 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.1` - linux; s390x

```console
$ docker pull couchdb@sha256:7c01108575f86bd4a58fb4339c622c656c573688ec5097740ddef31855118609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130484414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c467056de202277fe0f85cd31f0db9c565e7419d0bd380a8bac0d954d2d74c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:25 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Fri, 27 Sep 2024 02:43:26 GMT
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2001248de490d09e03580d82567df39a6377d1b7bc6438b80f045348802020`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e5c3868b3ab8d295a312e2627b5eb5aae4d26fe22fa4c8732f03dbc5e5256b`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 7.4 MB (7387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b190bf09204a63267db1b7c1910be8bd0a7c6961ce6299a95ac8bed3920d397e`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 355.7 KB (355665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a36fe4ec66e9bf52c1c64efcdee3d6f8eab451846c24ee867524f0767071a8`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 76.4 KB (76430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65c70f2bb55367e98e72296838eff96f1ade898641d684c30f6774d5beffbd8`  
		Last Modified: Mon, 07 Oct 2024 18:00:50 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dda488e868e46e2aae9e22b7ed97f6b41842fc63fe9a427338ea2aabba9298`  
		Last Modified: Mon, 07 Oct 2024 18:00:52 GMT  
		Size: 95.2 MB (95169632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bfdd9b127b6c65f5e53539c6efcb481130d1aa56901341b6b2b5568d78555e`  
		Last Modified: Mon, 07 Oct 2024 18:00:50 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c9cf06d126bbba924308104e73165d5c3002527357b26fe6d0741771714530`  
		Last Modified: Mon, 07 Oct 2024 18:00:50 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4ead5c81ad58a81ed283dade2b03c5098d40700352417cdb27d76046490aab`  
		Last Modified: Mon, 07 Oct 2024 18:00:51 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64f37e57a06d60981346ed1ec7cdabbfed4707a89ea6ef646f57eb466be0fd6`  
		Last Modified: Mon, 07 Oct 2024 18:00:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:624ce0dfd11046ffec42a75bf12328cf355188371cc41a0ad3f64b25b37f1cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498a97d04d7643704d491e91c6d50be39e65bf67ebd38c752df182304d0b2789`

```dockerfile
```

-	Layers:
	-	`sha256:f98ff86261737a399d3f3ce5e0bbea20360b7434be910a91936b35c71b0448e8`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 3.9 MB (3930054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5414a7b7baf8e81541f56911a98eb1042d18a02697efa0f4550963887ace6b7b`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 31.6 KB (31615 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.1-nouveau`

```console
$ docker pull couchdb@sha256:a2d5d17f69db3fd25b5ee6f6e6cabaaabb37d90cd3e3fa4b418b50cca601d1ff
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
$ docker pull couchdb@sha256:6cb6aa93c071a1f3d35eddad7dd50bde831a6b69f0e0b3eb25b855da2c5795ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155211011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6720b48cd575172fe484da0a28d6e560e005e57eaedf0d66422fa1f685c424a0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dd4e3ec72ebd08003da9bae2a4f91d7054c7f219464df5c99dff6b44357474`  
		Last Modified: Mon, 07 Oct 2024 18:00:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b137a87f378e3c4b496ef8aee954623363575617dc3a5c7483f8c3ad1e6d2f`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 7.7 MB (7653599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438ad86fea8079ebaffc58a077adcfe370c3ebf5fdcc586a3a436f3fe702b64d`  
		Last Modified: Mon, 07 Oct 2024 18:00:24 GMT  
		Size: 76.5 MB (76508600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3de680e3bb5f4da4aa8fb277abfa4e3f9c789f961838de4afe48155fb5703f`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 371.7 KB (371699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c47625cd46d9f532742c73d6953d6f24d949e77ca64418792b5f53b862d254`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 99.2 KB (99217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d1f9143bb84d6b7c608ee25f6afea8af5874e2ae35e88d5c30d0da7ffe310`  
		Last Modified: Mon, 07 Oct 2024 18:00:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d508b85b561fba7d2e644cd77f5b8a05aed8f90a778f04fddd00ffa7253bcd2`  
		Last Modified: Mon, 07 Oct 2024 18:00:25 GMT  
		Size: 41.4 MB (41419645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b28d630547bae5f947878ebecabba5ef9b005b5f9fc3048b4edd72f28b51e9`  
		Last Modified: Mon, 07 Oct 2024 18:00:23 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f017d58d202848d8c80f74a5bcab5b6764f4e0c5c5051b4ce573865abdc4e42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3477517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3d3c9e59015ec1d1b521062e7c828ab3abcb3628a8738b55effe9f47eaa5dd`

```dockerfile
```

-	Layers:
	-	`sha256:3a582c389a53f22cadcb0f1e17a3270ec996f89250ca740ea9dd3572660cf229`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 3.5 MB (3452948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ab1f52acee1d1347095589a024c76cdb40a50b698e950c8dd8d1cd4a966ebb`  
		Last Modified: Mon, 07 Oct 2024 18:00:21 GMT  
		Size: 24.6 KB (24569 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.1-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:a769a37fa918495b7b9b4d6507ca0d845f438ea9fec4c8a92669465c6585666a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149595951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459e06e7a4838283c6ad7127f3ea08a349130672bbabb29c65ce5a81445032c9`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:25 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Fri, 27 Sep 2024 02:43:26 GMT
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cdd8ece04acd2127415e13f8bec0227eb84f82d8c1084c908d6660ea0a1fb2`  
		Last Modified: Mon, 07 Oct 2024 18:03:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a6697c4dda07211a6fe83879e5371efb32a06f9108171fa7c01a9beb8930c`  
		Last Modified: Mon, 07 Oct 2024 18:03:56 GMT  
		Size: 7.4 MB (7387297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9308f390eede38eeba97ddf2aae327974fe41a32a9c9adce6fc2b1dc369f062c`  
		Last Modified: Mon, 07 Oct 2024 18:03:57 GMT  
		Size: 73.0 MB (72988074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec8e46df547a8e2dfffb0951bad8e1ba159f114823579b772d4da45be50686`  
		Last Modified: Mon, 07 Oct 2024 18:03:55 GMT  
		Size: 378.2 KB (378168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f6ae7c1a5fb4a8048ba668ff13896a99ee959b58956d5601dc4c0cb905c6a3`  
		Last Modified: Mon, 07 Oct 2024 18:03:56 GMT  
		Size: 99.6 KB (99558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c97dd50ac3b237728d0973ecdebc18615d542963f377f2400c5dbba8ba08b3d`  
		Last Modified: Mon, 07 Oct 2024 18:03:56 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5477fdaef2dcad89941d20a4fbed9eb177641739f37f7c08ccf8ca015a22e489`  
		Last Modified: Mon, 07 Oct 2024 18:03:58 GMT  
		Size: 41.3 MB (41250948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9097da2b45c386dcbc78bfa352e23bab39155aa34aba43b0bdfa5796857302`  
		Last Modified: Mon, 07 Oct 2024 18:03:57 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:9f1139ae96caf97f1fc0738b5558bd23e20ce0b46f6a7b0d4369c402b91851ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3472186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3390060b4240d5b09ec2424441b839043844b748371bbf08b059cd10bf311311`

```dockerfile
```

-	Layers:
	-	`sha256:298aeec794eba0490e889885e1758cfb76a700f527aaaec4a4d4f8d572b784ed`  
		Last Modified: Mon, 07 Oct 2024 18:03:55 GMT  
		Size: 3.4 MB (3447794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc4fc686d3e2892bd2e501a3d3506ddb951ce2fd4858fcedd71fc428ab3f0984`  
		Last Modified: Mon, 07 Oct 2024 18:03:55 GMT  
		Size: 24.4 KB (24392 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:92910f259df692ace51ac69d8a11e4c6fe37009c36e675fe3b3673adbb7dd589
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
$ docker pull couchdb@sha256:6f7304af9afc8cf0f0bee740d867584e2534bcd365aaba854f6a85d746ce695b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133500332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212fb806a99dd40948d6bbbd4a823fb5cf3329b47232a91cf38d126dfb028eff`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9442d790d6635e0b482db9e87cfb0cac90976dba8b8c97587193528324018d86`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdc3f69418039c0518a92ae7aba5811a85e436c9a6eb5122c28aae5b5f11c2e`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 7.7 MB (7653622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae297c75ee602d28290f293b626460f25e418eee654ce55b3832094ed3b8ad01`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 348.9 KB (348918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4250e6935cc5320d6b60fcb18f04d395f7da1124ffcf71b4e45e039776e94553`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 76.2 KB (76249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c412911b39adbd44f52383546496c2af710b6ccca5c9989e0ba373bc50b80e90`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd475490e141a14ac69667f3c350fcb6d140936cef9cd3007aa305d77e4cc5f6`  
		Last Modified: Mon, 07 Oct 2024 17:59:16 GMT  
		Size: 96.3 MB (96259732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5baaeef047eea69480cf0707d9e80c07f9a3d1b48f91eaa2ab40c01b1154d6`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374a0dd7ca701907840fe7937240a0ef12b8cb0daaf89a1cb2840a377272b8ec`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f09a5ca8e0ba7b12c4986347521af7a048b284dfb4bbad8c7f7bcbbc00118e`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8552ede7fbb1fb7d79984a5d6f3b386b0e261ad872026f1379e57881d893d42f`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:7b455ba696ae595140ce2d3688b57a4598a900bcc9ae90f74ee05e42d9eddc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9186f946aa7677ff5ce63c3755037aa75a3aaae00792b50fc00810fa16c96d23`

```dockerfile
```

-	Layers:
	-	`sha256:801a118eeb4f2f9e15b2a6fc955a4ffb05cf4f24a93952313e4299fea8503d19`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 3.9 MB (3931152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2a446b8215c1076b2dbea9b42b9b660a0c1f2effda481e563ed7da921101ed`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 31.8 KB (31805 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:7c01108575f86bd4a58fb4339c622c656c573688ec5097740ddef31855118609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130484414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c467056de202277fe0f85cd31f0db9c565e7419d0bd380a8bac0d954d2d74c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:25 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Fri, 27 Sep 2024 02:43:26 GMT
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2001248de490d09e03580d82567df39a6377d1b7bc6438b80f045348802020`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e5c3868b3ab8d295a312e2627b5eb5aae4d26fe22fa4c8732f03dbc5e5256b`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 7.4 MB (7387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b190bf09204a63267db1b7c1910be8bd0a7c6961ce6299a95ac8bed3920d397e`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 355.7 KB (355665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a36fe4ec66e9bf52c1c64efcdee3d6f8eab451846c24ee867524f0767071a8`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 76.4 KB (76430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65c70f2bb55367e98e72296838eff96f1ade898641d684c30f6774d5beffbd8`  
		Last Modified: Mon, 07 Oct 2024 18:00:50 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dda488e868e46e2aae9e22b7ed97f6b41842fc63fe9a427338ea2aabba9298`  
		Last Modified: Mon, 07 Oct 2024 18:00:52 GMT  
		Size: 95.2 MB (95169632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bfdd9b127b6c65f5e53539c6efcb481130d1aa56901341b6b2b5568d78555e`  
		Last Modified: Mon, 07 Oct 2024 18:00:50 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c9cf06d126bbba924308104e73165d5c3002527357b26fe6d0741771714530`  
		Last Modified: Mon, 07 Oct 2024 18:00:50 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4ead5c81ad58a81ed283dade2b03c5098d40700352417cdb27d76046490aab`  
		Last Modified: Mon, 07 Oct 2024 18:00:51 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64f37e57a06d60981346ed1ec7cdabbfed4707a89ea6ef646f57eb466be0fd6`  
		Last Modified: Mon, 07 Oct 2024 18:00:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:624ce0dfd11046ffec42a75bf12328cf355188371cc41a0ad3f64b25b37f1cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498a97d04d7643704d491e91c6d50be39e65bf67ebd38c752df182304d0b2789`

```dockerfile
```

-	Layers:
	-	`sha256:f98ff86261737a399d3f3ce5e0bbea20360b7434be910a91936b35c71b0448e8`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 3.9 MB (3930054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5414a7b7baf8e81541f56911a98eb1042d18a02697efa0f4550963887ace6b7b`  
		Last Modified: Mon, 07 Oct 2024 18:00:49 GMT  
		Size: 31.6 KB (31615 bytes)  
		MIME: application/vnd.in-toto+json
