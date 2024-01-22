<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.2`](#couchdb312)
-	[`couchdb:3.2`](#couchdb32)
-	[`couchdb:3.2.3`](#couchdb323)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.3`](#couchdb333)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:0645f919ef084fef3379fdcb611753f81eaa3e7265d647b3f4e86037da558e11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:bdf4f541d80a417654efd8b88cefe25b45b16be1fdaa504c51c1a0ea1f62d794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84170582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9e0b2d59d5e3f96700c32302064f63f410f699dad5f01f91c97fa6814b0359`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:08cfc7bf77cc2291c96890f44a435216cb1168c45cef77f7801430982c43ca58 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4648efdf070b378f12737b5cdacaded7b6294f27d0a0c1fb33849090813e920a`  
		Last Modified: Thu, 11 Jan 2024 02:43:48 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470868bfb524bf7ca9623396664e348a89684761a1fd6986622655b5b4b5e6c3`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404d8e6552c59dae95120b9096ee602535e814d7d77c2276cbfa0eb73384f0c2`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 6.7 MB (6703481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0775d070ce82ba86cf460cd9aad004be7c4e8995dd9dbae628685870ed4cc5`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 1.0 MB (1046505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3162a26a3ccad9270da1c9e8c38326ebcee7595aeb558cc56419b7a8bf589407`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 80.3 KB (80322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a37f164c0541e03da69484b0a5fe15cb8d421e583548d4151cc07acab5fa083`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8efd80bf60857dc4f71a6de701b31622b83850b9712f6527b843042514ae363`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 49.1 MB (49145132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c364e49a598fcbd9cb518392f480d90a929a7304aea3734dc7a1ae34abc71f`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9d181be91a0087f7617b5ac1b0a785e273ffb9d43e38232801a7df64c05d10`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 760.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56d617b1991c1261b0efb55a397aeacc286fcec2af6fbe5bbfda9e974001794`  
		Last Modified: Thu, 18 Jan 2024 18:13:32 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82812fa3b9a495a112f666242ea73b275bc3ca44295f7042a9df9ca337d881f9`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2` - unknown; unknown

```console
$ docker pull couchdb@sha256:0595161ee5607d6356a8cd9dbc1624291c7eaabbd2df4281ad34eedd9ed48e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c1b0a6037b209c46ce0635cba8ed6a3cfecc4abea322f223f4771b7403a0b6`

```dockerfile
```

-	Layers:
	-	`sha256:c899ce4ba26d35a7fb968d3a9bf538ee1bd809a10099b8bc5e6674e1440fa13f`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 3.5 MB (3517463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eb2bcc7b5f799521535443d3d35bc814e303424383af527378030917a9a40f6`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 31.6 KB (31582 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:425148c1fc1e31af733a6801168b9927b36d13ecee2105593468bdd15f9a198a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72615137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3588e69cec7b553ed8d15ab4476af16b35cd696401fd8733fc2cf33c6cf326e3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:0d7c08c3a192fbaded92a14e5eed44f5df7d00cd932ed45984ebb6b6e21446a6 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d982983796daa327ca72ca687e0d8417bb909e8256d666725dae5ad846525ae`  
		Last Modified: Thu, 11 Jan 2024 02:45:24 GMT  
		Size: 26.0 MB (25969811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1a78c86ecb35f073675b605f5f2dd61790d9d6ffd96d4ef99d760d11ad9ea9`  
		Last Modified: Thu, 18 Jan 2024 19:12:38 GMT  
		Size: 3.4 KB (3358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b0c5f7a37982b6c363bff53d5c764cb626dd47b9a0dd86f0234d32829f0dbb`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 6.6 MB (6576629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c78b8447e56be5eba47240e31cc278ac9daced65b046b58f941220a3d5220a2`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 951.3 KB (951324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd91ad113f4e6f2f1b2cb79413ec3af11db742705bd49879b6aad79e5cbd6637`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 80.2 KB (80196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de075c7dbe1608cf56d3ea139a8f628e26907227d44b267259c5ef424ea191e3`  
		Last Modified: Thu, 18 Jan 2024 19:27:03 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6968cf3ffe4a8fca9aa86dbaa4c3c204e1dc43f17d061a4abe89c819e0eb6e`  
		Last Modified: Thu, 18 Jan 2024 19:27:04 GMT  
		Size: 39.0 MB (39030225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa57d4f435faf6cb55674a13ec85b351e023aa37474ca488dcfa140d88eff3d`  
		Last Modified: Thu, 18 Jan 2024 19:27:03 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fcbaf102d8563985cb7ec6244b975cbf68cb2902373590136ed40e3be70d67`  
		Last Modified: Thu, 18 Jan 2024 19:27:03 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade91d080a3220a01f407f4aa11b1cf4cea32ef1d8148ed412809d4b8d81a96e`  
		Last Modified: Thu, 18 Jan 2024 19:27:04 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e44cd07c145d331e9db85be79b74f867826fdc0a14811a51c87aed647b55fd9`  
		Last Modified: Thu, 18 Jan 2024 19:27:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2` - unknown; unknown

```console
$ docker pull couchdb@sha256:c2f11748e00bce45102227b0ba239de5b818d28a446033268891ee02c5aaebbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2941978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a4d4e44bbbadb778a9fd0b69e58b6c2ccdcd88543bc2872f43def51f296bc3`

```dockerfile
```

-	Layers:
	-	`sha256:909d7b48f6844871ced209b4637e1282387fed1b07df0e339cf6b21c860c6110`  
		Last Modified: Thu, 18 Jan 2024 19:27:03 GMT  
		Size: 2.9 MB (2910563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4397363128d04814058125eda4d2890317814f9df79ea6ecaf132042e75e59d`  
		Last Modified: Thu, 18 Jan 2024 19:27:02 GMT  
		Size: 31.4 KB (31415 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:0645f919ef084fef3379fdcb611753f81eaa3e7265d647b3f4e86037da558e11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:bdf4f541d80a417654efd8b88cefe25b45b16be1fdaa504c51c1a0ea1f62d794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84170582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9e0b2d59d5e3f96700c32302064f63f410f699dad5f01f91c97fa6814b0359`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:08cfc7bf77cc2291c96890f44a435216cb1168c45cef77f7801430982c43ca58 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4648efdf070b378f12737b5cdacaded7b6294f27d0a0c1fb33849090813e920a`  
		Last Modified: Thu, 11 Jan 2024 02:43:48 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470868bfb524bf7ca9623396664e348a89684761a1fd6986622655b5b4b5e6c3`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404d8e6552c59dae95120b9096ee602535e814d7d77c2276cbfa0eb73384f0c2`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 6.7 MB (6703481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0775d070ce82ba86cf460cd9aad004be7c4e8995dd9dbae628685870ed4cc5`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 1.0 MB (1046505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3162a26a3ccad9270da1c9e8c38326ebcee7595aeb558cc56419b7a8bf589407`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 80.3 KB (80322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a37f164c0541e03da69484b0a5fe15cb8d421e583548d4151cc07acab5fa083`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8efd80bf60857dc4f71a6de701b31622b83850b9712f6527b843042514ae363`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 49.1 MB (49145132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c364e49a598fcbd9cb518392f480d90a929a7304aea3734dc7a1ae34abc71f`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9d181be91a0087f7617b5ac1b0a785e273ffb9d43e38232801a7df64c05d10`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 760.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56d617b1991c1261b0efb55a397aeacc286fcec2af6fbe5bbfda9e974001794`  
		Last Modified: Thu, 18 Jan 2024 18:13:32 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82812fa3b9a495a112f666242ea73b275bc3ca44295f7042a9df9ca337d881f9`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:0595161ee5607d6356a8cd9dbc1624291c7eaabbd2df4281ad34eedd9ed48e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c1b0a6037b209c46ce0635cba8ed6a3cfecc4abea322f223f4771b7403a0b6`

```dockerfile
```

-	Layers:
	-	`sha256:c899ce4ba26d35a7fb968d3a9bf538ee1bd809a10099b8bc5e6674e1440fa13f`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 3.5 MB (3517463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eb2bcc7b5f799521535443d3d35bc814e303424383af527378030917a9a40f6`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 31.6 KB (31582 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:425148c1fc1e31af733a6801168b9927b36d13ecee2105593468bdd15f9a198a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72615137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3588e69cec7b553ed8d15ab4476af16b35cd696401fd8733fc2cf33c6cf326e3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:0d7c08c3a192fbaded92a14e5eed44f5df7d00cd932ed45984ebb6b6e21446a6 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d982983796daa327ca72ca687e0d8417bb909e8256d666725dae5ad846525ae`  
		Last Modified: Thu, 11 Jan 2024 02:45:24 GMT  
		Size: 26.0 MB (25969811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1a78c86ecb35f073675b605f5f2dd61790d9d6ffd96d4ef99d760d11ad9ea9`  
		Last Modified: Thu, 18 Jan 2024 19:12:38 GMT  
		Size: 3.4 KB (3358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b0c5f7a37982b6c363bff53d5c764cb626dd47b9a0dd86f0234d32829f0dbb`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 6.6 MB (6576629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c78b8447e56be5eba47240e31cc278ac9daced65b046b58f941220a3d5220a2`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 951.3 KB (951324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd91ad113f4e6f2f1b2cb79413ec3af11db742705bd49879b6aad79e5cbd6637`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 80.2 KB (80196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de075c7dbe1608cf56d3ea139a8f628e26907227d44b267259c5ef424ea191e3`  
		Last Modified: Thu, 18 Jan 2024 19:27:03 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6968cf3ffe4a8fca9aa86dbaa4c3c204e1dc43f17d061a4abe89c819e0eb6e`  
		Last Modified: Thu, 18 Jan 2024 19:27:04 GMT  
		Size: 39.0 MB (39030225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa57d4f435faf6cb55674a13ec85b351e023aa37474ca488dcfa140d88eff3d`  
		Last Modified: Thu, 18 Jan 2024 19:27:03 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fcbaf102d8563985cb7ec6244b975cbf68cb2902373590136ed40e3be70d67`  
		Last Modified: Thu, 18 Jan 2024 19:27:03 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade91d080a3220a01f407f4aa11b1cf4cea32ef1d8148ed412809d4b8d81a96e`  
		Last Modified: Thu, 18 Jan 2024 19:27:04 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e44cd07c145d331e9db85be79b74f867826fdc0a14811a51c87aed647b55fd9`  
		Last Modified: Thu, 18 Jan 2024 19:27:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c2f11748e00bce45102227b0ba239de5b818d28a446033268891ee02c5aaebbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2941978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a4d4e44bbbadb778a9fd0b69e58b6c2ccdcd88543bc2872f43def51f296bc3`

```dockerfile
```

-	Layers:
	-	`sha256:909d7b48f6844871ced209b4637e1282387fed1b07df0e339cf6b21c860c6110`  
		Last Modified: Thu, 18 Jan 2024 19:27:03 GMT  
		Size: 2.9 MB (2910563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4397363128d04814058125eda4d2890317814f9df79ea6ecaf132042e75e59d`  
		Last Modified: Thu, 18 Jan 2024 19:27:02 GMT  
		Size: 31.4 KB (31415 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:0645f919ef084fef3379fdcb611753f81eaa3e7265d647b3f4e86037da558e11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:bdf4f541d80a417654efd8b88cefe25b45b16be1fdaa504c51c1a0ea1f62d794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84170582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9e0b2d59d5e3f96700c32302064f63f410f699dad5f01f91c97fa6814b0359`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:08cfc7bf77cc2291c96890f44a435216cb1168c45cef77f7801430982c43ca58 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4648efdf070b378f12737b5cdacaded7b6294f27d0a0c1fb33849090813e920a`  
		Last Modified: Thu, 11 Jan 2024 02:43:48 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470868bfb524bf7ca9623396664e348a89684761a1fd6986622655b5b4b5e6c3`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404d8e6552c59dae95120b9096ee602535e814d7d77c2276cbfa0eb73384f0c2`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 6.7 MB (6703481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0775d070ce82ba86cf460cd9aad004be7c4e8995dd9dbae628685870ed4cc5`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 1.0 MB (1046505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3162a26a3ccad9270da1c9e8c38326ebcee7595aeb558cc56419b7a8bf589407`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 80.3 KB (80322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a37f164c0541e03da69484b0a5fe15cb8d421e583548d4151cc07acab5fa083`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8efd80bf60857dc4f71a6de701b31622b83850b9712f6527b843042514ae363`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 49.1 MB (49145132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c364e49a598fcbd9cb518392f480d90a929a7304aea3734dc7a1ae34abc71f`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9d181be91a0087f7617b5ac1b0a785e273ffb9d43e38232801a7df64c05d10`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 760.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56d617b1991c1261b0efb55a397aeacc286fcec2af6fbe5bbfda9e974001794`  
		Last Modified: Thu, 18 Jan 2024 18:13:32 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82812fa3b9a495a112f666242ea73b275bc3ca44295f7042a9df9ca337d881f9`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:0595161ee5607d6356a8cd9dbc1624291c7eaabbd2df4281ad34eedd9ed48e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c1b0a6037b209c46ce0635cba8ed6a3cfecc4abea322f223f4771b7403a0b6`

```dockerfile
```

-	Layers:
	-	`sha256:c899ce4ba26d35a7fb968d3a9bf538ee1bd809a10099b8bc5e6674e1440fa13f`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 3.5 MB (3517463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eb2bcc7b5f799521535443d3d35bc814e303424383af527378030917a9a40f6`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 31.6 KB (31582 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:425148c1fc1e31af733a6801168b9927b36d13ecee2105593468bdd15f9a198a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72615137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3588e69cec7b553ed8d15ab4476af16b35cd696401fd8733fc2cf33c6cf326e3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:0d7c08c3a192fbaded92a14e5eed44f5df7d00cd932ed45984ebb6b6e21446a6 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d982983796daa327ca72ca687e0d8417bb909e8256d666725dae5ad846525ae`  
		Last Modified: Thu, 11 Jan 2024 02:45:24 GMT  
		Size: 26.0 MB (25969811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1a78c86ecb35f073675b605f5f2dd61790d9d6ffd96d4ef99d760d11ad9ea9`  
		Last Modified: Thu, 18 Jan 2024 19:12:38 GMT  
		Size: 3.4 KB (3358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b0c5f7a37982b6c363bff53d5c764cb626dd47b9a0dd86f0234d32829f0dbb`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 6.6 MB (6576629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c78b8447e56be5eba47240e31cc278ac9daced65b046b58f941220a3d5220a2`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 951.3 KB (951324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd91ad113f4e6f2f1b2cb79413ec3af11db742705bd49879b6aad79e5cbd6637`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 80.2 KB (80196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de075c7dbe1608cf56d3ea139a8f628e26907227d44b267259c5ef424ea191e3`  
		Last Modified: Thu, 18 Jan 2024 19:27:03 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6968cf3ffe4a8fca9aa86dbaa4c3c204e1dc43f17d061a4abe89c819e0eb6e`  
		Last Modified: Thu, 18 Jan 2024 19:27:04 GMT  
		Size: 39.0 MB (39030225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa57d4f435faf6cb55674a13ec85b351e023aa37474ca488dcfa140d88eff3d`  
		Last Modified: Thu, 18 Jan 2024 19:27:03 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fcbaf102d8563985cb7ec6244b975cbf68cb2902373590136ed40e3be70d67`  
		Last Modified: Thu, 18 Jan 2024 19:27:03 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade91d080a3220a01f407f4aa11b1cf4cea32ef1d8148ed412809d4b8d81a96e`  
		Last Modified: Thu, 18 Jan 2024 19:27:04 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e44cd07c145d331e9db85be79b74f867826fdc0a14811a51c87aed647b55fd9`  
		Last Modified: Thu, 18 Jan 2024 19:27:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:c2f11748e00bce45102227b0ba239de5b818d28a446033268891ee02c5aaebbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2941978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a4d4e44bbbadb778a9fd0b69e58b6c2ccdcd88543bc2872f43def51f296bc3`

```dockerfile
```

-	Layers:
	-	`sha256:909d7b48f6844871ced209b4637e1282387fed1b07df0e339cf6b21c860c6110`  
		Last Modified: Thu, 18 Jan 2024 19:27:03 GMT  
		Size: 2.9 MB (2910563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4397363128d04814058125eda4d2890317814f9df79ea6ecaf132042e75e59d`  
		Last Modified: Thu, 18 Jan 2024 19:27:02 GMT  
		Size: 31.4 KB (31415 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3`

```console
$ docker pull couchdb@sha256:3ca831841dae6f661cdcfd4b0f9a35627178c27732a5b00857162cb68cc1a28d
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

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:a6c2351fd35c463193f0775991f4619a8000a84cdd2bc8ef552ff65a9d116df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89638790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9602933014c5907bb2c8d43f726ed2373622f8c0636987af9bcf3a5f0c79ead`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5f63586ac0fd7679f03a38b2bb6a95b5b75f1dc39c4be0897995a04354db23`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4806581c93b54f52f0b08bb9dbf6d9d326c88930b406a7340af980bc8f768270`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 5.0 MB (5019733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8f182d248e8eaf090954e8c4852ae2a0dcc21d852c8909bcecfdc5be738992`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 394.4 KB (394350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c4e895eead2d5f1e750f0915735d88b7667d6dd91c9edfc2334c140def3da`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 77.9 KB (77870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096d0e49d7a91d8cb75a1416348c016174dc79b1d944f1aefd3fe7f5aba5230`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d050a15c1a57401d120413f3ef0c681d54def3ed9a00dec7fdacd1698f4dc2`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 52.7 MB (52721308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b5fe326ea02bda341bf09015da4158d57f825cc1eb45082d12249fa347fb7a`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf986debded9719af265c501f61e0191c50cbc0e285df8be650fbfe38f1dbf7`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f414ac70ae0c0a9bcdc3890668a92b5dd82f1c92125e60c18d68b0bb0c892c`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82812fa3b9a495a112f666242ea73b275bc3ca44295f7042a9df9ca337d881f9`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:25b4add69ad04ff48680e2b9a2f87ec8666d4b15013557e6d70e95f42907f839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95af21f1234feac3e769f41cbef67f3b28b8cecc2953e23304c5ec1f97a78d84`

```dockerfile
```

-	Layers:
	-	`sha256:902746ba0194033a33e5ccb12ab54639988083f18616bcd90a05561fc90787a0`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 3.3 MB (3295838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ba05299961375fbd390d8a9ffac7f36f8f3acb1bc24ef7f7cdd7caf76fbf7d`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:645eeba853b353a0880afe246a9c08f11b1db9f7069aeec06e86633c2ae7a9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88077003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ab4f86a454f930c5293207c881dc8a9a96504724631385596bb3fe22c6dad4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a59ba3e4f10a55c45f29d6706897bd99a03fcaf39b5fdca85dd7be539e43c4a`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 3.4 KB (3355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c1775ae673f1913d1b34db47129dd8496cf0c5b1e40754a379d344a4c39af9`  
		Last Modified: Thu, 18 Jan 2024 18:25:47 GMT  
		Size: 5.0 MB (5004083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db7ed076b4ca27f58fc0f25577270f4784e64c11783598b3447334756a7779a`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 350.5 KB (350533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d463fb07f7e8316a5f2ff4ced677b570c6e35870ff4e409ac92bc4965a8ca72`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 77.8 KB (77791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a0230918a06cce0cd48841eae3f8a3948f2822e949ae3f0e9a378d17f18ea0`  
		Last Modified: Thu, 18 Jan 2024 18:25:47 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e444d5a50d45faf9749ade5ba735be01f3ed499cfdadd0083713f79fd2719513`  
		Last Modified: Thu, 18 Jan 2024 18:25:49 GMT  
		Size: 52.6 MB (52572987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be04144325a578fe50a679412704b79165f2a03e9a5693f1a724f4cfa0b882d`  
		Last Modified: Thu, 18 Jan 2024 18:25:48 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658861fcf6e0a38fc7bc201bb87e65e3521683c5415d1d9b480ef0207b7c8a2`  
		Last Modified: Thu, 18 Jan 2024 18:25:48 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b7fa5576f4c549e826842527c9401ed1ed95f7a44a766d8aa31a85b6931893`  
		Last Modified: Thu, 18 Jan 2024 18:25:48 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fedb07453eabd9d0f541818e94dbc959d77c0ccca43d01efaef77db9a810c1`  
		Last Modified: Thu, 18 Jan 2024 18:25:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:5104a467f3b1d97bb1a4f02854ba2d4cddbed1e64d7a583a198fe20afa95915e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7fc37d6f1794004d31cafd9e41af529e6de349b4b6fc50d14ca3fa4aff4b25`

```dockerfile
```

-	Layers:
	-	`sha256:f66a91149ebc7c01c27ec52709522562e643f3f55a0cd67c928be24c0c53aa83`  
		Last Modified: Thu, 18 Jan 2024 18:25:47 GMT  
		Size: 3.3 MB (3296186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:397620cb518bf7fc4324e5cbc9c845fada5a8c67f905a0b08d8d59d05a4359f6`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 31.6 KB (31567 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:69e7bb7b08288d2ad5911d2f90d65624190641c3188be1498a659141b0a5f4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95365643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f15f1c43a1f277b35e33720b083578bf215588d35b14d6ae1a9426b2dfdb7b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6db52a5975ca141a51329334ae6e88c2292f71fbe05afc650101f9bea065e1f`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcc670e3b076d9245550182fc3f3f3e631c7ac042318dd344de58958ee36742`  
		Last Modified: Thu, 18 Jan 2024 18:41:04 GMT  
		Size: 5.8 MB (5839115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a6131d377e41d04166cbc404c9dea6eec8cff82017ff069298da8f447d197a`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 446.6 KB (446615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6c69adbbae2aa46ee77b6c8b440605e979556f85d5165a5c0671d9294357d4`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 77.8 KB (77831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8597146addb9ce87cdad5becbc50b3cf679a7afad871f3bbedbbfedf7bc71`  
		Last Modified: Thu, 18 Jan 2024 18:41:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522d544c2f0e982c8450228e8729faa2978db225d6f3680ee651c397432c93d`  
		Last Modified: Thu, 18 Jan 2024 18:41:07 GMT  
		Size: 53.7 MB (53700703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8dec663e5b1342f77a30a21ca3ad1660da2c0bd3cf28c65e0839f15fa66f20`  
		Last Modified: Thu, 18 Jan 2024 18:41:05 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3aa75c81e4c5e24b7098f1af4d33744e7c5c6286ec9dbaff87d3338dfb42ea0`  
		Last Modified: Thu, 18 Jan 2024 18:41:05 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95be43deb43b89954226ebe9598871a99c6294dce06dede85e7cd071991d0eb`  
		Last Modified: Thu, 18 Jan 2024 18:41:05 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6852b878032a76a59c61188b08d5e6085737e5fe384499aea66023b3165212`  
		Last Modified: Thu, 18 Jan 2024 18:41:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c6165efd2f26ab15ecc1a84a49cd156b01d04fcecd3ac87fcf1b49d668840d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3332087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389ec486b9fd5b339adbc5000265bbee7b701a55606d3b6f5d2a515f2e3b6691`

```dockerfile
```

-	Layers:
	-	`sha256:759287d64d2b8f87e3dbb8b0cf81b5ff2b9ea816e0fa9792c86d869e2725b592`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 3.3 MB (3300478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ff5c5acfdeab6765e9dade4462fde43947f3c41d62167e7349ff8153048087`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:0d78ccfcf452ca412da28e0fd29aaebbf4e0f9eb4e30ecf0b7cbf591799726e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86381115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c8e8d518db5442bf3e62da8a24c4b159ca471fc335ef646c9a640290e22454`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:77a92d4e9397475a6c68f4341baba607a7c875bc6e252de3e096482dd074f8ca in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a8470cec8ee9510bf45556c756635d84eb3cbc0220b52812522196008c6b0d3e`  
		Last Modified: Thu, 11 Jan 2024 01:51:19 GMT  
		Size: 29.7 MB (29656884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be83499ba256778626ad82f9fccd7164e71be3760487161f2ed4d8507339692`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 3.4 KB (3352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae10b9b22721e18b6fa8df8d8dd9b1e9c78450f802ede4945cb1291205404de7`  
		Last Modified: Sat, 20 Jan 2024 18:54:09 GMT  
		Size: 4.9 MB (4905513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98262054a3abcb8a53517cc3e83057413c0aed04cb6d3d9c01b1d4bab3aa7b17`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 357.5 KB (357466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ad4715d6dd594ec2fd231a01d4017944e79879f474a94611d9402cace0df73`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 77.8 KB (77815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adec8571498762cf768831b0cdd0a5bf0e976b2a65a3a2ca10c8c94d3c154f59`  
		Last Modified: Sat, 20 Jan 2024 18:54:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81435e5bf59142d2023bb566129cb197c3d9644728fbbdbc39558f7a99c14427`  
		Last Modified: Sat, 20 Jan 2024 18:54:11 GMT  
		Size: 51.4 MB (51375834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c05edc71f5f7e520e935527c545ced5d546770663df032718e8eaab4301b0e`  
		Last Modified: Sat, 20 Jan 2024 18:54:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d54553bef03697146cbc479a5b24465b84fecc5f4187ceed5f72be7be018bd`  
		Last Modified: Sat, 20 Jan 2024 18:54:10 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484cedac62572daea8476c4c881b70ddb5e8e6211414dd2769810b5a949eedd3`  
		Last Modified: Sat, 20 Jan 2024 18:54:10 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a73c8e6f40ec927189debd9f02f1a3500f41b84edc74f26cce60b557a22d9a`  
		Last Modified: Sat, 20 Jan 2024 18:54:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f1e2d4155a5990898279fa057614ee5f8fa2ac3d36230b49ee07fa64471c02ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3326969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b70b216f828433cdd3a051826187f1a45fcbb515efd5029491687c8f6e0fe45`

```dockerfile
```

-	Layers:
	-	`sha256:5b0775950ac0345039827bfc393978f41c5d432f6b455b6905759b7bbd15c040`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 3.3 MB (3295410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d863f59b35bd9fd762688e0c8db88852580209ab63f5fd73a0e31e48a048a7`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 31.6 KB (31559 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:0d26b2cbf4849059183c4054430f1704cdf131b9404786e233ed05f93ef6f906
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:de9cbe483c7c245917bdec70c15e04987cb674a450acc5d8613cd24daf243b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79645282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0770734989b23f20f21098a6fdabfd044a122d245dc0769e8bd168d04935fb3f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:08cfc7bf77cc2291c96890f44a435216cb1168c45cef77f7801430982c43ca58 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4648efdf070b378f12737b5cdacaded7b6294f27d0a0c1fb33849090813e920a`  
		Last Modified: Thu, 11 Jan 2024 02:43:48 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb6114e35cc47d594428e5f313019f5680a4ea4bdf497280303fd379114210d`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06982f2aa7fb16db4a7a41a1a2ca567b88e21545355e10853dd03aac5ada25ba`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 6.7 MB (6703446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d86f7417a3bbd39e87d4e1160473b3d1b6c6f6f11dc821a1ff5b0892b09e661`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 1.0 MB (1046497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c59d5b797cf73da5593b5a9c071ff024c1171545fc317d3524f275c47b950`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 80.3 KB (80333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8ee01dd96bf0469ad6e0788c30e7ddf3f4e20dcc61c723ce67c41b1b6b8151`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7549f8782da3e7ebe160d3f5b152fd6bbed2e063ea60daecd2a1791f92514d1b`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 44.6 MB (44619863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964033ec3b765dd82f9ff0c0f0c1ac302dd62c7501fc6435fd7f71b11c5bfff3`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5925746de937aeccb49187240ad489d272da916d1bb5bd3a1cb3cfafc2a1d095`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603f2136df0b84f0e123cf41ee8e67475369272ab665ea74ba6dc38849092558`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82812fa3b9a495a112f666242ea73b275bc3ca44295f7042a9df9ca337d881f9`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:79f04e08934f4b645065cf55f0bea365a099a889cad1b8cff0087141d2f0539e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e133c21cdf015e1400a809175debc983b34b751b82da3aa06e27a98152e36b80`

```dockerfile
```

-	Layers:
	-	`sha256:f7d91b3825a2c6ab1db062190f7912303b7187f4d5defaefbe4f649d3fb90fdf`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 3.0 MB (2955438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a4109360b17ccf4983bec0f870b9b85b0c482f7facfccc5a53b601292551b1d`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 31.3 KB (31282 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:32680bbc86000b0fb9391c9027b93549403acee5a9ab14a55db236031dddd0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74709870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d207dab7a7f74e6977129cdedf63b0b8fb5c2ddda0b6abbe61c1e170ed93f05`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:0d7c08c3a192fbaded92a14e5eed44f5df7d00cd932ed45984ebb6b6e21446a6 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d982983796daa327ca72ca687e0d8417bb909e8256d666725dae5ad846525ae`  
		Last Modified: Thu, 11 Jan 2024 02:45:24 GMT  
		Size: 26.0 MB (25969811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1a78c86ecb35f073675b605f5f2dd61790d9d6ffd96d4ef99d760d11ad9ea9`  
		Last Modified: Thu, 18 Jan 2024 19:12:38 GMT  
		Size: 3.4 KB (3358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b0c5f7a37982b6c363bff53d5c764cb626dd47b9a0dd86f0234d32829f0dbb`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 6.6 MB (6576629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c78b8447e56be5eba47240e31cc278ac9daced65b046b58f941220a3d5220a2`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 951.3 KB (951324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd91ad113f4e6f2f1b2cb79413ec3af11db742705bd49879b6aad79e5cbd6637`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 80.2 KB (80196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f85c71d610a52c7ae3e45b20d2a2015258efe431927e3564f494285183b17c7`  
		Last Modified: Thu, 18 Jan 2024 19:12:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12eff63a21967f2630eb4910f9b18d73f9323de7ba3c6d6549c3cf5aa51ab2d6`  
		Last Modified: Thu, 18 Jan 2024 19:12:41 GMT  
		Size: 41.1 MB (41124960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0797bb13160151e8025b57a37c5aead92b5f471dc8a483fc17391583ea13e7`  
		Last Modified: Thu, 18 Jan 2024 19:12:40 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0bc64833607e2198e0c09b5d61797096a72133b65ec67e57889817c86d1d9a`  
		Last Modified: Thu, 18 Jan 2024 19:12:41 GMT  
		Size: 763.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee52ebd6aa7d68170c137e56e42242b7fe9e59056b06d39ae470d548e5583976`  
		Last Modified: Thu, 18 Jan 2024 19:12:41 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c2957b74be48e9851a04cfe55880bd52dfe77841926e0c040f9f7dddc0f0f0`  
		Last Modified: Thu, 18 Jan 2024 19:12:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:37bebfbf6beb895866290411acff0181399392c5c183866a9e87401f7cd684aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb55c781ae994ee6e76ce636cf5f955bed026d5f0e0bd49dfc55a0d82f62d0b`

```dockerfile
```

-	Layers:
	-	`sha256:31bb008b7aafbd759a3fa9380e000dae562ab451a3e1d58536f6970a7a0143f7`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 3.0 MB (2961717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba11b86dd2b34fc3915f6674753aec5fb824e4d197d0cc02bd4686afbf7b8520`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 31.1 KB (31113 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:0d26b2cbf4849059183c4054430f1704cdf131b9404786e233ed05f93ef6f906
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:de9cbe483c7c245917bdec70c15e04987cb674a450acc5d8613cd24daf243b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79645282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0770734989b23f20f21098a6fdabfd044a122d245dc0769e8bd168d04935fb3f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:08cfc7bf77cc2291c96890f44a435216cb1168c45cef77f7801430982c43ca58 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4648efdf070b378f12737b5cdacaded7b6294f27d0a0c1fb33849090813e920a`  
		Last Modified: Thu, 11 Jan 2024 02:43:48 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb6114e35cc47d594428e5f313019f5680a4ea4bdf497280303fd379114210d`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06982f2aa7fb16db4a7a41a1a2ca567b88e21545355e10853dd03aac5ada25ba`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 6.7 MB (6703446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d86f7417a3bbd39e87d4e1160473b3d1b6c6f6f11dc821a1ff5b0892b09e661`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 1.0 MB (1046497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c59d5b797cf73da5593b5a9c071ff024c1171545fc317d3524f275c47b950`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 80.3 KB (80333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8ee01dd96bf0469ad6e0788c30e7ddf3f4e20dcc61c723ce67c41b1b6b8151`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7549f8782da3e7ebe160d3f5b152fd6bbed2e063ea60daecd2a1791f92514d1b`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 44.6 MB (44619863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964033ec3b765dd82f9ff0c0f0c1ac302dd62c7501fc6435fd7f71b11c5bfff3`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5925746de937aeccb49187240ad489d272da916d1bb5bd3a1cb3cfafc2a1d095`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603f2136df0b84f0e123cf41ee8e67475369272ab665ea74ba6dc38849092558`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82812fa3b9a495a112f666242ea73b275bc3ca44295f7042a9df9ca337d881f9`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:79f04e08934f4b645065cf55f0bea365a099a889cad1b8cff0087141d2f0539e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e133c21cdf015e1400a809175debc983b34b751b82da3aa06e27a98152e36b80`

```dockerfile
```

-	Layers:
	-	`sha256:f7d91b3825a2c6ab1db062190f7912303b7187f4d5defaefbe4f649d3fb90fdf`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 3.0 MB (2955438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a4109360b17ccf4983bec0f870b9b85b0c482f7facfccc5a53b601292551b1d`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 31.3 KB (31282 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:32680bbc86000b0fb9391c9027b93549403acee5a9ab14a55db236031dddd0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74709870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d207dab7a7f74e6977129cdedf63b0b8fb5c2ddda0b6abbe61c1e170ed93f05`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:0d7c08c3a192fbaded92a14e5eed44f5df7d00cd932ed45984ebb6b6e21446a6 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d982983796daa327ca72ca687e0d8417bb909e8256d666725dae5ad846525ae`  
		Last Modified: Thu, 11 Jan 2024 02:45:24 GMT  
		Size: 26.0 MB (25969811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1a78c86ecb35f073675b605f5f2dd61790d9d6ffd96d4ef99d760d11ad9ea9`  
		Last Modified: Thu, 18 Jan 2024 19:12:38 GMT  
		Size: 3.4 KB (3358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b0c5f7a37982b6c363bff53d5c764cb626dd47b9a0dd86f0234d32829f0dbb`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 6.6 MB (6576629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c78b8447e56be5eba47240e31cc278ac9daced65b046b58f941220a3d5220a2`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 951.3 KB (951324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd91ad113f4e6f2f1b2cb79413ec3af11db742705bd49879b6aad79e5cbd6637`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 80.2 KB (80196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f85c71d610a52c7ae3e45b20d2a2015258efe431927e3564f494285183b17c7`  
		Last Modified: Thu, 18 Jan 2024 19:12:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12eff63a21967f2630eb4910f9b18d73f9323de7ba3c6d6549c3cf5aa51ab2d6`  
		Last Modified: Thu, 18 Jan 2024 19:12:41 GMT  
		Size: 41.1 MB (41124960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0797bb13160151e8025b57a37c5aead92b5f471dc8a483fc17391583ea13e7`  
		Last Modified: Thu, 18 Jan 2024 19:12:40 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0bc64833607e2198e0c09b5d61797096a72133b65ec67e57889817c86d1d9a`  
		Last Modified: Thu, 18 Jan 2024 19:12:41 GMT  
		Size: 763.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee52ebd6aa7d68170c137e56e42242b7fe9e59056b06d39ae470d548e5583976`  
		Last Modified: Thu, 18 Jan 2024 19:12:41 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c2957b74be48e9851a04cfe55880bd52dfe77841926e0c040f9f7dddc0f0f0`  
		Last Modified: Thu, 18 Jan 2024 19:12:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:37bebfbf6beb895866290411acff0181399392c5c183866a9e87401f7cd684aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb55c781ae994ee6e76ce636cf5f955bed026d5f0e0bd49dfc55a0d82f62d0b`

```dockerfile
```

-	Layers:
	-	`sha256:31bb008b7aafbd759a3fa9380e000dae562ab451a3e1d58536f6970a7a0143f7`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 3.0 MB (2961717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba11b86dd2b34fc3915f6674753aec5fb824e4d197d0cc02bd4686afbf7b8520`  
		Last Modified: Thu, 18 Jan 2024 19:12:39 GMT  
		Size: 31.1 KB (31113 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:f440274b3e400cce09b83187bba793bc55542a9f1b3f01a3df16afefd7125730
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:b9abdb65f04c2ebcef331350e83d26b0c742def00f989cc5f3733c568dbce0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89105417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39e9553df1b89e97e32f1ee133d49e14c5234407d1593e697756b2dc5f4bd29`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.2.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e0331244baba07caa6e943b6f25ac97835c2350bcca983e3d7500827fefa4f`  
		Last Modified: Thu, 18 Jan 2024 18:13:24 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae9efdee466742e5b8cb4d7d3dfc7b4f506fb3329e934115ef677178926c29c`  
		Last Modified: Thu, 18 Jan 2024 18:13:24 GMT  
		Size: 5.0 MB (5019722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e735f5a8db169bbdb9ce5eb6b63aba90bec8924922d6cdb3360ca9c515d75aa0`  
		Last Modified: Thu, 18 Jan 2024 18:13:24 GMT  
		Size: 394.3 KB (394335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e72cfc2e0701a06b14df4c422ba99c3ca27e60a127b180672ee9fe6fb020de5`  
		Last Modified: Thu, 18 Jan 2024 18:13:24 GMT  
		Size: 77.9 KB (77879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f2491314ac95b937e12901839896496f172581a65800ba9d2fdaad8374a71f`  
		Last Modified: Thu, 18 Jan 2024 18:13:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec519a69dc22f40ba53543780617f7d57b26f31ecc3f11eb1b4973303b2a08`  
		Last Modified: Thu, 18 Jan 2024 18:13:26 GMT  
		Size: 52.2 MB (52188190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefe382e55bdb034535517d8e5481909e1df93ffc5e6708090683fbd12591eb5`  
		Last Modified: Thu, 18 Jan 2024 18:13:25 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa22227a300687bbc9645ddc7e6d9d7693bdbe16ef628b7c89c2451dd0601a`  
		Last Modified: Thu, 18 Jan 2024 18:13:25 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53805bc2e788700f93cc7ac408b7ee9ea4f0d06191b6f47cd705de2c24118ea`  
		Last Modified: Thu, 18 Jan 2024 18:13:26 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63a090bcdc4f2ce665ba06bc2bd161ba3ff94422c887ac65a9d1cf37ddde94f`  
		Last Modified: Thu, 18 Jan 2024 18:13:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:f8881ac1b11842300f23415a00ce048da990044bde0d685ad118fedb44f10d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57ad40d68b422ee3d06e73fcce0b9bd4577784db201955cd1964bcea608e0ef`

```dockerfile
```

-	Layers:
	-	`sha256:b591b5abb88f6c3e3f414dc6c011d2d957e83f19370737b6f93452bb8037d1e6`  
		Last Modified: Thu, 18 Jan 2024 18:13:24 GMT  
		Size: 3.3 MB (3270855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c8b8d335936cc7d8f1c0a1b9703f3460369a0a755a8dec97b22371cff450d2`  
		Last Modified: Thu, 18 Jan 2024 18:13:25 GMT  
		Size: 31.1 KB (31136 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.2.3`

```console
$ docker pull couchdb@sha256:f440274b3e400cce09b83187bba793bc55542a9f1b3f01a3df16afefd7125730
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchdb:3.2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:b9abdb65f04c2ebcef331350e83d26b0c742def00f989cc5f3733c568dbce0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89105417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39e9553df1b89e97e32f1ee133d49e14c5234407d1593e697756b2dc5f4bd29`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.2.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e0331244baba07caa6e943b6f25ac97835c2350bcca983e3d7500827fefa4f`  
		Last Modified: Thu, 18 Jan 2024 18:13:24 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae9efdee466742e5b8cb4d7d3dfc7b4f506fb3329e934115ef677178926c29c`  
		Last Modified: Thu, 18 Jan 2024 18:13:24 GMT  
		Size: 5.0 MB (5019722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e735f5a8db169bbdb9ce5eb6b63aba90bec8924922d6cdb3360ca9c515d75aa0`  
		Last Modified: Thu, 18 Jan 2024 18:13:24 GMT  
		Size: 394.3 KB (394335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e72cfc2e0701a06b14df4c422ba99c3ca27e60a127b180672ee9fe6fb020de5`  
		Last Modified: Thu, 18 Jan 2024 18:13:24 GMT  
		Size: 77.9 KB (77879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f2491314ac95b937e12901839896496f172581a65800ba9d2fdaad8374a71f`  
		Last Modified: Thu, 18 Jan 2024 18:13:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec519a69dc22f40ba53543780617f7d57b26f31ecc3f11eb1b4973303b2a08`  
		Last Modified: Thu, 18 Jan 2024 18:13:26 GMT  
		Size: 52.2 MB (52188190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefe382e55bdb034535517d8e5481909e1df93ffc5e6708090683fbd12591eb5`  
		Last Modified: Thu, 18 Jan 2024 18:13:25 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa22227a300687bbc9645ddc7e6d9d7693bdbe16ef628b7c89c2451dd0601a`  
		Last Modified: Thu, 18 Jan 2024 18:13:25 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53805bc2e788700f93cc7ac408b7ee9ea4f0d06191b6f47cd705de2c24118ea`  
		Last Modified: Thu, 18 Jan 2024 18:13:26 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63a090bcdc4f2ce665ba06bc2bd161ba3ff94422c887ac65a9d1cf37ddde94f`  
		Last Modified: Thu, 18 Jan 2024 18:13:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f8881ac1b11842300f23415a00ce048da990044bde0d685ad118fedb44f10d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57ad40d68b422ee3d06e73fcce0b9bd4577784db201955cd1964bcea608e0ef`

```dockerfile
```

-	Layers:
	-	`sha256:b591b5abb88f6c3e3f414dc6c011d2d957e83f19370737b6f93452bb8037d1e6`  
		Last Modified: Thu, 18 Jan 2024 18:13:24 GMT  
		Size: 3.3 MB (3270855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c8b8d335936cc7d8f1c0a1b9703f3460369a0a755a8dec97b22371cff450d2`  
		Last Modified: Thu, 18 Jan 2024 18:13:25 GMT  
		Size: 31.1 KB (31136 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:3ca831841dae6f661cdcfd4b0f9a35627178c27732a5b00857162cb68cc1a28d
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
$ docker pull couchdb@sha256:a6c2351fd35c463193f0775991f4619a8000a84cdd2bc8ef552ff65a9d116df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89638790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9602933014c5907bb2c8d43f726ed2373622f8c0636987af9bcf3a5f0c79ead`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5f63586ac0fd7679f03a38b2bb6a95b5b75f1dc39c4be0897995a04354db23`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4806581c93b54f52f0b08bb9dbf6d9d326c88930b406a7340af980bc8f768270`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 5.0 MB (5019733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8f182d248e8eaf090954e8c4852ae2a0dcc21d852c8909bcecfdc5be738992`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 394.4 KB (394350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c4e895eead2d5f1e750f0915735d88b7667d6dd91c9edfc2334c140def3da`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 77.9 KB (77870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096d0e49d7a91d8cb75a1416348c016174dc79b1d944f1aefd3fe7f5aba5230`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d050a15c1a57401d120413f3ef0c681d54def3ed9a00dec7fdacd1698f4dc2`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 52.7 MB (52721308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b5fe326ea02bda341bf09015da4158d57f825cc1eb45082d12249fa347fb7a`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf986debded9719af265c501f61e0191c50cbc0e285df8be650fbfe38f1dbf7`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f414ac70ae0c0a9bcdc3890668a92b5dd82f1c92125e60c18d68b0bb0c892c`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82812fa3b9a495a112f666242ea73b275bc3ca44295f7042a9df9ca337d881f9`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:25b4add69ad04ff48680e2b9a2f87ec8666d4b15013557e6d70e95f42907f839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95af21f1234feac3e769f41cbef67f3b28b8cecc2953e23304c5ec1f97a78d84`

```dockerfile
```

-	Layers:
	-	`sha256:902746ba0194033a33e5ccb12ab54639988083f18616bcd90a05561fc90787a0`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 3.3 MB (3295838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ba05299961375fbd390d8a9ffac7f36f8f3acb1bc24ef7f7cdd7caf76fbf7d`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:645eeba853b353a0880afe246a9c08f11b1db9f7069aeec06e86633c2ae7a9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88077003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ab4f86a454f930c5293207c881dc8a9a96504724631385596bb3fe22c6dad4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a59ba3e4f10a55c45f29d6706897bd99a03fcaf39b5fdca85dd7be539e43c4a`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 3.4 KB (3355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c1775ae673f1913d1b34db47129dd8496cf0c5b1e40754a379d344a4c39af9`  
		Last Modified: Thu, 18 Jan 2024 18:25:47 GMT  
		Size: 5.0 MB (5004083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db7ed076b4ca27f58fc0f25577270f4784e64c11783598b3447334756a7779a`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 350.5 KB (350533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d463fb07f7e8316a5f2ff4ced677b570c6e35870ff4e409ac92bc4965a8ca72`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 77.8 KB (77791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a0230918a06cce0cd48841eae3f8a3948f2822e949ae3f0e9a378d17f18ea0`  
		Last Modified: Thu, 18 Jan 2024 18:25:47 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e444d5a50d45faf9749ade5ba735be01f3ed499cfdadd0083713f79fd2719513`  
		Last Modified: Thu, 18 Jan 2024 18:25:49 GMT  
		Size: 52.6 MB (52572987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be04144325a578fe50a679412704b79165f2a03e9a5693f1a724f4cfa0b882d`  
		Last Modified: Thu, 18 Jan 2024 18:25:48 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658861fcf6e0a38fc7bc201bb87e65e3521683c5415d1d9b480ef0207b7c8a2`  
		Last Modified: Thu, 18 Jan 2024 18:25:48 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b7fa5576f4c549e826842527c9401ed1ed95f7a44a766d8aa31a85b6931893`  
		Last Modified: Thu, 18 Jan 2024 18:25:48 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fedb07453eabd9d0f541818e94dbc959d77c0ccca43d01efaef77db9a810c1`  
		Last Modified: Thu, 18 Jan 2024 18:25:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:5104a467f3b1d97bb1a4f02854ba2d4cddbed1e64d7a583a198fe20afa95915e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7fc37d6f1794004d31cafd9e41af529e6de349b4b6fc50d14ca3fa4aff4b25`

```dockerfile
```

-	Layers:
	-	`sha256:f66a91149ebc7c01c27ec52709522562e643f3f55a0cd67c928be24c0c53aa83`  
		Last Modified: Thu, 18 Jan 2024 18:25:47 GMT  
		Size: 3.3 MB (3296186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:397620cb518bf7fc4324e5cbc9c845fada5a8c67f905a0b08d8d59d05a4359f6`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 31.6 KB (31567 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:69e7bb7b08288d2ad5911d2f90d65624190641c3188be1498a659141b0a5f4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95365643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f15f1c43a1f277b35e33720b083578bf215588d35b14d6ae1a9426b2dfdb7b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6db52a5975ca141a51329334ae6e88c2292f71fbe05afc650101f9bea065e1f`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcc670e3b076d9245550182fc3f3f3e631c7ac042318dd344de58958ee36742`  
		Last Modified: Thu, 18 Jan 2024 18:41:04 GMT  
		Size: 5.8 MB (5839115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a6131d377e41d04166cbc404c9dea6eec8cff82017ff069298da8f447d197a`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 446.6 KB (446615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6c69adbbae2aa46ee77b6c8b440605e979556f85d5165a5c0671d9294357d4`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 77.8 KB (77831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8597146addb9ce87cdad5becbc50b3cf679a7afad871f3bbedbbfedf7bc71`  
		Last Modified: Thu, 18 Jan 2024 18:41:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522d544c2f0e982c8450228e8729faa2978db225d6f3680ee651c397432c93d`  
		Last Modified: Thu, 18 Jan 2024 18:41:07 GMT  
		Size: 53.7 MB (53700703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8dec663e5b1342f77a30a21ca3ad1660da2c0bd3cf28c65e0839f15fa66f20`  
		Last Modified: Thu, 18 Jan 2024 18:41:05 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3aa75c81e4c5e24b7098f1af4d33744e7c5c6286ec9dbaff87d3338dfb42ea0`  
		Last Modified: Thu, 18 Jan 2024 18:41:05 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95be43deb43b89954226ebe9598871a99c6294dce06dede85e7cd071991d0eb`  
		Last Modified: Thu, 18 Jan 2024 18:41:05 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6852b878032a76a59c61188b08d5e6085737e5fe384499aea66023b3165212`  
		Last Modified: Thu, 18 Jan 2024 18:41:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c6165efd2f26ab15ecc1a84a49cd156b01d04fcecd3ac87fcf1b49d668840d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3332087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389ec486b9fd5b339adbc5000265bbee7b701a55606d3b6f5d2a515f2e3b6691`

```dockerfile
```

-	Layers:
	-	`sha256:759287d64d2b8f87e3dbb8b0cf81b5ff2b9ea816e0fa9792c86d869e2725b592`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 3.3 MB (3300478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ff5c5acfdeab6765e9dade4462fde43947f3c41d62167e7349ff8153048087`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:0d78ccfcf452ca412da28e0fd29aaebbf4e0f9eb4e30ecf0b7cbf591799726e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86381115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c8e8d518db5442bf3e62da8a24c4b159ca471fc335ef646c9a640290e22454`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:77a92d4e9397475a6c68f4341baba607a7c875bc6e252de3e096482dd074f8ca in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a8470cec8ee9510bf45556c756635d84eb3cbc0220b52812522196008c6b0d3e`  
		Last Modified: Thu, 11 Jan 2024 01:51:19 GMT  
		Size: 29.7 MB (29656884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be83499ba256778626ad82f9fccd7164e71be3760487161f2ed4d8507339692`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 3.4 KB (3352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae10b9b22721e18b6fa8df8d8dd9b1e9c78450f802ede4945cb1291205404de7`  
		Last Modified: Sat, 20 Jan 2024 18:54:09 GMT  
		Size: 4.9 MB (4905513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98262054a3abcb8a53517cc3e83057413c0aed04cb6d3d9c01b1d4bab3aa7b17`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 357.5 KB (357466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ad4715d6dd594ec2fd231a01d4017944e79879f474a94611d9402cace0df73`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 77.8 KB (77815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adec8571498762cf768831b0cdd0a5bf0e976b2a65a3a2ca10c8c94d3c154f59`  
		Last Modified: Sat, 20 Jan 2024 18:54:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81435e5bf59142d2023bb566129cb197c3d9644728fbbdbc39558f7a99c14427`  
		Last Modified: Sat, 20 Jan 2024 18:54:11 GMT  
		Size: 51.4 MB (51375834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c05edc71f5f7e520e935527c545ced5d546770663df032718e8eaab4301b0e`  
		Last Modified: Sat, 20 Jan 2024 18:54:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d54553bef03697146cbc479a5b24465b84fecc5f4187ceed5f72be7be018bd`  
		Last Modified: Sat, 20 Jan 2024 18:54:10 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484cedac62572daea8476c4c881b70ddb5e8e6211414dd2769810b5a949eedd3`  
		Last Modified: Sat, 20 Jan 2024 18:54:10 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a73c8e6f40ec927189debd9f02f1a3500f41b84edc74f26cce60b557a22d9a`  
		Last Modified: Sat, 20 Jan 2024 18:54:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f1e2d4155a5990898279fa057614ee5f8fa2ac3d36230b49ee07fa64471c02ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3326969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b70b216f828433cdd3a051826187f1a45fcbb515efd5029491687c8f6e0fe45`

```dockerfile
```

-	Layers:
	-	`sha256:5b0775950ac0345039827bfc393978f41c5d432f6b455b6905759b7bbd15c040`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 3.3 MB (3295410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d863f59b35bd9fd762688e0c8db88852580209ab63f5fd73a0e31e48a048a7`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 31.6 KB (31559 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:3ca831841dae6f661cdcfd4b0f9a35627178c27732a5b00857162cb68cc1a28d
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
$ docker pull couchdb@sha256:a6c2351fd35c463193f0775991f4619a8000a84cdd2bc8ef552ff65a9d116df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89638790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9602933014c5907bb2c8d43f726ed2373622f8c0636987af9bcf3a5f0c79ead`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5f63586ac0fd7679f03a38b2bb6a95b5b75f1dc39c4be0897995a04354db23`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4806581c93b54f52f0b08bb9dbf6d9d326c88930b406a7340af980bc8f768270`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 5.0 MB (5019733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8f182d248e8eaf090954e8c4852ae2a0dcc21d852c8909bcecfdc5be738992`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 394.4 KB (394350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c4e895eead2d5f1e750f0915735d88b7667d6dd91c9edfc2334c140def3da`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 77.9 KB (77870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096d0e49d7a91d8cb75a1416348c016174dc79b1d944f1aefd3fe7f5aba5230`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d050a15c1a57401d120413f3ef0c681d54def3ed9a00dec7fdacd1698f4dc2`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 52.7 MB (52721308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b5fe326ea02bda341bf09015da4158d57f825cc1eb45082d12249fa347fb7a`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf986debded9719af265c501f61e0191c50cbc0e285df8be650fbfe38f1dbf7`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f414ac70ae0c0a9bcdc3890668a92b5dd82f1c92125e60c18d68b0bb0c892c`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82812fa3b9a495a112f666242ea73b275bc3ca44295f7042a9df9ca337d881f9`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:25b4add69ad04ff48680e2b9a2f87ec8666d4b15013557e6d70e95f42907f839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95af21f1234feac3e769f41cbef67f3b28b8cecc2953e23304c5ec1f97a78d84`

```dockerfile
```

-	Layers:
	-	`sha256:902746ba0194033a33e5ccb12ab54639988083f18616bcd90a05561fc90787a0`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 3.3 MB (3295838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ba05299961375fbd390d8a9ffac7f36f8f3acb1bc24ef7f7cdd7caf76fbf7d`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:645eeba853b353a0880afe246a9c08f11b1db9f7069aeec06e86633c2ae7a9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88077003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ab4f86a454f930c5293207c881dc8a9a96504724631385596bb3fe22c6dad4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a59ba3e4f10a55c45f29d6706897bd99a03fcaf39b5fdca85dd7be539e43c4a`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 3.4 KB (3355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c1775ae673f1913d1b34db47129dd8496cf0c5b1e40754a379d344a4c39af9`  
		Last Modified: Thu, 18 Jan 2024 18:25:47 GMT  
		Size: 5.0 MB (5004083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db7ed076b4ca27f58fc0f25577270f4784e64c11783598b3447334756a7779a`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 350.5 KB (350533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d463fb07f7e8316a5f2ff4ced677b570c6e35870ff4e409ac92bc4965a8ca72`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 77.8 KB (77791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a0230918a06cce0cd48841eae3f8a3948f2822e949ae3f0e9a378d17f18ea0`  
		Last Modified: Thu, 18 Jan 2024 18:25:47 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e444d5a50d45faf9749ade5ba735be01f3ed499cfdadd0083713f79fd2719513`  
		Last Modified: Thu, 18 Jan 2024 18:25:49 GMT  
		Size: 52.6 MB (52572987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be04144325a578fe50a679412704b79165f2a03e9a5693f1a724f4cfa0b882d`  
		Last Modified: Thu, 18 Jan 2024 18:25:48 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658861fcf6e0a38fc7bc201bb87e65e3521683c5415d1d9b480ef0207b7c8a2`  
		Last Modified: Thu, 18 Jan 2024 18:25:48 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b7fa5576f4c549e826842527c9401ed1ed95f7a44a766d8aa31a85b6931893`  
		Last Modified: Thu, 18 Jan 2024 18:25:48 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fedb07453eabd9d0f541818e94dbc959d77c0ccca43d01efaef77db9a810c1`  
		Last Modified: Thu, 18 Jan 2024 18:25:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:5104a467f3b1d97bb1a4f02854ba2d4cddbed1e64d7a583a198fe20afa95915e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7fc37d6f1794004d31cafd9e41af529e6de349b4b6fc50d14ca3fa4aff4b25`

```dockerfile
```

-	Layers:
	-	`sha256:f66a91149ebc7c01c27ec52709522562e643f3f55a0cd67c928be24c0c53aa83`  
		Last Modified: Thu, 18 Jan 2024 18:25:47 GMT  
		Size: 3.3 MB (3296186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:397620cb518bf7fc4324e5cbc9c845fada5a8c67f905a0b08d8d59d05a4359f6`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 31.6 KB (31567 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:69e7bb7b08288d2ad5911d2f90d65624190641c3188be1498a659141b0a5f4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95365643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f15f1c43a1f277b35e33720b083578bf215588d35b14d6ae1a9426b2dfdb7b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6db52a5975ca141a51329334ae6e88c2292f71fbe05afc650101f9bea065e1f`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcc670e3b076d9245550182fc3f3f3e631c7ac042318dd344de58958ee36742`  
		Last Modified: Thu, 18 Jan 2024 18:41:04 GMT  
		Size: 5.8 MB (5839115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a6131d377e41d04166cbc404c9dea6eec8cff82017ff069298da8f447d197a`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 446.6 KB (446615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6c69adbbae2aa46ee77b6c8b440605e979556f85d5165a5c0671d9294357d4`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 77.8 KB (77831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8597146addb9ce87cdad5becbc50b3cf679a7afad871f3bbedbbfedf7bc71`  
		Last Modified: Thu, 18 Jan 2024 18:41:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522d544c2f0e982c8450228e8729faa2978db225d6f3680ee651c397432c93d`  
		Last Modified: Thu, 18 Jan 2024 18:41:07 GMT  
		Size: 53.7 MB (53700703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8dec663e5b1342f77a30a21ca3ad1660da2c0bd3cf28c65e0839f15fa66f20`  
		Last Modified: Thu, 18 Jan 2024 18:41:05 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3aa75c81e4c5e24b7098f1af4d33744e7c5c6286ec9dbaff87d3338dfb42ea0`  
		Last Modified: Thu, 18 Jan 2024 18:41:05 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95be43deb43b89954226ebe9598871a99c6294dce06dede85e7cd071991d0eb`  
		Last Modified: Thu, 18 Jan 2024 18:41:05 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6852b878032a76a59c61188b08d5e6085737e5fe384499aea66023b3165212`  
		Last Modified: Thu, 18 Jan 2024 18:41:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c6165efd2f26ab15ecc1a84a49cd156b01d04fcecd3ac87fcf1b49d668840d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3332087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389ec486b9fd5b339adbc5000265bbee7b701a55606d3b6f5d2a515f2e3b6691`

```dockerfile
```

-	Layers:
	-	`sha256:759287d64d2b8f87e3dbb8b0cf81b5ff2b9ea816e0fa9792c86d869e2725b592`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 3.3 MB (3300478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ff5c5acfdeab6765e9dade4462fde43947f3c41d62167e7349ff8153048087`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:0d78ccfcf452ca412da28e0fd29aaebbf4e0f9eb4e30ecf0b7cbf591799726e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86381115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c8e8d518db5442bf3e62da8a24c4b159ca471fc335ef646c9a640290e22454`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:77a92d4e9397475a6c68f4341baba607a7c875bc6e252de3e096482dd074f8ca in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a8470cec8ee9510bf45556c756635d84eb3cbc0220b52812522196008c6b0d3e`  
		Last Modified: Thu, 11 Jan 2024 01:51:19 GMT  
		Size: 29.7 MB (29656884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be83499ba256778626ad82f9fccd7164e71be3760487161f2ed4d8507339692`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 3.4 KB (3352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae10b9b22721e18b6fa8df8d8dd9b1e9c78450f802ede4945cb1291205404de7`  
		Last Modified: Sat, 20 Jan 2024 18:54:09 GMT  
		Size: 4.9 MB (4905513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98262054a3abcb8a53517cc3e83057413c0aed04cb6d3d9c01b1d4bab3aa7b17`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 357.5 KB (357466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ad4715d6dd594ec2fd231a01d4017944e79879f474a94611d9402cace0df73`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 77.8 KB (77815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adec8571498762cf768831b0cdd0a5bf0e976b2a65a3a2ca10c8c94d3c154f59`  
		Last Modified: Sat, 20 Jan 2024 18:54:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81435e5bf59142d2023bb566129cb197c3d9644728fbbdbc39558f7a99c14427`  
		Last Modified: Sat, 20 Jan 2024 18:54:11 GMT  
		Size: 51.4 MB (51375834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c05edc71f5f7e520e935527c545ced5d546770663df032718e8eaab4301b0e`  
		Last Modified: Sat, 20 Jan 2024 18:54:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d54553bef03697146cbc479a5b24465b84fecc5f4187ceed5f72be7be018bd`  
		Last Modified: Sat, 20 Jan 2024 18:54:10 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484cedac62572daea8476c4c881b70ddb5e8e6211414dd2769810b5a949eedd3`  
		Last Modified: Sat, 20 Jan 2024 18:54:10 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a73c8e6f40ec927189debd9f02f1a3500f41b84edc74f26cce60b557a22d9a`  
		Last Modified: Sat, 20 Jan 2024 18:54:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f1e2d4155a5990898279fa057614ee5f8fa2ac3d36230b49ee07fa64471c02ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3326969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b70b216f828433cdd3a051826187f1a45fcbb515efd5029491687c8f6e0fe45`

```dockerfile
```

-	Layers:
	-	`sha256:5b0775950ac0345039827bfc393978f41c5d432f6b455b6905759b7bbd15c040`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 3.3 MB (3295410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d863f59b35bd9fd762688e0c8db88852580209ab63f5fd73a0e31e48a048a7`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 31.6 KB (31559 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:3ca831841dae6f661cdcfd4b0f9a35627178c27732a5b00857162cb68cc1a28d
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

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:a6c2351fd35c463193f0775991f4619a8000a84cdd2bc8ef552ff65a9d116df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89638790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9602933014c5907bb2c8d43f726ed2373622f8c0636987af9bcf3a5f0c79ead`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5f63586ac0fd7679f03a38b2bb6a95b5b75f1dc39c4be0897995a04354db23`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4806581c93b54f52f0b08bb9dbf6d9d326c88930b406a7340af980bc8f768270`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 5.0 MB (5019733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8f182d248e8eaf090954e8c4852ae2a0dcc21d852c8909bcecfdc5be738992`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 394.4 KB (394350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c4e895eead2d5f1e750f0915735d88b7667d6dd91c9edfc2334c140def3da`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 77.9 KB (77870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096d0e49d7a91d8cb75a1416348c016174dc79b1d944f1aefd3fe7f5aba5230`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d050a15c1a57401d120413f3ef0c681d54def3ed9a00dec7fdacd1698f4dc2`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 52.7 MB (52721308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b5fe326ea02bda341bf09015da4158d57f825cc1eb45082d12249fa347fb7a`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf986debded9719af265c501f61e0191c50cbc0e285df8be650fbfe38f1dbf7`  
		Last Modified: Thu, 18 Jan 2024 18:13:30 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f414ac70ae0c0a9bcdc3890668a92b5dd82f1c92125e60c18d68b0bb0c892c`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82812fa3b9a495a112f666242ea73b275bc3ca44295f7042a9df9ca337d881f9`  
		Last Modified: Thu, 18 Jan 2024 18:13:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:25b4add69ad04ff48680e2b9a2f87ec8666d4b15013557e6d70e95f42907f839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95af21f1234feac3e769f41cbef67f3b28b8cecc2953e23304c5ec1f97a78d84`

```dockerfile
```

-	Layers:
	-	`sha256:902746ba0194033a33e5ccb12ab54639988083f18616bcd90a05561fc90787a0`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 3.3 MB (3295838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ba05299961375fbd390d8a9ffac7f36f8f3acb1bc24ef7f7cdd7caf76fbf7d`  
		Last Modified: Thu, 18 Jan 2024 18:13:29 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:645eeba853b353a0880afe246a9c08f11b1db9f7069aeec06e86633c2ae7a9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88077003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ab4f86a454f930c5293207c881dc8a9a96504724631385596bb3fe22c6dad4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a59ba3e4f10a55c45f29d6706897bd99a03fcaf39b5fdca85dd7be539e43c4a`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 3.4 KB (3355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c1775ae673f1913d1b34db47129dd8496cf0c5b1e40754a379d344a4c39af9`  
		Last Modified: Thu, 18 Jan 2024 18:25:47 GMT  
		Size: 5.0 MB (5004083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db7ed076b4ca27f58fc0f25577270f4784e64c11783598b3447334756a7779a`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 350.5 KB (350533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d463fb07f7e8316a5f2ff4ced677b570c6e35870ff4e409ac92bc4965a8ca72`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 77.8 KB (77791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a0230918a06cce0cd48841eae3f8a3948f2822e949ae3f0e9a378d17f18ea0`  
		Last Modified: Thu, 18 Jan 2024 18:25:47 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e444d5a50d45faf9749ade5ba735be01f3ed499cfdadd0083713f79fd2719513`  
		Last Modified: Thu, 18 Jan 2024 18:25:49 GMT  
		Size: 52.6 MB (52572987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be04144325a578fe50a679412704b79165f2a03e9a5693f1a724f4cfa0b882d`  
		Last Modified: Thu, 18 Jan 2024 18:25:48 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658861fcf6e0a38fc7bc201bb87e65e3521683c5415d1d9b480ef0207b7c8a2`  
		Last Modified: Thu, 18 Jan 2024 18:25:48 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b7fa5576f4c549e826842527c9401ed1ed95f7a44a766d8aa31a85b6931893`  
		Last Modified: Thu, 18 Jan 2024 18:25:48 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fedb07453eabd9d0f541818e94dbc959d77c0ccca43d01efaef77db9a810c1`  
		Last Modified: Thu, 18 Jan 2024 18:25:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:5104a467f3b1d97bb1a4f02854ba2d4cddbed1e64d7a583a198fe20afa95915e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7fc37d6f1794004d31cafd9e41af529e6de349b4b6fc50d14ca3fa4aff4b25`

```dockerfile
```

-	Layers:
	-	`sha256:f66a91149ebc7c01c27ec52709522562e643f3f55a0cd67c928be24c0c53aa83`  
		Last Modified: Thu, 18 Jan 2024 18:25:47 GMT  
		Size: 3.3 MB (3296186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:397620cb518bf7fc4324e5cbc9c845fada5a8c67f905a0b08d8d59d05a4359f6`  
		Last Modified: Thu, 18 Jan 2024 18:25:46 GMT  
		Size: 31.6 KB (31567 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:69e7bb7b08288d2ad5911d2f90d65624190641c3188be1498a659141b0a5f4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95365643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f15f1c43a1f277b35e33720b083578bf215588d35b14d6ae1a9426b2dfdb7b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6db52a5975ca141a51329334ae6e88c2292f71fbe05afc650101f9bea065e1f`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcc670e3b076d9245550182fc3f3f3e631c7ac042318dd344de58958ee36742`  
		Last Modified: Thu, 18 Jan 2024 18:41:04 GMT  
		Size: 5.8 MB (5839115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a6131d377e41d04166cbc404c9dea6eec8cff82017ff069298da8f447d197a`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 446.6 KB (446615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6c69adbbae2aa46ee77b6c8b440605e979556f85d5165a5c0671d9294357d4`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 77.8 KB (77831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8597146addb9ce87cdad5becbc50b3cf679a7afad871f3bbedbbfedf7bc71`  
		Last Modified: Thu, 18 Jan 2024 18:41:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522d544c2f0e982c8450228e8729faa2978db225d6f3680ee651c397432c93d`  
		Last Modified: Thu, 18 Jan 2024 18:41:07 GMT  
		Size: 53.7 MB (53700703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8dec663e5b1342f77a30a21ca3ad1660da2c0bd3cf28c65e0839f15fa66f20`  
		Last Modified: Thu, 18 Jan 2024 18:41:05 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3aa75c81e4c5e24b7098f1af4d33744e7c5c6286ec9dbaff87d3338dfb42ea0`  
		Last Modified: Thu, 18 Jan 2024 18:41:05 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95be43deb43b89954226ebe9598871a99c6294dce06dede85e7cd071991d0eb`  
		Last Modified: Thu, 18 Jan 2024 18:41:05 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6852b878032a76a59c61188b08d5e6085737e5fe384499aea66023b3165212`  
		Last Modified: Thu, 18 Jan 2024 18:41:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:c6165efd2f26ab15ecc1a84a49cd156b01d04fcecd3ac87fcf1b49d668840d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3332087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389ec486b9fd5b339adbc5000265bbee7b701a55606d3b6f5d2a515f2e3b6691`

```dockerfile
```

-	Layers:
	-	`sha256:759287d64d2b8f87e3dbb8b0cf81b5ff2b9ea816e0fa9792c86d869e2725b592`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 3.3 MB (3300478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ff5c5acfdeab6765e9dade4462fde43947f3c41d62167e7349ff8153048087`  
		Last Modified: Thu, 18 Jan 2024 18:41:03 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:0d78ccfcf452ca412da28e0fd29aaebbf4e0f9eb4e30ecf0b7cbf591799726e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86381115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c8e8d518db5442bf3e62da8a24c4b159ca471fc335ef646c9a640290e22454`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:77a92d4e9397475a6c68f4341baba607a7c875bc6e252de3e096482dd074f8ca in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a8470cec8ee9510bf45556c756635d84eb3cbc0220b52812522196008c6b0d3e`  
		Last Modified: Thu, 11 Jan 2024 01:51:19 GMT  
		Size: 29.7 MB (29656884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be83499ba256778626ad82f9fccd7164e71be3760487161f2ed4d8507339692`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 3.4 KB (3352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae10b9b22721e18b6fa8df8d8dd9b1e9c78450f802ede4945cb1291205404de7`  
		Last Modified: Sat, 20 Jan 2024 18:54:09 GMT  
		Size: 4.9 MB (4905513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98262054a3abcb8a53517cc3e83057413c0aed04cb6d3d9c01b1d4bab3aa7b17`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 357.5 KB (357466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ad4715d6dd594ec2fd231a01d4017944e79879f474a94611d9402cace0df73`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 77.8 KB (77815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adec8571498762cf768831b0cdd0a5bf0e976b2a65a3a2ca10c8c94d3c154f59`  
		Last Modified: Sat, 20 Jan 2024 18:54:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81435e5bf59142d2023bb566129cb197c3d9644728fbbdbc39558f7a99c14427`  
		Last Modified: Sat, 20 Jan 2024 18:54:11 GMT  
		Size: 51.4 MB (51375834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c05edc71f5f7e520e935527c545ced5d546770663df032718e8eaab4301b0e`  
		Last Modified: Sat, 20 Jan 2024 18:54:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d54553bef03697146cbc479a5b24465b84fecc5f4187ceed5f72be7be018bd`  
		Last Modified: Sat, 20 Jan 2024 18:54:10 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484cedac62572daea8476c4c881b70ddb5e8e6211414dd2769810b5a949eedd3`  
		Last Modified: Sat, 20 Jan 2024 18:54:10 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a73c8e6f40ec927189debd9f02f1a3500f41b84edc74f26cce60b557a22d9a`  
		Last Modified: Sat, 20 Jan 2024 18:54:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:f1e2d4155a5990898279fa057614ee5f8fa2ac3d36230b49ee07fa64471c02ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3326969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b70b216f828433cdd3a051826187f1a45fcbb515efd5029491687c8f6e0fe45`

```dockerfile
```

-	Layers:
	-	`sha256:5b0775950ac0345039827bfc393978f41c5d432f6b455b6905759b7bbd15c040`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 3.3 MB (3295410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d863f59b35bd9fd762688e0c8db88852580209ab63f5fd73a0e31e48a048a7`  
		Last Modified: Sat, 20 Jan 2024 18:54:08 GMT  
		Size: 31.6 KB (31559 bytes)  
		MIME: application/vnd.in-toto+json
