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
-	[`couchdb:3.5.2`](#couchdb352)
-	[`couchdb:3.5.2-nouveau`](#couchdb352-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:9a84b943671e9587a690e0c4418e0bd89984b5045db84532add2e560e6b76127
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:6b8841ac81e6c9bb96886b5a5ef32cb6b94a1c95cca140afb12857149f25da70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148841671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7a82d4e15f8c7180838079160486fa79a7e62724b07975923372074eca8986`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:12:21 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:12:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 26 May 2026 19:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:12:31 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:12:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:37 GMT
ENV COUCHDB_VERSION=3.5.2
# Tue, 26 May 2026 19:12:37 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:12:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 26 May 2026 19:12:51 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 26 May 2026 19:12:51 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 26 May 2026 19:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 26 May 2026 19:12:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 26 May 2026 19:12:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:12:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 26 May 2026 19:12:51 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 26 May 2026 19:12:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad094000e370e01b9b0daa6c9c7d036ebb493677a3d834cc4dd37ca6ebc6433`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c41c50ddc17b9cb8a76c03fefdbb119878e96fc1b594843917da3d98e2369c`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 7.5 MB (7492175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde7e1f81bb73fc86574bc482826f379b59bce3f64ade593ea5deda639305113`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 417.6 KB (417592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae233ff04273726b94981e9d9496b6b32ca4a0154365cc8a9073945d8bfa14`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 338.6 KB (338589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7be48d8b355af1a2e6b7778b9c20e60a0d301cc4400f958db67b7995d3ceb0b`  
		Last Modified: Tue, 26 May 2026 19:13:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eaa84848643f9866a165135119d5a99dddaa33ac2e48702a613d918f3f8645`  
		Last Modified: Tue, 26 May 2026 19:13:08 GMT  
		Size: 110.8 MB (110807957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7425bf9721a6d60241f07146e898f8f3af4bab905b51ed31f45343e4443e98`  
		Last Modified: Tue, 26 May 2026 19:13:05 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ee2ba7b329f3620816b0e4f18c3c65580205c6a677c14c32bd18eb434a5c7b`  
		Last Modified: Tue, 26 May 2026 19:13:05 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00ed9b589a1f7c3fa1a54be71272252a8910960d018ab9a91d450394d2698e0`  
		Last Modified: Tue, 26 May 2026 19:13:06 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fe1cf8c2ac662e2a24e61bd2a1b38791c0c819c119de1bbb26f1eea89ad577`  
		Last Modified: Tue, 26 May 2026 19:13:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:1c41304f937925dc04b5634e04879a5f00960fc729b7adf90f9eee72e1d485ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31db4accb47515b040f715f98ead62fa20b2242d2e31103dd0bbbb375bd30002`

```dockerfile
```

-	Layers:
	-	`sha256:d53380103996b285e60c22f0619bf6a0454d7ba4db4b545589e5edff7d9b38d9`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 4.2 MB (4180083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a555635af560296c7a4de3e773c7fc48b702408f53bdec0d94124539cc93fbbc`  
		Last Modified: Tue, 26 May 2026 19:13:03 GMT  
		Size: 31.7 KB (31651 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b21bf95ca252a4f39adb63ac54beb08dfece635fb935f120f4e97af2d6755654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148608100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7728a6c9b6ccd474b41cb88a3b73a285022d3ec456689f5fe470cd5ed708c9e6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:15:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:15:25 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 26 May 2026 19:15:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:15:36 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:15:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:42 GMT
ENV COUCHDB_VERSION=3.5.2
# Tue, 26 May 2026 19:15:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:16:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 26 May 2026 19:16:00 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 26 May 2026 19:16:00 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 26 May 2026 19:16:00 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 26 May 2026 19:16:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 26 May 2026 19:16:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:16:00 GMT
VOLUME [/opt/couchdb/data]
# Tue, 26 May 2026 19:16:00 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 26 May 2026 19:16:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee81ff2242296c82709ee9022ec63a8fc58be49f0f1e18f9c59795a4161fc4a2`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad1beefd6a7da95ba934ccdb95d899e5bba2b377224f4bc0761e987c89986fb`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 7.3 MB (7261139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680f1018105ef13db426a95ff02c80c8eb8ea69a1cd9580162284b672d884a54`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 382.5 KB (382541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c7333c528bade7d773502c70c3b68869ded598f9a0a9eb67217e5ab914221e`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 338.7 KB (338692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc09b289ddedc4ea10f1e926124ab6ebd1738d021b2be451abc29136672f8b2b`  
		Last Modified: Tue, 26 May 2026 19:16:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd72831a514a1c868161f96df72438dcfbfbba5f2f7e51448d54a7c153457343`  
		Last Modified: Tue, 26 May 2026 19:16:18 GMT  
		Size: 110.5 MB (110478380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f46eb9f7b9f0ba04326f6e2f3357bde37624d606d35bdf5bde0c4b710eb0c16`  
		Last Modified: Tue, 26 May 2026 19:16:15 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad0c1c889813e2ebe1c372b1675a9f7ae650aa315e22ed82e392f81ee4ee0c6`  
		Last Modified: Tue, 26 May 2026 19:16:15 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f4cc3c59c4e6026dd23daefd1cb59e0eb63f19132e81a0faeb10eb0322c9bb`  
		Last Modified: Tue, 26 May 2026 19:16:17 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3666e26d26dd09323e6aba2ab4440738dff61d7cdd2d4410a2f0e62b8da72ee2`  
		Last Modified: Tue, 26 May 2026 19:16:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:8bff180137c0a38663dcbae6375d83a51777f58246ab4282ecc5b9e185e02241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e4db3c8990df7490fed7dcac5c7443ddca3c4144226007ce6e6ff3dea22b61`

```dockerfile
```

-	Layers:
	-	`sha256:6e83626ed08b8d9480a3581db27d36a51b72f694723487e6b8fd01c2c637fdaf`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 4.2 MB (4180379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31db02b19195bc885b67a6320a83e180ff9c5b74cfc73265bdc7bff58a8f841`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 31.8 KB (31845 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:5fea57e73aecc512b829b25e09deb2f8ae79b8e0d203bf8d3912ed57962ca2df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:b023387918d50d3845f8473ff48db48b4f1f2482924ad3ab2d63bb03ea9be41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150895583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4081591f6f0c7ba97c750131f877958e0833f16e21178d6d040c01069ffc46b1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:12:21 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:12:21 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 26 May 2026 19:12:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:12:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:12:45 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:45 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:12:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.2~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 26 May 2026 19:12:52 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 26 May 2026 19:12:52 GMT
VOLUME [/opt/nouveau/data]
# Tue, 26 May 2026 19:12:52 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 26 May 2026 19:12:52 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adfe4274313c392eaae20352b57638571532c448f9d84f803895a7be9d34d99`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b93c55a8a17efa21140a145fd562147dec16822626ea1fdbce157c87130b7d`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 7.5 MB (7492164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7c98c9da64692549be1b8d19d50b69c53473f24cb80d00d00bcc49d405703`  
		Last Modified: Tue, 26 May 2026 19:13:09 GMT  
		Size: 70.0 MB (70032507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d90032b71529deec699e234f8c1e5f230e15afb2af9ed78f7d0e0ec2ede3d`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 425.9 KB (425935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab98cb1d74db07915b7b1827c6a4bcf710244c844f86dfee323d670dac30646`  
		Last Modified: Tue, 26 May 2026 19:13:09 GMT  
		Size: 347.4 KB (347400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eded855bf9a27128e7cb32a1b5de87627789da0af98fe332221078cd232ee5c9`  
		Last Modified: Tue, 26 May 2026 19:13:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02921ca98efc95457685f61ec045d65e8ef5b0eb0583da320bf69b66d014a5fc`  
		Last Modified: Tue, 26 May 2026 19:13:10 GMT  
		Size: 42.8 MB (42815773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b11220b94c0da697b7694ad7215de07096e324d44080c7e14fe60d4cf4585eb`  
		Last Modified: Tue, 26 May 2026 19:13:09 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:8c778f5178140ba5d74207021493415318525e05d16193d1470c9706b9bde32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbd0f745d242a85ff69cd85d8e7cce3a421ff50bc4b7250f239a016b52b848c`

```dockerfile
```

-	Layers:
	-	`sha256:2b0e20389789aa223ce1281ba70d7e10d48fd4ab0bd37ae05eed938b3c59b532`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 3.4 MB (3364329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c68180b30148fc0ed0bd328a02bc8f8f40105dbe4f49492c10cc96cc819dd1f`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 24.4 KB (24430 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0f9f531bfa4789601ee3332831064ce0c36a3d310050b09642101b9d8dfd74d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150054078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866b12f85c6e83d60ad30361eac4681bbd18835ed93592503375780e9dc98a32`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:15:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:15:28 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 26 May 2026 19:15:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:15:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:15:50 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:50 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:15:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.2~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 26 May 2026 19:15:56 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 26 May 2026 19:15:56 GMT
VOLUME [/opt/nouveau/data]
# Tue, 26 May 2026 19:15:56 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 26 May 2026 19:15:56 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94b8c22a9aee84828061db0dd7d76c57cb2a7fd8e9323aaee931c95a0f6dc6c`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899235a1ecdb426e0b3da18b61f42992f10ee1fd1a10b2c541fd669297f2d5b2`  
		Last Modified: Tue, 26 May 2026 19:16:11 GMT  
		Size: 7.3 MB (7261186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bc6b67f11a43dcedc8cf7dc50c2154ff2c60d4d0c774fb49fbf2f46566bc9e`  
		Last Modified: Tue, 26 May 2026 19:16:13 GMT  
		Size: 69.2 MB (69179669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7429788cc833857a325c900b7a0c2016a5b5de0f2f72fe9aba140e4ba160aafe`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 390.2 KB (390234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873aa82ca7ed235720ae188282afa5273741e99dbdf33261c1a6fc59f6779db`  
		Last Modified: Tue, 26 May 2026 19:16:12 GMT  
		Size: 347.4 KB (347355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca6365ca4a609038d3e36cdce14dd01e8185aea71b1a223c88451270a4bc9f5`  
		Last Modified: Tue, 26 May 2026 19:16:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f241c015171f7d7834492271e36620bb63c15966b4ff3d9a3d8a8a1ec6a848ed`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 42.7 MB (42731840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c4929e8c4527ada0d772f38f8d68322cf21814750e8122e1806ae9b04928dc`  
		Last Modified: Tue, 26 May 2026 19:16:13 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dcd22f542736aefd4d2a30a7548d8ffb85effc726edb9436fb5c4411e52b3a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3387582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380190f460d059d992367b535aa7953a4933d47e782c86303c532a8b7b15431b`

```dockerfile
```

-	Layers:
	-	`sha256:2d5490b97830a7a6171783bf1e51b72cc215ba1c2ff0827e6d39f519ac60f47b`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 3.4 MB (3362970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d46173a258ed8d68f45424b620960e6ad3380b9d4e7632b7c2489b8fe44c102`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 24.6 KB (24612 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:9cce5bc04939873f599c1ea6dc1cd4c7f167c211d66f3b75c4194bea1ed414c4
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
$ docker pull couchdb@sha256:da9dfd0b56b3f19f977bdf49b88bcbaac99cab1b137c0a1e6f0eacdc16dac825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139021530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5389ab5904456ba37bc7dcc4b60ce55420ccb79bf6f58486ccc5ed64c9e314`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:23:39 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 19 May 2026 23:23:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:23:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:23:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:53 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 19 May 2026 23:23:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:24:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 19 May 2026 23:24:07 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 19 May 2026 23:24:07 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 19 May 2026 23:24:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 19 May 2026 23:24:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 19 May 2026 23:24:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:24:07 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 May 2026 23:24:07 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 19 May 2026 23:24:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1262100da0332167345f1c3f8a8958fa9a26874c27a4b57b6a3a30856037301f`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ada3b1dc40cc15c77f2669616d8c01ea1138da9b81fc178bee72aa0538bfb6`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 7.9 MB (7884230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2414144aa61f08516e81e5fdfd052c4e4f0e1502d90dcdd8abf0e2b6b68995`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 401.8 KB (401770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135f72b7003198b2a94e736b698889c65472538ee43218073f30592400c94c72`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 76.5 KB (76515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76c826d6272c2e2b12dfddef78fc3d67096b627464b457e4957432ef8f88869`  
		Last Modified: Tue, 19 May 2026 23:24:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beba1e49e0306ddfebc9e1b048d9b1c11b6bab6e93342992c8537ac36719ae10`  
		Last Modified: Tue, 19 May 2026 23:24:25 GMT  
		Size: 102.4 MB (102420035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c21ae961cc871d4dbdec90d331edc5a0fd7dd76672dc41e03624ccff1ada048`  
		Last Modified: Tue, 19 May 2026 23:24:22 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4dd5d9fafaf05c89374d93f2212ce0cdecefe313d8ea9ef5d3d7bbd9fd504c`  
		Last Modified: Tue, 19 May 2026 23:24:23 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7984aba3dbbb4eb6e29d581bca0bdb234a8edf69a094debd1eb55ca739e7d1`  
		Last Modified: Tue, 19 May 2026 23:24:23 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d41909fdbd5f49d26bcf56adceadb68df102431f4fa1faec539e888ac0b114f`  
		Last Modified: Tue, 19 May 2026 23:24:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:f0fc03dfaf8bda1f4f036a5310dfd064549350dde25f5b90ad11683ff086b5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d698b479d5e1e28523c60764e45db15661ce65609fd3e136c5f1118337f8aa0`

```dockerfile
```

-	Layers:
	-	`sha256:fb84baa222cf5738f1fc4eda1aa42743c3d324f36d9378cf4dc5c642c599bc26`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 4.1 MB (4125413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c589b3463b8e04d89e1627ed9442cca79f5d301117a77e8e425cff7eb8d826`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4ba0bdf097abd17ae046318d9c76996bf3e4ab2cfe23035b1145ee20844bc3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138432129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7640d7a1a9851a160111f910f34fcdb4731c03d9288ba1f7bd3da327e8a01a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:27:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 19 May 2026 23:27:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:27:21 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:27:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:27 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 19 May 2026 23:27:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:27:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 19 May 2026 23:27:39 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 19 May 2026 23:27:39 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 19 May 2026 23:27:39 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 19 May 2026 23:27:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 19 May 2026 23:27:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:27:39 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 May 2026 23:27:39 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 19 May 2026 23:27:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e24e8c7fa768cc75e150b10e330b1a3a0dae912a24792f5390bb8e784d276e`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9be4175f9e60c07473387372d8b1cc1d73a9ca8371b0f9e862c969768332df`  
		Last Modified: Tue, 19 May 2026 23:27:53 GMT  
		Size: 7.7 MB (7695136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60895f958d75b236cbd3de1a7743caa9e7e5541440dc66e3570b8aee43b8460d`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 370.5 KB (370518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b727c0acdbaf659ee8d9719167b91704919f9b7261443de1634fb4134c896691`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 76.5 KB (76494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7b37b356bbcf3e6ec862220aafb20c2d2cdf6f4271416dda5aa35b50063742`  
		Last Modified: Tue, 19 May 2026 23:27:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84790b386021daac75f5318352d72adb33c403620ccb6ef75a4145752d31ded`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 102.2 MB (102169501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561a494cfc5b960fa1f0d22909ab94a0eb86faaccb0ffb511df42dbd2e6acbd6`  
		Last Modified: Tue, 19 May 2026 23:27:54 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc2e727f7d8d0ac6b84d7f32fd4a674ec3ec855702794c727fa4c5a31f7d277`  
		Last Modified: Tue, 19 May 2026 23:27:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffef35d93e31e4c7a411a7f382d68fdc09c0dce5e39d3e1b51baf52032914350`  
		Last Modified: Tue, 19 May 2026 23:27:55 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03290f47b7e4fdfd4a628ec8ce171c4c15aa514f56a489351cd2d819b019209a`  
		Last Modified: Tue, 19 May 2026 23:27:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:349654ff9e5346cee26e33294616538047ecda436e09a34b45efd236fee9060d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7f538c545a1031ff02a6c87b5dd80dcf3110b8b99893f4a26fdb170d14bbe2`

```dockerfile
```

-	Layers:
	-	`sha256:e755df63d492cacf092f8cf8bca007aff36d9d3f56e410d75beb5e35c8a3d408`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 4.1 MB (4125682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:babc27fcaf933d28f19d1aa7a1d216f997fb332cc79b527263d664b4f945e1e9`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:e781ab57f107167881e4db431f78e4f064e945de629ea29bf316660ba74c2960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135799283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062e4f15317b3254d5e2464e22455b60685314becd06ed6aec4158195e33b9ef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:19:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 May 2026 00:19:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 20 May 2026 00:19:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 20 May 2026 00:19:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 May 2026 00:19:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:27 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 20 May 2026 00:20:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 20 May 2026 00:20:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 20 May 2026 00:20:42 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 20 May 2026 00:20:42 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 20 May 2026 00:20:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 00:20:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 20 May 2026 00:20:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 May 2026 00:20:42 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 May 2026 00:20:42 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 20 May 2026 00:20:42 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2119d20228b0ee7dc34f2d8ae50ddc482133d4a46b75ef39cee53837e06a0b`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a006620367a25e0aa2b2d85669f3382121b884eac2d944403ea899a9f28bc3a`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 7.4 MB (7400088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a087ffd583427a623a7fbb6d5cd92146fa7fe562b3691275df4895f13a96e4`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 372.2 KB (372152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d614b0a4ac50680b2c89e16a8817e441882e4f8a74c0efa6a724b927bfe5d32c`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 76.5 KB (76539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89faf5f17de2b2b482ddd66c4d475c7b419239d8742d05dbd95eaaa6d8b6ebe`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf982cfac72c8ce5675c24908face2e97a41c66c513fa73a7f98f32887929e0`  
		Last Modified: Wed, 20 May 2026 00:21:04 GMT  
		Size: 101.1 MB (101056473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737006e8dd12dc6a7920d4dbba81a2adcf894b9cfd9f08ab2d3d145a8cd45709`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e2d485598b4cebfc1a39eebe635307861eaa609fb69ff124c4f154eda4967c`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa737a67a9719364a9f105ceed1a7ec93c62cab245ba118dd0e4a833951aaee`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bfdb266525bb6bb7c2ae862c3481a27a3daffcf35d31fdc308a35b0ca885e3`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:d021b449200ed580cbbbe31a87fbc1819de9e7184a28bce4de7c1a2320239f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aca100fbcff26d70e9c7b924c2c1e92801717ad8da1b502e4ef4426921c585a`

```dockerfile
```

-	Layers:
	-	`sha256:4ba18fc91a85113f0265a18ad5ef30da02285ac1407b69d4061a53071b7a8dc0`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 4.1 MB (4121609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70d0601c2dade617704cfd0f266a23794d0e8fb0d1aa9449d1b9417f1c595b8f`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:b65a46e8e77e3ceb3cc7422e50ba4a8cf13b1edb45865d9b9bd4f9afeead8498
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
$ docker pull couchdb@sha256:1b28577b7e1406b3097460f849c00ea0ad9e3d222e6f2468773509f43cb8a2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156557052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f559137e9771bc303aa4ca977cbb1c8aab911b77e4d2b6e86c44e18fdcbd79`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:23:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 19 May 2026 23:23:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:23:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:23:57 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:58 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:24:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 19 May 2026 23:24:02 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 19 May 2026 23:24:02 GMT
VOLUME [/opt/nouveau/data]
# Tue, 19 May 2026 23:24:02 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 19 May 2026 23:24:02 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034254b8e01952c9c67ffb0d8201fea6ebaf4775ea8cd7ac91b509de3f1ed3cc`  
		Last Modified: Tue, 19 May 2026 23:24:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ab98cf14d02a29c4aa86f540fe6c9889bd595c7a5db98d9d74981914478c16`  
		Last Modified: Tue, 19 May 2026 23:24:19 GMT  
		Size: 7.9 MB (7884170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df177a882181db0ec0c60e4aaf9fd94a18c1e34280e5e15946ed2cd69c4904b0`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 77.5 MB (77477910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2fcee25a09246222319e9d38fef98b79c45d8595a47e3e3d9e462078276f09`  
		Last Modified: Tue, 19 May 2026 23:24:18 GMT  
		Size: 424.1 KB (424149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3576391464b6e7080306d56d23930c9ea9ba29bd0f95e3be148fe155b12a1de7`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 99.6 KB (99563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babd490be78878864bc284dcf28a23e501af9f9260196bb80f61429b8d461e1e`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59817ab8b38f3c70e51a30216d2038aa6eba6ff190c71bdce4d7fcfb976ebd08`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 42.4 MB (42435835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aee7e3b66f991598df233f16dd0b28b833e965fbdb7e02a4370c18806a70b7`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:626d48c311ffef0cf077ed4d2e06c70f4bb5dda0863d6623f6b580dae5330064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc25db8e2d359542585ef547dd522d304d4bddf3581e9bd5e43eec9c2255092`

```dockerfile
```

-	Layers:
	-	`sha256:bdac17e5c586326819a4977371c126aca1b183b1a4e823a9bfafd8ee4559a90b`  
		Last Modified: Tue, 19 May 2026 23:24:19 GMT  
		Size: 3.7 MB (3658653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3454d1187cebbe56eb5cef5de8e167ba87117fa0d0547c1d40e8e9152059bf96`  
		Last Modified: Tue, 19 May 2026 23:24:18 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:cefdb1385ab4a451d2aea210ccc3ea8760acaa52067780e3a4836be3e39da549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155435730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36ceedfbd6190ca9b093c68d82626c05d620f7a694f0efc30c37d909654e6cd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:27:19 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 19 May 2026 23:27:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:27:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:27:38 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:38 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:27:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 19 May 2026 23:27:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 19 May 2026 23:27:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 19 May 2026 23:27:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 19 May 2026 23:27:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b431e0800be10532b8cdccd281d397a606f541a408e919fe06261c077301a006`  
		Last Modified: Tue, 19 May 2026 23:27:57 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42477eae5cec1dedc000ef75f969c8a87f8769385122615b007e689d818716dc`  
		Last Modified: Tue, 19 May 2026 23:27:58 GMT  
		Size: 7.7 MB (7695083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a0fe90886376d1d4d332acfec00cd36ca36b57e90eaf4785f5aafbc63ae938`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 76.8 MB (76793468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c465194c14ac1c736796410733d7a5dd83b39c68678383ed896651efea8df5d5`  
		Last Modified: Tue, 19 May 2026 23:27:58 GMT  
		Size: 392.8 KB (392782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d9b7f356e47858f4d282ed5f6d14748a682626af2ec2c978da028b1f07d89f`  
		Last Modified: Tue, 19 May 2026 23:27:59 GMT  
		Size: 99.5 KB (99507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7288fcfdfcbdabf602e1d2b92be07ebd2731eb28a2c85ef2449a25f9ff79b92`  
		Last Modified: Tue, 19 May 2026 23:27:59 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eb77540f225caf0dfd731cd23c6d99c4eacab7fcc32501206406f3f058a84e`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 42.3 MB (42337966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c05e22b278e6181c2299b996a4312ce0d6f6f193cc6d490ad06bacf56bddb4e`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b291a7b3423e66d516c470f2bd971e08d78f6da85685811ec75a2e44afeb9b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aacc0519a174443d14e7e47f321ddc3d964ee5c2a44354f8776f70174215d93`

```dockerfile
```

-	Layers:
	-	`sha256:1f9e0d0e366e8d52579f2d7bbea0d58216660c96b6ed8aef682d7e2dd8dd6635`  
		Last Modified: Tue, 19 May 2026 23:27:58 GMT  
		Size: 3.7 MB (3657321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2e306c7e7342dc8957898406f6555b25411a7f849b9aa21a7fd768e2f9b3c5c`  
		Last Modified: Tue, 19 May 2026 23:27:57 GMT  
		Size: 24.4 KB (24384 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:4dc2a0634528573ef1a7cf7f418b30902b021c6f36a8f97ab045b809a25cdbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150172945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bbd6c813f57e84313da6c907f21e34ca378e73a80a6881e14f03e124f96546`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:19:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 May 2026 00:19:26 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 20 May 2026 00:19:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 20 May 2026 00:19:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 May 2026 00:19:50 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:50 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 20 May 2026 00:20:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 20 May 2026 00:20:48 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 20 May 2026 00:20:48 GMT
VOLUME [/opt/nouveau/data]
# Wed, 20 May 2026 00:20:48 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 20 May 2026 00:20:48 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735715cce2082c3ee3f9a3e1340e641fd3c8a4c27a986dfa1e0711d23ab1bfd3`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d408f2f91f087b84b8fc0b5eaab3a385e9c71c6d1aea5cdd41add6b52a42875`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 7.4 MB (7400058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9862fef3db5700ef619b2c3c7787c171007e7038deabe8151310df8531e354c4`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 73.2 MB (73225383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa09fc31e5567156b4208ae4d6e44d3f8c7fcc9372b1f65223c892703e7b785`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 394.5 KB (394501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eb29090836c1a783acc896684e8094b507792c57f4e34f997b56fbbe53038e`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 99.7 KB (99671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6bf9c655d2ba99361dd631c89376c408f4241337194d618f695647f46b1893`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70b8ea5924d1d6ddeed842229d696c5d7339bd591d0a4e18332a1f853a14128`  
		Last Modified: Wed, 20 May 2026 00:21:04 GMT  
		Size: 42.2 MB (42162858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa511f6c6cad159de580bb827928f4c832dd41ea35ceadcdaa771c67a8626b38`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:ab6d822426e364949911ae45953e5655df9dd41fd3fe427a2c6ffcadb3c58b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e185b56f0a0f457d0e0345bf17a86dd144c6c0429136757651eaf6c322a5b998`

```dockerfile
```

-	Layers:
	-	`sha256:f350fdb2b2edbfa085859a68071502e2d0eda2f585d913dea3203739704f57fe`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 3.6 MB (3649186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16c57fb6fb6ffd2ff26271b6130b1d5df9c6e6c7cdf5779f88c271f91018c041`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:9cce5bc04939873f599c1ea6dc1cd4c7f167c211d66f3b75c4194bea1ed414c4
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
$ docker pull couchdb@sha256:da9dfd0b56b3f19f977bdf49b88bcbaac99cab1b137c0a1e6f0eacdc16dac825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139021530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5389ab5904456ba37bc7dcc4b60ce55420ccb79bf6f58486ccc5ed64c9e314`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:23:39 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 19 May 2026 23:23:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:23:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:23:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:53 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 19 May 2026 23:23:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:24:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 19 May 2026 23:24:07 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 19 May 2026 23:24:07 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 19 May 2026 23:24:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 19 May 2026 23:24:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 19 May 2026 23:24:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:24:07 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 May 2026 23:24:07 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 19 May 2026 23:24:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1262100da0332167345f1c3f8a8958fa9a26874c27a4b57b6a3a30856037301f`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ada3b1dc40cc15c77f2669616d8c01ea1138da9b81fc178bee72aa0538bfb6`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 7.9 MB (7884230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2414144aa61f08516e81e5fdfd052c4e4f0e1502d90dcdd8abf0e2b6b68995`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 401.8 KB (401770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135f72b7003198b2a94e736b698889c65472538ee43218073f30592400c94c72`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 76.5 KB (76515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76c826d6272c2e2b12dfddef78fc3d67096b627464b457e4957432ef8f88869`  
		Last Modified: Tue, 19 May 2026 23:24:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beba1e49e0306ddfebc9e1b048d9b1c11b6bab6e93342992c8537ac36719ae10`  
		Last Modified: Tue, 19 May 2026 23:24:25 GMT  
		Size: 102.4 MB (102420035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c21ae961cc871d4dbdec90d331edc5a0fd7dd76672dc41e03624ccff1ada048`  
		Last Modified: Tue, 19 May 2026 23:24:22 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4dd5d9fafaf05c89374d93f2212ce0cdecefe313d8ea9ef5d3d7bbd9fd504c`  
		Last Modified: Tue, 19 May 2026 23:24:23 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7984aba3dbbb4eb6e29d581bca0bdb234a8edf69a094debd1eb55ca739e7d1`  
		Last Modified: Tue, 19 May 2026 23:24:23 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d41909fdbd5f49d26bcf56adceadb68df102431f4fa1faec539e888ac0b114f`  
		Last Modified: Tue, 19 May 2026 23:24:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f0fc03dfaf8bda1f4f036a5310dfd064549350dde25f5b90ad11683ff086b5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d698b479d5e1e28523c60764e45db15661ce65609fd3e136c5f1118337f8aa0`

```dockerfile
```

-	Layers:
	-	`sha256:fb84baa222cf5738f1fc4eda1aa42743c3d324f36d9378cf4dc5c642c599bc26`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 4.1 MB (4125413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c589b3463b8e04d89e1627ed9442cca79f5d301117a77e8e425cff7eb8d826`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4ba0bdf097abd17ae046318d9c76996bf3e4ab2cfe23035b1145ee20844bc3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138432129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7640d7a1a9851a160111f910f34fcdb4731c03d9288ba1f7bd3da327e8a01a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:27:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 19 May 2026 23:27:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:27:21 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:27:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:27 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 19 May 2026 23:27:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:27:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 19 May 2026 23:27:39 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 19 May 2026 23:27:39 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 19 May 2026 23:27:39 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 19 May 2026 23:27:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 19 May 2026 23:27:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:27:39 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 May 2026 23:27:39 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 19 May 2026 23:27:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e24e8c7fa768cc75e150b10e330b1a3a0dae912a24792f5390bb8e784d276e`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9be4175f9e60c07473387372d8b1cc1d73a9ca8371b0f9e862c969768332df`  
		Last Modified: Tue, 19 May 2026 23:27:53 GMT  
		Size: 7.7 MB (7695136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60895f958d75b236cbd3de1a7743caa9e7e5541440dc66e3570b8aee43b8460d`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 370.5 KB (370518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b727c0acdbaf659ee8d9719167b91704919f9b7261443de1634fb4134c896691`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 76.5 KB (76494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7b37b356bbcf3e6ec862220aafb20c2d2cdf6f4271416dda5aa35b50063742`  
		Last Modified: Tue, 19 May 2026 23:27:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84790b386021daac75f5318352d72adb33c403620ccb6ef75a4145752d31ded`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 102.2 MB (102169501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561a494cfc5b960fa1f0d22909ab94a0eb86faaccb0ffb511df42dbd2e6acbd6`  
		Last Modified: Tue, 19 May 2026 23:27:54 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc2e727f7d8d0ac6b84d7f32fd4a674ec3ec855702794c727fa4c5a31f7d277`  
		Last Modified: Tue, 19 May 2026 23:27:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffef35d93e31e4c7a411a7f382d68fdc09c0dce5e39d3e1b51baf52032914350`  
		Last Modified: Tue, 19 May 2026 23:27:55 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03290f47b7e4fdfd4a628ec8ce171c4c15aa514f56a489351cd2d819b019209a`  
		Last Modified: Tue, 19 May 2026 23:27:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:349654ff9e5346cee26e33294616538047ecda436e09a34b45efd236fee9060d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7f538c545a1031ff02a6c87b5dd80dcf3110b8b99893f4a26fdb170d14bbe2`

```dockerfile
```

-	Layers:
	-	`sha256:e755df63d492cacf092f8cf8bca007aff36d9d3f56e410d75beb5e35c8a3d408`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 4.1 MB (4125682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:babc27fcaf933d28f19d1aa7a1d216f997fb332cc79b527263d664b4f945e1e9`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:e781ab57f107167881e4db431f78e4f064e945de629ea29bf316660ba74c2960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135799283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062e4f15317b3254d5e2464e22455b60685314becd06ed6aec4158195e33b9ef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:19:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 May 2026 00:19:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 20 May 2026 00:19:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 20 May 2026 00:19:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 May 2026 00:19:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:27 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 20 May 2026 00:20:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 20 May 2026 00:20:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 20 May 2026 00:20:42 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 20 May 2026 00:20:42 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 20 May 2026 00:20:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 00:20:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 20 May 2026 00:20:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 May 2026 00:20:42 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 May 2026 00:20:42 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 20 May 2026 00:20:42 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2119d20228b0ee7dc34f2d8ae50ddc482133d4a46b75ef39cee53837e06a0b`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a006620367a25e0aa2b2d85669f3382121b884eac2d944403ea899a9f28bc3a`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 7.4 MB (7400088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a087ffd583427a623a7fbb6d5cd92146fa7fe562b3691275df4895f13a96e4`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 372.2 KB (372152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d614b0a4ac50680b2c89e16a8817e441882e4f8a74c0efa6a724b927bfe5d32c`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 76.5 KB (76539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89faf5f17de2b2b482ddd66c4d475c7b419239d8742d05dbd95eaaa6d8b6ebe`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf982cfac72c8ce5675c24908face2e97a41c66c513fa73a7f98f32887929e0`  
		Last Modified: Wed, 20 May 2026 00:21:04 GMT  
		Size: 101.1 MB (101056473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737006e8dd12dc6a7920d4dbba81a2adcf894b9cfd9f08ab2d3d145a8cd45709`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e2d485598b4cebfc1a39eebe635307861eaa609fb69ff124c4f154eda4967c`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa737a67a9719364a9f105ceed1a7ec93c62cab245ba118dd0e4a833951aaee`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bfdb266525bb6bb7c2ae862c3481a27a3daffcf35d31fdc308a35b0ca885e3`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d021b449200ed580cbbbe31a87fbc1819de9e7184a28bce4de7c1a2320239f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aca100fbcff26d70e9c7b924c2c1e92801717ad8da1b502e4ef4426921c585a`

```dockerfile
```

-	Layers:
	-	`sha256:4ba18fc91a85113f0265a18ad5ef30da02285ac1407b69d4061a53071b7a8dc0`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 4.1 MB (4121609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70d0601c2dade617704cfd0f266a23794d0e8fb0d1aa9449d1b9417f1c595b8f`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:b65a46e8e77e3ceb3cc7422e50ba4a8cf13b1edb45865d9b9bd4f9afeead8498
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
$ docker pull couchdb@sha256:1b28577b7e1406b3097460f849c00ea0ad9e3d222e6f2468773509f43cb8a2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156557052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f559137e9771bc303aa4ca977cbb1c8aab911b77e4d2b6e86c44e18fdcbd79`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:23:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 19 May 2026 23:23:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:23:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:23:57 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:58 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:24:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 19 May 2026 23:24:02 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 19 May 2026 23:24:02 GMT
VOLUME [/opt/nouveau/data]
# Tue, 19 May 2026 23:24:02 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 19 May 2026 23:24:02 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034254b8e01952c9c67ffb0d8201fea6ebaf4775ea8cd7ac91b509de3f1ed3cc`  
		Last Modified: Tue, 19 May 2026 23:24:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ab98cf14d02a29c4aa86f540fe6c9889bd595c7a5db98d9d74981914478c16`  
		Last Modified: Tue, 19 May 2026 23:24:19 GMT  
		Size: 7.9 MB (7884170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df177a882181db0ec0c60e4aaf9fd94a18c1e34280e5e15946ed2cd69c4904b0`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 77.5 MB (77477910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2fcee25a09246222319e9d38fef98b79c45d8595a47e3e3d9e462078276f09`  
		Last Modified: Tue, 19 May 2026 23:24:18 GMT  
		Size: 424.1 KB (424149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3576391464b6e7080306d56d23930c9ea9ba29bd0f95e3be148fe155b12a1de7`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 99.6 KB (99563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babd490be78878864bc284dcf28a23e501af9f9260196bb80f61429b8d461e1e`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59817ab8b38f3c70e51a30216d2038aa6eba6ff190c71bdce4d7fcfb976ebd08`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 42.4 MB (42435835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aee7e3b66f991598df233f16dd0b28b833e965fbdb7e02a4370c18806a70b7`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:626d48c311ffef0cf077ed4d2e06c70f4bb5dda0863d6623f6b580dae5330064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc25db8e2d359542585ef547dd522d304d4bddf3581e9bd5e43eec9c2255092`

```dockerfile
```

-	Layers:
	-	`sha256:bdac17e5c586326819a4977371c126aca1b183b1a4e823a9bfafd8ee4559a90b`  
		Last Modified: Tue, 19 May 2026 23:24:19 GMT  
		Size: 3.7 MB (3658653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3454d1187cebbe56eb5cef5de8e167ba87117fa0d0547c1d40e8e9152059bf96`  
		Last Modified: Tue, 19 May 2026 23:24:18 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:cefdb1385ab4a451d2aea210ccc3ea8760acaa52067780e3a4836be3e39da549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155435730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36ceedfbd6190ca9b093c68d82626c05d620f7a694f0efc30c37d909654e6cd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:27:19 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 19 May 2026 23:27:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:27:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:27:38 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:38 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:27:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 19 May 2026 23:27:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 19 May 2026 23:27:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 19 May 2026 23:27:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 19 May 2026 23:27:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b431e0800be10532b8cdccd281d397a606f541a408e919fe06261c077301a006`  
		Last Modified: Tue, 19 May 2026 23:27:57 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42477eae5cec1dedc000ef75f969c8a87f8769385122615b007e689d818716dc`  
		Last Modified: Tue, 19 May 2026 23:27:58 GMT  
		Size: 7.7 MB (7695083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a0fe90886376d1d4d332acfec00cd36ca36b57e90eaf4785f5aafbc63ae938`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 76.8 MB (76793468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c465194c14ac1c736796410733d7a5dd83b39c68678383ed896651efea8df5d5`  
		Last Modified: Tue, 19 May 2026 23:27:58 GMT  
		Size: 392.8 KB (392782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d9b7f356e47858f4d282ed5f6d14748a682626af2ec2c978da028b1f07d89f`  
		Last Modified: Tue, 19 May 2026 23:27:59 GMT  
		Size: 99.5 KB (99507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7288fcfdfcbdabf602e1d2b92be07ebd2731eb28a2c85ef2449a25f9ff79b92`  
		Last Modified: Tue, 19 May 2026 23:27:59 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eb77540f225caf0dfd731cd23c6d99c4eacab7fcc32501206406f3f058a84e`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 42.3 MB (42337966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c05e22b278e6181c2299b996a4312ce0d6f6f193cc6d490ad06bacf56bddb4e`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b291a7b3423e66d516c470f2bd971e08d78f6da85685811ec75a2e44afeb9b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aacc0519a174443d14e7e47f321ddc3d964ee5c2a44354f8776f70174215d93`

```dockerfile
```

-	Layers:
	-	`sha256:1f9e0d0e366e8d52579f2d7bbea0d58216660c96b6ed8aef682d7e2dd8dd6635`  
		Last Modified: Tue, 19 May 2026 23:27:58 GMT  
		Size: 3.7 MB (3657321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2e306c7e7342dc8957898406f6555b25411a7f849b9aa21a7fd768e2f9b3c5c`  
		Last Modified: Tue, 19 May 2026 23:27:57 GMT  
		Size: 24.4 KB (24384 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:4dc2a0634528573ef1a7cf7f418b30902b021c6f36a8f97ab045b809a25cdbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150172945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bbd6c813f57e84313da6c907f21e34ca378e73a80a6881e14f03e124f96546`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:19:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 May 2026 00:19:26 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 20 May 2026 00:19:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 20 May 2026 00:19:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 May 2026 00:19:50 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:50 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 20 May 2026 00:20:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 20 May 2026 00:20:48 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 20 May 2026 00:20:48 GMT
VOLUME [/opt/nouveau/data]
# Wed, 20 May 2026 00:20:48 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 20 May 2026 00:20:48 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735715cce2082c3ee3f9a3e1340e641fd3c8a4c27a986dfa1e0711d23ab1bfd3`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d408f2f91f087b84b8fc0b5eaab3a385e9c71c6d1aea5cdd41add6b52a42875`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 7.4 MB (7400058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9862fef3db5700ef619b2c3c7787c171007e7038deabe8151310df8531e354c4`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 73.2 MB (73225383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa09fc31e5567156b4208ae4d6e44d3f8c7fcc9372b1f65223c892703e7b785`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 394.5 KB (394501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eb29090836c1a783acc896684e8094b507792c57f4e34f997b56fbbe53038e`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 99.7 KB (99671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6bf9c655d2ba99361dd631c89376c408f4241337194d618f695647f46b1893`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70b8ea5924d1d6ddeed842229d696c5d7339bd591d0a4e18332a1f853a14128`  
		Last Modified: Wed, 20 May 2026 00:21:04 GMT  
		Size: 42.2 MB (42162858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa511f6c6cad159de580bb827928f4c832dd41ea35ceadcdaa771c67a8626b38`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:ab6d822426e364949911ae45953e5655df9dd41fd3fe427a2c6ffcadb3c58b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e185b56f0a0f457d0e0345bf17a86dd144c6c0429136757651eaf6c322a5b998`

```dockerfile
```

-	Layers:
	-	`sha256:f350fdb2b2edbfa085859a68071502e2d0eda2f585d913dea3203739704f57fe`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 3.6 MB (3649186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16c57fb6fb6ffd2ff26271b6130b1d5df9c6e6c7cdf5779f88c271f91018c041`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:9a84b943671e9587a690e0c4418e0bd89984b5045db84532add2e560e6b76127
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5` - linux; amd64

```console
$ docker pull couchdb@sha256:6b8841ac81e6c9bb96886b5a5ef32cb6b94a1c95cca140afb12857149f25da70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148841671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7a82d4e15f8c7180838079160486fa79a7e62724b07975923372074eca8986`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:12:21 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:12:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 26 May 2026 19:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:12:31 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:12:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:37 GMT
ENV COUCHDB_VERSION=3.5.2
# Tue, 26 May 2026 19:12:37 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:12:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 26 May 2026 19:12:51 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 26 May 2026 19:12:51 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 26 May 2026 19:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 26 May 2026 19:12:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 26 May 2026 19:12:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:12:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 26 May 2026 19:12:51 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 26 May 2026 19:12:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad094000e370e01b9b0daa6c9c7d036ebb493677a3d834cc4dd37ca6ebc6433`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c41c50ddc17b9cb8a76c03fefdbb119878e96fc1b594843917da3d98e2369c`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 7.5 MB (7492175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde7e1f81bb73fc86574bc482826f379b59bce3f64ade593ea5deda639305113`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 417.6 KB (417592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae233ff04273726b94981e9d9496b6b32ca4a0154365cc8a9073945d8bfa14`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 338.6 KB (338589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7be48d8b355af1a2e6b7778b9c20e60a0d301cc4400f958db67b7995d3ceb0b`  
		Last Modified: Tue, 26 May 2026 19:13:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eaa84848643f9866a165135119d5a99dddaa33ac2e48702a613d918f3f8645`  
		Last Modified: Tue, 26 May 2026 19:13:08 GMT  
		Size: 110.8 MB (110807957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7425bf9721a6d60241f07146e898f8f3af4bab905b51ed31f45343e4443e98`  
		Last Modified: Tue, 26 May 2026 19:13:05 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ee2ba7b329f3620816b0e4f18c3c65580205c6a677c14c32bd18eb434a5c7b`  
		Last Modified: Tue, 26 May 2026 19:13:05 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00ed9b589a1f7c3fa1a54be71272252a8910960d018ab9a91d450394d2698e0`  
		Last Modified: Tue, 26 May 2026 19:13:06 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fe1cf8c2ac662e2a24e61bd2a1b38791c0c819c119de1bbb26f1eea89ad577`  
		Last Modified: Tue, 26 May 2026 19:13:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:1c41304f937925dc04b5634e04879a5f00960fc729b7adf90f9eee72e1d485ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31db4accb47515b040f715f98ead62fa20b2242d2e31103dd0bbbb375bd30002`

```dockerfile
```

-	Layers:
	-	`sha256:d53380103996b285e60c22f0619bf6a0454d7ba4db4b545589e5edff7d9b38d9`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 4.2 MB (4180083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a555635af560296c7a4de3e773c7fc48b702408f53bdec0d94124539cc93fbbc`  
		Last Modified: Tue, 26 May 2026 19:13:03 GMT  
		Size: 31.7 KB (31651 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b21bf95ca252a4f39adb63ac54beb08dfece635fb935f120f4e97af2d6755654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148608100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7728a6c9b6ccd474b41cb88a3b73a285022d3ec456689f5fe470cd5ed708c9e6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:15:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:15:25 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 26 May 2026 19:15:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:15:36 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:15:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:42 GMT
ENV COUCHDB_VERSION=3.5.2
# Tue, 26 May 2026 19:15:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:16:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 26 May 2026 19:16:00 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 26 May 2026 19:16:00 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 26 May 2026 19:16:00 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 26 May 2026 19:16:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 26 May 2026 19:16:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:16:00 GMT
VOLUME [/opt/couchdb/data]
# Tue, 26 May 2026 19:16:00 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 26 May 2026 19:16:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee81ff2242296c82709ee9022ec63a8fc58be49f0f1e18f9c59795a4161fc4a2`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad1beefd6a7da95ba934ccdb95d899e5bba2b377224f4bc0761e987c89986fb`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 7.3 MB (7261139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680f1018105ef13db426a95ff02c80c8eb8ea69a1cd9580162284b672d884a54`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 382.5 KB (382541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c7333c528bade7d773502c70c3b68869ded598f9a0a9eb67217e5ab914221e`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 338.7 KB (338692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc09b289ddedc4ea10f1e926124ab6ebd1738d021b2be451abc29136672f8b2b`  
		Last Modified: Tue, 26 May 2026 19:16:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd72831a514a1c868161f96df72438dcfbfbba5f2f7e51448d54a7c153457343`  
		Last Modified: Tue, 26 May 2026 19:16:18 GMT  
		Size: 110.5 MB (110478380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f46eb9f7b9f0ba04326f6e2f3357bde37624d606d35bdf5bde0c4b710eb0c16`  
		Last Modified: Tue, 26 May 2026 19:16:15 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad0c1c889813e2ebe1c372b1675a9f7ae650aa315e22ed82e392f81ee4ee0c6`  
		Last Modified: Tue, 26 May 2026 19:16:15 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f4cc3c59c4e6026dd23daefd1cb59e0eb63f19132e81a0faeb10eb0322c9bb`  
		Last Modified: Tue, 26 May 2026 19:16:17 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3666e26d26dd09323e6aba2ab4440738dff61d7cdd2d4410a2f0e62b8da72ee2`  
		Last Modified: Tue, 26 May 2026 19:16:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:8bff180137c0a38663dcbae6375d83a51777f58246ab4282ecc5b9e185e02241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e4db3c8990df7490fed7dcac5c7443ddca3c4144226007ce6e6ff3dea22b61`

```dockerfile
```

-	Layers:
	-	`sha256:6e83626ed08b8d9480a3581db27d36a51b72f694723487e6b8fd01c2c637fdaf`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 4.2 MB (4180379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31db02b19195bc885b67a6320a83e180ff9c5b74cfc73265bdc7bff58a8f841`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 31.8 KB (31845 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:5fea57e73aecc512b829b25e09deb2f8ae79b8e0d203bf8d3912ed57962ca2df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:b023387918d50d3845f8473ff48db48b4f1f2482924ad3ab2d63bb03ea9be41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150895583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4081591f6f0c7ba97c750131f877958e0833f16e21178d6d040c01069ffc46b1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:12:21 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:12:21 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 26 May 2026 19:12:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:12:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:12:45 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:45 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:12:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.2~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 26 May 2026 19:12:52 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 26 May 2026 19:12:52 GMT
VOLUME [/opt/nouveau/data]
# Tue, 26 May 2026 19:12:52 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 26 May 2026 19:12:52 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adfe4274313c392eaae20352b57638571532c448f9d84f803895a7be9d34d99`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b93c55a8a17efa21140a145fd562147dec16822626ea1fdbce157c87130b7d`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 7.5 MB (7492164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7c98c9da64692549be1b8d19d50b69c53473f24cb80d00d00bcc49d405703`  
		Last Modified: Tue, 26 May 2026 19:13:09 GMT  
		Size: 70.0 MB (70032507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d90032b71529deec699e234f8c1e5f230e15afb2af9ed78f7d0e0ec2ede3d`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 425.9 KB (425935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab98cb1d74db07915b7b1827c6a4bcf710244c844f86dfee323d670dac30646`  
		Last Modified: Tue, 26 May 2026 19:13:09 GMT  
		Size: 347.4 KB (347400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eded855bf9a27128e7cb32a1b5de87627789da0af98fe332221078cd232ee5c9`  
		Last Modified: Tue, 26 May 2026 19:13:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02921ca98efc95457685f61ec045d65e8ef5b0eb0583da320bf69b66d014a5fc`  
		Last Modified: Tue, 26 May 2026 19:13:10 GMT  
		Size: 42.8 MB (42815773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b11220b94c0da697b7694ad7215de07096e324d44080c7e14fe60d4cf4585eb`  
		Last Modified: Tue, 26 May 2026 19:13:09 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:8c778f5178140ba5d74207021493415318525e05d16193d1470c9706b9bde32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbd0f745d242a85ff69cd85d8e7cce3a421ff50bc4b7250f239a016b52b848c`

```dockerfile
```

-	Layers:
	-	`sha256:2b0e20389789aa223ce1281ba70d7e10d48fd4ab0bd37ae05eed938b3c59b532`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 3.4 MB (3364329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c68180b30148fc0ed0bd328a02bc8f8f40105dbe4f49492c10cc96cc819dd1f`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 24.4 KB (24430 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0f9f531bfa4789601ee3332831064ce0c36a3d310050b09642101b9d8dfd74d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150054078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866b12f85c6e83d60ad30361eac4681bbd18835ed93592503375780e9dc98a32`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:15:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:15:28 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 26 May 2026 19:15:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:15:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:15:50 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:50 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:15:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.2~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 26 May 2026 19:15:56 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 26 May 2026 19:15:56 GMT
VOLUME [/opt/nouveau/data]
# Tue, 26 May 2026 19:15:56 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 26 May 2026 19:15:56 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94b8c22a9aee84828061db0dd7d76c57cb2a7fd8e9323aaee931c95a0f6dc6c`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899235a1ecdb426e0b3da18b61f42992f10ee1fd1a10b2c541fd669297f2d5b2`  
		Last Modified: Tue, 26 May 2026 19:16:11 GMT  
		Size: 7.3 MB (7261186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bc6b67f11a43dcedc8cf7dc50c2154ff2c60d4d0c774fb49fbf2f46566bc9e`  
		Last Modified: Tue, 26 May 2026 19:16:13 GMT  
		Size: 69.2 MB (69179669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7429788cc833857a325c900b7a0c2016a5b5de0f2f72fe9aba140e4ba160aafe`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 390.2 KB (390234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873aa82ca7ed235720ae188282afa5273741e99dbdf33261c1a6fc59f6779db`  
		Last Modified: Tue, 26 May 2026 19:16:12 GMT  
		Size: 347.4 KB (347355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca6365ca4a609038d3e36cdce14dd01e8185aea71b1a223c88451270a4bc9f5`  
		Last Modified: Tue, 26 May 2026 19:16:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f241c015171f7d7834492271e36620bb63c15966b4ff3d9a3d8a8a1ec6a848ed`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 42.7 MB (42731840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c4929e8c4527ada0d772f38f8d68322cf21814750e8122e1806ae9b04928dc`  
		Last Modified: Tue, 26 May 2026 19:16:13 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dcd22f542736aefd4d2a30a7548d8ffb85effc726edb9436fb5c4411e52b3a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3387582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380190f460d059d992367b535aa7953a4933d47e782c86303c532a8b7b15431b`

```dockerfile
```

-	Layers:
	-	`sha256:2d5490b97830a7a6171783bf1e51b72cc215ba1c2ff0827e6d39f519ac60f47b`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 3.4 MB (3362970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d46173a258ed8d68f45424b620960e6ad3380b9d4e7632b7c2489b8fe44c102`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 24.6 KB (24612 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2`

```console
$ docker pull couchdb@sha256:9a84b943671e9587a690e0c4418e0bd89984b5045db84532add2e560e6b76127
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2` - linux; amd64

```console
$ docker pull couchdb@sha256:6b8841ac81e6c9bb96886b5a5ef32cb6b94a1c95cca140afb12857149f25da70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148841671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7a82d4e15f8c7180838079160486fa79a7e62724b07975923372074eca8986`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:12:21 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:12:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 26 May 2026 19:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:12:31 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:12:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:37 GMT
ENV COUCHDB_VERSION=3.5.2
# Tue, 26 May 2026 19:12:37 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:12:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 26 May 2026 19:12:51 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 26 May 2026 19:12:51 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 26 May 2026 19:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 26 May 2026 19:12:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 26 May 2026 19:12:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:12:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 26 May 2026 19:12:51 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 26 May 2026 19:12:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad094000e370e01b9b0daa6c9c7d036ebb493677a3d834cc4dd37ca6ebc6433`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c41c50ddc17b9cb8a76c03fefdbb119878e96fc1b594843917da3d98e2369c`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 7.5 MB (7492175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde7e1f81bb73fc86574bc482826f379b59bce3f64ade593ea5deda639305113`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 417.6 KB (417592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae233ff04273726b94981e9d9496b6b32ca4a0154365cc8a9073945d8bfa14`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 338.6 KB (338589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7be48d8b355af1a2e6b7778b9c20e60a0d301cc4400f958db67b7995d3ceb0b`  
		Last Modified: Tue, 26 May 2026 19:13:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eaa84848643f9866a165135119d5a99dddaa33ac2e48702a613d918f3f8645`  
		Last Modified: Tue, 26 May 2026 19:13:08 GMT  
		Size: 110.8 MB (110807957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7425bf9721a6d60241f07146e898f8f3af4bab905b51ed31f45343e4443e98`  
		Last Modified: Tue, 26 May 2026 19:13:05 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ee2ba7b329f3620816b0e4f18c3c65580205c6a677c14c32bd18eb434a5c7b`  
		Last Modified: Tue, 26 May 2026 19:13:05 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00ed9b589a1f7c3fa1a54be71272252a8910960d018ab9a91d450394d2698e0`  
		Last Modified: Tue, 26 May 2026 19:13:06 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fe1cf8c2ac662e2a24e61bd2a1b38791c0c819c119de1bbb26f1eea89ad577`  
		Last Modified: Tue, 26 May 2026 19:13:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:1c41304f937925dc04b5634e04879a5f00960fc729b7adf90f9eee72e1d485ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31db4accb47515b040f715f98ead62fa20b2242d2e31103dd0bbbb375bd30002`

```dockerfile
```

-	Layers:
	-	`sha256:d53380103996b285e60c22f0619bf6a0454d7ba4db4b545589e5edff7d9b38d9`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 4.2 MB (4180083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a555635af560296c7a4de3e773c7fc48b702408f53bdec0d94124539cc93fbbc`  
		Last Modified: Tue, 26 May 2026 19:13:03 GMT  
		Size: 31.7 KB (31651 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b21bf95ca252a4f39adb63ac54beb08dfece635fb935f120f4e97af2d6755654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148608100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7728a6c9b6ccd474b41cb88a3b73a285022d3ec456689f5fe470cd5ed708c9e6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:15:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:15:25 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 26 May 2026 19:15:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:15:36 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:15:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:42 GMT
ENV COUCHDB_VERSION=3.5.2
# Tue, 26 May 2026 19:15:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:16:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 26 May 2026 19:16:00 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 26 May 2026 19:16:00 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 26 May 2026 19:16:00 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 26 May 2026 19:16:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 26 May 2026 19:16:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:16:00 GMT
VOLUME [/opt/couchdb/data]
# Tue, 26 May 2026 19:16:00 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 26 May 2026 19:16:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee81ff2242296c82709ee9022ec63a8fc58be49f0f1e18f9c59795a4161fc4a2`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad1beefd6a7da95ba934ccdb95d899e5bba2b377224f4bc0761e987c89986fb`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 7.3 MB (7261139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680f1018105ef13db426a95ff02c80c8eb8ea69a1cd9580162284b672d884a54`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 382.5 KB (382541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c7333c528bade7d773502c70c3b68869ded598f9a0a9eb67217e5ab914221e`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 338.7 KB (338692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc09b289ddedc4ea10f1e926124ab6ebd1738d021b2be451abc29136672f8b2b`  
		Last Modified: Tue, 26 May 2026 19:16:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd72831a514a1c868161f96df72438dcfbfbba5f2f7e51448d54a7c153457343`  
		Last Modified: Tue, 26 May 2026 19:16:18 GMT  
		Size: 110.5 MB (110478380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f46eb9f7b9f0ba04326f6e2f3357bde37624d606d35bdf5bde0c4b710eb0c16`  
		Last Modified: Tue, 26 May 2026 19:16:15 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad0c1c889813e2ebe1c372b1675a9f7ae650aa315e22ed82e392f81ee4ee0c6`  
		Last Modified: Tue, 26 May 2026 19:16:15 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f4cc3c59c4e6026dd23daefd1cb59e0eb63f19132e81a0faeb10eb0322c9bb`  
		Last Modified: Tue, 26 May 2026 19:16:17 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3666e26d26dd09323e6aba2ab4440738dff61d7cdd2d4410a2f0e62b8da72ee2`  
		Last Modified: Tue, 26 May 2026 19:16:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:8bff180137c0a38663dcbae6375d83a51777f58246ab4282ecc5b9e185e02241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e4db3c8990df7490fed7dcac5c7443ddca3c4144226007ce6e6ff3dea22b61`

```dockerfile
```

-	Layers:
	-	`sha256:6e83626ed08b8d9480a3581db27d36a51b72f694723487e6b8fd01c2c637fdaf`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 4.2 MB (4180379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31db02b19195bc885b67a6320a83e180ff9c5b74cfc73265bdc7bff58a8f841`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 31.8 KB (31845 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2-nouveau`

```console
$ docker pull couchdb@sha256:5fea57e73aecc512b829b25e09deb2f8ae79b8e0d203bf8d3912ed57962ca2df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:b023387918d50d3845f8473ff48db48b4f1f2482924ad3ab2d63bb03ea9be41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150895583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4081591f6f0c7ba97c750131f877958e0833f16e21178d6d040c01069ffc46b1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:12:21 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:12:21 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 26 May 2026 19:12:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:12:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:12:45 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:45 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:12:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.2~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 26 May 2026 19:12:52 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 26 May 2026 19:12:52 GMT
VOLUME [/opt/nouveau/data]
# Tue, 26 May 2026 19:12:52 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 26 May 2026 19:12:52 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adfe4274313c392eaae20352b57638571532c448f9d84f803895a7be9d34d99`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b93c55a8a17efa21140a145fd562147dec16822626ea1fdbce157c87130b7d`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 7.5 MB (7492164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7c98c9da64692549be1b8d19d50b69c53473f24cb80d00d00bcc49d405703`  
		Last Modified: Tue, 26 May 2026 19:13:09 GMT  
		Size: 70.0 MB (70032507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d90032b71529deec699e234f8c1e5f230e15afb2af9ed78f7d0e0ec2ede3d`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 425.9 KB (425935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab98cb1d74db07915b7b1827c6a4bcf710244c844f86dfee323d670dac30646`  
		Last Modified: Tue, 26 May 2026 19:13:09 GMT  
		Size: 347.4 KB (347400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eded855bf9a27128e7cb32a1b5de87627789da0af98fe332221078cd232ee5c9`  
		Last Modified: Tue, 26 May 2026 19:13:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02921ca98efc95457685f61ec045d65e8ef5b0eb0583da320bf69b66d014a5fc`  
		Last Modified: Tue, 26 May 2026 19:13:10 GMT  
		Size: 42.8 MB (42815773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b11220b94c0da697b7694ad7215de07096e324d44080c7e14fe60d4cf4585eb`  
		Last Modified: Tue, 26 May 2026 19:13:09 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:8c778f5178140ba5d74207021493415318525e05d16193d1470c9706b9bde32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbd0f745d242a85ff69cd85d8e7cce3a421ff50bc4b7250f239a016b52b848c`

```dockerfile
```

-	Layers:
	-	`sha256:2b0e20389789aa223ce1281ba70d7e10d48fd4ab0bd37ae05eed938b3c59b532`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 3.4 MB (3364329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c68180b30148fc0ed0bd328a02bc8f8f40105dbe4f49492c10cc96cc819dd1f`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 24.4 KB (24430 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0f9f531bfa4789601ee3332831064ce0c36a3d310050b09642101b9d8dfd74d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150054078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866b12f85c6e83d60ad30361eac4681bbd18835ed93592503375780e9dc98a32`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:15:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:15:28 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 26 May 2026 19:15:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:15:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:15:50 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:50 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:15:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.2~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 26 May 2026 19:15:56 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 26 May 2026 19:15:56 GMT
VOLUME [/opt/nouveau/data]
# Tue, 26 May 2026 19:15:56 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 26 May 2026 19:15:56 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94b8c22a9aee84828061db0dd7d76c57cb2a7fd8e9323aaee931c95a0f6dc6c`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899235a1ecdb426e0b3da18b61f42992f10ee1fd1a10b2c541fd669297f2d5b2`  
		Last Modified: Tue, 26 May 2026 19:16:11 GMT  
		Size: 7.3 MB (7261186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bc6b67f11a43dcedc8cf7dc50c2154ff2c60d4d0c774fb49fbf2f46566bc9e`  
		Last Modified: Tue, 26 May 2026 19:16:13 GMT  
		Size: 69.2 MB (69179669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7429788cc833857a325c900b7a0c2016a5b5de0f2f72fe9aba140e4ba160aafe`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 390.2 KB (390234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873aa82ca7ed235720ae188282afa5273741e99dbdf33261c1a6fc59f6779db`  
		Last Modified: Tue, 26 May 2026 19:16:12 GMT  
		Size: 347.4 KB (347355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca6365ca4a609038d3e36cdce14dd01e8185aea71b1a223c88451270a4bc9f5`  
		Last Modified: Tue, 26 May 2026 19:16:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f241c015171f7d7834492271e36620bb63c15966b4ff3d9a3d8a8a1ec6a848ed`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 42.7 MB (42731840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c4929e8c4527ada0d772f38f8d68322cf21814750e8122e1806ae9b04928dc`  
		Last Modified: Tue, 26 May 2026 19:16:13 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dcd22f542736aefd4d2a30a7548d8ffb85effc726edb9436fb5c4411e52b3a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3387582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380190f460d059d992367b535aa7953a4933d47e782c86303c532a8b7b15431b`

```dockerfile
```

-	Layers:
	-	`sha256:2d5490b97830a7a6171783bf1e51b72cc215ba1c2ff0827e6d39f519ac60f47b`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 3.4 MB (3362970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d46173a258ed8d68f45424b620960e6ad3380b9d4e7632b7c2489b8fe44c102`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 24.6 KB (24612 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:9a84b943671e9587a690e0c4418e0bd89984b5045db84532add2e560e6b76127
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:6b8841ac81e6c9bb96886b5a5ef32cb6b94a1c95cca140afb12857149f25da70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148841671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7a82d4e15f8c7180838079160486fa79a7e62724b07975923372074eca8986`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:12:21 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:12:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 26 May 2026 19:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:12:31 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:12:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:37 GMT
ENV COUCHDB_VERSION=3.5.2
# Tue, 26 May 2026 19:12:37 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:12:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 26 May 2026 19:12:51 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 26 May 2026 19:12:51 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 26 May 2026 19:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 26 May 2026 19:12:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 26 May 2026 19:12:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:12:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 26 May 2026 19:12:51 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 26 May 2026 19:12:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad094000e370e01b9b0daa6c9c7d036ebb493677a3d834cc4dd37ca6ebc6433`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c41c50ddc17b9cb8a76c03fefdbb119878e96fc1b594843917da3d98e2369c`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 7.5 MB (7492175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde7e1f81bb73fc86574bc482826f379b59bce3f64ade593ea5deda639305113`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 417.6 KB (417592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae233ff04273726b94981e9d9496b6b32ca4a0154365cc8a9073945d8bfa14`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 338.6 KB (338589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7be48d8b355af1a2e6b7778b9c20e60a0d301cc4400f958db67b7995d3ceb0b`  
		Last Modified: Tue, 26 May 2026 19:13:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eaa84848643f9866a165135119d5a99dddaa33ac2e48702a613d918f3f8645`  
		Last Modified: Tue, 26 May 2026 19:13:08 GMT  
		Size: 110.8 MB (110807957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7425bf9721a6d60241f07146e898f8f3af4bab905b51ed31f45343e4443e98`  
		Last Modified: Tue, 26 May 2026 19:13:05 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ee2ba7b329f3620816b0e4f18c3c65580205c6a677c14c32bd18eb434a5c7b`  
		Last Modified: Tue, 26 May 2026 19:13:05 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00ed9b589a1f7c3fa1a54be71272252a8910960d018ab9a91d450394d2698e0`  
		Last Modified: Tue, 26 May 2026 19:13:06 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fe1cf8c2ac662e2a24e61bd2a1b38791c0c819c119de1bbb26f1eea89ad577`  
		Last Modified: Tue, 26 May 2026 19:13:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:1c41304f937925dc04b5634e04879a5f00960fc729b7adf90f9eee72e1d485ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31db4accb47515b040f715f98ead62fa20b2242d2e31103dd0bbbb375bd30002`

```dockerfile
```

-	Layers:
	-	`sha256:d53380103996b285e60c22f0619bf6a0454d7ba4db4b545589e5edff7d9b38d9`  
		Last Modified: Tue, 26 May 2026 19:13:04 GMT  
		Size: 4.2 MB (4180083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a555635af560296c7a4de3e773c7fc48b702408f53bdec0d94124539cc93fbbc`  
		Last Modified: Tue, 26 May 2026 19:13:03 GMT  
		Size: 31.7 KB (31651 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b21bf95ca252a4f39adb63ac54beb08dfece635fb935f120f4e97af2d6755654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148608100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7728a6c9b6ccd474b41cb88a3b73a285022d3ec456689f5fe470cd5ed708c9e6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:15:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:15:25 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 26 May 2026 19:15:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:15:36 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:15:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:42 GMT
ENV COUCHDB_VERSION=3.5.2
# Tue, 26 May 2026 19:15:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:16:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 26 May 2026 19:16:00 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 26 May 2026 19:16:00 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 26 May 2026 19:16:00 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 26 May 2026 19:16:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 26 May 2026 19:16:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:16:00 GMT
VOLUME [/opt/couchdb/data]
# Tue, 26 May 2026 19:16:00 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 26 May 2026 19:16:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee81ff2242296c82709ee9022ec63a8fc58be49f0f1e18f9c59795a4161fc4a2`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad1beefd6a7da95ba934ccdb95d899e5bba2b377224f4bc0761e987c89986fb`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 7.3 MB (7261139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680f1018105ef13db426a95ff02c80c8eb8ea69a1cd9580162284b672d884a54`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 382.5 KB (382541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c7333c528bade7d773502c70c3b68869ded598f9a0a9eb67217e5ab914221e`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 338.7 KB (338692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc09b289ddedc4ea10f1e926124ab6ebd1738d021b2be451abc29136672f8b2b`  
		Last Modified: Tue, 26 May 2026 19:16:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd72831a514a1c868161f96df72438dcfbfbba5f2f7e51448d54a7c153457343`  
		Last Modified: Tue, 26 May 2026 19:16:18 GMT  
		Size: 110.5 MB (110478380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f46eb9f7b9f0ba04326f6e2f3357bde37624d606d35bdf5bde0c4b710eb0c16`  
		Last Modified: Tue, 26 May 2026 19:16:15 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad0c1c889813e2ebe1c372b1675a9f7ae650aa315e22ed82e392f81ee4ee0c6`  
		Last Modified: Tue, 26 May 2026 19:16:15 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f4cc3c59c4e6026dd23daefd1cb59e0eb63f19132e81a0faeb10eb0322c9bb`  
		Last Modified: Tue, 26 May 2026 19:16:17 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3666e26d26dd09323e6aba2ab4440738dff61d7cdd2d4410a2f0e62b8da72ee2`  
		Last Modified: Tue, 26 May 2026 19:16:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:8bff180137c0a38663dcbae6375d83a51777f58246ab4282ecc5b9e185e02241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e4db3c8990df7490fed7dcac5c7443ddca3c4144226007ce6e6ff3dea22b61`

```dockerfile
```

-	Layers:
	-	`sha256:6e83626ed08b8d9480a3581db27d36a51b72f694723487e6b8fd01c2c637fdaf`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 4.2 MB (4180379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31db02b19195bc885b67a6320a83e180ff9c5b74cfc73265bdc7bff58a8f841`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 31.8 KB (31845 bytes)  
		MIME: application/vnd.in-toto+json
