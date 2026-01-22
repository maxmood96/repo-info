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
$ docker pull couchdb@sha256:807777b6959fc62a2c9aacb106801958aeb5cd1ad6702ea088b097fc9254c812
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
$ docker pull couchdb@sha256:2faf97d82be3b8e2e0fd173e3bc4e67884e9011d879c714a8141eee09df8adc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142052823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7592237039b089be7b880c271678bc3579faac60cb0587b345e23fec5a9eee2b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:14:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:14:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:14:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:14:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:14:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:14:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:14:56 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 13 Jan 2026 02:14:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:15:10 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:15:10 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:15:10 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65668050ee4fff6ffc324deeecc855a5edc306f51f75495afda962d9b95fee3`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef092487b8e085fdd5a53276c40804702cbb30056554f07cb62e2a585fb504`  
		Last Modified: Tue, 13 Jan 2026 02:15:34 GMT  
		Size: 7.9 MB (7882815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1625328358e7c4f114db767f71d128159db9927da240b55ec3ff572ac32f271e`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 401.8 KB (401765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ea7c769291675b331353621a8a96dcb7d17c0635a82cf72edba9e480076ed7`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 76.5 KB (76468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3befc99dc1ef62e4e1a0159203d775cc92ebc726e0337970bd1d937558a687bc`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95626de1d3cc022e0ce5e46ae38ec64d43761a98f86359d38a406c49cfc1e21b`  
		Last Modified: Tue, 13 Jan 2026 02:15:28 GMT  
		Size: 105.5 MB (105457774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be435982d8e428187ab0e23eae0a28b0a4ad61778dfa22f55e3a7157100905d7`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54435d0898ce3275b13d988e710467402ab4e9c30caee10184ac59350825be94`  
		Last Modified: Tue, 13 Jan 2026 02:15:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a47f4532a195230a2d585c3853de7c4e893a2aeb302dc9311e234a440f65db1`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c26d4890aa2a7493468c0f215e2cc6db87c9c89d751ab496afc608dc39a90a`  
		Last Modified: Tue, 13 Jan 2026 02:15:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:fa8c717021cc9fc013daae4ba425d930ec405ecb3a8fbe0fa9f176d341294586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d931371c4b2577bf9b491cab1882aeaffc04948bd594fa4518dac27887a3cace`

```dockerfile
```

-	Layers:
	-	`sha256:b51bfcbaddf6f778122953634cec76bf80f8b87c2df375435f470c16035a6133`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e447e3285c5f32e36954b4e69925a6b22330d15789d572059cc34e64f69ab3`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6b0db438d94421e92e27205855d09734387555d0fc8600ae45cff6d7bc2fdccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141410286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9b49c67b1da801d07afc112059f0cdd53e608651866ed69d81532688b27952`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:20:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:20:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:20:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:20:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:20:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:20:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:20:22 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 13 Jan 2026 02:20:23 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:20:36 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:20:36 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:20:36 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3ca5a073a02ca64d9249d2d01fa3abec601f82df4068f9d5ea27ddd387e5a`  
		Last Modified: Tue, 13 Jan 2026 02:21:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8eca98d844737e7391af0ba3bd078c33c9b79484694a82e1a51f2a29ebfc0b`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 7.7 MB (7693190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d4cff2a33ca97c469fc8ab6c3284395941ba8b2cff8f4361b3ab4a1b366eb5`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 370.5 KB (370523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1750e79248720e1a6c634304014602e07922aebc5e6023966b221b9f20ec3caa`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58782965d94ab6045938a5166643200c31af7af20c84605939e3838508c56a6e`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b24eaea20d17a3d6692890e122cfa1219e4f614dc51c6330fee6ffe9a08394`  
		Last Modified: Tue, 13 Jan 2026 02:21:07 GMT  
		Size: 105.2 MB (105156763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c03434704503155ed2343afd552fb957cce1a8b2680b8b7d8344138e2a6597`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d999d45b1b181000acaa083e513b632b05025450d49f6009d16400b8cf257624`  
		Last Modified: Tue, 13 Jan 2026 02:20:52 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc56c71044322b328f24d81b4873610894af8d49b91b8a31513590266fe49`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cd1196c4cb96149708b21622838788a0cf61a569067e10485f4f12efecb2c4`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:8ed481b2cca03c4b8f6865b96bc4487ca3baf31d374e87e1042258c20f49835e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058521c08ed24183df84ea24cb46e15ee8bdab36f0b6edc88fad29b3d2b84dd6`

```dockerfile
```

-	Layers:
	-	`sha256:6ce1950ba463d86989dad05da95562dec1791435eea9bfe733ae0d0dd83cbf76`  
		Last Modified: Tue, 13 Jan 2026 05:34:22 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50d4d6e4b72e86f1a95b7c50ce2ca2099a3a9a898205250f448399f4b707c08`  
		Last Modified: Tue, 13 Jan 2026 05:34:23 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:139b01b18130e4eba640cb445a9e7d1b3e3a3fcd027825f6ff3f9b71cc5b0285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bd435ca916c01cf53ce4171ab2c6b4b5274da8320019459562442221c81ef3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:10:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:10:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:11:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:11:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:11:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:11:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:11:12 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 13 Jan 2026 02:11:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:11:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:11:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:11:28 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:11:28 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917438ccf21f82cc4ec739c692b1e6658c435f0a12c554886df4b813b8393a07`  
		Last Modified: Tue, 13 Jan 2026 02:11:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992643008fb7fd06b94615d5a14ccc131460a03377233b78dd99940b3cb5a0d8`  
		Last Modified: Tue, 13 Jan 2026 02:11:47 GMT  
		Size: 7.4 MB (7398641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba4b929d3acd257fa813f3e05d9fe6f3ae2dd7d64f6bfad71fd98dba1a96dcd`  
		Last Modified: Tue, 13 Jan 2026 02:11:47 GMT  
		Size: 372.1 KB (372125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ca133eea8fb7e3e077be0ffb572d23a957e13cd0b40350b832226ea242cb7f`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 76.5 KB (76524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba6813ea1a509056adbb50701a6b9865c4a565465f877d267838570fa89c579`  
		Last Modified: Tue, 13 Jan 2026 02:11:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec669509929847ca409489e4d842bcb9ed817d58a6c6aa844116db80bc9edf66`  
		Last Modified: Tue, 13 Jan 2026 02:11:50 GMT  
		Size: 104.0 MB (104028284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06976128bdee8873e804e0c7ae73bbc13a363bba2a49d7a8e04c2d7855445774`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa29432fe4cf4e91ebf233fa162f196d07e46067ef2f20dc60efa8d8cf5938e4`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24ae66325dcc03c8efe8a49da9e0281c0633a1a5a2c36069aef9b74c9031229`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75955a7c6c4ebbb7ff713f82d362ae34076e2a937b9d33528de8c9b734ebed53`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:15142dad18f8914978b877cc135a50744dac73512016cf1c52553f3c69450438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13526edacd43b322a1e160ea21b1af95d90bee139a9ab8011dfedb3c3e4dfe84`

```dockerfile
```

-	Layers:
	-	`sha256:2965573c39f0ef0700fb3ffa54797b2030fb98a69f07925d459c7ff9af51d001`  
		Last Modified: Tue, 13 Jan 2026 02:35:21 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d5ce1f869bb7d38d07b5d96b3f9ab7cb0d5095985b441e97d8f837a4865583d`  
		Last Modified: Tue, 13 Jan 2026 02:35:22 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:5e3817f5d2201583513d949d6eac0b1d80210c6aa6bf6c2224aa2ebe47bc28cb
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
$ docker pull couchdb@sha256:42f9a35d1efda446f5b9fdb594bdddd3d5ed206f7709395195787fbd13e5ad21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156454284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036fec60d81a0640468c84a8ab8b24076fe4f18ffcaa319c5042beee216fa24e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:15:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:15:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:15:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:15:29 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:29 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:15:35 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:15:35 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:15:35 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:15:35 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:15:35 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c834d3aa6aa1da84b367673eef2a5defda4c0a6aad9a85c1c2e1f8b62bb44fd9`  
		Last Modified: Tue, 13 Jan 2026 02:15:51 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fd8037c3f5048c25e79b7e47b64dba31ed258b3cd21bc6dadbcd36167c8365`  
		Last Modified: Tue, 13 Jan 2026 02:15:51 GMT  
		Size: 7.9 MB (7882903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11ee3d1543b2c5e62d73c98423445473edc94adc96b3b016536c6091284ba13`  
		Last Modified: Tue, 13 Jan 2026 02:15:53 GMT  
		Size: 77.4 MB (77380783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f90d57870c99c4e73f48597d4ef590f6ce8f250da2e4763c6eadbac7254a716`  
		Last Modified: Tue, 13 Jan 2026 02:16:00 GMT  
		Size: 424.2 KB (424157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f97172c82c74b8a0cddd5c66b9220fff14f737bd1fa8f158fd799aacddac1b`  
		Last Modified: Tue, 13 Jan 2026 02:16:00 GMT  
		Size: 99.6 KB (99557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200974d13c17278793a656b27a69a741c454fa4b56b35dab14d78d195fc05610`  
		Last Modified: Tue, 13 Jan 2026 02:16:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75876e25c55566e584310d0969acf710ab2331cd8e7e444e8d2d29d28989f221`  
		Last Modified: Tue, 13 Jan 2026 02:15:54 GMT  
		Size: 42.4 MB (42436433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d06fbc7300cb5e82a9eba336329c31ebc1dafa8c95520fd2ed2339bd9dae4d6`  
		Last Modified: Tue, 13 Jan 2026 02:16:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dbd2f2f9b113ca9737a845cfc958babbab8a2872e4779e2f39399c5428e09578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65f465453f712c9a4e51486a3f7ae4f69d56514ad3f9f57e5b7f14fe98bb9a4`

```dockerfile
```

-	Layers:
	-	`sha256:cfdac44fc4100793a76ec5945deec66105528ef1786dc7f5d563a89216d270b2`  
		Last Modified: Tue, 13 Jan 2026 05:34:26 GMT  
		Size: 3.7 MB (3658099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a24cd09a6b98e0a5c34370502688d6d23633227b2ae453edb8d7b57fd95c4402`  
		Last Modified: Tue, 13 Jan 2026 02:15:51 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:34039d5ed14a1c27b7af653d30ef8d04ab4da250283482a6926c9f9d67d38dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155326005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534de1b157c124931435b169c227299f70f5a18fa09e67ef97de1a048de73090`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:20:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:20:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:20:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:20:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:20:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:20:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:21:00 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:21:00 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:21:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:21:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:21:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:21:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:21:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c557e8470a8a15f08a810286fc29f026da97144910c8cb843d46251278ee184`  
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a950b57072984c0e96c033ed51300854efba14b435d84da94826cd198297a83`  
		Last Modified: Tue, 13 Jan 2026 02:21:31 GMT  
		Size: 7.7 MB (7693146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb5da74a812f294be30343ff89ed9604ba248e5e135425a3bb7906968f1e64`  
		Last Modified: Tue, 13 Jan 2026 02:21:23 GMT  
		Size: 76.7 MB (76691847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66868d5948d44e96078e5fa525df7e09c89d0e7cc0cb09f0fc48aeeb30707c4e`  
		Last Modified: Tue, 13 Jan 2026 02:21:30 GMT  
		Size: 392.7 KB (392739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b4cd7f59188339c71711d75181a6f4fd7fab268e8ca419321d58f9759d5a1`  
		Last Modified: Tue, 13 Jan 2026 02:21:22 GMT  
		Size: 99.5 KB (99466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d1f922c928a80bb685cb6e00a39fd3e289a4a71153df9e0713dc6f8ca02ff`  
		Last Modified: Tue, 13 Jan 2026 02:21:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a9a35bcdaffcf54721526f54af996ac768b9174620e4c63db9965d9df21250`  
		Last Modified: Tue, 13 Jan 2026 02:21:24 GMT  
		Size: 42.3 MB (42339037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6912598d1a802a2bd6ac00a98fbe61355007e81d599a86a596d2eb2306e37347`  
		Last Modified: Tue, 13 Jan 2026 02:21:23 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:05d5c8faab853cd6342bd862473efd6a0ef1e36ad8a8d662a4d9bda0df468fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b019f9cacd2b003329688e392435d942055450c0b59e2f32a6248a85a7b9f3d8`

```dockerfile
```

-	Layers:
	-	`sha256:6d88198d1f122d7c6ee4b1ac07a559c13e3675218835db2550b515d10a23b739`  
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 3.7 MB (3656775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceb99cef1c693ed23e90314454a0ad427bfc99d16beeef04f91e068596fb7504`  
		Last Modified: Tue, 13 Jan 2026 05:34:35 GMT  
		Size: 24.7 KB (24702 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:090226f5f3381e086d4ca01905405b65bf2cbda4054d3eeea595666cf296f079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150087066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d697e036a9dc8f41a88f6bf82f3c5ef10241a1245b55b62fd42c3131681f04`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:11:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:11:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:12:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:12:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:12:20 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:20 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:12:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:12:28 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:12:28 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:12:28 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:12:28 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73bbb2b620b04ded8354b575b5134f4a498c331a7c6039ec6259f44f2e55ee4`  
		Last Modified: Tue, 13 Jan 2026 02:12:49 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebfeaea45624160791afec65772aef817d039bf449f8688c0147dbbcc27f9e2`  
		Last Modified: Tue, 13 Jan 2026 02:12:50 GMT  
		Size: 7.4 MB (7398640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8651b9ab7326e7aa269290a9c469fca82ecf80dfe7d638dcb856c21e1630ef9a`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 73.1 MB (73143293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acff0900ca2683b601b51373dc2f6f260ac3500b6e8ce9c8d4c678f25d35fb4b`  
		Last Modified: Tue, 13 Jan 2026 02:12:49 GMT  
		Size: 394.5 KB (394487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84412345919376d985a34e5620ace1867e5cc1b817280bcb02e00cf6a7a4d8c`  
		Last Modified: Tue, 13 Jan 2026 02:12:57 GMT  
		Size: 99.7 KB (99650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c09398cba81cc4d6231fae65fbcd9f3a583ee297ab1323f084116107bd3e24`  
		Last Modified: Tue, 13 Jan 2026 02:12:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1194cd6b832369837b0dddcedd825c3b8f7721b5e7ec3f4c3c70e732d9e200`  
		Last Modified: Tue, 13 Jan 2026 02:12:52 GMT  
		Size: 42.2 MB (42164704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546ce6ac21b40929413de3114353fd57420d4452084eca81b3909d4c036ac8d9`  
		Last Modified: Tue, 13 Jan 2026 02:12:57 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:188e240d273a0cf3218a6907208cab9335a609571450fe212fe5af1c7bd48f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341cc961a96be1e8cf31a4dbd08fffd6c38bf891f16824357ff2997c8502ba3e`

```dockerfile
```

-	Layers:
	-	`sha256:ca51397e2dca8c25972475a34a2d3cc7779d73d0f6924ca91cdf703cd450188f`  
		Last Modified: Tue, 13 Jan 2026 02:35:26 GMT  
		Size: 3.6 MB (3648628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:570e02ee2ecf094a674b942bda5990333d969a63ad2a1908c907d4ab0bf2e248`  
		Last Modified: Tue, 13 Jan 2026 02:12:49 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:79ee45d0b6f735727989aad838265c7e90103b3ccf0350c2e87fff4081282a2e
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
$ docker pull couchdb@sha256:8ef0a04b2239e8d866fe8e0eebc72d7c0ad15dda2b530308c4c1b6393cf90ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139015220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edf20b5c27c82c97afb48f0a425290210b5030af4a5e5c11d83cef0b7b39450`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:15:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:16:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:16:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:16:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:16:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:16:10 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 13 Jan 2026 02:16:10 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:16:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:16:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:16:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:16:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:16:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:16:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:16:23 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:16:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:16:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273919e82c352c9f4e6cf0411272319b0233243139e70a3262a5b85cf6cee7b6`  
		Last Modified: Tue, 13 Jan 2026 02:16:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046556b37207d8f42bda47a4c7349d081e707c8d0b95f538e647e846806f66f8`  
		Last Modified: Tue, 13 Jan 2026 02:16:46 GMT  
		Size: 7.9 MB (7882841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980f4534d63c4550e4430ebdaa4f20cbc0e952ac496625d1a5c1562a4d8a7df8`  
		Last Modified: Tue, 13 Jan 2026 02:16:36 GMT  
		Size: 401.8 KB (401773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701857d6ee2fedbce6dfdb9f1724131c5e72632b82ec4702432016d9980e3c74`  
		Last Modified: Tue, 13 Jan 2026 02:16:36 GMT  
		Size: 76.5 KB (76524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433290a3aebf6ca3501ab2cbf16c6b6c4816c8a7685f166aa57ec58ff30a1f21`  
		Last Modified: Tue, 13 Jan 2026 02:16:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d0d05971862f2d01862ebc084ab8b561562e8070503fa663c889bb72efa4bf`  
		Last Modified: Tue, 13 Jan 2026 02:16:54 GMT  
		Size: 102.4 MB (102420077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e98dbdf723fee0422d3f2ce58448f5de3b6da329e923baf7928c17ea0191ed`  
		Last Modified: Tue, 13 Jan 2026 02:16:38 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd3a5b4e241146faa56adf749caa3ee7e1ee96413c2c26283fbb828662c7a1`  
		Last Modified: Tue, 13 Jan 2026 02:16:46 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14c06f7ee3aaa5402e6e24efdfeef184d0241d136d5a3d92ac1145829856178`  
		Last Modified: Tue, 13 Jan 2026 02:16:39 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e4ce922e2278d7ffb02b94d8eeb9e93e9ea662465d96b270b6248e12403da3`  
		Last Modified: Tue, 13 Jan 2026 02:16:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:040ee0f019b21a0d06786499decbe2757e53dfea21d734780578700e02d0deed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28894f5e2a516b4fa4c82762c708642f3870352389d90a1ee3313274e34b066`

```dockerfile
```

-	Layers:
	-	`sha256:c77083a88483b74b425e250a335c68098c8be77c42412f9cc4c6d7144923091e`  
		Last Modified: Tue, 13 Jan 2026 02:16:36 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5efedac1c87a348951da2270b30ef1c7932d759b8da14775891e9ff6e25e1928`  
		Last Modified: Tue, 13 Jan 2026 02:16:36 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:1af7c91436e599ab8f4fae3002a5bfac1263c50f6b0e8505240553b88f7acea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138422550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826f37a2f2000dc2845971cf7abac8a0b76323496483e4a140b1e456c9e3337a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:21:17 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:21:17 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:21:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:21:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:21:26 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:21:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:21:31 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 13 Jan 2026 02:21:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:21:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:21:44 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:21:44 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:21:44 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:21:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:21:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:21:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:21:44 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:21:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afb235c9cd033ee5e31809a77e65c965b16eb7f884f506c17397113f79c0198`  
		Last Modified: Tue, 13 Jan 2026 02:21:57 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75968d17e63ff8441c1ee5d8699c0cf8b327568b173971076d8985f1e8ffbe7b`  
		Last Modified: Tue, 13 Jan 2026 02:22:07 GMT  
		Size: 7.7 MB (7693187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e0783e8739b88f04c92eb1b3936f5047d8a36ba4044fbf5fe21580ceb39f0c`  
		Last Modified: Tue, 13 Jan 2026 02:22:09 GMT  
		Size: 370.5 KB (370522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d88aa04437e2ce164a28fd76913203215b1003379a5c835da38c57ceb6900ee`  
		Last Modified: Tue, 13 Jan 2026 02:22:06 GMT  
		Size: 76.5 KB (76482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d032fa4100c076bee3e5cf37b8a3b1b2a3de179b8118cbefb7a153a96da1c37`  
		Last Modified: Tue, 13 Jan 2026 02:22:06 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce57e808f2a9831c927cbec451efdea32a3082f88d25f35b5baff7da114c4fab`  
		Last Modified: Tue, 13 Jan 2026 02:22:14 GMT  
		Size: 102.2 MB (102169041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11db5c308963aceb8beaada642c7e71ae7449a090fd88316616154d50b8119ad`  
		Last Modified: Tue, 13 Jan 2026 02:21:58 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee4dd86fbd2c326e30cc521ca4e359963a65520372f58de359be0571e2753da`  
		Last Modified: Tue, 13 Jan 2026 02:21:59 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3918fc48c45c64d7a9d60bec4cce028537d75297a8d88eaf6bdeccc7dd712e`  
		Last Modified: Tue, 13 Jan 2026 02:22:06 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ce7b287af1d5de35d38fcd17af289d9af21e1e3a3e9db336510be0f63dc753`  
		Last Modified: Tue, 13 Jan 2026 02:22:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:c54a8accd27432c02853d47b7c55f7b9008e7681cf224b5265ff148e6da9ad99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28826f2132e4601b4ee2c5574493de2237676c2734667860ac67e8c2877ae33`

```dockerfile
```

-	Layers:
	-	`sha256:2b3ee0c7b1ccfa193ab1dcc72e14fc8f89f0ebfd3c06d1742767a560d12eb7f0`  
		Last Modified: Tue, 13 Jan 2026 05:34:44 GMT  
		Size: 4.1 MB (4125664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20c92a325d7b334410edd982cf7efdca1b61238606683f7ca6a9788c22cab8fc`  
		Last Modified: Tue, 13 Jan 2026 05:34:45 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:06d269308016856c8a2842ef5ab895d42d2657cdfd771ddd270c5a36123d3bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135793601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d737cba8646c24fa6b1ee3d1257dce3086824c2917e28997bcb7f2de869234`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:12:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:12:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:12:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:12:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:54 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 13 Jan 2026 02:12:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:13:09 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:13:09 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:13:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485d372642975bebfa1a9e8ae9395f15d571f0417420c777905c28d64a2b2f9d`  
		Last Modified: Tue, 13 Jan 2026 02:13:28 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69711dd15fee6f3d2ddb9d99a111262a82c12bd0efc597671a710e24b40cf8`  
		Last Modified: Tue, 13 Jan 2026 02:13:38 GMT  
		Size: 7.4 MB (7398631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40148f85ebce9e7f165cf9f74d2ca2064133ae2d56f1cc04cf1bc986ccf2dcb4`  
		Last Modified: Tue, 13 Jan 2026 02:13:37 GMT  
		Size: 372.1 KB (372137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ffd3610106102547c57aad98e600d685f6dbb163bbcf00efdc7a0722df608`  
		Last Modified: Tue, 13 Jan 2026 02:13:28 GMT  
		Size: 76.5 KB (76549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126faf625507cec0622126ff7e1606026406e150400954f77184125a23fcc646`  
		Last Modified: Tue, 13 Jan 2026 02:13:37 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68e4bbfb3d5682088bf5684a52b2c0560c421d735078174a69b1691c9b1a186`  
		Last Modified: Tue, 13 Jan 2026 02:13:31 GMT  
		Size: 101.1 MB (101056441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0be475e56fe2c3cedeac33307059ae08b9694c18599d73e01f86cad2f2811b`  
		Last Modified: Tue, 13 Jan 2026 02:13:29 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4034b7b4cb801e6fdeac097c268cd99f9bd67b06b3b7a5702424ac6623115c4f`  
		Last Modified: Tue, 13 Jan 2026 02:13:30 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8747f3bfef41d8c94bf3797d7d24b7bc216a14e8b4eba46f7790992c48cc12c`  
		Last Modified: Tue, 13 Jan 2026 02:13:37 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ba2b604dedb448bcb5b2c7723d54396bffaa4d0841fcdf6f02ede674819903`  
		Last Modified: Tue, 13 Jan 2026 02:13:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:bb4aae3ee3ddf5c028b6e0975f6741a641d45d3a0fb6f4eb3e626db91c5ba827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf4d12fc47edd521dfc88cc6344da32da1a6e7af769d553ced6e492bd377639`

```dockerfile
```

-	Layers:
	-	`sha256:c98afd37f3e444831a659e0e3a0c9d6982a87350fe658d349e5fc21e136a183c`  
		Last Modified: Tue, 13 Jan 2026 05:34:48 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17b4c4915378568a51ff1a90cecdb4a3d6a05404bed548ce2133877d129fc14b`  
		Last Modified: Tue, 13 Jan 2026 05:34:52 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:f674509597cb2246ef6b35a20bdb3348710c861fec65a5d27ffed2e791b55155
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
$ docker pull couchdb@sha256:26a101fa397f4a5ea51c63347edd06160e0eedad47f72710ed9d1374b8bc9ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156453580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e334d6b6aeb0568f94a4fde635ff05e3ae46720c64b78e4a2a6e555bec7a1e89`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:16:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:16:29 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:16:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:16:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:16:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:16:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:16:48 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:16:48 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:16:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:16:53 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:16:53 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:16:53 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:16:53 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b35917d978112f9be4d6a8e1684394e7f59b7322fdb9837f9186888c7e7cb20`  
		Last Modified: Tue, 13 Jan 2026 02:17:17 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7640be4ecf658b81eb9d0f9c99cbe92504028ceac2455a5ed450db418d6767`  
		Last Modified: Tue, 13 Jan 2026 02:17:08 GMT  
		Size: 7.9 MB (7882786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e5113e0bc38736c1ebb3d009f67ad8916a61047581cf29382ea1635668fa1`  
		Last Modified: Tue, 13 Jan 2026 02:17:10 GMT  
		Size: 77.4 MB (77380594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54ec4a4daac83741d28e7727d85cc835764641939a207eea5fc6ef89f02b342`  
		Last Modified: Tue, 13 Jan 2026 02:17:08 GMT  
		Size: 424.1 KB (424137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d844b322bf381853cef7725090a1277b4fd37e78678dd5676deea34504f037`  
		Last Modified: Tue, 13 Jan 2026 02:17:09 GMT  
		Size: 99.5 KB (99535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b3b6576456713a7e553f0a9e398d3b6ac6fea2690a5df7741dc29905c5d80b`  
		Last Modified: Tue, 13 Jan 2026 02:17:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698d51cf70127c70b0ea92bb00f8d42cf87bd1a235e92fcbb341b75939e4e0cd`  
		Last Modified: Tue, 13 Jan 2026 02:17:24 GMT  
		Size: 42.4 MB (42436078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4196cfcab8ea171ffccbbde3d93d965694a0b118c78f015aa55729cf054e41e3`  
		Last Modified: Tue, 13 Jan 2026 02:17:17 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:95b2277a2a6de862de6cf46a6fea87d809d80cd7eac50a989f1e94d7cf531032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed829a980979afec6b61845323b8aefc4ac9c7985195cda16c6ffd2137f2e15`

```dockerfile
```

-	Layers:
	-	`sha256:13ec81de43fd1dfea8a19368e26ba6c6180f4d7fd685ddff15dd1e385b0d80a7`  
		Last Modified: Tue, 13 Jan 2026 02:17:08 GMT  
		Size: 3.7 MB (3657793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca8c12ef89424df6024f769bee47d73e79e9ae910f85529a6d53fbfc184c26b`  
		Last Modified: Tue, 13 Jan 2026 05:34:54 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:fa3feb65966c539064d2a7a66c8ccb7a53bff437da1ad6149c84135fb8d8ae16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155325157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fd6378c4557c93373eab99e9f3067837f801b341b1aefc75a2379f67dffcd3`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:22:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:22:29 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:22:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:22:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:22:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:22:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:22:50 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:22:50 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:22:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:22:56 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:22:56 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:22:56 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:22:56 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb077f697a9faa28df744a1f3c43fedf166dfbffa9e7df93f422228c5aceeece`  
		Last Modified: Tue, 13 Jan 2026 02:23:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6eb57c01e90651acba770ed9077031c2d1f894e820a6a77fab5fc3f062c5ac`  
		Last Modified: Tue, 13 Jan 2026 02:23:21 GMT  
		Size: 7.7 MB (7693195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92378f8e2c7fa5184fef765384307a8f0d8d4be6ab9aef65ae867d78df1c7220`  
		Last Modified: Tue, 13 Jan 2026 02:23:14 GMT  
		Size: 76.7 MB (76691818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6eb9ed2f797a97ee19983ec050f73e5f63e2f8a6b65f873309932b79ed2b68`  
		Last Modified: Tue, 13 Jan 2026 02:23:23 GMT  
		Size: 392.8 KB (392750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6149b46e4eb75af61de43c8d402dd4882d4b893beea4bdf54286e15c4545189`  
		Last Modified: Tue, 13 Jan 2026 02:23:20 GMT  
		Size: 99.5 KB (99498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffafb2a57977e0b46429ecdddcf7d4f022cb81a1cf5a16a973ca642467283206`  
		Last Modified: Tue, 13 Jan 2026 02:23:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7327d876b5fc48a1f620ef884d5f099170a9f3ba0cd76bcd13ef5bc178484d`  
		Last Modified: Tue, 13 Jan 2026 02:23:24 GMT  
		Size: 42.3 MB (42338126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcbedab60f1f391d8b76cde4fe951e417fcf8398ffd0a21a17e514866dd65be`  
		Last Modified: Tue, 13 Jan 2026 02:23:20 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:0639378fd9d886129360c9912849209745d36d896959397d38f1cbb86537a70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32503132b6c763ff4d8a3dae8d64b7ffebbb7be055446ca04d1da4d650793322`

```dockerfile
```

-	Layers:
	-	`sha256:8fed2b96d03fec5bd2ffcb9c2047eed905ae0055e78883d72a0ad69945da364a`  
		Last Modified: Tue, 13 Jan 2026 02:23:12 GMT  
		Size: 3.7 MB (3656457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513ffde7b0239b89449a03ce6f1941b2103e9413ed74e3c48db64c966a5d668d`  
		Last Modified: Tue, 13 Jan 2026 02:23:12 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:d8310b09c09bb86311fc0d20caee3dc6e9ea1c00a7d890fbfed2d92935bd443f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150085454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7aa8cf3a1f5500b43166ed80e51d929fb95c72fc4f518959c8bb3ab77564e49`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:12:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:12:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:54 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:12:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:13:01 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:13:01 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:13:09 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:13:09 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6187f269fed90cb531578d5ce0c70db6e093f17ff45b0cdb75956c0aff675043`  
		Last Modified: Tue, 13 Jan 2026 02:13:31 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fb53f062453b42c75ea8f0cb60b2607baf16ca195ea532dac5fa9232fc1827`  
		Last Modified: Tue, 13 Jan 2026 02:13:31 GMT  
		Size: 7.4 MB (7398612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8754b5ef02317455892a604f13b0337c3dbfdd7739b3b4fb8bb5aa0e94cbca`  
		Last Modified: Tue, 13 Jan 2026 02:13:33 GMT  
		Size: 73.1 MB (73143381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec503071519b2f9bc91847a32b0ce1b15cbc37eb1a24667f4b033078d87209e`  
		Last Modified: Tue, 13 Jan 2026 02:13:31 GMT  
		Size: 394.5 KB (394492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dba370b1c20c518861500f081dc16544840e1363e2d2150a38c01fe0c435dbc`  
		Last Modified: Tue, 13 Jan 2026 02:13:37 GMT  
		Size: 99.7 KB (99662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af16770030b6fc01bfece38887d4772174ac129ba6ce8f1651975816cdd66438`  
		Last Modified: Tue, 13 Jan 2026 02:13:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bb134a8049ee72b7180016a4e44df0bac984b21fe06c8ed189ed53f3e652bb`  
		Last Modified: Tue, 13 Jan 2026 02:13:33 GMT  
		Size: 42.2 MB (42163013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86724168c9c049aafce76075619933f0012959c1a8a75e8f5cad631ba20e2388`  
		Last Modified: Tue, 13 Jan 2026 02:13:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f221a018d30bf55f86d39972e99d8ae5c06bea260a85fc7943004c10ff28b633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798925e57d69cf9c5b92b2c45116eac00d5b1f4406fbc671ff89c760c4291b64`

```dockerfile
```

-	Layers:
	-	`sha256:ef1b883e44bcf62343d6d4802bd82e74491e93a0ffcdcbbfb35cc2be3d0eb312`  
		Last Modified: Tue, 13 Jan 2026 05:35:04 GMT  
		Size: 3.6 MB (3648322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f8d3abdd1c57406c637e1cf5cc687fc1dc845f44e320f852c8c42e449dad553`  
		Last Modified: Tue, 13 Jan 2026 02:13:31 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:79ee45d0b6f735727989aad838265c7e90103b3ccf0350c2e87fff4081282a2e
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
$ docker pull couchdb@sha256:8ef0a04b2239e8d866fe8e0eebc72d7c0ad15dda2b530308c4c1b6393cf90ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139015220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edf20b5c27c82c97afb48f0a425290210b5030af4a5e5c11d83cef0b7b39450`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:15:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:16:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:16:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:16:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:16:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:16:10 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 13 Jan 2026 02:16:10 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:16:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:16:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:16:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:16:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:16:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:16:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:16:23 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:16:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:16:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273919e82c352c9f4e6cf0411272319b0233243139e70a3262a5b85cf6cee7b6`  
		Last Modified: Tue, 13 Jan 2026 02:16:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046556b37207d8f42bda47a4c7349d081e707c8d0b95f538e647e846806f66f8`  
		Last Modified: Tue, 13 Jan 2026 02:16:46 GMT  
		Size: 7.9 MB (7882841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980f4534d63c4550e4430ebdaa4f20cbc0e952ac496625d1a5c1562a4d8a7df8`  
		Last Modified: Tue, 13 Jan 2026 02:16:36 GMT  
		Size: 401.8 KB (401773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701857d6ee2fedbce6dfdb9f1724131c5e72632b82ec4702432016d9980e3c74`  
		Last Modified: Tue, 13 Jan 2026 02:16:36 GMT  
		Size: 76.5 KB (76524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433290a3aebf6ca3501ab2cbf16c6b6c4816c8a7685f166aa57ec58ff30a1f21`  
		Last Modified: Tue, 13 Jan 2026 02:16:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d0d05971862f2d01862ebc084ab8b561562e8070503fa663c889bb72efa4bf`  
		Last Modified: Tue, 13 Jan 2026 02:16:54 GMT  
		Size: 102.4 MB (102420077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e98dbdf723fee0422d3f2ce58448f5de3b6da329e923baf7928c17ea0191ed`  
		Last Modified: Tue, 13 Jan 2026 02:16:38 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd3a5b4e241146faa56adf749caa3ee7e1ee96413c2c26283fbb828662c7a1`  
		Last Modified: Tue, 13 Jan 2026 02:16:46 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14c06f7ee3aaa5402e6e24efdfeef184d0241d136d5a3d92ac1145829856178`  
		Last Modified: Tue, 13 Jan 2026 02:16:39 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e4ce922e2278d7ffb02b94d8eeb9e93e9ea662465d96b270b6248e12403da3`  
		Last Modified: Tue, 13 Jan 2026 02:16:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:040ee0f019b21a0d06786499decbe2757e53dfea21d734780578700e02d0deed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28894f5e2a516b4fa4c82762c708642f3870352389d90a1ee3313274e34b066`

```dockerfile
```

-	Layers:
	-	`sha256:c77083a88483b74b425e250a335c68098c8be77c42412f9cc4c6d7144923091e`  
		Last Modified: Tue, 13 Jan 2026 02:16:36 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5efedac1c87a348951da2270b30ef1c7932d759b8da14775891e9ff6e25e1928`  
		Last Modified: Tue, 13 Jan 2026 02:16:36 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:1af7c91436e599ab8f4fae3002a5bfac1263c50f6b0e8505240553b88f7acea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138422550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826f37a2f2000dc2845971cf7abac8a0b76323496483e4a140b1e456c9e3337a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:21:17 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:21:17 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:21:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:21:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:21:26 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:21:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:21:31 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 13 Jan 2026 02:21:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:21:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:21:44 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:21:44 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:21:44 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:21:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:21:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:21:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:21:44 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:21:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afb235c9cd033ee5e31809a77e65c965b16eb7f884f506c17397113f79c0198`  
		Last Modified: Tue, 13 Jan 2026 02:21:57 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75968d17e63ff8441c1ee5d8699c0cf8b327568b173971076d8985f1e8ffbe7b`  
		Last Modified: Tue, 13 Jan 2026 02:22:07 GMT  
		Size: 7.7 MB (7693187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e0783e8739b88f04c92eb1b3936f5047d8a36ba4044fbf5fe21580ceb39f0c`  
		Last Modified: Tue, 13 Jan 2026 02:22:09 GMT  
		Size: 370.5 KB (370522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d88aa04437e2ce164a28fd76913203215b1003379a5c835da38c57ceb6900ee`  
		Last Modified: Tue, 13 Jan 2026 02:22:06 GMT  
		Size: 76.5 KB (76482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d032fa4100c076bee3e5cf37b8a3b1b2a3de179b8118cbefb7a153a96da1c37`  
		Last Modified: Tue, 13 Jan 2026 02:22:06 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce57e808f2a9831c927cbec451efdea32a3082f88d25f35b5baff7da114c4fab`  
		Last Modified: Tue, 13 Jan 2026 02:22:14 GMT  
		Size: 102.2 MB (102169041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11db5c308963aceb8beaada642c7e71ae7449a090fd88316616154d50b8119ad`  
		Last Modified: Tue, 13 Jan 2026 02:21:58 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee4dd86fbd2c326e30cc521ca4e359963a65520372f58de359be0571e2753da`  
		Last Modified: Tue, 13 Jan 2026 02:21:59 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3918fc48c45c64d7a9d60bec4cce028537d75297a8d88eaf6bdeccc7dd712e`  
		Last Modified: Tue, 13 Jan 2026 02:22:06 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ce7b287af1d5de35d38fcd17af289d9af21e1e3a3e9db336510be0f63dc753`  
		Last Modified: Tue, 13 Jan 2026 02:22:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c54a8accd27432c02853d47b7c55f7b9008e7681cf224b5265ff148e6da9ad99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28826f2132e4601b4ee2c5574493de2237676c2734667860ac67e8c2877ae33`

```dockerfile
```

-	Layers:
	-	`sha256:2b3ee0c7b1ccfa193ab1dcc72e14fc8f89f0ebfd3c06d1742767a560d12eb7f0`  
		Last Modified: Tue, 13 Jan 2026 05:34:44 GMT  
		Size: 4.1 MB (4125664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20c92a325d7b334410edd982cf7efdca1b61238606683f7ca6a9788c22cab8fc`  
		Last Modified: Tue, 13 Jan 2026 05:34:45 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:06d269308016856c8a2842ef5ab895d42d2657cdfd771ddd270c5a36123d3bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135793601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d737cba8646c24fa6b1ee3d1257dce3086824c2917e28997bcb7f2de869234`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:12:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:12:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:12:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:12:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:54 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 13 Jan 2026 02:12:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:13:09 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:13:09 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:13:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485d372642975bebfa1a9e8ae9395f15d571f0417420c777905c28d64a2b2f9d`  
		Last Modified: Tue, 13 Jan 2026 02:13:28 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69711dd15fee6f3d2ddb9d99a111262a82c12bd0efc597671a710e24b40cf8`  
		Last Modified: Tue, 13 Jan 2026 02:13:38 GMT  
		Size: 7.4 MB (7398631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40148f85ebce9e7f165cf9f74d2ca2064133ae2d56f1cc04cf1bc986ccf2dcb4`  
		Last Modified: Tue, 13 Jan 2026 02:13:37 GMT  
		Size: 372.1 KB (372137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ffd3610106102547c57aad98e600d685f6dbb163bbcf00efdc7a0722df608`  
		Last Modified: Tue, 13 Jan 2026 02:13:28 GMT  
		Size: 76.5 KB (76549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126faf625507cec0622126ff7e1606026406e150400954f77184125a23fcc646`  
		Last Modified: Tue, 13 Jan 2026 02:13:37 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68e4bbfb3d5682088bf5684a52b2c0560c421d735078174a69b1691c9b1a186`  
		Last Modified: Tue, 13 Jan 2026 02:13:31 GMT  
		Size: 101.1 MB (101056441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0be475e56fe2c3cedeac33307059ae08b9694c18599d73e01f86cad2f2811b`  
		Last Modified: Tue, 13 Jan 2026 02:13:29 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4034b7b4cb801e6fdeac097c268cd99f9bd67b06b3b7a5702424ac6623115c4f`  
		Last Modified: Tue, 13 Jan 2026 02:13:30 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8747f3bfef41d8c94bf3797d7d24b7bc216a14e8b4eba46f7790992c48cc12c`  
		Last Modified: Tue, 13 Jan 2026 02:13:37 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ba2b604dedb448bcb5b2c7723d54396bffaa4d0841fcdf6f02ede674819903`  
		Last Modified: Tue, 13 Jan 2026 02:13:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:bb4aae3ee3ddf5c028b6e0975f6741a641d45d3a0fb6f4eb3e626db91c5ba827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf4d12fc47edd521dfc88cc6344da32da1a6e7af769d553ced6e492bd377639`

```dockerfile
```

-	Layers:
	-	`sha256:c98afd37f3e444831a659e0e3a0c9d6982a87350fe658d349e5fc21e136a183c`  
		Last Modified: Tue, 13 Jan 2026 05:34:48 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17b4c4915378568a51ff1a90cecdb4a3d6a05404bed548ce2133877d129fc14b`  
		Last Modified: Tue, 13 Jan 2026 05:34:52 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:f674509597cb2246ef6b35a20bdb3348710c861fec65a5d27ffed2e791b55155
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
$ docker pull couchdb@sha256:26a101fa397f4a5ea51c63347edd06160e0eedad47f72710ed9d1374b8bc9ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156453580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e334d6b6aeb0568f94a4fde635ff05e3ae46720c64b78e4a2a6e555bec7a1e89`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:16:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:16:29 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:16:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:16:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:16:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:16:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:16:48 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:16:48 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:16:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:16:53 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:16:53 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:16:53 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:16:53 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b35917d978112f9be4d6a8e1684394e7f59b7322fdb9837f9186888c7e7cb20`  
		Last Modified: Tue, 13 Jan 2026 02:17:17 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7640be4ecf658b81eb9d0f9c99cbe92504028ceac2455a5ed450db418d6767`  
		Last Modified: Tue, 13 Jan 2026 02:17:08 GMT  
		Size: 7.9 MB (7882786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e5113e0bc38736c1ebb3d009f67ad8916a61047581cf29382ea1635668fa1`  
		Last Modified: Tue, 13 Jan 2026 02:17:10 GMT  
		Size: 77.4 MB (77380594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54ec4a4daac83741d28e7727d85cc835764641939a207eea5fc6ef89f02b342`  
		Last Modified: Tue, 13 Jan 2026 02:17:08 GMT  
		Size: 424.1 KB (424137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d844b322bf381853cef7725090a1277b4fd37e78678dd5676deea34504f037`  
		Last Modified: Tue, 13 Jan 2026 02:17:09 GMT  
		Size: 99.5 KB (99535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b3b6576456713a7e553f0a9e398d3b6ac6fea2690a5df7741dc29905c5d80b`  
		Last Modified: Tue, 13 Jan 2026 02:17:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698d51cf70127c70b0ea92bb00f8d42cf87bd1a235e92fcbb341b75939e4e0cd`  
		Last Modified: Tue, 13 Jan 2026 02:17:24 GMT  
		Size: 42.4 MB (42436078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4196cfcab8ea171ffccbbde3d93d965694a0b118c78f015aa55729cf054e41e3`  
		Last Modified: Tue, 13 Jan 2026 02:17:17 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:95b2277a2a6de862de6cf46a6fea87d809d80cd7eac50a989f1e94d7cf531032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed829a980979afec6b61845323b8aefc4ac9c7985195cda16c6ffd2137f2e15`

```dockerfile
```

-	Layers:
	-	`sha256:13ec81de43fd1dfea8a19368e26ba6c6180f4d7fd685ddff15dd1e385b0d80a7`  
		Last Modified: Tue, 13 Jan 2026 02:17:08 GMT  
		Size: 3.7 MB (3657793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca8c12ef89424df6024f769bee47d73e79e9ae910f85529a6d53fbfc184c26b`  
		Last Modified: Tue, 13 Jan 2026 05:34:54 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:fa3feb65966c539064d2a7a66c8ccb7a53bff437da1ad6149c84135fb8d8ae16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155325157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fd6378c4557c93373eab99e9f3067837f801b341b1aefc75a2379f67dffcd3`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:22:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:22:29 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:22:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:22:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:22:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:22:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:22:50 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:22:50 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:22:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:22:56 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:22:56 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:22:56 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:22:56 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb077f697a9faa28df744a1f3c43fedf166dfbffa9e7df93f422228c5aceeece`  
		Last Modified: Tue, 13 Jan 2026 02:23:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6eb57c01e90651acba770ed9077031c2d1f894e820a6a77fab5fc3f062c5ac`  
		Last Modified: Tue, 13 Jan 2026 02:23:21 GMT  
		Size: 7.7 MB (7693195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92378f8e2c7fa5184fef765384307a8f0d8d4be6ab9aef65ae867d78df1c7220`  
		Last Modified: Tue, 13 Jan 2026 02:23:14 GMT  
		Size: 76.7 MB (76691818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6eb9ed2f797a97ee19983ec050f73e5f63e2f8a6b65f873309932b79ed2b68`  
		Last Modified: Tue, 13 Jan 2026 02:23:23 GMT  
		Size: 392.8 KB (392750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6149b46e4eb75af61de43c8d402dd4882d4b893beea4bdf54286e15c4545189`  
		Last Modified: Tue, 13 Jan 2026 02:23:20 GMT  
		Size: 99.5 KB (99498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffafb2a57977e0b46429ecdddcf7d4f022cb81a1cf5a16a973ca642467283206`  
		Last Modified: Tue, 13 Jan 2026 02:23:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7327d876b5fc48a1f620ef884d5f099170a9f3ba0cd76bcd13ef5bc178484d`  
		Last Modified: Tue, 13 Jan 2026 02:23:24 GMT  
		Size: 42.3 MB (42338126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcbedab60f1f391d8b76cde4fe951e417fcf8398ffd0a21a17e514866dd65be`  
		Last Modified: Tue, 13 Jan 2026 02:23:20 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:0639378fd9d886129360c9912849209745d36d896959397d38f1cbb86537a70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32503132b6c763ff4d8a3dae8d64b7ffebbb7be055446ca04d1da4d650793322`

```dockerfile
```

-	Layers:
	-	`sha256:8fed2b96d03fec5bd2ffcb9c2047eed905ae0055e78883d72a0ad69945da364a`  
		Last Modified: Tue, 13 Jan 2026 02:23:12 GMT  
		Size: 3.7 MB (3656457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513ffde7b0239b89449a03ce6f1941b2103e9413ed74e3c48db64c966a5d668d`  
		Last Modified: Tue, 13 Jan 2026 02:23:12 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:d8310b09c09bb86311fc0d20caee3dc6e9ea1c00a7d890fbfed2d92935bd443f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150085454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7aa8cf3a1f5500b43166ed80e51d929fb95c72fc4f518959c8bb3ab77564e49`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:12:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:12:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:54 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:12:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:13:01 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:13:01 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:13:09 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:13:09 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:13:09 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6187f269fed90cb531578d5ce0c70db6e093f17ff45b0cdb75956c0aff675043`  
		Last Modified: Tue, 13 Jan 2026 02:13:31 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fb53f062453b42c75ea8f0cb60b2607baf16ca195ea532dac5fa9232fc1827`  
		Last Modified: Tue, 13 Jan 2026 02:13:31 GMT  
		Size: 7.4 MB (7398612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8754b5ef02317455892a604f13b0337c3dbfdd7739b3b4fb8bb5aa0e94cbca`  
		Last Modified: Tue, 13 Jan 2026 02:13:33 GMT  
		Size: 73.1 MB (73143381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec503071519b2f9bc91847a32b0ce1b15cbc37eb1a24667f4b033078d87209e`  
		Last Modified: Tue, 13 Jan 2026 02:13:31 GMT  
		Size: 394.5 KB (394492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dba370b1c20c518861500f081dc16544840e1363e2d2150a38c01fe0c435dbc`  
		Last Modified: Tue, 13 Jan 2026 02:13:37 GMT  
		Size: 99.7 KB (99662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af16770030b6fc01bfece38887d4772174ac129ba6ce8f1651975816cdd66438`  
		Last Modified: Tue, 13 Jan 2026 02:13:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bb134a8049ee72b7180016a4e44df0bac984b21fe06c8ed189ed53f3e652bb`  
		Last Modified: Tue, 13 Jan 2026 02:13:33 GMT  
		Size: 42.2 MB (42163013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86724168c9c049aafce76075619933f0012959c1a8a75e8f5cad631ba20e2388`  
		Last Modified: Tue, 13 Jan 2026 02:13:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f221a018d30bf55f86d39972e99d8ae5c06bea260a85fc7943004c10ff28b633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798925e57d69cf9c5b92b2c45116eac00d5b1f4406fbc671ff89c760c4291b64`

```dockerfile
```

-	Layers:
	-	`sha256:ef1b883e44bcf62343d6d4802bd82e74491e93a0ffcdcbbfb35cc2be3d0eb312`  
		Last Modified: Tue, 13 Jan 2026 05:35:04 GMT  
		Size: 3.6 MB (3648322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f8d3abdd1c57406c637e1cf5cc687fc1dc845f44e320f852c8c42e449dad553`  
		Last Modified: Tue, 13 Jan 2026 02:13:31 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:807777b6959fc62a2c9aacb106801958aeb5cd1ad6702ea088b097fc9254c812
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
$ docker pull couchdb@sha256:2faf97d82be3b8e2e0fd173e3bc4e67884e9011d879c714a8141eee09df8adc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142052823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7592237039b089be7b880c271678bc3579faac60cb0587b345e23fec5a9eee2b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:14:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:14:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:14:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:14:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:14:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:14:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:14:56 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 13 Jan 2026 02:14:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:15:10 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:15:10 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:15:10 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65668050ee4fff6ffc324deeecc855a5edc306f51f75495afda962d9b95fee3`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef092487b8e085fdd5a53276c40804702cbb30056554f07cb62e2a585fb504`  
		Last Modified: Tue, 13 Jan 2026 02:15:34 GMT  
		Size: 7.9 MB (7882815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1625328358e7c4f114db767f71d128159db9927da240b55ec3ff572ac32f271e`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 401.8 KB (401765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ea7c769291675b331353621a8a96dcb7d17c0635a82cf72edba9e480076ed7`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 76.5 KB (76468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3befc99dc1ef62e4e1a0159203d775cc92ebc726e0337970bd1d937558a687bc`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95626de1d3cc022e0ce5e46ae38ec64d43761a98f86359d38a406c49cfc1e21b`  
		Last Modified: Tue, 13 Jan 2026 02:15:28 GMT  
		Size: 105.5 MB (105457774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be435982d8e428187ab0e23eae0a28b0a4ad61778dfa22f55e3a7157100905d7`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54435d0898ce3275b13d988e710467402ab4e9c30caee10184ac59350825be94`  
		Last Modified: Tue, 13 Jan 2026 02:15:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a47f4532a195230a2d585c3853de7c4e893a2aeb302dc9311e234a440f65db1`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c26d4890aa2a7493468c0f215e2cc6db87c9c89d751ab496afc608dc39a90a`  
		Last Modified: Tue, 13 Jan 2026 02:15:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:fa8c717021cc9fc013daae4ba425d930ec405ecb3a8fbe0fa9f176d341294586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d931371c4b2577bf9b491cab1882aeaffc04948bd594fa4518dac27887a3cace`

```dockerfile
```

-	Layers:
	-	`sha256:b51bfcbaddf6f778122953634cec76bf80f8b87c2df375435f470c16035a6133`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e447e3285c5f32e36954b4e69925a6b22330d15789d572059cc34e64f69ab3`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6b0db438d94421e92e27205855d09734387555d0fc8600ae45cff6d7bc2fdccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141410286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9b49c67b1da801d07afc112059f0cdd53e608651866ed69d81532688b27952`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:20:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:20:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:20:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:20:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:20:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:20:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:20:22 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 13 Jan 2026 02:20:23 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:20:36 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:20:36 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:20:36 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3ca5a073a02ca64d9249d2d01fa3abec601f82df4068f9d5ea27ddd387e5a`  
		Last Modified: Tue, 13 Jan 2026 02:21:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8eca98d844737e7391af0ba3bd078c33c9b79484694a82e1a51f2a29ebfc0b`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 7.7 MB (7693190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d4cff2a33ca97c469fc8ab6c3284395941ba8b2cff8f4361b3ab4a1b366eb5`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 370.5 KB (370523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1750e79248720e1a6c634304014602e07922aebc5e6023966b221b9f20ec3caa`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58782965d94ab6045938a5166643200c31af7af20c84605939e3838508c56a6e`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b24eaea20d17a3d6692890e122cfa1219e4f614dc51c6330fee6ffe9a08394`  
		Last Modified: Tue, 13 Jan 2026 02:21:07 GMT  
		Size: 105.2 MB (105156763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c03434704503155ed2343afd552fb957cce1a8b2680b8b7d8344138e2a6597`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d999d45b1b181000acaa083e513b632b05025450d49f6009d16400b8cf257624`  
		Last Modified: Tue, 13 Jan 2026 02:20:52 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc56c71044322b328f24d81b4873610894af8d49b91b8a31513590266fe49`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cd1196c4cb96149708b21622838788a0cf61a569067e10485f4f12efecb2c4`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:8ed481b2cca03c4b8f6865b96bc4487ca3baf31d374e87e1042258c20f49835e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058521c08ed24183df84ea24cb46e15ee8bdab36f0b6edc88fad29b3d2b84dd6`

```dockerfile
```

-	Layers:
	-	`sha256:6ce1950ba463d86989dad05da95562dec1791435eea9bfe733ae0d0dd83cbf76`  
		Last Modified: Tue, 13 Jan 2026 05:34:22 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50d4d6e4b72e86f1a95b7c50ce2ca2099a3a9a898205250f448399f4b707c08`  
		Last Modified: Tue, 13 Jan 2026 05:34:23 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:139b01b18130e4eba640cb445a9e7d1b3e3a3fcd027825f6ff3f9b71cc5b0285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bd435ca916c01cf53ce4171ab2c6b4b5274da8320019459562442221c81ef3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:10:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:10:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:11:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:11:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:11:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:11:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:11:12 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 13 Jan 2026 02:11:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:11:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:11:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:11:28 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:11:28 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917438ccf21f82cc4ec739c692b1e6658c435f0a12c554886df4b813b8393a07`  
		Last Modified: Tue, 13 Jan 2026 02:11:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992643008fb7fd06b94615d5a14ccc131460a03377233b78dd99940b3cb5a0d8`  
		Last Modified: Tue, 13 Jan 2026 02:11:47 GMT  
		Size: 7.4 MB (7398641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba4b929d3acd257fa813f3e05d9fe6f3ae2dd7d64f6bfad71fd98dba1a96dcd`  
		Last Modified: Tue, 13 Jan 2026 02:11:47 GMT  
		Size: 372.1 KB (372125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ca133eea8fb7e3e077be0ffb572d23a957e13cd0b40350b832226ea242cb7f`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 76.5 KB (76524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba6813ea1a509056adbb50701a6b9865c4a565465f877d267838570fa89c579`  
		Last Modified: Tue, 13 Jan 2026 02:11:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec669509929847ca409489e4d842bcb9ed817d58a6c6aa844116db80bc9edf66`  
		Last Modified: Tue, 13 Jan 2026 02:11:50 GMT  
		Size: 104.0 MB (104028284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06976128bdee8873e804e0c7ae73bbc13a363bba2a49d7a8e04c2d7855445774`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa29432fe4cf4e91ebf233fa162f196d07e46067ef2f20dc60efa8d8cf5938e4`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24ae66325dcc03c8efe8a49da9e0281c0633a1a5a2c36069aef9b74c9031229`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75955a7c6c4ebbb7ff713f82d362ae34076e2a937b9d33528de8c9b734ebed53`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:15142dad18f8914978b877cc135a50744dac73512016cf1c52553f3c69450438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13526edacd43b322a1e160ea21b1af95d90bee139a9ab8011dfedb3c3e4dfe84`

```dockerfile
```

-	Layers:
	-	`sha256:2965573c39f0ef0700fb3ffa54797b2030fb98a69f07925d459c7ff9af51d001`  
		Last Modified: Tue, 13 Jan 2026 02:35:21 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d5ce1f869bb7d38d07b5d96b3f9ab7cb0d5095985b441e97d8f837a4865583d`  
		Last Modified: Tue, 13 Jan 2026 02:35:22 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:5e3817f5d2201583513d949d6eac0b1d80210c6aa6bf6c2224aa2ebe47bc28cb
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
$ docker pull couchdb@sha256:42f9a35d1efda446f5b9fdb594bdddd3d5ed206f7709395195787fbd13e5ad21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156454284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036fec60d81a0640468c84a8ab8b24076fe4f18ffcaa319c5042beee216fa24e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:15:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:15:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:15:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:15:29 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:29 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:15:35 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:15:35 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:15:35 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:15:35 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:15:35 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c834d3aa6aa1da84b367673eef2a5defda4c0a6aad9a85c1c2e1f8b62bb44fd9`  
		Last Modified: Tue, 13 Jan 2026 02:15:51 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fd8037c3f5048c25e79b7e47b64dba31ed258b3cd21bc6dadbcd36167c8365`  
		Last Modified: Tue, 13 Jan 2026 02:15:51 GMT  
		Size: 7.9 MB (7882903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11ee3d1543b2c5e62d73c98423445473edc94adc96b3b016536c6091284ba13`  
		Last Modified: Tue, 13 Jan 2026 02:15:53 GMT  
		Size: 77.4 MB (77380783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f90d57870c99c4e73f48597d4ef590f6ce8f250da2e4763c6eadbac7254a716`  
		Last Modified: Tue, 13 Jan 2026 02:16:00 GMT  
		Size: 424.2 KB (424157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f97172c82c74b8a0cddd5c66b9220fff14f737bd1fa8f158fd799aacddac1b`  
		Last Modified: Tue, 13 Jan 2026 02:16:00 GMT  
		Size: 99.6 KB (99557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200974d13c17278793a656b27a69a741c454fa4b56b35dab14d78d195fc05610`  
		Last Modified: Tue, 13 Jan 2026 02:16:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75876e25c55566e584310d0969acf710ab2331cd8e7e444e8d2d29d28989f221`  
		Last Modified: Tue, 13 Jan 2026 02:15:54 GMT  
		Size: 42.4 MB (42436433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d06fbc7300cb5e82a9eba336329c31ebc1dafa8c95520fd2ed2339bd9dae4d6`  
		Last Modified: Tue, 13 Jan 2026 02:16:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dbd2f2f9b113ca9737a845cfc958babbab8a2872e4779e2f39399c5428e09578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65f465453f712c9a4e51486a3f7ae4f69d56514ad3f9f57e5b7f14fe98bb9a4`

```dockerfile
```

-	Layers:
	-	`sha256:cfdac44fc4100793a76ec5945deec66105528ef1786dc7f5d563a89216d270b2`  
		Last Modified: Tue, 13 Jan 2026 05:34:26 GMT  
		Size: 3.7 MB (3658099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a24cd09a6b98e0a5c34370502688d6d23633227b2ae453edb8d7b57fd95c4402`  
		Last Modified: Tue, 13 Jan 2026 02:15:51 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:34039d5ed14a1c27b7af653d30ef8d04ab4da250283482a6926c9f9d67d38dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155326005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534de1b157c124931435b169c227299f70f5a18fa09e67ef97de1a048de73090`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:20:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:20:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:20:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:20:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:20:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:20:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:21:00 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:21:00 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:21:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:21:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:21:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:21:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:21:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c557e8470a8a15f08a810286fc29f026da97144910c8cb843d46251278ee184`  
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a950b57072984c0e96c033ed51300854efba14b435d84da94826cd198297a83`  
		Last Modified: Tue, 13 Jan 2026 02:21:31 GMT  
		Size: 7.7 MB (7693146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb5da74a812f294be30343ff89ed9604ba248e5e135425a3bb7906968f1e64`  
		Last Modified: Tue, 13 Jan 2026 02:21:23 GMT  
		Size: 76.7 MB (76691847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66868d5948d44e96078e5fa525df7e09c89d0e7cc0cb09f0fc48aeeb30707c4e`  
		Last Modified: Tue, 13 Jan 2026 02:21:30 GMT  
		Size: 392.7 KB (392739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b4cd7f59188339c71711d75181a6f4fd7fab268e8ca419321d58f9759d5a1`  
		Last Modified: Tue, 13 Jan 2026 02:21:22 GMT  
		Size: 99.5 KB (99466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d1f922c928a80bb685cb6e00a39fd3e289a4a71153df9e0713dc6f8ca02ff`  
		Last Modified: Tue, 13 Jan 2026 02:21:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a9a35bcdaffcf54721526f54af996ac768b9174620e4c63db9965d9df21250`  
		Last Modified: Tue, 13 Jan 2026 02:21:24 GMT  
		Size: 42.3 MB (42339037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6912598d1a802a2bd6ac00a98fbe61355007e81d599a86a596d2eb2306e37347`  
		Last Modified: Tue, 13 Jan 2026 02:21:23 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:05d5c8faab853cd6342bd862473efd6a0ef1e36ad8a8d662a4d9bda0df468fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b019f9cacd2b003329688e392435d942055450c0b59e2f32a6248a85a7b9f3d8`

```dockerfile
```

-	Layers:
	-	`sha256:6d88198d1f122d7c6ee4b1ac07a559c13e3675218835db2550b515d10a23b739`  
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 3.7 MB (3656775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceb99cef1c693ed23e90314454a0ad427bfc99d16beeef04f91e068596fb7504`  
		Last Modified: Tue, 13 Jan 2026 05:34:35 GMT  
		Size: 24.7 KB (24702 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:090226f5f3381e086d4ca01905405b65bf2cbda4054d3eeea595666cf296f079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150087066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d697e036a9dc8f41a88f6bf82f3c5ef10241a1245b55b62fd42c3131681f04`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:11:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:11:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:12:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:12:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:12:20 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:20 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:12:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:12:28 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:12:28 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:12:28 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:12:28 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73bbb2b620b04ded8354b575b5134f4a498c331a7c6039ec6259f44f2e55ee4`  
		Last Modified: Tue, 13 Jan 2026 02:12:49 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebfeaea45624160791afec65772aef817d039bf449f8688c0147dbbcc27f9e2`  
		Last Modified: Tue, 13 Jan 2026 02:12:50 GMT  
		Size: 7.4 MB (7398640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8651b9ab7326e7aa269290a9c469fca82ecf80dfe7d638dcb856c21e1630ef9a`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 73.1 MB (73143293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acff0900ca2683b601b51373dc2f6f260ac3500b6e8ce9c8d4c678f25d35fb4b`  
		Last Modified: Tue, 13 Jan 2026 02:12:49 GMT  
		Size: 394.5 KB (394487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84412345919376d985a34e5620ace1867e5cc1b817280bcb02e00cf6a7a4d8c`  
		Last Modified: Tue, 13 Jan 2026 02:12:57 GMT  
		Size: 99.7 KB (99650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c09398cba81cc4d6231fae65fbcd9f3a583ee297ab1323f084116107bd3e24`  
		Last Modified: Tue, 13 Jan 2026 02:12:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1194cd6b832369837b0dddcedd825c3b8f7721b5e7ec3f4c3c70e732d9e200`  
		Last Modified: Tue, 13 Jan 2026 02:12:52 GMT  
		Size: 42.2 MB (42164704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546ce6ac21b40929413de3114353fd57420d4452084eca81b3909d4c036ac8d9`  
		Last Modified: Tue, 13 Jan 2026 02:12:57 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:188e240d273a0cf3218a6907208cab9335a609571450fe212fe5af1c7bd48f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341cc961a96be1e8cf31a4dbd08fffd6c38bf891f16824357ff2997c8502ba3e`

```dockerfile
```

-	Layers:
	-	`sha256:ca51397e2dca8c25972475a34a2d3cc7779d73d0f6924ca91cdf703cd450188f`  
		Last Modified: Tue, 13 Jan 2026 02:35:26 GMT  
		Size: 3.6 MB (3648628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:570e02ee2ecf094a674b942bda5990333d969a63ad2a1908c907d4ab0bf2e248`  
		Last Modified: Tue, 13 Jan 2026 02:12:49 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1`

```console
$ docker pull couchdb@sha256:807777b6959fc62a2c9aacb106801958aeb5cd1ad6702ea088b097fc9254c812
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.1` - linux; amd64

```console
$ docker pull couchdb@sha256:2faf97d82be3b8e2e0fd173e3bc4e67884e9011d879c714a8141eee09df8adc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142052823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7592237039b089be7b880c271678bc3579faac60cb0587b345e23fec5a9eee2b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:14:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:14:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:14:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:14:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:14:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:14:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:14:56 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 13 Jan 2026 02:14:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:15:10 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:15:10 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:15:10 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65668050ee4fff6ffc324deeecc855a5edc306f51f75495afda962d9b95fee3`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef092487b8e085fdd5a53276c40804702cbb30056554f07cb62e2a585fb504`  
		Last Modified: Tue, 13 Jan 2026 02:15:34 GMT  
		Size: 7.9 MB (7882815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1625328358e7c4f114db767f71d128159db9927da240b55ec3ff572ac32f271e`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 401.8 KB (401765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ea7c769291675b331353621a8a96dcb7d17c0635a82cf72edba9e480076ed7`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 76.5 KB (76468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3befc99dc1ef62e4e1a0159203d775cc92ebc726e0337970bd1d937558a687bc`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95626de1d3cc022e0ce5e46ae38ec64d43761a98f86359d38a406c49cfc1e21b`  
		Last Modified: Tue, 13 Jan 2026 02:15:28 GMT  
		Size: 105.5 MB (105457774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be435982d8e428187ab0e23eae0a28b0a4ad61778dfa22f55e3a7157100905d7`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54435d0898ce3275b13d988e710467402ab4e9c30caee10184ac59350825be94`  
		Last Modified: Tue, 13 Jan 2026 02:15:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a47f4532a195230a2d585c3853de7c4e893a2aeb302dc9311e234a440f65db1`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c26d4890aa2a7493468c0f215e2cc6db87c9c89d751ab496afc608dc39a90a`  
		Last Modified: Tue, 13 Jan 2026 02:15:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:fa8c717021cc9fc013daae4ba425d930ec405ecb3a8fbe0fa9f176d341294586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d931371c4b2577bf9b491cab1882aeaffc04948bd594fa4518dac27887a3cace`

```dockerfile
```

-	Layers:
	-	`sha256:b51bfcbaddf6f778122953634cec76bf80f8b87c2df375435f470c16035a6133`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e447e3285c5f32e36954b4e69925a6b22330d15789d572059cc34e64f69ab3`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6b0db438d94421e92e27205855d09734387555d0fc8600ae45cff6d7bc2fdccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141410286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9b49c67b1da801d07afc112059f0cdd53e608651866ed69d81532688b27952`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:20:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:20:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:20:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:20:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:20:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:20:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:20:22 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 13 Jan 2026 02:20:23 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:20:36 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:20:36 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:20:36 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3ca5a073a02ca64d9249d2d01fa3abec601f82df4068f9d5ea27ddd387e5a`  
		Last Modified: Tue, 13 Jan 2026 02:21:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8eca98d844737e7391af0ba3bd078c33c9b79484694a82e1a51f2a29ebfc0b`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 7.7 MB (7693190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d4cff2a33ca97c469fc8ab6c3284395941ba8b2cff8f4361b3ab4a1b366eb5`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 370.5 KB (370523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1750e79248720e1a6c634304014602e07922aebc5e6023966b221b9f20ec3caa`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58782965d94ab6045938a5166643200c31af7af20c84605939e3838508c56a6e`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b24eaea20d17a3d6692890e122cfa1219e4f614dc51c6330fee6ffe9a08394`  
		Last Modified: Tue, 13 Jan 2026 02:21:07 GMT  
		Size: 105.2 MB (105156763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c03434704503155ed2343afd552fb957cce1a8b2680b8b7d8344138e2a6597`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d999d45b1b181000acaa083e513b632b05025450d49f6009d16400b8cf257624`  
		Last Modified: Tue, 13 Jan 2026 02:20:52 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc56c71044322b328f24d81b4873610894af8d49b91b8a31513590266fe49`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cd1196c4cb96149708b21622838788a0cf61a569067e10485f4f12efecb2c4`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:8ed481b2cca03c4b8f6865b96bc4487ca3baf31d374e87e1042258c20f49835e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058521c08ed24183df84ea24cb46e15ee8bdab36f0b6edc88fad29b3d2b84dd6`

```dockerfile
```

-	Layers:
	-	`sha256:6ce1950ba463d86989dad05da95562dec1791435eea9bfe733ae0d0dd83cbf76`  
		Last Modified: Tue, 13 Jan 2026 05:34:22 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50d4d6e4b72e86f1a95b7c50ce2ca2099a3a9a898205250f448399f4b707c08`  
		Last Modified: Tue, 13 Jan 2026 05:34:23 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; s390x

```console
$ docker pull couchdb@sha256:139b01b18130e4eba640cb445a9e7d1b3e3a3fcd027825f6ff3f9b71cc5b0285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bd435ca916c01cf53ce4171ab2c6b4b5274da8320019459562442221c81ef3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:10:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:10:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:11:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:11:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:11:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:11:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:11:12 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 13 Jan 2026 02:11:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:11:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:11:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:11:28 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:11:28 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917438ccf21f82cc4ec739c692b1e6658c435f0a12c554886df4b813b8393a07`  
		Last Modified: Tue, 13 Jan 2026 02:11:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992643008fb7fd06b94615d5a14ccc131460a03377233b78dd99940b3cb5a0d8`  
		Last Modified: Tue, 13 Jan 2026 02:11:47 GMT  
		Size: 7.4 MB (7398641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba4b929d3acd257fa813f3e05d9fe6f3ae2dd7d64f6bfad71fd98dba1a96dcd`  
		Last Modified: Tue, 13 Jan 2026 02:11:47 GMT  
		Size: 372.1 KB (372125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ca133eea8fb7e3e077be0ffb572d23a957e13cd0b40350b832226ea242cb7f`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 76.5 KB (76524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba6813ea1a509056adbb50701a6b9865c4a565465f877d267838570fa89c579`  
		Last Modified: Tue, 13 Jan 2026 02:11:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec669509929847ca409489e4d842bcb9ed817d58a6c6aa844116db80bc9edf66`  
		Last Modified: Tue, 13 Jan 2026 02:11:50 GMT  
		Size: 104.0 MB (104028284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06976128bdee8873e804e0c7ae73bbc13a363bba2a49d7a8e04c2d7855445774`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa29432fe4cf4e91ebf233fa162f196d07e46067ef2f20dc60efa8d8cf5938e4`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24ae66325dcc03c8efe8a49da9e0281c0633a1a5a2c36069aef9b74c9031229`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75955a7c6c4ebbb7ff713f82d362ae34076e2a937b9d33528de8c9b734ebed53`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:15142dad18f8914978b877cc135a50744dac73512016cf1c52553f3c69450438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13526edacd43b322a1e160ea21b1af95d90bee139a9ab8011dfedb3c3e4dfe84`

```dockerfile
```

-	Layers:
	-	`sha256:2965573c39f0ef0700fb3ffa54797b2030fb98a69f07925d459c7ff9af51d001`  
		Last Modified: Tue, 13 Jan 2026 02:35:21 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d5ce1f869bb7d38d07b5d96b3f9ab7cb0d5095985b441e97d8f837a4865583d`  
		Last Modified: Tue, 13 Jan 2026 02:35:22 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1-nouveau`

```console
$ docker pull couchdb@sha256:5e3817f5d2201583513d949d6eac0b1d80210c6aa6bf6c2224aa2ebe47bc28cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.1-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:42f9a35d1efda446f5b9fdb594bdddd3d5ed206f7709395195787fbd13e5ad21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156454284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036fec60d81a0640468c84a8ab8b24076fe4f18ffcaa319c5042beee216fa24e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:15:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:15:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:15:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:15:29 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:29 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:15:35 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:15:35 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:15:35 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:15:35 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:15:35 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c834d3aa6aa1da84b367673eef2a5defda4c0a6aad9a85c1c2e1f8b62bb44fd9`  
		Last Modified: Tue, 13 Jan 2026 02:15:51 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fd8037c3f5048c25e79b7e47b64dba31ed258b3cd21bc6dadbcd36167c8365`  
		Last Modified: Tue, 13 Jan 2026 02:15:51 GMT  
		Size: 7.9 MB (7882903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11ee3d1543b2c5e62d73c98423445473edc94adc96b3b016536c6091284ba13`  
		Last Modified: Tue, 13 Jan 2026 02:15:53 GMT  
		Size: 77.4 MB (77380783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f90d57870c99c4e73f48597d4ef590f6ce8f250da2e4763c6eadbac7254a716`  
		Last Modified: Tue, 13 Jan 2026 02:16:00 GMT  
		Size: 424.2 KB (424157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f97172c82c74b8a0cddd5c66b9220fff14f737bd1fa8f158fd799aacddac1b`  
		Last Modified: Tue, 13 Jan 2026 02:16:00 GMT  
		Size: 99.6 KB (99557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200974d13c17278793a656b27a69a741c454fa4b56b35dab14d78d195fc05610`  
		Last Modified: Tue, 13 Jan 2026 02:16:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75876e25c55566e584310d0969acf710ab2331cd8e7e444e8d2d29d28989f221`  
		Last Modified: Tue, 13 Jan 2026 02:15:54 GMT  
		Size: 42.4 MB (42436433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d06fbc7300cb5e82a9eba336329c31ebc1dafa8c95520fd2ed2339bd9dae4d6`  
		Last Modified: Tue, 13 Jan 2026 02:16:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dbd2f2f9b113ca9737a845cfc958babbab8a2872e4779e2f39399c5428e09578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65f465453f712c9a4e51486a3f7ae4f69d56514ad3f9f57e5b7f14fe98bb9a4`

```dockerfile
```

-	Layers:
	-	`sha256:cfdac44fc4100793a76ec5945deec66105528ef1786dc7f5d563a89216d270b2`  
		Last Modified: Tue, 13 Jan 2026 05:34:26 GMT  
		Size: 3.7 MB (3658099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a24cd09a6b98e0a5c34370502688d6d23633227b2ae453edb8d7b57fd95c4402`  
		Last Modified: Tue, 13 Jan 2026 02:15:51 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:34039d5ed14a1c27b7af653d30ef8d04ab4da250283482a6926c9f9d67d38dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155326005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534de1b157c124931435b169c227299f70f5a18fa09e67ef97de1a048de73090`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:20:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:20:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:20:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:20:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:20:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:20:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:21:00 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:21:00 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:21:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:21:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:21:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:21:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:21:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c557e8470a8a15f08a810286fc29f026da97144910c8cb843d46251278ee184`  
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a950b57072984c0e96c033ed51300854efba14b435d84da94826cd198297a83`  
		Last Modified: Tue, 13 Jan 2026 02:21:31 GMT  
		Size: 7.7 MB (7693146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb5da74a812f294be30343ff89ed9604ba248e5e135425a3bb7906968f1e64`  
		Last Modified: Tue, 13 Jan 2026 02:21:23 GMT  
		Size: 76.7 MB (76691847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66868d5948d44e96078e5fa525df7e09c89d0e7cc0cb09f0fc48aeeb30707c4e`  
		Last Modified: Tue, 13 Jan 2026 02:21:30 GMT  
		Size: 392.7 KB (392739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b4cd7f59188339c71711d75181a6f4fd7fab268e8ca419321d58f9759d5a1`  
		Last Modified: Tue, 13 Jan 2026 02:21:22 GMT  
		Size: 99.5 KB (99466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d1f922c928a80bb685cb6e00a39fd3e289a4a71153df9e0713dc6f8ca02ff`  
		Last Modified: Tue, 13 Jan 2026 02:21:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a9a35bcdaffcf54721526f54af996ac768b9174620e4c63db9965d9df21250`  
		Last Modified: Tue, 13 Jan 2026 02:21:24 GMT  
		Size: 42.3 MB (42339037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6912598d1a802a2bd6ac00a98fbe61355007e81d599a86a596d2eb2306e37347`  
		Last Modified: Tue, 13 Jan 2026 02:21:23 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:05d5c8faab853cd6342bd862473efd6a0ef1e36ad8a8d662a4d9bda0df468fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b019f9cacd2b003329688e392435d942055450c0b59e2f32a6248a85a7b9f3d8`

```dockerfile
```

-	Layers:
	-	`sha256:6d88198d1f122d7c6ee4b1ac07a559c13e3675218835db2550b515d10a23b739`  
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 3.7 MB (3656775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceb99cef1c693ed23e90314454a0ad427bfc99d16beeef04f91e068596fb7504`  
		Last Modified: Tue, 13 Jan 2026 05:34:35 GMT  
		Size: 24.7 KB (24702 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:090226f5f3381e086d4ca01905405b65bf2cbda4054d3eeea595666cf296f079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150087066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d697e036a9dc8f41a88f6bf82f3c5ef10241a1245b55b62fd42c3131681f04`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:11:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:11:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 13 Jan 2026 02:12:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:12:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:12:20 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:20 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:12:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 13 Jan 2026 02:12:28 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 13 Jan 2026 02:12:28 GMT
VOLUME [/opt/nouveau/data]
# Tue, 13 Jan 2026 02:12:28 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 13 Jan 2026 02:12:28 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73bbb2b620b04ded8354b575b5134f4a498c331a7c6039ec6259f44f2e55ee4`  
		Last Modified: Tue, 13 Jan 2026 02:12:49 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebfeaea45624160791afec65772aef817d039bf449f8688c0147dbbcc27f9e2`  
		Last Modified: Tue, 13 Jan 2026 02:12:50 GMT  
		Size: 7.4 MB (7398640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8651b9ab7326e7aa269290a9c469fca82ecf80dfe7d638dcb856c21e1630ef9a`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 73.1 MB (73143293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acff0900ca2683b601b51373dc2f6f260ac3500b6e8ce9c8d4c678f25d35fb4b`  
		Last Modified: Tue, 13 Jan 2026 02:12:49 GMT  
		Size: 394.5 KB (394487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84412345919376d985a34e5620ace1867e5cc1b817280bcb02e00cf6a7a4d8c`  
		Last Modified: Tue, 13 Jan 2026 02:12:57 GMT  
		Size: 99.7 KB (99650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c09398cba81cc4d6231fae65fbcd9f3a583ee297ab1323f084116107bd3e24`  
		Last Modified: Tue, 13 Jan 2026 02:12:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1194cd6b832369837b0dddcedd825c3b8f7721b5e7ec3f4c3c70e732d9e200`  
		Last Modified: Tue, 13 Jan 2026 02:12:52 GMT  
		Size: 42.2 MB (42164704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546ce6ac21b40929413de3114353fd57420d4452084eca81b3909d4c036ac8d9`  
		Last Modified: Tue, 13 Jan 2026 02:12:57 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:188e240d273a0cf3218a6907208cab9335a609571450fe212fe5af1c7bd48f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341cc961a96be1e8cf31a4dbd08fffd6c38bf891f16824357ff2997c8502ba3e`

```dockerfile
```

-	Layers:
	-	`sha256:ca51397e2dca8c25972475a34a2d3cc7779d73d0f6924ca91cdf703cd450188f`  
		Last Modified: Tue, 13 Jan 2026 02:35:26 GMT  
		Size: 3.6 MB (3648628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:570e02ee2ecf094a674b942bda5990333d969a63ad2a1908c907d4ab0bf2e248`  
		Last Modified: Tue, 13 Jan 2026 02:12:49 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:807777b6959fc62a2c9aacb106801958aeb5cd1ad6702ea088b097fc9254c812
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
$ docker pull couchdb@sha256:2faf97d82be3b8e2e0fd173e3bc4e67884e9011d879c714a8141eee09df8adc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142052823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7592237039b089be7b880c271678bc3579faac60cb0587b345e23fec5a9eee2b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:14:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:14:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:14:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:14:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:14:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:14:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:14:56 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 13 Jan 2026 02:14:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:15:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:15:10 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:15:10 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:15:10 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65668050ee4fff6ffc324deeecc855a5edc306f51f75495afda962d9b95fee3`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef092487b8e085fdd5a53276c40804702cbb30056554f07cb62e2a585fb504`  
		Last Modified: Tue, 13 Jan 2026 02:15:34 GMT  
		Size: 7.9 MB (7882815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1625328358e7c4f114db767f71d128159db9927da240b55ec3ff572ac32f271e`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 401.8 KB (401765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ea7c769291675b331353621a8a96dcb7d17c0635a82cf72edba9e480076ed7`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 76.5 KB (76468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3befc99dc1ef62e4e1a0159203d775cc92ebc726e0337970bd1d937558a687bc`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95626de1d3cc022e0ce5e46ae38ec64d43761a98f86359d38a406c49cfc1e21b`  
		Last Modified: Tue, 13 Jan 2026 02:15:28 GMT  
		Size: 105.5 MB (105457774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be435982d8e428187ab0e23eae0a28b0a4ad61778dfa22f55e3a7157100905d7`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54435d0898ce3275b13d988e710467402ab4e9c30caee10184ac59350825be94`  
		Last Modified: Tue, 13 Jan 2026 02:15:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a47f4532a195230a2d585c3853de7c4e893a2aeb302dc9311e234a440f65db1`  
		Last Modified: Tue, 13 Jan 2026 02:15:33 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c26d4890aa2a7493468c0f215e2cc6db87c9c89d751ab496afc608dc39a90a`  
		Last Modified: Tue, 13 Jan 2026 02:15:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:fa8c717021cc9fc013daae4ba425d930ec405ecb3a8fbe0fa9f176d341294586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d931371c4b2577bf9b491cab1882aeaffc04948bd594fa4518dac27887a3cace`

```dockerfile
```

-	Layers:
	-	`sha256:b51bfcbaddf6f778122953634cec76bf80f8b87c2df375435f470c16035a6133`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e447e3285c5f32e36954b4e69925a6b22330d15789d572059cc34e64f69ab3`  
		Last Modified: Tue, 13 Jan 2026 02:15:24 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6b0db438d94421e92e27205855d09734387555d0fc8600ae45cff6d7bc2fdccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141410286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9b49c67b1da801d07afc112059f0cdd53e608651866ed69d81532688b27952`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:20:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:20:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:20:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:20:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:20:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:20:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:20:22 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 13 Jan 2026 02:20:23 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:20:36 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:20:36 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:20:36 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:20:36 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3ca5a073a02ca64d9249d2d01fa3abec601f82df4068f9d5ea27ddd387e5a`  
		Last Modified: Tue, 13 Jan 2026 02:21:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8eca98d844737e7391af0ba3bd078c33c9b79484694a82e1a51f2a29ebfc0b`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 7.7 MB (7693190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d4cff2a33ca97c469fc8ab6c3284395941ba8b2cff8f4361b3ab4a1b366eb5`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 370.5 KB (370523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1750e79248720e1a6c634304014602e07922aebc5e6023966b221b9f20ec3caa`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58782965d94ab6045938a5166643200c31af7af20c84605939e3838508c56a6e`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b24eaea20d17a3d6692890e122cfa1219e4f614dc51c6330fee6ffe9a08394`  
		Last Modified: Tue, 13 Jan 2026 02:21:07 GMT  
		Size: 105.2 MB (105156763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c03434704503155ed2343afd552fb957cce1a8b2680b8b7d8344138e2a6597`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d999d45b1b181000acaa083e513b632b05025450d49f6009d16400b8cf257624`  
		Last Modified: Tue, 13 Jan 2026 02:20:52 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc56c71044322b328f24d81b4873610894af8d49b91b8a31513590266fe49`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cd1196c4cb96149708b21622838788a0cf61a569067e10485f4f12efecb2c4`  
		Last Modified: Tue, 13 Jan 2026 02:20:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:8ed481b2cca03c4b8f6865b96bc4487ca3baf31d374e87e1042258c20f49835e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058521c08ed24183df84ea24cb46e15ee8bdab36f0b6edc88fad29b3d2b84dd6`

```dockerfile
```

-	Layers:
	-	`sha256:6ce1950ba463d86989dad05da95562dec1791435eea9bfe733ae0d0dd83cbf76`  
		Last Modified: Tue, 13 Jan 2026 05:34:22 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50d4d6e4b72e86f1a95b7c50ce2ca2099a3a9a898205250f448399f4b707c08`  
		Last Modified: Tue, 13 Jan 2026 05:34:23 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:139b01b18130e4eba640cb445a9e7d1b3e3a3fcd027825f6ff3f9b71cc5b0285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bd435ca916c01cf53ce4171ab2c6b4b5274da8320019459562442221c81ef3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:10:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Jan 2026 02:10:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 13 Jan 2026 02:11:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:11:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 13 Jan 2026 02:11:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Jan 2026 02:11:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:11:12 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 13 Jan 2026 02:11:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 13 Jan 2026 02:11:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 02:11:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:11:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Jan 2026 02:11:28 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 13 Jan 2026 02:11:28 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917438ccf21f82cc4ec739c692b1e6658c435f0a12c554886df4b813b8393a07`  
		Last Modified: Tue, 13 Jan 2026 02:11:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992643008fb7fd06b94615d5a14ccc131460a03377233b78dd99940b3cb5a0d8`  
		Last Modified: Tue, 13 Jan 2026 02:11:47 GMT  
		Size: 7.4 MB (7398641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba4b929d3acd257fa813f3e05d9fe6f3ae2dd7d64f6bfad71fd98dba1a96dcd`  
		Last Modified: Tue, 13 Jan 2026 02:11:47 GMT  
		Size: 372.1 KB (372125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ca133eea8fb7e3e077be0ffb572d23a957e13cd0b40350b832226ea242cb7f`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 76.5 KB (76524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba6813ea1a509056adbb50701a6b9865c4a565465f877d267838570fa89c579`  
		Last Modified: Tue, 13 Jan 2026 02:11:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec669509929847ca409489e4d842bcb9ed817d58a6c6aa844116db80bc9edf66`  
		Last Modified: Tue, 13 Jan 2026 02:11:50 GMT  
		Size: 104.0 MB (104028284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06976128bdee8873e804e0c7ae73bbc13a363bba2a49d7a8e04c2d7855445774`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa29432fe4cf4e91ebf233fa162f196d07e46067ef2f20dc60efa8d8cf5938e4`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24ae66325dcc03c8efe8a49da9e0281c0633a1a5a2c36069aef9b74c9031229`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75955a7c6c4ebbb7ff713f82d362ae34076e2a937b9d33528de8c9b734ebed53`  
		Last Modified: Tue, 13 Jan 2026 02:11:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:15142dad18f8914978b877cc135a50744dac73512016cf1c52553f3c69450438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13526edacd43b322a1e160ea21b1af95d90bee139a9ab8011dfedb3c3e4dfe84`

```dockerfile
```

-	Layers:
	-	`sha256:2965573c39f0ef0700fb3ffa54797b2030fb98a69f07925d459c7ff9af51d001`  
		Last Modified: Tue, 13 Jan 2026 02:35:21 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d5ce1f869bb7d38d07b5d96b3f9ab7cb0d5095985b441e97d8f837a4865583d`  
		Last Modified: Tue, 13 Jan 2026 02:35:22 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json
