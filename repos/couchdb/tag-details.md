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
$ docker pull couchdb@sha256:94d0d67147335d37df957f3ace915c06eccf4c1d58ad558d614aae31f42b3187
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
$ docker pull couchdb@sha256:b8bdc4d8197b9750ad9ef55b4451df82c2552a1e48d25cb8d27f86901b0f45cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142051769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33093ab0977f79e9ab863423ea5f4dbca301ef181fc2d582a00cc9c7f828f0b2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 02:43:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 03 Feb 2026 02:43:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 02:43:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 02:43:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:57 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 03 Feb 2026 02:43:57 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 02:44:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Feb 2026 02:44:09 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 03 Feb 2026 02:44:09 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:44:10 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Feb 2026 02:44:10 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 03 Feb 2026 02:44:10 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f95f560da8e3bdb596e84a890ee559e80ffcd0ffb2154713b84dd9160890245`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592f333a628d569980303d3af9357c11ca01d55d117a3196fcee0f788b6f5e64`  
		Last Modified: Tue, 03 Feb 2026 02:44:23 GMT  
		Size: 7.9 MB (7883160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46c85312097de70d8c3bb3d7ee5e3673c1731b6d313d4b6530de6f23ef9b703`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 401.8 KB (401799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ce674f9f9d416860b6ebffbf149ef1784a8da66ef19fd90f0abe6e5c8e8c09`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 76.5 KB (76541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd653d782a5746a5d49d07d4802d8aee9a39c177c89a61b9e02b8179ad5443d`  
		Last Modified: Tue, 03 Feb 2026 02:44:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd05477ed76b6361c96a6d5a6c5aa0b0e2b6be7d21f838cbf5fc17d0afe2b94`  
		Last Modified: Tue, 03 Feb 2026 02:44:27 GMT  
		Size: 105.5 MB (105456346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbe85d7425385b2507026901a39d017eb7273857ed496f22bec013c79fcdbb7`  
		Last Modified: Tue, 03 Feb 2026 02:44:24 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92911ab6e4d1ec2897e491318968d3ddced0573c5f8e4b798656729a21a3448`  
		Last Modified: Tue, 03 Feb 2026 02:44:24 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9634e08b060e5bb74c236c6c3796b6f1c7bd45c2ec7c0cd648b6f46ba77ae208`  
		Last Modified: Tue, 03 Feb 2026 02:44:25 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928bfbf0e88dd45b798f5b852dc8ab17fc67c4ba815089838ef07188049bde07`  
		Last Modified: Tue, 03 Feb 2026 02:44:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:28fea4b5eef08c55dc31fb28c5fa3ce0b4e9c97da4a66d34340a0c83f31e488d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e0218401bdf13e40ccb7e8c80392ff02a670f0efcaf8559d00dc8718dc5be7`

```dockerfile
```

-	Layers:
	-	`sha256:6dda1c9ccabd43968c41a96d68ffa5d4e866caadac602f60485d0be2b85ce991`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f5c1ba2284296507eb9bd9ed9f407820c80912f37156ddd0bf69cb46f7990e`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8eca98d844737e7391af0ba3bd078c33c9b79484694a82e1a51f2a29ebfc0b`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 7.7 MB (7693190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d4cff2a33ca97c469fc8ab6c3284395941ba8b2cff8f4361b3ab4a1b366eb5`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:54 GMT  
		Size: 105.2 MB (105156763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c03434704503155ed2343afd552fb957cce1a8b2680b8b7d8344138e2a6597`  
		Last Modified: Tue, 13 Jan 2026 02:20:52 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d999d45b1b181000acaa083e513b632b05025450d49f6009d16400b8cf257624`  
		Last Modified: Tue, 13 Jan 2026 02:20:52 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc56c71044322b328f24d81b4873610894af8d49b91b8a31513590266fe49`  
		Last Modified: Tue, 13 Jan 2026 02:20:53 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cd1196c4cb96149708b21622838788a0cf61a569067e10485f4f12efecb2c4`  
		Last Modified: Tue, 13 Jan 2026 02:20:53 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50d4d6e4b72e86f1a95b7c50ce2ca2099a3a9a898205250f448399f4b707c08`  
		Last Modified: Tue, 13 Jan 2026 02:20:50 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:b89995d4cc477862a92b00132e63e9bdbeaa2e1275399b8c499b4ae8ff484283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96adb63f1df519a3512423ccc509050f50f1aa43b8377a35e9f8c4f876bd01fc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:45:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 03:45:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 03 Feb 2026 03:45:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 03:45:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 03:45:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:47 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 03 Feb 2026 03:45:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:46:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Feb 2026 03:46:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 03 Feb 2026 03:46:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02b13c2167da67366f3b654df0b591a74a3ceda0090898972764c16c230c05d`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106bb0fe71c6f312e2b1f959ca60f93081c3ee9281519aa63c3d43e8dd80a695`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 7.4 MB (7398885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e553654c359f6f0b8b1971a834e87804e73de794834a70588cf062e0dfa737be`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 372.1 KB (372135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4b0edbcef0c9ef2e30cbb6abc0dd368eb2da9cd9092867b563c0474dc73628`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 76.5 KB (76541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec92d49aef09eb0f577a0d64c82ee3a193ce554f913871aea28e0fbc0c547d7`  
		Last Modified: Tue, 03 Feb 2026 03:46:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc9b0eb3cf5654309cf322615685bbb1ea31e67782f9536ce65890c8fb83fb8`  
		Last Modified: Tue, 03 Feb 2026 03:46:28 GMT  
		Size: 104.0 MB (104028287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4810a95d166c559450d5305e9bc0afbd6f19fcfda85855677ff4e8bf7e68e6`  
		Last Modified: Tue, 03 Feb 2026 03:46:25 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c1119ba5c69ff7a21a171a1ac2426fa7672882940a8817641966dbc1e349f`  
		Last Modified: Tue, 03 Feb 2026 03:46:25 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e5f136944350478b46d365514b083f6088c42948cb115e4bdd7da7b0784b78`  
		Last Modified: Tue, 03 Feb 2026 03:46:26 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16af054f32548ea40fd3afa36f7d37e965983c035312f702653ec8f1cbc143d3`  
		Last Modified: Tue, 03 Feb 2026 03:46:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:423824caae2974643c0d72cdafd5f8a8b9894e8218c49e1f54f92b9c667d96a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f153ea1b594180284242ac7bb097fd386410f9a814283f2119059be22202fcf`

```dockerfile
```

-	Layers:
	-	`sha256:f340e5b4727b7d09238aef9c6694ab43abc848711d767fabbf3c5394102bd764`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0db4b1900a587958931c2cbf5f8e1ed873e849a9b6d08b3f2ade31ab9563bf`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:5ccd971808f4b7eec5d5599174f15e68598259bfc2fa9283a5aba07b94e70388
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
$ docker pull couchdb@sha256:2b64016ceeedcbe65bec9fdf719a6f0520cfdeda292899f948b6f02ecd72aa1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156454720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0f8c67278d19a9a18cdec7e5a892300ef237a9fcb7816241ddfc8788de4735`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:44 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 02:43:44 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 03 Feb 2026 02:43:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 02:44:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 02:44:07 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:07 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 02:44:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 03 Feb 2026 02:44:13 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 03 Feb 2026 02:44:13 GMT
VOLUME [/opt/nouveau/data]
# Tue, 03 Feb 2026 02:44:13 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 03 Feb 2026 02:44:13 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2f1fc1251780f2123a88ec6b1625b1f161e25efd41504f70275dd8f31e9329`  
		Last Modified: Tue, 03 Feb 2026 02:44:29 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5b07b90d99f75c07ac2962182cea4a914e329742759219dfe660055213a6b0`  
		Last Modified: Tue, 03 Feb 2026 02:44:30 GMT  
		Size: 7.9 MB (7883128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83372eb1b6397a36f36e6013bece01cee7cedc014fe3c311f470925ff65780d2`  
		Last Modified: Tue, 03 Feb 2026 02:44:32 GMT  
		Size: 77.4 MB (77380918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a88a440b80b25b36f61a176bd75bbc21ca304a8472923e1fb782a959cdcd37`  
		Last Modified: Tue, 03 Feb 2026 02:44:29 GMT  
		Size: 424.2 KB (424191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc7794c0a906c77aa52409af359f9083b620d147ff60ced85f511e3c9efbf7b`  
		Last Modified: Tue, 03 Feb 2026 02:44:30 GMT  
		Size: 99.6 KB (99598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f1ccbf7f15bb9c4d67592591c93463832f045a5095f2390029a39828fe5b01`  
		Last Modified: Tue, 03 Feb 2026 02:44:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94db2487c03661363dca2d3abbff43337442842d60496b36cf89965c61b4b675`  
		Last Modified: Tue, 03 Feb 2026 02:44:32 GMT  
		Size: 42.4 MB (42436519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86df68ccc130acb38f0147f5f25e98e16307e733aafc12d8fe390c61eeeec70d`  
		Last Modified: Tue, 03 Feb 2026 02:44:32 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a2e8e6d0b224a88404c2c544ef4ec64038b9451cf97397e54bcc80ffe6a324fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e5b9b18ba252c2abc60b8ed958e735792e18d91541469a84c2ed7c00a35615`

```dockerfile
```

-	Layers:
	-	`sha256:326038181cc4d4767c5270a11f64e357cb051045d992d4f641600a02521311fa`  
		Last Modified: Tue, 03 Feb 2026 02:44:30 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84365dc8ddfed096f5d9a6f1a58b73cd21db638f5ff79daa6bb9be0048d37fd7`  
		Last Modified: Tue, 03 Feb 2026 02:44:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 7.7 MB (7693146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb5da74a812f294be30343ff89ed9604ba248e5e135425a3bb7906968f1e64`  
		Last Modified: Tue, 13 Jan 2026 02:21:23 GMT  
		Size: 76.7 MB (76691847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66868d5948d44e96078e5fa525df7e09c89d0e7cc0cb09f0fc48aeeb30707c4e`  
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 392.7 KB (392739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b4cd7f59188339c71711d75181a6f4fd7fab268e8ca419321d58f9759d5a1`  
		Last Modified: Tue, 13 Jan 2026 02:21:22 GMT  
		Size: 99.5 KB (99466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d1f922c928a80bb685cb6e00a39fd3e289a4a71153df9e0713dc6f8ca02ff`  
		Last Modified: Tue, 13 Jan 2026 02:21:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 24.7 KB (24702 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:22dc44a88a0371f80361ab6f85a5b7d39458b202c85522dc7ebc658ded7ae3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150097020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09c5eaf4739c8c3e5790287157dc7d86b0374248f3234dcc0a370df426bfb5a`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:45:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 03:45:47 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 03 Feb 2026 03:45:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 03:46:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 03:46:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 03:46:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 03 Feb 2026 03:46:16 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 03 Feb 2026 03:46:16 GMT
VOLUME [/opt/nouveau/data]
# Tue, 03 Feb 2026 03:46:16 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 03 Feb 2026 03:46:16 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb860f9d20bff7fff3a85718356f5a554630a0edef1b792a07e2f891c31e2e47`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0bfe0ea53c745bcc02b9c320ebc361f18862f770f2a63f769ff6c59bc52096`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 7.4 MB (7398867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df89cda60390f6a4bc70aa899d6a3ad5c95a3be0e9e4be9b6dfef46b249e25b`  
		Last Modified: Tue, 03 Feb 2026 03:46:39 GMT  
		Size: 73.2 MB (73153103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b698866ee0126f695019926dac18f75d2468d0db7629c0a629c305e05daaef1f`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 394.5 KB (394482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc97975a9bb1f45325c001458ab917b47dd350cbd5f3a01066d5e0360dcf257`  
		Last Modified: Tue, 03 Feb 2026 03:46:38 GMT  
		Size: 99.7 KB (99657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c10d1aa33dbbc68010a89d231eed3c5338967ea2aa309234c6729fbead0b0`  
		Last Modified: Tue, 03 Feb 2026 03:46:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357ec97a4a96a0cad87e65c19bae5cb4476e8a753023ce27074575c2f8e103b0`  
		Last Modified: Tue, 03 Feb 2026 03:46:40 GMT  
		Size: 42.2 MB (42164646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62682c9cfe85a9b667830d2cf0305ef7b2324664f19e6e84de8eb123d94b481d`  
		Last Modified: Tue, 03 Feb 2026 03:46:39 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:86dfe5c4619f7a3ff038b187699a59be7c657c4d7b11872406fac86e1f8ec333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb2292c9e53fad4174e4281b6cd5aec35a6c3ab33f6700814b6d62030254abf`

```dockerfile
```

-	Layers:
	-	`sha256:33c40b2d5f4d455f3d140993dc0be02e39beed228047c960ed3c21c55c8db8d9`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8a7bb80c2b3c2960a931b6888cee83ac2e0223bb152adb2f5f1cba40b708861`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:313b7a449b04e2a8932f9fae9bc97be981d008fd421feeb02093360ca7bc646c
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
$ docker pull couchdb@sha256:aac77b412f9b677997c99662c0a023dade216b707de7a8bdc4d469d2f5e81643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139015389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a51bdd69ab04116edb43a01de5ec2a751ea377b2cb2b649f43f752b717d2fc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:02 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 02:44:02 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 03 Feb 2026 02:44:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 02:44:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:15 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 03 Feb 2026 02:44:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 02:44:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Feb 2026 02:44:27 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 03 Feb 2026 02:44:27 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 03 Feb 2026 02:44:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 03 Feb 2026 02:44:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:44:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:44:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Feb 2026 02:44:28 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 03 Feb 2026 02:44:28 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45b1da3f12207180a76ed743d41046755fa50bdeaffcc59635187d8f834beeb`  
		Last Modified: Tue, 03 Feb 2026 02:44:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4186beca0d86885f3d742d955ccbce4e0ccb84238863b6a9fb2be122679fce5`  
		Last Modified: Tue, 03 Feb 2026 02:44:41 GMT  
		Size: 7.9 MB (7883138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb16d31e9d2f5b969fc1eecb4fcc84d4edd117a897d2733e413285ba1449ce`  
		Last Modified: Tue, 03 Feb 2026 02:44:41 GMT  
		Size: 401.8 KB (401793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade8f22c2d1e880fdbfe161eacd8d4b82c2d73d9227485b5d5725a92e89c66e1`  
		Last Modified: Tue, 03 Feb 2026 02:44:41 GMT  
		Size: 76.5 KB (76509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c95cd4895b2aa5faf8f05fb0fd9f3c0e12a8c3bd452553d6514cd6cb0a7154`  
		Last Modified: Tue, 03 Feb 2026 02:44:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54dec8167d3120dd598f8afd9acb96717f1d9d513cad6ef490d15a6d21f1df4f`  
		Last Modified: Tue, 03 Feb 2026 02:44:44 GMT  
		Size: 102.4 MB (102420033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc86784552f1429f42f967125813a34a797b3759c187c43ab0e6ca67e8385c1`  
		Last Modified: Tue, 03 Feb 2026 02:44:42 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4fdf2b1daee4c6150b61ad856a57b4d588c13c6e31195c8471ec70567e765`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7f3d2ff49bae51a619633133dc33a53d61f170ce355e343c22257fa2d34f97`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622358bb33282a035317f5c9d179cdd98d13b3525a9ec50d5d1136e4ae0db733`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:ac86e0510fbb316d0de63fc3fa2ca75e1c6187273ba4d9ab35a8ff9b63e275cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b81d5c6af5e1f4e4eb2b5362dd8a839943b57cc3293d1e0c7ffc832531ea36`

```dockerfile
```

-	Layers:
	-	`sha256:ccc292c37925ef7039affe11b7fc28e94277ae27ab9f9c05a446fac277f91e97`  
		Last Modified: Tue, 03 Feb 2026 02:44:41 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e923ae4bc753d366f140b7364747979bd3f80c578fdcf023858d577b0c2ac37`  
		Last Modified: Tue, 03 Feb 2026 02:44:41 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:21:57 GMT  
		Size: 7.7 MB (7693187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e0783e8739b88f04c92eb1b3936f5047d8a36ba4044fbf5fe21580ceb39f0c`  
		Last Modified: Tue, 13 Jan 2026 02:21:57 GMT  
		Size: 370.5 KB (370522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d88aa04437e2ce164a28fd76913203215b1003379a5c835da38c57ceb6900ee`  
		Last Modified: Tue, 13 Jan 2026 02:21:57 GMT  
		Size: 76.5 KB (76482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d032fa4100c076bee3e5cf37b8a3b1b2a3de179b8118cbefb7a153a96da1c37`  
		Last Modified: Tue, 13 Jan 2026 02:21:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce57e808f2a9831c927cbec451efdea32a3082f88d25f35b5baff7da114c4fab`  
		Last Modified: Tue, 13 Jan 2026 02:22:01 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:21:59 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ce7b287af1d5de35d38fcd17af289d9af21e1e3a3e9db336510be0f63dc753`  
		Last Modified: Tue, 13 Jan 2026 02:21:59 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:21:57 GMT  
		Size: 4.1 MB (4125664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20c92a325d7b334410edd982cf7efdca1b61238606683f7ca6a9788c22cab8fc`  
		Last Modified: Tue, 13 Jan 2026 02:21:57 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:dc2029d0e0f8f74befed1d78a4b9ad3ae2385bf1be51b3640d28af647fd220a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135793804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be05d50ccc6f272f4fb39265c4055811fbbb2f0b7eb699af3d13ff48f87a34f8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:45:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 03:45:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 03 Feb 2026 03:45:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 03:45:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 03:45:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:47 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 03 Feb 2026 03:46:45 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 03:47:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Feb 2026 03:47:02 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 03 Feb 2026 03:47:02 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 03 Feb 2026 03:47:02 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 03 Feb 2026 03:47:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 03:47:02 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:47:02 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Feb 2026 03:47:02 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 03 Feb 2026 03:47:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02b13c2167da67366f3b654df0b591a74a3ceda0090898972764c16c230c05d`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106bb0fe71c6f312e2b1f959ca60f93081c3ee9281519aa63c3d43e8dd80a695`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 7.4 MB (7398885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e553654c359f6f0b8b1971a834e87804e73de794834a70588cf062e0dfa737be`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 372.1 KB (372135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4b0edbcef0c9ef2e30cbb6abc0dd368eb2da9cd9092867b563c0474dc73628`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 76.5 KB (76541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1443d2fd613a346a729eeb94921553b0eafeab4c3875b86dc306ee7777335ba`  
		Last Modified: Tue, 03 Feb 2026 03:47:21 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697c9fed441ad0ba1463bd93962ddb0977d8f5b6c8f37022a38ffa2cfa93f61e`  
		Last Modified: Tue, 03 Feb 2026 03:47:23 GMT  
		Size: 101.1 MB (101056421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c478697576a996f6f9762244b5f0501c144d6812e3f14e09a1c5dc5bcf9bf3d4`  
		Last Modified: Tue, 03 Feb 2026 03:47:21 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ca0de162f1d0f05891a48753d932cfb34fef3c040349ababa26cb115f38e58`  
		Last Modified: Tue, 03 Feb 2026 03:47:21 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3bda17fbc7d4720c68633b09a1b6aa5c600d322e37cd8afb0cc022f021620f`  
		Last Modified: Tue, 03 Feb 2026 03:47:22 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b776900ab2b08e2708646deeff0cac7b3886b80057b0114111c5cb95a219062b`  
		Last Modified: Tue, 03 Feb 2026 03:47:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:cc3e2c1199ae634af8fb1b642cc65010ec43a35bae9bc96d868f7b3cf230c443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416f4f0676a2fa51d0d43b96258f20266a991397826f4c902ae8c89514fa304c`

```dockerfile
```

-	Layers:
	-	`sha256:90e227cf439725b4ac0683f0cde55ab3bac521e02273fc513fc8a48cc408b03d`  
		Last Modified: Tue, 03 Feb 2026 03:47:21 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d8a9c351f6371d1b78dd226c0937e4e48669b0b5fc6adb562f38ac9b03b4ca5`  
		Last Modified: Tue, 03 Feb 2026 03:47:21 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:37817405c0fe7d7f90b58cfa5a98468be5589335e95b63678d82d70a7d0c85b6
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
$ docker pull couchdb@sha256:2469daedfc14b00896bba205842e88693907313ffaf2a8a8dcda5abed460fb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156454338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9e50bc855af74b66ba87f72d681e0d2d3c38363ef8adae21f2969904a8f882`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 02:44:03 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 03 Feb 2026 02:44:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 02:44:19 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 02:44:23 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:23 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 02:44:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 03 Feb 2026 02:44:28 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 03 Feb 2026 02:44:28 GMT
VOLUME [/opt/nouveau/data]
# Tue, 03 Feb 2026 02:44:28 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 03 Feb 2026 02:44:28 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a113b4fd8821b9e44f5da0ae5217897eacd0245f12a04f7f7917a073dd6f3`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0630102d2ee40e20e9dbfaffa3fb102c86ef0002977ac757d0ee0168851861f2`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
		Size: 7.9 MB (7883109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3df44a49e67c1dc0e295dd329594accc26d4c30f314e56dddd35daa08d6ecc`  
		Last Modified: Tue, 03 Feb 2026 02:44:45 GMT  
		Size: 77.4 MB (77380926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4fe4c9403067b25d790ff59bae6d7795babd88f380542b39a147211a31aa4a`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
		Size: 424.2 KB (424169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05cb5011018aaaa46bd1d01128f36dd9a9fe0dde7350465c74c3614ef49b6a6`  
		Last Modified: Tue, 03 Feb 2026 02:44:44 GMT  
		Size: 99.6 KB (99574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f51e348c7df894594cef898f9ba84b5d2d357668ce05ed9a38f1c4bf0d887`  
		Last Modified: Tue, 03 Feb 2026 02:44:45 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2980f82eb9489857b06e17a4497f937fc61d8177e28bbbb4b6ea54c69c7b8f`  
		Last Modified: Tue, 03 Feb 2026 02:44:46 GMT  
		Size: 42.4 MB (42436190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aef9766520afd1455b8579ac6253f1e552aa7e3aef7c8f4fba787ddcd3e1357`  
		Last Modified: Tue, 03 Feb 2026 02:44:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c4070acadca58f5aa2c28851a339ee48c63c853c7722c0bedb93ae72a3173a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb142a2159a1d314b02d87ce9361ff8f4c75550a4555036e0ca01bc215fefe8`

```dockerfile
```

-	Layers:
	-	`sha256:192eac4dc4d64aecdfef84e6ae45cd578c04a8611f650a5697e4912c96b572f6`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
		Size: 3.7 MB (3657789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4336cc059dd79e7d7cc5d3fee1bef653defb7cb8a1ca26c21347c531b282a7`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:23:12 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6eb57c01e90651acba770ed9077031c2d1f894e820a6a77fab5fc3f062c5ac`  
		Last Modified: Tue, 13 Jan 2026 02:23:13 GMT  
		Size: 7.7 MB (7693195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92378f8e2c7fa5184fef765384307a8f0d8d4be6ab9aef65ae867d78df1c7220`  
		Last Modified: Tue, 13 Jan 2026 02:23:14 GMT  
		Size: 76.7 MB (76691818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6eb9ed2f797a97ee19983ec050f73e5f63e2f8a6b65f873309932b79ed2b68`  
		Last Modified: Tue, 13 Jan 2026 02:23:12 GMT  
		Size: 392.8 KB (392750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6149b46e4eb75af61de43c8d402dd4882d4b893beea4bdf54286e15c4545189`  
		Last Modified: Tue, 13 Jan 2026 02:23:13 GMT  
		Size: 99.5 KB (99498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffafb2a57977e0b46429ecdddcf7d4f022cb81a1cf5a16a973ca642467283206`  
		Last Modified: Tue, 13 Jan 2026 02:23:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7327d876b5fc48a1f620ef884d5f099170a9f3ba0cd76bcd13ef5bc178484d`  
		Last Modified: Tue, 13 Jan 2026 02:23:15 GMT  
		Size: 42.3 MB (42338126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcbedab60f1f391d8b76cde4fe951e417fcf8398ffd0a21a17e514866dd65be`  
		Last Modified: Tue, 13 Jan 2026 02:23:15 GMT  
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
$ docker pull couchdb@sha256:0dff9b22178942afd31c4704706389ace99f8b6d4ef20f300d44c720f6ca5950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150095350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f00e1cceda2f091b85971a5ebfe9b85646dd3a34f04b536a40df915319662e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:45:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 03:45:47 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 03 Feb 2026 03:45:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 03:46:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 03:46:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 03:47:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 03 Feb 2026 03:47:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 03 Feb 2026 03:47:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 03 Feb 2026 03:47:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 03 Feb 2026 03:47:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb860f9d20bff7fff3a85718356f5a554630a0edef1b792a07e2f891c31e2e47`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0bfe0ea53c745bcc02b9c320ebc361f18862f770f2a63f769ff6c59bc52096`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 7.4 MB (7398867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df89cda60390f6a4bc70aa899d6a3ad5c95a3be0e9e4be9b6dfef46b249e25b`  
		Last Modified: Tue, 03 Feb 2026 03:46:39 GMT  
		Size: 73.2 MB (73153103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b698866ee0126f695019926dac18f75d2468d0db7629c0a629c305e05daaef1f`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 394.5 KB (394482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc97975a9bb1f45325c001458ab917b47dd350cbd5f3a01066d5e0360dcf257`  
		Last Modified: Tue, 03 Feb 2026 03:46:38 GMT  
		Size: 99.7 KB (99657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c10d1aa33dbbc68010a89d231eed3c5338967ea2aa309234c6729fbead0b0`  
		Last Modified: Tue, 03 Feb 2026 03:46:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826d3a179c9b053eb5b8e5e6d8c7176dcd13f7da532db2f38ddd56741ee87414`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 42.2 MB (42162977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd5a74e8aeead2c02c39c1b43ab35c50401b4bc6672b714aa717f086dd387e8`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f34ab014080b714b57cc50344a1e813ebfa6fabad3a6f1fac14823cae1ab6333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2496185fb9a73a22b3a5471e312359965d1b76d0cf8c63d5e3a9b613a7a97d25`

```dockerfile
```

-	Layers:
	-	`sha256:9f6534cc4934972cf6c8345edc81ad797aff63247271196393ff6be249a8ff34`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 3.6 MB (3648318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb7d53e05b358825210d7ddf7fe81467db60b8e7dcd9373389e691ff4f9f6e67`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:313b7a449b04e2a8932f9fae9bc97be981d008fd421feeb02093360ca7bc646c
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
$ docker pull couchdb@sha256:aac77b412f9b677997c99662c0a023dade216b707de7a8bdc4d469d2f5e81643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139015389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a51bdd69ab04116edb43a01de5ec2a751ea377b2cb2b649f43f752b717d2fc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:02 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 02:44:02 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 03 Feb 2026 02:44:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 02:44:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:15 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 03 Feb 2026 02:44:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 02:44:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Feb 2026 02:44:27 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 03 Feb 2026 02:44:27 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 03 Feb 2026 02:44:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 03 Feb 2026 02:44:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:44:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:44:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Feb 2026 02:44:28 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 03 Feb 2026 02:44:28 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45b1da3f12207180a76ed743d41046755fa50bdeaffcc59635187d8f834beeb`  
		Last Modified: Tue, 03 Feb 2026 02:44:41 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4186beca0d86885f3d742d955ccbce4e0ccb84238863b6a9fb2be122679fce5`  
		Last Modified: Tue, 03 Feb 2026 02:44:41 GMT  
		Size: 7.9 MB (7883138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb16d31e9d2f5b969fc1eecb4fcc84d4edd117a897d2733e413285ba1449ce`  
		Last Modified: Tue, 03 Feb 2026 02:44:41 GMT  
		Size: 401.8 KB (401793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade8f22c2d1e880fdbfe161eacd8d4b82c2d73d9227485b5d5725a92e89c66e1`  
		Last Modified: Tue, 03 Feb 2026 02:44:41 GMT  
		Size: 76.5 KB (76509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c95cd4895b2aa5faf8f05fb0fd9f3c0e12a8c3bd452553d6514cd6cb0a7154`  
		Last Modified: Tue, 03 Feb 2026 02:44:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54dec8167d3120dd598f8afd9acb96717f1d9d513cad6ef490d15a6d21f1df4f`  
		Last Modified: Tue, 03 Feb 2026 02:44:44 GMT  
		Size: 102.4 MB (102420033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc86784552f1429f42f967125813a34a797b3759c187c43ab0e6ca67e8385c1`  
		Last Modified: Tue, 03 Feb 2026 02:44:42 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4fdf2b1daee4c6150b61ad856a57b4d588c13c6e31195c8471ec70567e765`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7f3d2ff49bae51a619633133dc33a53d61f170ce355e343c22257fa2d34f97`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622358bb33282a035317f5c9d179cdd98d13b3525a9ec50d5d1136e4ae0db733`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ac86e0510fbb316d0de63fc3fa2ca75e1c6187273ba4d9ab35a8ff9b63e275cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b81d5c6af5e1f4e4eb2b5362dd8a839943b57cc3293d1e0c7ffc832531ea36`

```dockerfile
```

-	Layers:
	-	`sha256:ccc292c37925ef7039affe11b7fc28e94277ae27ab9f9c05a446fac277f91e97`  
		Last Modified: Tue, 03 Feb 2026 02:44:41 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e923ae4bc753d366f140b7364747979bd3f80c578fdcf023858d577b0c2ac37`  
		Last Modified: Tue, 03 Feb 2026 02:44:41 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:21:57 GMT  
		Size: 7.7 MB (7693187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e0783e8739b88f04c92eb1b3936f5047d8a36ba4044fbf5fe21580ceb39f0c`  
		Last Modified: Tue, 13 Jan 2026 02:21:57 GMT  
		Size: 370.5 KB (370522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d88aa04437e2ce164a28fd76913203215b1003379a5c835da38c57ceb6900ee`  
		Last Modified: Tue, 13 Jan 2026 02:21:57 GMT  
		Size: 76.5 KB (76482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d032fa4100c076bee3e5cf37b8a3b1b2a3de179b8118cbefb7a153a96da1c37`  
		Last Modified: Tue, 13 Jan 2026 02:21:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce57e808f2a9831c927cbec451efdea32a3082f88d25f35b5baff7da114c4fab`  
		Last Modified: Tue, 13 Jan 2026 02:22:01 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:21:59 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ce7b287af1d5de35d38fcd17af289d9af21e1e3a3e9db336510be0f63dc753`  
		Last Modified: Tue, 13 Jan 2026 02:21:59 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:21:57 GMT  
		Size: 4.1 MB (4125664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20c92a325d7b334410edd982cf7efdca1b61238606683f7ca6a9788c22cab8fc`  
		Last Modified: Tue, 13 Jan 2026 02:21:57 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:dc2029d0e0f8f74befed1d78a4b9ad3ae2385bf1be51b3640d28af647fd220a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135793804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be05d50ccc6f272f4fb39265c4055811fbbb2f0b7eb699af3d13ff48f87a34f8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:45:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 03:45:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 03 Feb 2026 03:45:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 03:45:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 03:45:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:47 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 03 Feb 2026 03:46:45 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 03:47:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Feb 2026 03:47:02 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 03 Feb 2026 03:47:02 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 03 Feb 2026 03:47:02 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 03 Feb 2026 03:47:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 03:47:02 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:47:02 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Feb 2026 03:47:02 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 03 Feb 2026 03:47:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02b13c2167da67366f3b654df0b591a74a3ceda0090898972764c16c230c05d`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106bb0fe71c6f312e2b1f959ca60f93081c3ee9281519aa63c3d43e8dd80a695`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 7.4 MB (7398885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e553654c359f6f0b8b1971a834e87804e73de794834a70588cf062e0dfa737be`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 372.1 KB (372135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4b0edbcef0c9ef2e30cbb6abc0dd368eb2da9cd9092867b563c0474dc73628`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 76.5 KB (76541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1443d2fd613a346a729eeb94921553b0eafeab4c3875b86dc306ee7777335ba`  
		Last Modified: Tue, 03 Feb 2026 03:47:21 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697c9fed441ad0ba1463bd93962ddb0977d8f5b6c8f37022a38ffa2cfa93f61e`  
		Last Modified: Tue, 03 Feb 2026 03:47:23 GMT  
		Size: 101.1 MB (101056421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c478697576a996f6f9762244b5f0501c144d6812e3f14e09a1c5dc5bcf9bf3d4`  
		Last Modified: Tue, 03 Feb 2026 03:47:21 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ca0de162f1d0f05891a48753d932cfb34fef3c040349ababa26cb115f38e58`  
		Last Modified: Tue, 03 Feb 2026 03:47:21 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3bda17fbc7d4720c68633b09a1b6aa5c600d322e37cd8afb0cc022f021620f`  
		Last Modified: Tue, 03 Feb 2026 03:47:22 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b776900ab2b08e2708646deeff0cac7b3886b80057b0114111c5cb95a219062b`  
		Last Modified: Tue, 03 Feb 2026 03:47:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:cc3e2c1199ae634af8fb1b642cc65010ec43a35bae9bc96d868f7b3cf230c443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416f4f0676a2fa51d0d43b96258f20266a991397826f4c902ae8c89514fa304c`

```dockerfile
```

-	Layers:
	-	`sha256:90e227cf439725b4ac0683f0cde55ab3bac521e02273fc513fc8a48cc408b03d`  
		Last Modified: Tue, 03 Feb 2026 03:47:21 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d8a9c351f6371d1b78dd226c0937e4e48669b0b5fc6adb562f38ac9b03b4ca5`  
		Last Modified: Tue, 03 Feb 2026 03:47:21 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:37817405c0fe7d7f90b58cfa5a98468be5589335e95b63678d82d70a7d0c85b6
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
$ docker pull couchdb@sha256:2469daedfc14b00896bba205842e88693907313ffaf2a8a8dcda5abed460fb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156454338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9e50bc855af74b66ba87f72d681e0d2d3c38363ef8adae21f2969904a8f882`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 02:44:03 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 03 Feb 2026 02:44:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 02:44:19 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 02:44:23 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:23 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 02:44:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 03 Feb 2026 02:44:28 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 03 Feb 2026 02:44:28 GMT
VOLUME [/opt/nouveau/data]
# Tue, 03 Feb 2026 02:44:28 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 03 Feb 2026 02:44:28 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a113b4fd8821b9e44f5da0ae5217897eacd0245f12a04f7f7917a073dd6f3`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0630102d2ee40e20e9dbfaffa3fb102c86ef0002977ac757d0ee0168851861f2`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
		Size: 7.9 MB (7883109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3df44a49e67c1dc0e295dd329594accc26d4c30f314e56dddd35daa08d6ecc`  
		Last Modified: Tue, 03 Feb 2026 02:44:45 GMT  
		Size: 77.4 MB (77380926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4fe4c9403067b25d790ff59bae6d7795babd88f380542b39a147211a31aa4a`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
		Size: 424.2 KB (424169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05cb5011018aaaa46bd1d01128f36dd9a9fe0dde7350465c74c3614ef49b6a6`  
		Last Modified: Tue, 03 Feb 2026 02:44:44 GMT  
		Size: 99.6 KB (99574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f51e348c7df894594cef898f9ba84b5d2d357668ce05ed9a38f1c4bf0d887`  
		Last Modified: Tue, 03 Feb 2026 02:44:45 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2980f82eb9489857b06e17a4497f937fc61d8177e28bbbb4b6ea54c69c7b8f`  
		Last Modified: Tue, 03 Feb 2026 02:44:46 GMT  
		Size: 42.4 MB (42436190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aef9766520afd1455b8579ac6253f1e552aa7e3aef7c8f4fba787ddcd3e1357`  
		Last Modified: Tue, 03 Feb 2026 02:44:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c4070acadca58f5aa2c28851a339ee48c63c853c7722c0bedb93ae72a3173a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb142a2159a1d314b02d87ce9361ff8f4c75550a4555036e0ca01bc215fefe8`

```dockerfile
```

-	Layers:
	-	`sha256:192eac4dc4d64aecdfef84e6ae45cd578c04a8611f650a5697e4912c96b572f6`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
		Size: 3.7 MB (3657789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4336cc059dd79e7d7cc5d3fee1bef653defb7cb8a1ca26c21347c531b282a7`  
		Last Modified: Tue, 03 Feb 2026 02:44:43 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:23:12 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6eb57c01e90651acba770ed9077031c2d1f894e820a6a77fab5fc3f062c5ac`  
		Last Modified: Tue, 13 Jan 2026 02:23:13 GMT  
		Size: 7.7 MB (7693195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92378f8e2c7fa5184fef765384307a8f0d8d4be6ab9aef65ae867d78df1c7220`  
		Last Modified: Tue, 13 Jan 2026 02:23:14 GMT  
		Size: 76.7 MB (76691818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6eb9ed2f797a97ee19983ec050f73e5f63e2f8a6b65f873309932b79ed2b68`  
		Last Modified: Tue, 13 Jan 2026 02:23:12 GMT  
		Size: 392.8 KB (392750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6149b46e4eb75af61de43c8d402dd4882d4b893beea4bdf54286e15c4545189`  
		Last Modified: Tue, 13 Jan 2026 02:23:13 GMT  
		Size: 99.5 KB (99498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffafb2a57977e0b46429ecdddcf7d4f022cb81a1cf5a16a973ca642467283206`  
		Last Modified: Tue, 13 Jan 2026 02:23:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7327d876b5fc48a1f620ef884d5f099170a9f3ba0cd76bcd13ef5bc178484d`  
		Last Modified: Tue, 13 Jan 2026 02:23:15 GMT  
		Size: 42.3 MB (42338126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcbedab60f1f391d8b76cde4fe951e417fcf8398ffd0a21a17e514866dd65be`  
		Last Modified: Tue, 13 Jan 2026 02:23:15 GMT  
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
$ docker pull couchdb@sha256:0dff9b22178942afd31c4704706389ace99f8b6d4ef20f300d44c720f6ca5950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150095350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f00e1cceda2f091b85971a5ebfe9b85646dd3a34f04b536a40df915319662e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:45:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 03:45:47 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 03 Feb 2026 03:45:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 03:46:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 03:46:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 03:47:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 03 Feb 2026 03:47:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 03 Feb 2026 03:47:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 03 Feb 2026 03:47:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 03 Feb 2026 03:47:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb860f9d20bff7fff3a85718356f5a554630a0edef1b792a07e2f891c31e2e47`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0bfe0ea53c745bcc02b9c320ebc361f18862f770f2a63f769ff6c59bc52096`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 7.4 MB (7398867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df89cda60390f6a4bc70aa899d6a3ad5c95a3be0e9e4be9b6dfef46b249e25b`  
		Last Modified: Tue, 03 Feb 2026 03:46:39 GMT  
		Size: 73.2 MB (73153103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b698866ee0126f695019926dac18f75d2468d0db7629c0a629c305e05daaef1f`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 394.5 KB (394482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc97975a9bb1f45325c001458ab917b47dd350cbd5f3a01066d5e0360dcf257`  
		Last Modified: Tue, 03 Feb 2026 03:46:38 GMT  
		Size: 99.7 KB (99657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c10d1aa33dbbc68010a89d231eed3c5338967ea2aa309234c6729fbead0b0`  
		Last Modified: Tue, 03 Feb 2026 03:46:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826d3a179c9b053eb5b8e5e6d8c7176dcd13f7da532db2f38ddd56741ee87414`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 42.2 MB (42162977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd5a74e8aeead2c02c39c1b43ab35c50401b4bc6672b714aa717f086dd387e8`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f34ab014080b714b57cc50344a1e813ebfa6fabad3a6f1fac14823cae1ab6333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2496185fb9a73a22b3a5471e312359965d1b76d0cf8c63d5e3a9b613a7a97d25`

```dockerfile
```

-	Layers:
	-	`sha256:9f6534cc4934972cf6c8345edc81ad797aff63247271196393ff6be249a8ff34`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 3.6 MB (3648318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb7d53e05b358825210d7ddf7fe81467db60b8e7dcd9373389e691ff4f9f6e67`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:94d0d67147335d37df957f3ace915c06eccf4c1d58ad558d614aae31f42b3187
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
$ docker pull couchdb@sha256:b8bdc4d8197b9750ad9ef55b4451df82c2552a1e48d25cb8d27f86901b0f45cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142051769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33093ab0977f79e9ab863423ea5f4dbca301ef181fc2d582a00cc9c7f828f0b2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 02:43:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 03 Feb 2026 02:43:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 02:43:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 02:43:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:57 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 03 Feb 2026 02:43:57 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 02:44:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Feb 2026 02:44:09 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 03 Feb 2026 02:44:09 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:44:10 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Feb 2026 02:44:10 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 03 Feb 2026 02:44:10 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f95f560da8e3bdb596e84a890ee559e80ffcd0ffb2154713b84dd9160890245`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592f333a628d569980303d3af9357c11ca01d55d117a3196fcee0f788b6f5e64`  
		Last Modified: Tue, 03 Feb 2026 02:44:23 GMT  
		Size: 7.9 MB (7883160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46c85312097de70d8c3bb3d7ee5e3673c1731b6d313d4b6530de6f23ef9b703`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 401.8 KB (401799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ce674f9f9d416860b6ebffbf149ef1784a8da66ef19fd90f0abe6e5c8e8c09`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 76.5 KB (76541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd653d782a5746a5d49d07d4802d8aee9a39c177c89a61b9e02b8179ad5443d`  
		Last Modified: Tue, 03 Feb 2026 02:44:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd05477ed76b6361c96a6d5a6c5aa0b0e2b6be7d21f838cbf5fc17d0afe2b94`  
		Last Modified: Tue, 03 Feb 2026 02:44:27 GMT  
		Size: 105.5 MB (105456346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbe85d7425385b2507026901a39d017eb7273857ed496f22bec013c79fcdbb7`  
		Last Modified: Tue, 03 Feb 2026 02:44:24 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92911ab6e4d1ec2897e491318968d3ddced0573c5f8e4b798656729a21a3448`  
		Last Modified: Tue, 03 Feb 2026 02:44:24 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9634e08b060e5bb74c236c6c3796b6f1c7bd45c2ec7c0cd648b6f46ba77ae208`  
		Last Modified: Tue, 03 Feb 2026 02:44:25 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928bfbf0e88dd45b798f5b852dc8ab17fc67c4ba815089838ef07188049bde07`  
		Last Modified: Tue, 03 Feb 2026 02:44:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:28fea4b5eef08c55dc31fb28c5fa3ce0b4e9c97da4a66d34340a0c83f31e488d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e0218401bdf13e40ccb7e8c80392ff02a670f0efcaf8559d00dc8718dc5be7`

```dockerfile
```

-	Layers:
	-	`sha256:6dda1c9ccabd43968c41a96d68ffa5d4e866caadac602f60485d0be2b85ce991`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f5c1ba2284296507eb9bd9ed9f407820c80912f37156ddd0bf69cb46f7990e`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8eca98d844737e7391af0ba3bd078c33c9b79484694a82e1a51f2a29ebfc0b`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 7.7 MB (7693190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d4cff2a33ca97c469fc8ab6c3284395941ba8b2cff8f4361b3ab4a1b366eb5`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:54 GMT  
		Size: 105.2 MB (105156763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c03434704503155ed2343afd552fb957cce1a8b2680b8b7d8344138e2a6597`  
		Last Modified: Tue, 13 Jan 2026 02:20:52 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d999d45b1b181000acaa083e513b632b05025450d49f6009d16400b8cf257624`  
		Last Modified: Tue, 13 Jan 2026 02:20:52 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc56c71044322b328f24d81b4873610894af8d49b91b8a31513590266fe49`  
		Last Modified: Tue, 13 Jan 2026 02:20:53 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cd1196c4cb96149708b21622838788a0cf61a569067e10485f4f12efecb2c4`  
		Last Modified: Tue, 13 Jan 2026 02:20:53 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50d4d6e4b72e86f1a95b7c50ce2ca2099a3a9a898205250f448399f4b707c08`  
		Last Modified: Tue, 13 Jan 2026 02:20:50 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:b89995d4cc477862a92b00132e63e9bdbeaa2e1275399b8c499b4ae8ff484283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96adb63f1df519a3512423ccc509050f50f1aa43b8377a35e9f8c4f876bd01fc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:45:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 03:45:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 03 Feb 2026 03:45:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 03:45:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 03:45:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:47 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 03 Feb 2026 03:45:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:46:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Feb 2026 03:46:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 03 Feb 2026 03:46:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02b13c2167da67366f3b654df0b591a74a3ceda0090898972764c16c230c05d`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106bb0fe71c6f312e2b1f959ca60f93081c3ee9281519aa63c3d43e8dd80a695`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 7.4 MB (7398885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e553654c359f6f0b8b1971a834e87804e73de794834a70588cf062e0dfa737be`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 372.1 KB (372135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4b0edbcef0c9ef2e30cbb6abc0dd368eb2da9cd9092867b563c0474dc73628`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 76.5 KB (76541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec92d49aef09eb0f577a0d64c82ee3a193ce554f913871aea28e0fbc0c547d7`  
		Last Modified: Tue, 03 Feb 2026 03:46:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc9b0eb3cf5654309cf322615685bbb1ea31e67782f9536ce65890c8fb83fb8`  
		Last Modified: Tue, 03 Feb 2026 03:46:28 GMT  
		Size: 104.0 MB (104028287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4810a95d166c559450d5305e9bc0afbd6f19fcfda85855677ff4e8bf7e68e6`  
		Last Modified: Tue, 03 Feb 2026 03:46:25 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c1119ba5c69ff7a21a171a1ac2426fa7672882940a8817641966dbc1e349f`  
		Last Modified: Tue, 03 Feb 2026 03:46:25 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e5f136944350478b46d365514b083f6088c42948cb115e4bdd7da7b0784b78`  
		Last Modified: Tue, 03 Feb 2026 03:46:26 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16af054f32548ea40fd3afa36f7d37e965983c035312f702653ec8f1cbc143d3`  
		Last Modified: Tue, 03 Feb 2026 03:46:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:423824caae2974643c0d72cdafd5f8a8b9894e8218c49e1f54f92b9c667d96a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f153ea1b594180284242ac7bb097fd386410f9a814283f2119059be22202fcf`

```dockerfile
```

-	Layers:
	-	`sha256:f340e5b4727b7d09238aef9c6694ab43abc848711d767fabbf3c5394102bd764`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0db4b1900a587958931c2cbf5f8e1ed873e849a9b6d08b3f2ade31ab9563bf`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:5ccd971808f4b7eec5d5599174f15e68598259bfc2fa9283a5aba07b94e70388
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
$ docker pull couchdb@sha256:2b64016ceeedcbe65bec9fdf719a6f0520cfdeda292899f948b6f02ecd72aa1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156454720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0f8c67278d19a9a18cdec7e5a892300ef237a9fcb7816241ddfc8788de4735`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:44 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 02:43:44 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 03 Feb 2026 02:43:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 02:44:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 02:44:07 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:07 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 02:44:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 03 Feb 2026 02:44:13 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 03 Feb 2026 02:44:13 GMT
VOLUME [/opt/nouveau/data]
# Tue, 03 Feb 2026 02:44:13 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 03 Feb 2026 02:44:13 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2f1fc1251780f2123a88ec6b1625b1f161e25efd41504f70275dd8f31e9329`  
		Last Modified: Tue, 03 Feb 2026 02:44:29 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5b07b90d99f75c07ac2962182cea4a914e329742759219dfe660055213a6b0`  
		Last Modified: Tue, 03 Feb 2026 02:44:30 GMT  
		Size: 7.9 MB (7883128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83372eb1b6397a36f36e6013bece01cee7cedc014fe3c311f470925ff65780d2`  
		Last Modified: Tue, 03 Feb 2026 02:44:32 GMT  
		Size: 77.4 MB (77380918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a88a440b80b25b36f61a176bd75bbc21ca304a8472923e1fb782a959cdcd37`  
		Last Modified: Tue, 03 Feb 2026 02:44:29 GMT  
		Size: 424.2 KB (424191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc7794c0a906c77aa52409af359f9083b620d147ff60ced85f511e3c9efbf7b`  
		Last Modified: Tue, 03 Feb 2026 02:44:30 GMT  
		Size: 99.6 KB (99598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f1ccbf7f15bb9c4d67592591c93463832f045a5095f2390029a39828fe5b01`  
		Last Modified: Tue, 03 Feb 2026 02:44:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94db2487c03661363dca2d3abbff43337442842d60496b36cf89965c61b4b675`  
		Last Modified: Tue, 03 Feb 2026 02:44:32 GMT  
		Size: 42.4 MB (42436519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86df68ccc130acb38f0147f5f25e98e16307e733aafc12d8fe390c61eeeec70d`  
		Last Modified: Tue, 03 Feb 2026 02:44:32 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a2e8e6d0b224a88404c2c544ef4ec64038b9451cf97397e54bcc80ffe6a324fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e5b9b18ba252c2abc60b8ed958e735792e18d91541469a84c2ed7c00a35615`

```dockerfile
```

-	Layers:
	-	`sha256:326038181cc4d4767c5270a11f64e357cb051045d992d4f641600a02521311fa`  
		Last Modified: Tue, 03 Feb 2026 02:44:30 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84365dc8ddfed096f5d9a6f1a58b73cd21db638f5ff79daa6bb9be0048d37fd7`  
		Last Modified: Tue, 03 Feb 2026 02:44:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 7.7 MB (7693146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb5da74a812f294be30343ff89ed9604ba248e5e135425a3bb7906968f1e64`  
		Last Modified: Tue, 13 Jan 2026 02:21:23 GMT  
		Size: 76.7 MB (76691847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66868d5948d44e96078e5fa525df7e09c89d0e7cc0cb09f0fc48aeeb30707c4e`  
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 392.7 KB (392739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b4cd7f59188339c71711d75181a6f4fd7fab268e8ca419321d58f9759d5a1`  
		Last Modified: Tue, 13 Jan 2026 02:21:22 GMT  
		Size: 99.5 KB (99466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d1f922c928a80bb685cb6e00a39fd3e289a4a71153df9e0713dc6f8ca02ff`  
		Last Modified: Tue, 13 Jan 2026 02:21:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 24.7 KB (24702 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:22dc44a88a0371f80361ab6f85a5b7d39458b202c85522dc7ebc658ded7ae3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150097020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09c5eaf4739c8c3e5790287157dc7d86b0374248f3234dcc0a370df426bfb5a`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:45:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 03:45:47 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 03 Feb 2026 03:45:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 03:46:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 03:46:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 03:46:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 03 Feb 2026 03:46:16 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 03 Feb 2026 03:46:16 GMT
VOLUME [/opt/nouveau/data]
# Tue, 03 Feb 2026 03:46:16 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 03 Feb 2026 03:46:16 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb860f9d20bff7fff3a85718356f5a554630a0edef1b792a07e2f891c31e2e47`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0bfe0ea53c745bcc02b9c320ebc361f18862f770f2a63f769ff6c59bc52096`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 7.4 MB (7398867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df89cda60390f6a4bc70aa899d6a3ad5c95a3be0e9e4be9b6dfef46b249e25b`  
		Last Modified: Tue, 03 Feb 2026 03:46:39 GMT  
		Size: 73.2 MB (73153103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b698866ee0126f695019926dac18f75d2468d0db7629c0a629c305e05daaef1f`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 394.5 KB (394482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc97975a9bb1f45325c001458ab917b47dd350cbd5f3a01066d5e0360dcf257`  
		Last Modified: Tue, 03 Feb 2026 03:46:38 GMT  
		Size: 99.7 KB (99657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c10d1aa33dbbc68010a89d231eed3c5338967ea2aa309234c6729fbead0b0`  
		Last Modified: Tue, 03 Feb 2026 03:46:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357ec97a4a96a0cad87e65c19bae5cb4476e8a753023ce27074575c2f8e103b0`  
		Last Modified: Tue, 03 Feb 2026 03:46:40 GMT  
		Size: 42.2 MB (42164646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62682c9cfe85a9b667830d2cf0305ef7b2324664f19e6e84de8eb123d94b481d`  
		Last Modified: Tue, 03 Feb 2026 03:46:39 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:86dfe5c4619f7a3ff038b187699a59be7c657c4d7b11872406fac86e1f8ec333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb2292c9e53fad4174e4281b6cd5aec35a6c3ab33f6700814b6d62030254abf`

```dockerfile
```

-	Layers:
	-	`sha256:33c40b2d5f4d455f3d140993dc0be02e39beed228047c960ed3c21c55c8db8d9`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8a7bb80c2b3c2960a931b6888cee83ac2e0223bb152adb2f5f1cba40b708861`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1`

```console
$ docker pull couchdb@sha256:94d0d67147335d37df957f3ace915c06eccf4c1d58ad558d614aae31f42b3187
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
$ docker pull couchdb@sha256:b8bdc4d8197b9750ad9ef55b4451df82c2552a1e48d25cb8d27f86901b0f45cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142051769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33093ab0977f79e9ab863423ea5f4dbca301ef181fc2d582a00cc9c7f828f0b2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 02:43:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 03 Feb 2026 02:43:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 02:43:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 02:43:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:57 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 03 Feb 2026 02:43:57 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 02:44:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Feb 2026 02:44:09 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 03 Feb 2026 02:44:09 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:44:10 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Feb 2026 02:44:10 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 03 Feb 2026 02:44:10 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f95f560da8e3bdb596e84a890ee559e80ffcd0ffb2154713b84dd9160890245`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592f333a628d569980303d3af9357c11ca01d55d117a3196fcee0f788b6f5e64`  
		Last Modified: Tue, 03 Feb 2026 02:44:23 GMT  
		Size: 7.9 MB (7883160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46c85312097de70d8c3bb3d7ee5e3673c1731b6d313d4b6530de6f23ef9b703`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 401.8 KB (401799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ce674f9f9d416860b6ebffbf149ef1784a8da66ef19fd90f0abe6e5c8e8c09`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 76.5 KB (76541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd653d782a5746a5d49d07d4802d8aee9a39c177c89a61b9e02b8179ad5443d`  
		Last Modified: Tue, 03 Feb 2026 02:44:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd05477ed76b6361c96a6d5a6c5aa0b0e2b6be7d21f838cbf5fc17d0afe2b94`  
		Last Modified: Tue, 03 Feb 2026 02:44:27 GMT  
		Size: 105.5 MB (105456346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbe85d7425385b2507026901a39d017eb7273857ed496f22bec013c79fcdbb7`  
		Last Modified: Tue, 03 Feb 2026 02:44:24 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92911ab6e4d1ec2897e491318968d3ddced0573c5f8e4b798656729a21a3448`  
		Last Modified: Tue, 03 Feb 2026 02:44:24 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9634e08b060e5bb74c236c6c3796b6f1c7bd45c2ec7c0cd648b6f46ba77ae208`  
		Last Modified: Tue, 03 Feb 2026 02:44:25 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928bfbf0e88dd45b798f5b852dc8ab17fc67c4ba815089838ef07188049bde07`  
		Last Modified: Tue, 03 Feb 2026 02:44:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:28fea4b5eef08c55dc31fb28c5fa3ce0b4e9c97da4a66d34340a0c83f31e488d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e0218401bdf13e40ccb7e8c80392ff02a670f0efcaf8559d00dc8718dc5be7`

```dockerfile
```

-	Layers:
	-	`sha256:6dda1c9ccabd43968c41a96d68ffa5d4e866caadac602f60485d0be2b85ce991`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f5c1ba2284296507eb9bd9ed9f407820c80912f37156ddd0bf69cb46f7990e`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8eca98d844737e7391af0ba3bd078c33c9b79484694a82e1a51f2a29ebfc0b`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 7.7 MB (7693190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d4cff2a33ca97c469fc8ab6c3284395941ba8b2cff8f4361b3ab4a1b366eb5`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:54 GMT  
		Size: 105.2 MB (105156763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c03434704503155ed2343afd552fb957cce1a8b2680b8b7d8344138e2a6597`  
		Last Modified: Tue, 13 Jan 2026 02:20:52 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d999d45b1b181000acaa083e513b632b05025450d49f6009d16400b8cf257624`  
		Last Modified: Tue, 13 Jan 2026 02:20:52 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc56c71044322b328f24d81b4873610894af8d49b91b8a31513590266fe49`  
		Last Modified: Tue, 13 Jan 2026 02:20:53 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cd1196c4cb96149708b21622838788a0cf61a569067e10485f4f12efecb2c4`  
		Last Modified: Tue, 13 Jan 2026 02:20:53 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50d4d6e4b72e86f1a95b7c50ce2ca2099a3a9a898205250f448399f4b707c08`  
		Last Modified: Tue, 13 Jan 2026 02:20:50 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; s390x

```console
$ docker pull couchdb@sha256:b89995d4cc477862a92b00132e63e9bdbeaa2e1275399b8c499b4ae8ff484283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96adb63f1df519a3512423ccc509050f50f1aa43b8377a35e9f8c4f876bd01fc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:45:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 03:45:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 03 Feb 2026 03:45:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 03:45:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 03:45:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:47 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 03 Feb 2026 03:45:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:46:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Feb 2026 03:46:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 03 Feb 2026 03:46:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02b13c2167da67366f3b654df0b591a74a3ceda0090898972764c16c230c05d`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106bb0fe71c6f312e2b1f959ca60f93081c3ee9281519aa63c3d43e8dd80a695`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 7.4 MB (7398885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e553654c359f6f0b8b1971a834e87804e73de794834a70588cf062e0dfa737be`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 372.1 KB (372135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4b0edbcef0c9ef2e30cbb6abc0dd368eb2da9cd9092867b563c0474dc73628`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 76.5 KB (76541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec92d49aef09eb0f577a0d64c82ee3a193ce554f913871aea28e0fbc0c547d7`  
		Last Modified: Tue, 03 Feb 2026 03:46:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc9b0eb3cf5654309cf322615685bbb1ea31e67782f9536ce65890c8fb83fb8`  
		Last Modified: Tue, 03 Feb 2026 03:46:28 GMT  
		Size: 104.0 MB (104028287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4810a95d166c559450d5305e9bc0afbd6f19fcfda85855677ff4e8bf7e68e6`  
		Last Modified: Tue, 03 Feb 2026 03:46:25 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c1119ba5c69ff7a21a171a1ac2426fa7672882940a8817641966dbc1e349f`  
		Last Modified: Tue, 03 Feb 2026 03:46:25 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e5f136944350478b46d365514b083f6088c42948cb115e4bdd7da7b0784b78`  
		Last Modified: Tue, 03 Feb 2026 03:46:26 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16af054f32548ea40fd3afa36f7d37e965983c035312f702653ec8f1cbc143d3`  
		Last Modified: Tue, 03 Feb 2026 03:46:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:423824caae2974643c0d72cdafd5f8a8b9894e8218c49e1f54f92b9c667d96a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f153ea1b594180284242ac7bb097fd386410f9a814283f2119059be22202fcf`

```dockerfile
```

-	Layers:
	-	`sha256:f340e5b4727b7d09238aef9c6694ab43abc848711d767fabbf3c5394102bd764`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0db4b1900a587958931c2cbf5f8e1ed873e849a9b6d08b3f2ade31ab9563bf`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1-nouveau`

```console
$ docker pull couchdb@sha256:5ccd971808f4b7eec5d5599174f15e68598259bfc2fa9283a5aba07b94e70388
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
$ docker pull couchdb@sha256:2b64016ceeedcbe65bec9fdf719a6f0520cfdeda292899f948b6f02ecd72aa1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156454720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0f8c67278d19a9a18cdec7e5a892300ef237a9fcb7816241ddfc8788de4735`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:44 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 02:43:44 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 03 Feb 2026 02:43:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 02:44:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 02:44:07 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:07 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 02:44:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 03 Feb 2026 02:44:13 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 03 Feb 2026 02:44:13 GMT
VOLUME [/opt/nouveau/data]
# Tue, 03 Feb 2026 02:44:13 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 03 Feb 2026 02:44:13 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2f1fc1251780f2123a88ec6b1625b1f161e25efd41504f70275dd8f31e9329`  
		Last Modified: Tue, 03 Feb 2026 02:44:29 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5b07b90d99f75c07ac2962182cea4a914e329742759219dfe660055213a6b0`  
		Last Modified: Tue, 03 Feb 2026 02:44:30 GMT  
		Size: 7.9 MB (7883128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83372eb1b6397a36f36e6013bece01cee7cedc014fe3c311f470925ff65780d2`  
		Last Modified: Tue, 03 Feb 2026 02:44:32 GMT  
		Size: 77.4 MB (77380918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a88a440b80b25b36f61a176bd75bbc21ca304a8472923e1fb782a959cdcd37`  
		Last Modified: Tue, 03 Feb 2026 02:44:29 GMT  
		Size: 424.2 KB (424191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc7794c0a906c77aa52409af359f9083b620d147ff60ced85f511e3c9efbf7b`  
		Last Modified: Tue, 03 Feb 2026 02:44:30 GMT  
		Size: 99.6 KB (99598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f1ccbf7f15bb9c4d67592591c93463832f045a5095f2390029a39828fe5b01`  
		Last Modified: Tue, 03 Feb 2026 02:44:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94db2487c03661363dca2d3abbff43337442842d60496b36cf89965c61b4b675`  
		Last Modified: Tue, 03 Feb 2026 02:44:32 GMT  
		Size: 42.4 MB (42436519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86df68ccc130acb38f0147f5f25e98e16307e733aafc12d8fe390c61eeeec70d`  
		Last Modified: Tue, 03 Feb 2026 02:44:32 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a2e8e6d0b224a88404c2c544ef4ec64038b9451cf97397e54bcc80ffe6a324fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e5b9b18ba252c2abc60b8ed958e735792e18d91541469a84c2ed7c00a35615`

```dockerfile
```

-	Layers:
	-	`sha256:326038181cc4d4767c5270a11f64e357cb051045d992d4f641600a02521311fa`  
		Last Modified: Tue, 03 Feb 2026 02:44:30 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84365dc8ddfed096f5d9a6f1a58b73cd21db638f5ff79daa6bb9be0048d37fd7`  
		Last Modified: Tue, 03 Feb 2026 02:44:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 7.7 MB (7693146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb5da74a812f294be30343ff89ed9604ba248e5e135425a3bb7906968f1e64`  
		Last Modified: Tue, 13 Jan 2026 02:21:23 GMT  
		Size: 76.7 MB (76691847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66868d5948d44e96078e5fa525df7e09c89d0e7cc0cb09f0fc48aeeb30707c4e`  
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 392.7 KB (392739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b4cd7f59188339c71711d75181a6f4fd7fab268e8ca419321d58f9759d5a1`  
		Last Modified: Tue, 13 Jan 2026 02:21:22 GMT  
		Size: 99.5 KB (99466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d1f922c928a80bb685cb6e00a39fd3e289a4a71153df9e0713dc6f8ca02ff`  
		Last Modified: Tue, 13 Jan 2026 02:21:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:21:21 GMT  
		Size: 24.7 KB (24702 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:22dc44a88a0371f80361ab6f85a5b7d39458b202c85522dc7ebc658ded7ae3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150097020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09c5eaf4739c8c3e5790287157dc7d86b0374248f3234dcc0a370df426bfb5a`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:45:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 03:45:47 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 03 Feb 2026 03:45:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 03:46:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 03:46:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 03:46:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 03 Feb 2026 03:46:16 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 03 Feb 2026 03:46:16 GMT
VOLUME [/opt/nouveau/data]
# Tue, 03 Feb 2026 03:46:16 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 03 Feb 2026 03:46:16 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb860f9d20bff7fff3a85718356f5a554630a0edef1b792a07e2f891c31e2e47`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0bfe0ea53c745bcc02b9c320ebc361f18862f770f2a63f769ff6c59bc52096`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 7.4 MB (7398867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df89cda60390f6a4bc70aa899d6a3ad5c95a3be0e9e4be9b6dfef46b249e25b`  
		Last Modified: Tue, 03 Feb 2026 03:46:39 GMT  
		Size: 73.2 MB (73153103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b698866ee0126f695019926dac18f75d2468d0db7629c0a629c305e05daaef1f`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 394.5 KB (394482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc97975a9bb1f45325c001458ab917b47dd350cbd5f3a01066d5e0360dcf257`  
		Last Modified: Tue, 03 Feb 2026 03:46:38 GMT  
		Size: 99.7 KB (99657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c10d1aa33dbbc68010a89d231eed3c5338967ea2aa309234c6729fbead0b0`  
		Last Modified: Tue, 03 Feb 2026 03:46:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357ec97a4a96a0cad87e65c19bae5cb4476e8a753023ce27074575c2f8e103b0`  
		Last Modified: Tue, 03 Feb 2026 03:46:40 GMT  
		Size: 42.2 MB (42164646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62682c9cfe85a9b667830d2cf0305ef7b2324664f19e6e84de8eb123d94b481d`  
		Last Modified: Tue, 03 Feb 2026 03:46:39 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:86dfe5c4619f7a3ff038b187699a59be7c657c4d7b11872406fac86e1f8ec333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb2292c9e53fad4174e4281b6cd5aec35a6c3ab33f6700814b6d62030254abf`

```dockerfile
```

-	Layers:
	-	`sha256:33c40b2d5f4d455f3d140993dc0be02e39beed228047c960ed3c21c55c8db8d9`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8a7bb80c2b3c2960a931b6888cee83ac2e0223bb152adb2f5f1cba40b708861`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:94d0d67147335d37df957f3ace915c06eccf4c1d58ad558d614aae31f42b3187
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
$ docker pull couchdb@sha256:b8bdc4d8197b9750ad9ef55b4451df82c2552a1e48d25cb8d27f86901b0f45cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142051769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33093ab0977f79e9ab863423ea5f4dbca301ef181fc2d582a00cc9c7f828f0b2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 02:43:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 03 Feb 2026 02:43:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 02:43:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 02:43:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:57 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 03 Feb 2026 02:43:57 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 02:44:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Feb 2026 02:44:09 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 03 Feb 2026 02:44:09 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:44:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:44:10 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Feb 2026 02:44:10 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 03 Feb 2026 02:44:10 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f95f560da8e3bdb596e84a890ee559e80ffcd0ffb2154713b84dd9160890245`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592f333a628d569980303d3af9357c11ca01d55d117a3196fcee0f788b6f5e64`  
		Last Modified: Tue, 03 Feb 2026 02:44:23 GMT  
		Size: 7.9 MB (7883160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46c85312097de70d8c3bb3d7ee5e3673c1731b6d313d4b6530de6f23ef9b703`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 401.8 KB (401799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ce674f9f9d416860b6ebffbf149ef1784a8da66ef19fd90f0abe6e5c8e8c09`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 76.5 KB (76541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd653d782a5746a5d49d07d4802d8aee9a39c177c89a61b9e02b8179ad5443d`  
		Last Modified: Tue, 03 Feb 2026 02:44:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd05477ed76b6361c96a6d5a6c5aa0b0e2b6be7d21f838cbf5fc17d0afe2b94`  
		Last Modified: Tue, 03 Feb 2026 02:44:27 GMT  
		Size: 105.5 MB (105456346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbe85d7425385b2507026901a39d017eb7273857ed496f22bec013c79fcdbb7`  
		Last Modified: Tue, 03 Feb 2026 02:44:24 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92911ab6e4d1ec2897e491318968d3ddced0573c5f8e4b798656729a21a3448`  
		Last Modified: Tue, 03 Feb 2026 02:44:24 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9634e08b060e5bb74c236c6c3796b6f1c7bd45c2ec7c0cd648b6f46ba77ae208`  
		Last Modified: Tue, 03 Feb 2026 02:44:25 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928bfbf0e88dd45b798f5b852dc8ab17fc67c4ba815089838ef07188049bde07`  
		Last Modified: Tue, 03 Feb 2026 02:44:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:28fea4b5eef08c55dc31fb28c5fa3ce0b4e9c97da4a66d34340a0c83f31e488d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e0218401bdf13e40ccb7e8c80392ff02a670f0efcaf8559d00dc8718dc5be7`

```dockerfile
```

-	Layers:
	-	`sha256:6dda1c9ccabd43968c41a96d68ffa5d4e866caadac602f60485d0be2b85ce991`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f5c1ba2284296507eb9bd9ed9f407820c80912f37156ddd0bf69cb46f7990e`  
		Last Modified: Tue, 03 Feb 2026 02:44:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8eca98d844737e7391af0ba3bd078c33c9b79484694a82e1a51f2a29ebfc0b`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 7.7 MB (7693190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d4cff2a33ca97c469fc8ab6c3284395941ba8b2cff8f4361b3ab4a1b366eb5`  
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:54 GMT  
		Size: 105.2 MB (105156763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c03434704503155ed2343afd552fb957cce1a8b2680b8b7d8344138e2a6597`  
		Last Modified: Tue, 13 Jan 2026 02:20:52 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d999d45b1b181000acaa083e513b632b05025450d49f6009d16400b8cf257624`  
		Last Modified: Tue, 13 Jan 2026 02:20:52 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc56c71044322b328f24d81b4873610894af8d49b91b8a31513590266fe49`  
		Last Modified: Tue, 13 Jan 2026 02:20:53 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cd1196c4cb96149708b21622838788a0cf61a569067e10485f4f12efecb2c4`  
		Last Modified: Tue, 13 Jan 2026 02:20:53 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:51 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50d4d6e4b72e86f1a95b7c50ce2ca2099a3a9a898205250f448399f4b707c08`  
		Last Modified: Tue, 13 Jan 2026 02:20:50 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:b89995d4cc477862a92b00132e63e9bdbeaa2e1275399b8c499b4ae8ff484283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138765663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96adb63f1df519a3512423ccc509050f50f1aa43b8377a35e9f8c4f876bd01fc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:45:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 03:45:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 03 Feb 2026 03:45:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 03:45:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 03:45:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:47 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 03 Feb 2026 03:45:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 03:46:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:46:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Feb 2026 03:46:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 03 Feb 2026 03:46:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02b13c2167da67366f3b654df0b591a74a3ceda0090898972764c16c230c05d`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106bb0fe71c6f312e2b1f959ca60f93081c3ee9281519aa63c3d43e8dd80a695`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 7.4 MB (7398885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e553654c359f6f0b8b1971a834e87804e73de794834a70588cf062e0dfa737be`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 372.1 KB (372135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4b0edbcef0c9ef2e30cbb6abc0dd368eb2da9cd9092867b563c0474dc73628`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 76.5 KB (76541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec92d49aef09eb0f577a0d64c82ee3a193ce554f913871aea28e0fbc0c547d7`  
		Last Modified: Tue, 03 Feb 2026 03:46:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc9b0eb3cf5654309cf322615685bbb1ea31e67782f9536ce65890c8fb83fb8`  
		Last Modified: Tue, 03 Feb 2026 03:46:28 GMT  
		Size: 104.0 MB (104028287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4810a95d166c559450d5305e9bc0afbd6f19fcfda85855677ff4e8bf7e68e6`  
		Last Modified: Tue, 03 Feb 2026 03:46:25 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c1119ba5c69ff7a21a171a1ac2426fa7672882940a8817641966dbc1e349f`  
		Last Modified: Tue, 03 Feb 2026 03:46:25 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e5f136944350478b46d365514b083f6088c42948cb115e4bdd7da7b0784b78`  
		Last Modified: Tue, 03 Feb 2026 03:46:26 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16af054f32548ea40fd3afa36f7d37e965983c035312f702653ec8f1cbc143d3`  
		Last Modified: Tue, 03 Feb 2026 03:46:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:423824caae2974643c0d72cdafd5f8a8b9894e8218c49e1f54f92b9c667d96a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f153ea1b594180284242ac7bb097fd386410f9a814283f2119059be22202fcf`

```dockerfile
```

-	Layers:
	-	`sha256:f340e5b4727b7d09238aef9c6694ab43abc848711d767fabbf3c5394102bd764`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0db4b1900a587958931c2cbf5f8e1ed873e849a9b6d08b3f2ade31ab9563bf`  
		Last Modified: Tue, 03 Feb 2026 03:46:24 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json
