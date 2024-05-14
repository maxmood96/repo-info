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
$ docker pull couchdb@sha256:9eb869e458626703352ad1c3cb1602da6903dcc92f8eccd53a5975bbe7926641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:9bdb01573635b4cd01fcc7b7ebcb91a6044d67d44cc11a6d5cb5fdcfac0d8197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84325786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741e2cfcf1994002ee8f9245bf9702083b584927a7dccaeba00fafb6e83e7824`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:ea1fe4f19165d885a1f3d523e0ebdcc3e863e6b93717c8022529edb674a52e2d in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:6299ae3fea5d052b297d91a57200563362b8f2c95358c6e3010d6fa3ed44e7c4`  
		Last Modified: Tue, 14 May 2024 01:33:45 GMT  
		Size: 27.3 MB (27337664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64995ff8a19be3b1538ca8c771cf87d328c3c5a3d0bc0e9d30ca79f1f7691020`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc93e0c57e240329ac976a785b58e90ffefc382dab2cc84fadf027b034c7569b`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 6.7 MB (6703201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d9965634f52b56d3565561137b0502717aa07e18cb50749bad82621896ab3a`  
		Last Modified: Tue, 14 May 2024 02:56:22 GMT  
		Size: 1.0 MB (1046493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1d69e804cc62a84fa4974458b330d883ceea0a8601ab75df7c72b47193e2d7`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 80.3 KB (80331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da90c3e7a6363a01fdebe43b09d54ae207c3edf603093dc11354a59830f1147`  
		Last Modified: Tue, 14 May 2024 02:56:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93544d8936b311f1c1c1acb6629bcf10ce47a289e03c4239fadca7c5e08f85e3`  
		Last Modified: Tue, 14 May 2024 02:56:23 GMT  
		Size: 49.2 MB (49151182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d9b1555e7055515e1825debda2d7b0421a8195eb69dbe6bc1884f00a603066`  
		Last Modified: Tue, 14 May 2024 02:56:22 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7184fd55e18b1bc05fc4997f38d206feea47b96788742e1ac079f6330e80c5`  
		Last Modified: Tue, 14 May 2024 02:56:22 GMT  
		Size: 761.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e348cb4a7fda11eab1fb68fbb978cd329e246aed8ad17904e7388e109062a2a2`  
		Last Modified: Tue, 14 May 2024 02:56:23 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948d16d1e515223e6503ae0351554f4bce89d433f39500c46d5c809d38d33eef`  
		Last Modified: Tue, 14 May 2024 02:56:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2` - unknown; unknown

```console
$ docker pull couchdb@sha256:c33e444f2196768c243f95cc127c881cb63134697be1bd4421180f70e2c01724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4470067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b4696a1f3e122241c9a3dbfd1169ffc3b9fa55171e76f0a9e431287ca91ffc`

```dockerfile
```

-	Layers:
	-	`sha256:b9ab6cbe1a9cb9596f866ef211c8bdde7258cb81ea218403abeb44811d5bcac6`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 4.4 MB (4438481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a092ac3bed2922138aaa76e68c5e01208e19694fc330fdd76f4ccb4d202f2d14`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 31.6 KB (31586 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0427a1b391a7a79bc7a71d8e653e1b057f2858efa54fe4ca33f89474b0b65819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72754682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d5a4bfe6da4508fd000e2a8d825415b11b5d635e90164662ed9c37651a00b7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bd84662eb5c566f361c169149ba683475c50ddc528270daf67d40c8e98ed12a7 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:57c62469eb2b8cb9a971714401ad24a78c171e2f6dab20314e1c5f0dab7a8639`  
		Last Modified: Wed, 24 Apr 2024 04:15:23 GMT  
		Size: 26.1 MB (26109830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420a3201a4f26b888ff27d75ebf5058fa178d5c5eaa591c34c3d78e9bb30c1e`  
		Last Modified: Wed, 24 Apr 2024 16:56:10 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730c01675a685b8c8377c245c4e5ebe2212ef31b76334d30f331d66060d45d39`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 6.6 MB (6576423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9928902a2afd882ed0192b334f236be8f74bf4334c6541b70b02347e8154f053`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 951.4 KB (951356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5944347da619792f62bead433ab612cd7d0714005e34a57430d843920461bb4c`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 80.2 KB (80183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6990feec48b73ca7c23fa9d8ce9713f258223ef2976e3f1edf97c950c64f6a41`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f00b2410daaa479c15e171e919facac382487e61dd1b382b4811adb03532f8`  
		Last Modified: Wed, 24 Apr 2024 17:16:53 GMT  
		Size: 39.0 MB (39029944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7e14d737c13d37152083872b21d4a61dbae26deb4480285f0e7d85d38d1965`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdb67dd6341985ecc381d3d4f4fc2c1c982874aa054261900aed809ce40b9de`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c80a24ac525d7ec75ce0db6d9efa6cf71bcc212651f09c305e797ab52f39d9`  
		Last Modified: Wed, 24 Apr 2024 17:16:52 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7761ef10106a1712390c18c07283cc37315454f5ac6d947699782a8d3fb356e6`  
		Last Modified: Wed, 24 Apr 2024 17:16:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2` - unknown; unknown

```console
$ docker pull couchdb@sha256:ffa185e0b42c866be20f772df803dc11e09b9a410ead792b51df2daaab0b5762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e29a55a6d863bc1021614a56a37957f78d8bcf027b5771b6e097adbf90a550`

```dockerfile
```

-	Layers:
	-	`sha256:2c05c22d4c2d7fec8b8ee20f327e5d27b6c1a7a7bcd80e4f28be0608c058a5ab`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 3.8 MB (3750111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff701624cf5b840e6fba6131a93d6e47d492b4765716a7d3d8baf7689e54f1d9`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 31.4 KB (31419 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:9eb869e458626703352ad1c3cb1602da6903dcc92f8eccd53a5975bbe7926641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:9bdb01573635b4cd01fcc7b7ebcb91a6044d67d44cc11a6d5cb5fdcfac0d8197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84325786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741e2cfcf1994002ee8f9245bf9702083b584927a7dccaeba00fafb6e83e7824`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:ea1fe4f19165d885a1f3d523e0ebdcc3e863e6b93717c8022529edb674a52e2d in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:6299ae3fea5d052b297d91a57200563362b8f2c95358c6e3010d6fa3ed44e7c4`  
		Last Modified: Tue, 14 May 2024 01:33:45 GMT  
		Size: 27.3 MB (27337664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64995ff8a19be3b1538ca8c771cf87d328c3c5a3d0bc0e9d30ca79f1f7691020`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc93e0c57e240329ac976a785b58e90ffefc382dab2cc84fadf027b034c7569b`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 6.7 MB (6703201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d9965634f52b56d3565561137b0502717aa07e18cb50749bad82621896ab3a`  
		Last Modified: Tue, 14 May 2024 02:56:22 GMT  
		Size: 1.0 MB (1046493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1d69e804cc62a84fa4974458b330d883ceea0a8601ab75df7c72b47193e2d7`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 80.3 KB (80331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da90c3e7a6363a01fdebe43b09d54ae207c3edf603093dc11354a59830f1147`  
		Last Modified: Tue, 14 May 2024 02:56:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93544d8936b311f1c1c1acb6629bcf10ce47a289e03c4239fadca7c5e08f85e3`  
		Last Modified: Tue, 14 May 2024 02:56:23 GMT  
		Size: 49.2 MB (49151182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d9b1555e7055515e1825debda2d7b0421a8195eb69dbe6bc1884f00a603066`  
		Last Modified: Tue, 14 May 2024 02:56:22 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7184fd55e18b1bc05fc4997f38d206feea47b96788742e1ac079f6330e80c5`  
		Last Modified: Tue, 14 May 2024 02:56:22 GMT  
		Size: 761.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e348cb4a7fda11eab1fb68fbb978cd329e246aed8ad17904e7388e109062a2a2`  
		Last Modified: Tue, 14 May 2024 02:56:23 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948d16d1e515223e6503ae0351554f4bce89d433f39500c46d5c809d38d33eef`  
		Last Modified: Tue, 14 May 2024 02:56:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c33e444f2196768c243f95cc127c881cb63134697be1bd4421180f70e2c01724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4470067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b4696a1f3e122241c9a3dbfd1169ffc3b9fa55171e76f0a9e431287ca91ffc`

```dockerfile
```

-	Layers:
	-	`sha256:b9ab6cbe1a9cb9596f866ef211c8bdde7258cb81ea218403abeb44811d5bcac6`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 4.4 MB (4438481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a092ac3bed2922138aaa76e68c5e01208e19694fc330fdd76f4ccb4d202f2d14`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 31.6 KB (31586 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0427a1b391a7a79bc7a71d8e653e1b057f2858efa54fe4ca33f89474b0b65819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72754682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d5a4bfe6da4508fd000e2a8d825415b11b5d635e90164662ed9c37651a00b7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bd84662eb5c566f361c169149ba683475c50ddc528270daf67d40c8e98ed12a7 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:57c62469eb2b8cb9a971714401ad24a78c171e2f6dab20314e1c5f0dab7a8639`  
		Last Modified: Wed, 24 Apr 2024 04:15:23 GMT  
		Size: 26.1 MB (26109830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420a3201a4f26b888ff27d75ebf5058fa178d5c5eaa591c34c3d78e9bb30c1e`  
		Last Modified: Wed, 24 Apr 2024 16:56:10 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730c01675a685b8c8377c245c4e5ebe2212ef31b76334d30f331d66060d45d39`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 6.6 MB (6576423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9928902a2afd882ed0192b334f236be8f74bf4334c6541b70b02347e8154f053`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 951.4 KB (951356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5944347da619792f62bead433ab612cd7d0714005e34a57430d843920461bb4c`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 80.2 KB (80183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6990feec48b73ca7c23fa9d8ce9713f258223ef2976e3f1edf97c950c64f6a41`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f00b2410daaa479c15e171e919facac382487e61dd1b382b4811adb03532f8`  
		Last Modified: Wed, 24 Apr 2024 17:16:53 GMT  
		Size: 39.0 MB (39029944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7e14d737c13d37152083872b21d4a61dbae26deb4480285f0e7d85d38d1965`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdb67dd6341985ecc381d3d4f4fc2c1c982874aa054261900aed809ce40b9de`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c80a24ac525d7ec75ce0db6d9efa6cf71bcc212651f09c305e797ab52f39d9`  
		Last Modified: Wed, 24 Apr 2024 17:16:52 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7761ef10106a1712390c18c07283cc37315454f5ac6d947699782a8d3fb356e6`  
		Last Modified: Wed, 24 Apr 2024 17:16:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ffa185e0b42c866be20f772df803dc11e09b9a410ead792b51df2daaab0b5762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e29a55a6d863bc1021614a56a37957f78d8bcf027b5771b6e097adbf90a550`

```dockerfile
```

-	Layers:
	-	`sha256:2c05c22d4c2d7fec8b8ee20f327e5d27b6c1a7a7bcd80e4f28be0608c058a5ab`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 3.8 MB (3750111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff701624cf5b840e6fba6131a93d6e47d492b4765716a7d3d8baf7689e54f1d9`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 31.4 KB (31419 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:9eb869e458626703352ad1c3cb1602da6903dcc92f8eccd53a5975bbe7926641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:9bdb01573635b4cd01fcc7b7ebcb91a6044d67d44cc11a6d5cb5fdcfac0d8197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84325786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741e2cfcf1994002ee8f9245bf9702083b584927a7dccaeba00fafb6e83e7824`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:ea1fe4f19165d885a1f3d523e0ebdcc3e863e6b93717c8022529edb674a52e2d in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:6299ae3fea5d052b297d91a57200563362b8f2c95358c6e3010d6fa3ed44e7c4`  
		Last Modified: Tue, 14 May 2024 01:33:45 GMT  
		Size: 27.3 MB (27337664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64995ff8a19be3b1538ca8c771cf87d328c3c5a3d0bc0e9d30ca79f1f7691020`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc93e0c57e240329ac976a785b58e90ffefc382dab2cc84fadf027b034c7569b`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 6.7 MB (6703201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d9965634f52b56d3565561137b0502717aa07e18cb50749bad82621896ab3a`  
		Last Modified: Tue, 14 May 2024 02:56:22 GMT  
		Size: 1.0 MB (1046493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1d69e804cc62a84fa4974458b330d883ceea0a8601ab75df7c72b47193e2d7`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 80.3 KB (80331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da90c3e7a6363a01fdebe43b09d54ae207c3edf603093dc11354a59830f1147`  
		Last Modified: Tue, 14 May 2024 02:56:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93544d8936b311f1c1c1acb6629bcf10ce47a289e03c4239fadca7c5e08f85e3`  
		Last Modified: Tue, 14 May 2024 02:56:23 GMT  
		Size: 49.2 MB (49151182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d9b1555e7055515e1825debda2d7b0421a8195eb69dbe6bc1884f00a603066`  
		Last Modified: Tue, 14 May 2024 02:56:22 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7184fd55e18b1bc05fc4997f38d206feea47b96788742e1ac079f6330e80c5`  
		Last Modified: Tue, 14 May 2024 02:56:22 GMT  
		Size: 761.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e348cb4a7fda11eab1fb68fbb978cd329e246aed8ad17904e7388e109062a2a2`  
		Last Modified: Tue, 14 May 2024 02:56:23 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948d16d1e515223e6503ae0351554f4bce89d433f39500c46d5c809d38d33eef`  
		Last Modified: Tue, 14 May 2024 02:56:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:c33e444f2196768c243f95cc127c881cb63134697be1bd4421180f70e2c01724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4470067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b4696a1f3e122241c9a3dbfd1169ffc3b9fa55171e76f0a9e431287ca91ffc`

```dockerfile
```

-	Layers:
	-	`sha256:b9ab6cbe1a9cb9596f866ef211c8bdde7258cb81ea218403abeb44811d5bcac6`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 4.4 MB (4438481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a092ac3bed2922138aaa76e68c5e01208e19694fc330fdd76f4ccb4d202f2d14`  
		Last Modified: Tue, 14 May 2024 02:56:21 GMT  
		Size: 31.6 KB (31586 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0427a1b391a7a79bc7a71d8e653e1b057f2858efa54fe4ca33f89474b0b65819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72754682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d5a4bfe6da4508fd000e2a8d825415b11b5d635e90164662ed9c37651a00b7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bd84662eb5c566f361c169149ba683475c50ddc528270daf67d40c8e98ed12a7 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:57c62469eb2b8cb9a971714401ad24a78c171e2f6dab20314e1c5f0dab7a8639`  
		Last Modified: Wed, 24 Apr 2024 04:15:23 GMT  
		Size: 26.1 MB (26109830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420a3201a4f26b888ff27d75ebf5058fa178d5c5eaa591c34c3d78e9bb30c1e`  
		Last Modified: Wed, 24 Apr 2024 16:56:10 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730c01675a685b8c8377c245c4e5ebe2212ef31b76334d30f331d66060d45d39`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 6.6 MB (6576423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9928902a2afd882ed0192b334f236be8f74bf4334c6541b70b02347e8154f053`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 951.4 KB (951356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5944347da619792f62bead433ab612cd7d0714005e34a57430d843920461bb4c`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 80.2 KB (80183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6990feec48b73ca7c23fa9d8ce9713f258223ef2976e3f1edf97c950c64f6a41`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f00b2410daaa479c15e171e919facac382487e61dd1b382b4811adb03532f8`  
		Last Modified: Wed, 24 Apr 2024 17:16:53 GMT  
		Size: 39.0 MB (39029944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7e14d737c13d37152083872b21d4a61dbae26deb4480285f0e7d85d38d1965`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdb67dd6341985ecc381d3d4f4fc2c1c982874aa054261900aed809ce40b9de`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c80a24ac525d7ec75ce0db6d9efa6cf71bcc212651f09c305e797ab52f39d9`  
		Last Modified: Wed, 24 Apr 2024 17:16:52 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7761ef10106a1712390c18c07283cc37315454f5ac6d947699782a8d3fb356e6`  
		Last Modified: Wed, 24 Apr 2024 17:16:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:ffa185e0b42c866be20f772df803dc11e09b9a410ead792b51df2daaab0b5762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e29a55a6d863bc1021614a56a37957f78d8bcf027b5771b6e097adbf90a550`

```dockerfile
```

-	Layers:
	-	`sha256:2c05c22d4c2d7fec8b8ee20f327e5d27b6c1a7a7bcd80e4f28be0608c058a5ab`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 3.8 MB (3750111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff701624cf5b840e6fba6131a93d6e47d492b4765716a7d3d8baf7689e54f1d9`  
		Last Modified: Wed, 24 Apr 2024 17:16:51 GMT  
		Size: 31.4 KB (31419 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3`

```console
$ docker pull couchdb@sha256:1c9b191b061a3b8f678b6084c2af0fa478ef1506fe910edcc5c2c9f1f8f35a73
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
$ docker pull couchdb@sha256:4331421a2e5dff323618e823c60efcc1ae8eacbe318319945e4855800d80fd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89655707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e531576bbaefd82bf65c1645920e94469b7e49ec5c3ad840d545fb9eeab148c9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d906fcb7e77b51c81aba3df31e682564bfc67c9ee478357ba93ccd921360a295`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bdf844da7575b7a40112dfc38f45b64fc0309377eb7cdb323e8094bf1330d6`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 5.0 MB (5019697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c432908a4bea2a28515a63bdf25cec4cd7d30946cc8345733a17f742b92f8a2`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 394.3 KB (394318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0901a2ab1c8cf3bcfdf8539468bd3aabf9d367f2b3db9f1a1dc4e05849b51bcd`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 77.9 KB (77891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49ef1bac64f318092a920be080d071cae96b005a5bda54778e86df20c1e38aa`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144b0b16749fe2b786daa57858eb3f1d70da0fb15365e5ad92122b065ce51e52`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 52.7 MB (52722303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832249bf8a9bb00720985cfed188497d1de365c9aaf52ea3b61ee1d59bdec669`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca46de6fcc9c3d401ed229e4613ebc74de01b085c9f11a6b0d370f85e0f8067`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc2999f6ec16d99fc4ead75fe603e73db9a37f9dca77aa0e40e9566e0407305`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6536369e9e5921aef5e7173fc3372a996702c23bb6b850a0799ae5c762baefc9`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:773db3b1f338a1cb34126e05583d59e8defefca80d4bb7a031887434aa5c117c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522035137d5c1936095a79d50124269c66969a0853f2551641cfbfa24f250cdd`

```dockerfile
```

-	Layers:
	-	`sha256:dc6b608370ebad9c972b3749519a5bfb9a6209849f052b64d9c2dfc18efc27c3`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 4.0 MB (3965078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79751d31bbe331aca7734b8c91c8d80b89d7369796647f7044b3073049aac7c1`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 31.7 KB (31730 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f0e9b2c649a6724a24d2fad16ef90e14854d2a30be1eac01136b37ef8ca75fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88100685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4158510fdd76185be535e81514159eeeb23941484eb43479a99b9bebde744489`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a159f04f5ba449e2ac588d65dac07b043f3869765baaa698f95493ff0b771f36`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 3.3 KB (3349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3d37b9bbcc43de1f8fe8118c41081cdcfd966be8958b1580a55f5bf7c28f2d`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 5.0 MB (5004097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286cf5fbaea9e4f37a8f90443318d2871d9713908a665e662dc92d60d3834920`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 350.5 KB (350540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e46401911bbcb91945b101aa870c0e07bb1375043745db2dbb7e7f5bb9606f`  
		Last Modified: Wed, 24 Apr 2024 16:33:39 GMT  
		Size: 77.8 KB (77805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccef9aef5aa61d73182fb3588b6057882ab40b9df4a38eaaa6b0b1e4bde19e6`  
		Last Modified: Wed, 24 Apr 2024 16:33:39 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1d39ab8449fcc390c58a6154c0ce1b84e3744cf58b9328561d547ec9f4f9cd`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 52.6 MB (52573310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e70f98e6ef6a3d89751ebb0a1ca161863df9ce35bbf9e3e5f67d0c008a2aa1`  
		Last Modified: Wed, 24 Apr 2024 16:33:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42909ec628ccda6f4c354819ff59a4e6694dea073705aba035e4881e2c98b7f`  
		Last Modified: Wed, 24 Apr 2024 16:33:40 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02019e9d3e69204668325fa500054957eaeff2ea662474a7fba7d35e2ec2d52d`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1852a167c7c17f616cfb8af6e64f66ce24e126c77bff92ddc5c24cb07f6db796`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ec658f3a337854cc192e391a55c35fa0845050edd7a7bc291b54046200bee5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed006c670980e9d3a71a17ba24813c4d71ba9e7c0529d8c9177e9f3fb9fef89e`

```dockerfile
```

-	Layers:
	-	`sha256:4ba15cba561d024911c651ed74ab31b845e759ecbc1ed4a3465f1c23ff71485f`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 4.0 MB (3965312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d0f5469c522b5bd39214ac5a04134c1472292202b433de6ad699d17ed2a545`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 31.7 KB (31740 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:58156bd24dfd7de4227f32f2dbde19f9acab236ab7d52ed51b15811b19f29814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95382853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107df9c0c0bbf7bc6c9bc7639943efd8d44aff0852963b413ef3559e84d1619a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf93d48de5264d046dc227a4328348a5ea98f8e5e17f3e44d45ea98e9c0e37`  
		Last Modified: Tue, 14 May 2024 07:25:07 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029e3d567de2a5542d5bfe4bd503ee45d6d696e74c26694e1c7bd08cb3cbbb2b`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 5.8 MB (5839119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89646478ea3afd92bdc34e494f0065b7e16ba2d0dcbc68e3873a4cd85ac0f6f6`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 446.6 KB (446638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5849ebb34c9f0408a08f2b9f9db21571eb050743cce644f69c7061041d499412`  
		Last Modified: Tue, 14 May 2024 07:25:09 GMT  
		Size: 77.8 KB (77836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1fd03b0ed7fa194ee23ef921f686c04a7faeb6f9ade2bd8ced8298341d56e7`  
		Last Modified: Tue, 14 May 2024 07:25:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa1e4d4072a4816c3de34f524ab4b2844328c1a6241e54fa07920f6aa2f1632`  
		Last Modified: Tue, 14 May 2024 07:25:11 GMT  
		Size: 53.7 MB (53700522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe786dabcaebd644d5eeb21594657da050a313f9292b3c065bcec9b2062af839`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35f04877d50ddb49947e9ec9fd1cd70955e2648c10ab1ee6a548efaa1ea865`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74919c23b96621fbba9071ef08f76ad12eff2d4a424b8b464fe71f3da76e544`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5094108149380d384cfc1787f1111c32697f41ac74ffc663eb77e88ecbcacc1d`  
		Last Modified: Tue, 14 May 2024 07:25:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:b4240c74cc620cb13c95219d0cd4ebddb3c152a9cc6c6f9c768b1d41ccb7e2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903c624fd72120f948fe122cc9954fe45c482b1e74e26b0eda2a40313d739dc9`

```dockerfile
```

-	Layers:
	-	`sha256:c997d4f66204e210e94dca5c7dd72af9d9c30c50fa2c23150c1f3f55abea3fe5`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 4.0 MB (3969610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:779824a851a2435907e1243f288941db96a8065847d330c4df65929055494b46`  
		Last Modified: Tue, 14 May 2024 07:25:07 GMT  
		Size: 31.8 KB (31780 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:8468aca9a5cbbaa6100efa87302661ce255feb45b6e50986a0d565e85345dfea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86397842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74463f0ad8a9e79556f2d92b80851de5a94d5547dda4183e65bff33d8f06dfec`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17949f5b9178ff1f3dce8917d65f6abb49fa54851e8a88b3e0aecc1743f9b47`  
		Last Modified: Tue, 14 May 2024 07:12:14 GMT  
		Size: 3.3 KB (3349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec78ff4e8cf95d46165b4d84b185bed3ac8ea331c246d1915ca1c70a76c2b6c`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 4.9 MB (4905536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b810001bf2a7e98cb5e0ba1e9b1997a57d1d5d4ff86cced5a78c4febb4f7eb01`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 357.4 KB (357436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b269993425a3098b5e0b499fe3db204c94a8be0ae19360b3da54256fa2003f`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 77.8 KB (77836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281891daf068f5795ee2a24ba747a80ec915f8229c131a925a2c5a29be72437d`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7989fc17c203a837193f1aa6faab79d4a0219c82ac4fec1ce3e099f1d8666b0f`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 51.4 MB (51375789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e8d59c4b116719043dacc2dcdc2a0d667eb73da2c3f03bf6a946bae551ca17`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b024bfc2555c5ff15c877ffa24d5893096351c23d861094be82172b21244505`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b058b59294f503329c5691063af2d32c36da46e2d0bf4af1c55275d7d42d6e0b`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48caa89c0ae55f706e44f768b7a231e55670970dbec0bb4b05c3404a6cfbfbe`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f111937931c3b100dfca90df9bea0d3df521194f4009489616638f863975e372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725927a02b9b4713f3245424fdd91c84333cb7aad4a15b0dea68b51261edc36a`

```dockerfile
```

-	Layers:
	-	`sha256:ede20e200e411cf8dda2d4a31cc6c72fbeb9accbe9310106eeeaf75f60ce103f`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 4.0 MB (3964648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16afbe0c3eff6c45da1676533800c7b55a674f0375bafe76ee8cb7f50124174b`  
		Last Modified: Tue, 14 May 2024 07:12:14 GMT  
		Size: 31.7 KB (31730 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:49157aa0ec9898342722701c1d11d47849ff67a0c23636eee76d952c9cd8babd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:99a8d3d98e690b0ed008196da6bcb61ec266fba251085fcc91550d7329f22cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79794261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8848ef09ab8a1c7598177a29790755c425a3701a90b1228a824c783b4d964f9e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:ea1fe4f19165d885a1f3d523e0ebdcc3e863e6b93717c8022529edb674a52e2d in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:6299ae3fea5d052b297d91a57200563362b8f2c95358c6e3010d6fa3ed44e7c4`  
		Last Modified: Tue, 14 May 2024 01:33:45 GMT  
		Size: 27.3 MB (27337664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120d280897b52790c521380e988d1b7f440b1104e8ef0c03bfee4c084a523e41`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcc0e8cb5b2af41389c249846684d665e29d5c1d6279d662bc8aa252c27eb1b`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 6.7 MB (6703108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d547b20d6dc93615841fe02493b3da1d48695ec4663f9d7a21d74011ae11fa30`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 1.0 MB (1046475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3200923fadff846b1b8ff105ab93147d2ec1c177a4696c64b76043a7a98e14`  
		Last Modified: Tue, 14 May 2024 02:56:18 GMT  
		Size: 80.3 KB (80310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831b2d95f7e980ddad7cc8a09a59127d047207edb1d3d8761e19f9e8f8a35e78`  
		Last Modified: Tue, 14 May 2024 02:56:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68b91ab93f7676588bf7e75fd6ec4c714ca1d0eb0ed84052da9b6755056b82c`  
		Last Modified: Tue, 14 May 2024 02:56:20 GMT  
		Size: 44.6 MB (44619785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb425a1339d2b3491320f3898fced2d41c5801f625cfad6bd23d00ef5f9d131e`  
		Last Modified: Tue, 14 May 2024 02:56:19 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9beba0adbe5ffb43c629546f83a5419c0452bb828ee48952119deafc80c13ea7`  
		Last Modified: Tue, 14 May 2024 02:56:19 GMT  
		Size: 764.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d24f1ff2d2ffae722bbb25b5c5b9ea46b70b327d52e5cd8f9ce08b096532695`  
		Last Modified: Tue, 14 May 2024 02:56:19 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e2401e13b7997753923643a988f112d6f227d9d4f15c6acb1943383b899412`  
		Last Modified: Tue, 14 May 2024 02:56:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:e78899ca1c3b1c40092a525b5a0ac1f11af3314fbacc8d73b8a56136c2e5711e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114fe8852e1c25dcd2296cae3b4a578dff13b7aee6d09b777757e33c9e4e979d`

```dockerfile
```

-	Layers:
	-	`sha256:812cae74aac918f77a28403b016e287ca0404a8373af31974cadba013e403b22`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 3.8 MB (3807390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7009f4db8b371adc88cc47e649ff5757a5f91ab306813d43767f021fa7e159c2`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 31.3 KB (31285 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0c969212388accccf2d61fb6f6e78aebd78972005f230dd5db6c4c05204dc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74849228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f61b60a7714dad6a2522e6b3613a6d1027f97608e477c30b4865cbde383cb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bd84662eb5c566f361c169149ba683475c50ddc528270daf67d40c8e98ed12a7 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:57c62469eb2b8cb9a971714401ad24a78c171e2f6dab20314e1c5f0dab7a8639`  
		Last Modified: Wed, 24 Apr 2024 04:15:23 GMT  
		Size: 26.1 MB (26109830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420a3201a4f26b888ff27d75ebf5058fa178d5c5eaa591c34c3d78e9bb30c1e`  
		Last Modified: Wed, 24 Apr 2024 16:56:10 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730c01675a685b8c8377c245c4e5ebe2212ef31b76334d30f331d66060d45d39`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 6.6 MB (6576423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9928902a2afd882ed0192b334f236be8f74bf4334c6541b70b02347e8154f053`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 951.4 KB (951356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5944347da619792f62bead433ab612cd7d0714005e34a57430d843920461bb4c`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 80.2 KB (80183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5c964b1b26f8af96eae06527b8dc4a843bfeaef6afad2e396b940b4d4c6bdc`  
		Last Modified: Wed, 24 Apr 2024 16:56:12 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4f7ce23b7fad5284eb04795293b23568037e28999f154f07e75aca2e45c00d`  
		Last Modified: Wed, 24 Apr 2024 16:56:13 GMT  
		Size: 41.1 MB (41124494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4129a058b0d1f7348c8962092fbe54ec29098332d3c4aad540e5e1ad2b4f9b4`  
		Last Modified: Wed, 24 Apr 2024 16:56:12 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ce20201fba531f35f5fc0781d2b5fbca2921dc390913bed14af8cc7cb51df2`  
		Last Modified: Wed, 24 Apr 2024 16:56:12 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa5202db8c6ccd9f582bf96931260b0932f021def7ad23b17c267271d952ac0`  
		Last Modified: Wed, 24 Apr 2024 16:56:13 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33212bf6b082948c8e229ec262e3de40b3899505fb7603793fc59dd3bde63e7d`  
		Last Modified: Wed, 24 Apr 2024 16:56:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:658ab26df0ba9c9ddd26a7e8f067ce5759dbf8bcf9d194def5f3e908aaaab644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3845275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f6c80466d75a9a390828485938ecdc1cadc5e0f9b7a9ab24dae9fa925ce71a`

```dockerfile
```

-	Layers:
	-	`sha256:5c5af47cb8e1f25914b02ac2b41e51aed35d9e689515bfb9f630c1c400225889`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 3.8 MB (3813991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da94d86c3472cf7ca26220b664623b39f8d6c3ee8c9652c1c0addd0e20b62314`  
		Last Modified: Wed, 24 Apr 2024 16:56:10 GMT  
		Size: 31.3 KB (31284 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:49157aa0ec9898342722701c1d11d47849ff67a0c23636eee76d952c9cd8babd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:99a8d3d98e690b0ed008196da6bcb61ec266fba251085fcc91550d7329f22cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79794261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8848ef09ab8a1c7598177a29790755c425a3701a90b1228a824c783b4d964f9e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:ea1fe4f19165d885a1f3d523e0ebdcc3e863e6b93717c8022529edb674a52e2d in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:6299ae3fea5d052b297d91a57200563362b8f2c95358c6e3010d6fa3ed44e7c4`  
		Last Modified: Tue, 14 May 2024 01:33:45 GMT  
		Size: 27.3 MB (27337664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120d280897b52790c521380e988d1b7f440b1104e8ef0c03bfee4c084a523e41`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcc0e8cb5b2af41389c249846684d665e29d5c1d6279d662bc8aa252c27eb1b`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 6.7 MB (6703108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d547b20d6dc93615841fe02493b3da1d48695ec4663f9d7a21d74011ae11fa30`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 1.0 MB (1046475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3200923fadff846b1b8ff105ab93147d2ec1c177a4696c64b76043a7a98e14`  
		Last Modified: Tue, 14 May 2024 02:56:18 GMT  
		Size: 80.3 KB (80310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831b2d95f7e980ddad7cc8a09a59127d047207edb1d3d8761e19f9e8f8a35e78`  
		Last Modified: Tue, 14 May 2024 02:56:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68b91ab93f7676588bf7e75fd6ec4c714ca1d0eb0ed84052da9b6755056b82c`  
		Last Modified: Tue, 14 May 2024 02:56:20 GMT  
		Size: 44.6 MB (44619785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb425a1339d2b3491320f3898fced2d41c5801f625cfad6bd23d00ef5f9d131e`  
		Last Modified: Tue, 14 May 2024 02:56:19 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9beba0adbe5ffb43c629546f83a5419c0452bb828ee48952119deafc80c13ea7`  
		Last Modified: Tue, 14 May 2024 02:56:19 GMT  
		Size: 764.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d24f1ff2d2ffae722bbb25b5c5b9ea46b70b327d52e5cd8f9ce08b096532695`  
		Last Modified: Tue, 14 May 2024 02:56:19 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e2401e13b7997753923643a988f112d6f227d9d4f15c6acb1943383b899412`  
		Last Modified: Tue, 14 May 2024 02:56:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:e78899ca1c3b1c40092a525b5a0ac1f11af3314fbacc8d73b8a56136c2e5711e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114fe8852e1c25dcd2296cae3b4a578dff13b7aee6d09b777757e33c9e4e979d`

```dockerfile
```

-	Layers:
	-	`sha256:812cae74aac918f77a28403b016e287ca0404a8373af31974cadba013e403b22`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 3.8 MB (3807390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7009f4db8b371adc88cc47e649ff5757a5f91ab306813d43767f021fa7e159c2`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 31.3 KB (31285 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0c969212388accccf2d61fb6f6e78aebd78972005f230dd5db6c4c05204dc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74849228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f61b60a7714dad6a2522e6b3613a6d1027f97608e477c30b4865cbde383cb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bd84662eb5c566f361c169149ba683475c50ddc528270daf67d40c8e98ed12a7 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:57c62469eb2b8cb9a971714401ad24a78c171e2f6dab20314e1c5f0dab7a8639`  
		Last Modified: Wed, 24 Apr 2024 04:15:23 GMT  
		Size: 26.1 MB (26109830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420a3201a4f26b888ff27d75ebf5058fa178d5c5eaa591c34c3d78e9bb30c1e`  
		Last Modified: Wed, 24 Apr 2024 16:56:10 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730c01675a685b8c8377c245c4e5ebe2212ef31b76334d30f331d66060d45d39`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 6.6 MB (6576423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9928902a2afd882ed0192b334f236be8f74bf4334c6541b70b02347e8154f053`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 951.4 KB (951356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5944347da619792f62bead433ab612cd7d0714005e34a57430d843920461bb4c`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 80.2 KB (80183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5c964b1b26f8af96eae06527b8dc4a843bfeaef6afad2e396b940b4d4c6bdc`  
		Last Modified: Wed, 24 Apr 2024 16:56:12 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4f7ce23b7fad5284eb04795293b23568037e28999f154f07e75aca2e45c00d`  
		Last Modified: Wed, 24 Apr 2024 16:56:13 GMT  
		Size: 41.1 MB (41124494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4129a058b0d1f7348c8962092fbe54ec29098332d3c4aad540e5e1ad2b4f9b4`  
		Last Modified: Wed, 24 Apr 2024 16:56:12 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ce20201fba531f35f5fc0781d2b5fbca2921dc390913bed14af8cc7cb51df2`  
		Last Modified: Wed, 24 Apr 2024 16:56:12 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa5202db8c6ccd9f582bf96931260b0932f021def7ad23b17c267271d952ac0`  
		Last Modified: Wed, 24 Apr 2024 16:56:13 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33212bf6b082948c8e229ec262e3de40b3899505fb7603793fc59dd3bde63e7d`  
		Last Modified: Wed, 24 Apr 2024 16:56:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:658ab26df0ba9c9ddd26a7e8f067ce5759dbf8bcf9d194def5f3e908aaaab644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3845275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f6c80466d75a9a390828485938ecdc1cadc5e0f9b7a9ab24dae9fa925ce71a`

```dockerfile
```

-	Layers:
	-	`sha256:5c5af47cb8e1f25914b02ac2b41e51aed35d9e689515bfb9f630c1c400225889`  
		Last Modified: Wed, 24 Apr 2024 16:56:11 GMT  
		Size: 3.8 MB (3813991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da94d86c3472cf7ca26220b664623b39f8d6c3ee8c9652c1c0addd0e20b62314`  
		Last Modified: Wed, 24 Apr 2024 16:56:10 GMT  
		Size: 31.3 KB (31284 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:1d446e8539d26cd6af1663716149dcbb5c4f3e995161f1c1a458336805503ab3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:3bbe719c45d5c2f0a19b8de6a86daa5bfd6d1a3fb35b5e85fefea812e256020d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89121318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b370af5fd7f64c6a1887c54f6384cb1f5c66de6b4fb9da54e2053885fc2abc46`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51589e8f5f8d73aece6e4b1be397505f594535b27f5bcc8850d170188032a16`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2612832a9af0e96376f40bef3e40e219a40a8adc033fe6d786a30cc82d7e0328`  
		Last Modified: Tue, 14 May 2024 02:56:16 GMT  
		Size: 5.0 MB (5019765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096d7567c39d84fab5064a48063b2696789b925030a4881f2198d37961265766`  
		Last Modified: Tue, 14 May 2024 02:56:16 GMT  
		Size: 394.3 KB (394324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e4f2d993c6a0a0ef3e62b9c255c4d9ad3eb69bd865a30bbe487dd4e7bd3ae5`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 77.9 KB (77914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7f74b95eccc92261bf6524529003c3b418dcb1f1eaa698e0bf5b71ee64e42a`  
		Last Modified: Tue, 14 May 2024 02:56:16 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b31cb0ae6990eb6ff48dcf622bd09e748ca1ff73cce4531c9c6218c27d8656a`  
		Last Modified: Tue, 14 May 2024 02:56:18 GMT  
		Size: 52.2 MB (52188057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec16ae1b38e979c17cc2f47212de43efdc09cc2e989622dc1a099cc28ccd000`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4563c408f3e5dfb2dd3a73053533522753fe33be3a3e44d00398077abc4460d`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 999.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6628be1633f929cdb11abdabada724b0e28a963c6f1a9cebb1d893b011cbdb`  
		Last Modified: Tue, 14 May 2024 02:56:18 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb902059e907599ba4724b1881080c6ec4d973317fcb95b4b8f95e4bf824fd1d`  
		Last Modified: Tue, 14 May 2024 02:56:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:3570dd636791dc562325c7199aeb7741a89daaa5db94641e3097d88869eea5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed774fadb76ab4e1a3fa8392a0c13fcbd90b85171a2a56e4be776836e5e5db4`

```dockerfile
```

-	Layers:
	-	`sha256:19293f0134e9780c850e501f6c43f2adeb7f5b633272bb8b6f2b3403e66c473b`  
		Last Modified: Tue, 14 May 2024 02:56:16 GMT  
		Size: 3.9 MB (3935940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e522e7fddbc2604031db06b5087bde860d3d335e331e676e3251c516788f28f1`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 31.1 KB (31137 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.2.3`

```console
$ docker pull couchdb@sha256:1d446e8539d26cd6af1663716149dcbb5c4f3e995161f1c1a458336805503ab3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchdb:3.2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:3bbe719c45d5c2f0a19b8de6a86daa5bfd6d1a3fb35b5e85fefea812e256020d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89121318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b370af5fd7f64c6a1887c54f6384cb1f5c66de6b4fb9da54e2053885fc2abc46`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51589e8f5f8d73aece6e4b1be397505f594535b27f5bcc8850d170188032a16`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2612832a9af0e96376f40bef3e40e219a40a8adc033fe6d786a30cc82d7e0328`  
		Last Modified: Tue, 14 May 2024 02:56:16 GMT  
		Size: 5.0 MB (5019765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096d7567c39d84fab5064a48063b2696789b925030a4881f2198d37961265766`  
		Last Modified: Tue, 14 May 2024 02:56:16 GMT  
		Size: 394.3 KB (394324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e4f2d993c6a0a0ef3e62b9c255c4d9ad3eb69bd865a30bbe487dd4e7bd3ae5`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 77.9 KB (77914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7f74b95eccc92261bf6524529003c3b418dcb1f1eaa698e0bf5b71ee64e42a`  
		Last Modified: Tue, 14 May 2024 02:56:16 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b31cb0ae6990eb6ff48dcf622bd09e748ca1ff73cce4531c9c6218c27d8656a`  
		Last Modified: Tue, 14 May 2024 02:56:18 GMT  
		Size: 52.2 MB (52188057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec16ae1b38e979c17cc2f47212de43efdc09cc2e989622dc1a099cc28ccd000`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4563c408f3e5dfb2dd3a73053533522753fe33be3a3e44d00398077abc4460d`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 999.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6628be1633f929cdb11abdabada724b0e28a963c6f1a9cebb1d893b011cbdb`  
		Last Modified: Tue, 14 May 2024 02:56:18 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb902059e907599ba4724b1881080c6ec4d973317fcb95b4b8f95e4bf824fd1d`  
		Last Modified: Tue, 14 May 2024 02:56:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:3570dd636791dc562325c7199aeb7741a89daaa5db94641e3097d88869eea5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed774fadb76ab4e1a3fa8392a0c13fcbd90b85171a2a56e4be776836e5e5db4`

```dockerfile
```

-	Layers:
	-	`sha256:19293f0134e9780c850e501f6c43f2adeb7f5b633272bb8b6f2b3403e66c473b`  
		Last Modified: Tue, 14 May 2024 02:56:16 GMT  
		Size: 3.9 MB (3935940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e522e7fddbc2604031db06b5087bde860d3d335e331e676e3251c516788f28f1`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 31.1 KB (31137 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:1c9b191b061a3b8f678b6084c2af0fa478ef1506fe910edcc5c2c9f1f8f35a73
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
$ docker pull couchdb@sha256:4331421a2e5dff323618e823c60efcc1ae8eacbe318319945e4855800d80fd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89655707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e531576bbaefd82bf65c1645920e94469b7e49ec5c3ad840d545fb9eeab148c9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d906fcb7e77b51c81aba3df31e682564bfc67c9ee478357ba93ccd921360a295`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bdf844da7575b7a40112dfc38f45b64fc0309377eb7cdb323e8094bf1330d6`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 5.0 MB (5019697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c432908a4bea2a28515a63bdf25cec4cd7d30946cc8345733a17f742b92f8a2`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 394.3 KB (394318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0901a2ab1c8cf3bcfdf8539468bd3aabf9d367f2b3db9f1a1dc4e05849b51bcd`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 77.9 KB (77891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49ef1bac64f318092a920be080d071cae96b005a5bda54778e86df20c1e38aa`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144b0b16749fe2b786daa57858eb3f1d70da0fb15365e5ad92122b065ce51e52`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 52.7 MB (52722303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832249bf8a9bb00720985cfed188497d1de365c9aaf52ea3b61ee1d59bdec669`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca46de6fcc9c3d401ed229e4613ebc74de01b085c9f11a6b0d370f85e0f8067`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc2999f6ec16d99fc4ead75fe603e73db9a37f9dca77aa0e40e9566e0407305`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6536369e9e5921aef5e7173fc3372a996702c23bb6b850a0799ae5c762baefc9`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:773db3b1f338a1cb34126e05583d59e8defefca80d4bb7a031887434aa5c117c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522035137d5c1936095a79d50124269c66969a0853f2551641cfbfa24f250cdd`

```dockerfile
```

-	Layers:
	-	`sha256:dc6b608370ebad9c972b3749519a5bfb9a6209849f052b64d9c2dfc18efc27c3`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 4.0 MB (3965078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79751d31bbe331aca7734b8c91c8d80b89d7369796647f7044b3073049aac7c1`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 31.7 KB (31730 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f0e9b2c649a6724a24d2fad16ef90e14854d2a30be1eac01136b37ef8ca75fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88100685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4158510fdd76185be535e81514159eeeb23941484eb43479a99b9bebde744489`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a159f04f5ba449e2ac588d65dac07b043f3869765baaa698f95493ff0b771f36`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 3.3 KB (3349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3d37b9bbcc43de1f8fe8118c41081cdcfd966be8958b1580a55f5bf7c28f2d`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 5.0 MB (5004097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286cf5fbaea9e4f37a8f90443318d2871d9713908a665e662dc92d60d3834920`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 350.5 KB (350540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e46401911bbcb91945b101aa870c0e07bb1375043745db2dbb7e7f5bb9606f`  
		Last Modified: Wed, 24 Apr 2024 16:33:39 GMT  
		Size: 77.8 KB (77805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccef9aef5aa61d73182fb3588b6057882ab40b9df4a38eaaa6b0b1e4bde19e6`  
		Last Modified: Wed, 24 Apr 2024 16:33:39 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1d39ab8449fcc390c58a6154c0ce1b84e3744cf58b9328561d547ec9f4f9cd`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 52.6 MB (52573310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e70f98e6ef6a3d89751ebb0a1ca161863df9ce35bbf9e3e5f67d0c008a2aa1`  
		Last Modified: Wed, 24 Apr 2024 16:33:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42909ec628ccda6f4c354819ff59a4e6694dea073705aba035e4881e2c98b7f`  
		Last Modified: Wed, 24 Apr 2024 16:33:40 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02019e9d3e69204668325fa500054957eaeff2ea662474a7fba7d35e2ec2d52d`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1852a167c7c17f616cfb8af6e64f66ce24e126c77bff92ddc5c24cb07f6db796`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ec658f3a337854cc192e391a55c35fa0845050edd7a7bc291b54046200bee5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed006c670980e9d3a71a17ba24813c4d71ba9e7c0529d8c9177e9f3fb9fef89e`

```dockerfile
```

-	Layers:
	-	`sha256:4ba15cba561d024911c651ed74ab31b845e759ecbc1ed4a3465f1c23ff71485f`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 4.0 MB (3965312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d0f5469c522b5bd39214ac5a04134c1472292202b433de6ad699d17ed2a545`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 31.7 KB (31740 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:58156bd24dfd7de4227f32f2dbde19f9acab236ab7d52ed51b15811b19f29814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95382853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107df9c0c0bbf7bc6c9bc7639943efd8d44aff0852963b413ef3559e84d1619a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf93d48de5264d046dc227a4328348a5ea98f8e5e17f3e44d45ea98e9c0e37`  
		Last Modified: Tue, 14 May 2024 07:25:07 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029e3d567de2a5542d5bfe4bd503ee45d6d696e74c26694e1c7bd08cb3cbbb2b`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 5.8 MB (5839119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89646478ea3afd92bdc34e494f0065b7e16ba2d0dcbc68e3873a4cd85ac0f6f6`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 446.6 KB (446638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5849ebb34c9f0408a08f2b9f9db21571eb050743cce644f69c7061041d499412`  
		Last Modified: Tue, 14 May 2024 07:25:09 GMT  
		Size: 77.8 KB (77836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1fd03b0ed7fa194ee23ef921f686c04a7faeb6f9ade2bd8ced8298341d56e7`  
		Last Modified: Tue, 14 May 2024 07:25:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa1e4d4072a4816c3de34f524ab4b2844328c1a6241e54fa07920f6aa2f1632`  
		Last Modified: Tue, 14 May 2024 07:25:11 GMT  
		Size: 53.7 MB (53700522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe786dabcaebd644d5eeb21594657da050a313f9292b3c065bcec9b2062af839`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35f04877d50ddb49947e9ec9fd1cd70955e2648c10ab1ee6a548efaa1ea865`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74919c23b96621fbba9071ef08f76ad12eff2d4a424b8b464fe71f3da76e544`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5094108149380d384cfc1787f1111c32697f41ac74ffc663eb77e88ecbcacc1d`  
		Last Modified: Tue, 14 May 2024 07:25:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:b4240c74cc620cb13c95219d0cd4ebddb3c152a9cc6c6f9c768b1d41ccb7e2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903c624fd72120f948fe122cc9954fe45c482b1e74e26b0eda2a40313d739dc9`

```dockerfile
```

-	Layers:
	-	`sha256:c997d4f66204e210e94dca5c7dd72af9d9c30c50fa2c23150c1f3f55abea3fe5`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 4.0 MB (3969610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:779824a851a2435907e1243f288941db96a8065847d330c4df65929055494b46`  
		Last Modified: Tue, 14 May 2024 07:25:07 GMT  
		Size: 31.8 KB (31780 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:8468aca9a5cbbaa6100efa87302661ce255feb45b6e50986a0d565e85345dfea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86397842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74463f0ad8a9e79556f2d92b80851de5a94d5547dda4183e65bff33d8f06dfec`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17949f5b9178ff1f3dce8917d65f6abb49fa54851e8a88b3e0aecc1743f9b47`  
		Last Modified: Tue, 14 May 2024 07:12:14 GMT  
		Size: 3.3 KB (3349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec78ff4e8cf95d46165b4d84b185bed3ac8ea331c246d1915ca1c70a76c2b6c`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 4.9 MB (4905536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b810001bf2a7e98cb5e0ba1e9b1997a57d1d5d4ff86cced5a78c4febb4f7eb01`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 357.4 KB (357436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b269993425a3098b5e0b499fe3db204c94a8be0ae19360b3da54256fa2003f`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 77.8 KB (77836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281891daf068f5795ee2a24ba747a80ec915f8229c131a925a2c5a29be72437d`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7989fc17c203a837193f1aa6faab79d4a0219c82ac4fec1ce3e099f1d8666b0f`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 51.4 MB (51375789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e8d59c4b116719043dacc2dcdc2a0d667eb73da2c3f03bf6a946bae551ca17`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b024bfc2555c5ff15c877ffa24d5893096351c23d861094be82172b21244505`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b058b59294f503329c5691063af2d32c36da46e2d0bf4af1c55275d7d42d6e0b`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48caa89c0ae55f706e44f768b7a231e55670970dbec0bb4b05c3404a6cfbfbe`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f111937931c3b100dfca90df9bea0d3df521194f4009489616638f863975e372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725927a02b9b4713f3245424fdd91c84333cb7aad4a15b0dea68b51261edc36a`

```dockerfile
```

-	Layers:
	-	`sha256:ede20e200e411cf8dda2d4a31cc6c72fbeb9accbe9310106eeeaf75f60ce103f`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 4.0 MB (3964648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16afbe0c3eff6c45da1676533800c7b55a674f0375bafe76ee8cb7f50124174b`  
		Last Modified: Tue, 14 May 2024 07:12:14 GMT  
		Size: 31.7 KB (31730 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:1c9b191b061a3b8f678b6084c2af0fa478ef1506fe910edcc5c2c9f1f8f35a73
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
$ docker pull couchdb@sha256:4331421a2e5dff323618e823c60efcc1ae8eacbe318319945e4855800d80fd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89655707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e531576bbaefd82bf65c1645920e94469b7e49ec5c3ad840d545fb9eeab148c9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d906fcb7e77b51c81aba3df31e682564bfc67c9ee478357ba93ccd921360a295`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bdf844da7575b7a40112dfc38f45b64fc0309377eb7cdb323e8094bf1330d6`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 5.0 MB (5019697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c432908a4bea2a28515a63bdf25cec4cd7d30946cc8345733a17f742b92f8a2`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 394.3 KB (394318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0901a2ab1c8cf3bcfdf8539468bd3aabf9d367f2b3db9f1a1dc4e05849b51bcd`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 77.9 KB (77891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49ef1bac64f318092a920be080d071cae96b005a5bda54778e86df20c1e38aa`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144b0b16749fe2b786daa57858eb3f1d70da0fb15365e5ad92122b065ce51e52`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 52.7 MB (52722303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832249bf8a9bb00720985cfed188497d1de365c9aaf52ea3b61ee1d59bdec669`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca46de6fcc9c3d401ed229e4613ebc74de01b085c9f11a6b0d370f85e0f8067`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc2999f6ec16d99fc4ead75fe603e73db9a37f9dca77aa0e40e9566e0407305`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6536369e9e5921aef5e7173fc3372a996702c23bb6b850a0799ae5c762baefc9`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:773db3b1f338a1cb34126e05583d59e8defefca80d4bb7a031887434aa5c117c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522035137d5c1936095a79d50124269c66969a0853f2551641cfbfa24f250cdd`

```dockerfile
```

-	Layers:
	-	`sha256:dc6b608370ebad9c972b3749519a5bfb9a6209849f052b64d9c2dfc18efc27c3`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 4.0 MB (3965078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79751d31bbe331aca7734b8c91c8d80b89d7369796647f7044b3073049aac7c1`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 31.7 KB (31730 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f0e9b2c649a6724a24d2fad16ef90e14854d2a30be1eac01136b37ef8ca75fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88100685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4158510fdd76185be535e81514159eeeb23941484eb43479a99b9bebde744489`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a159f04f5ba449e2ac588d65dac07b043f3869765baaa698f95493ff0b771f36`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 3.3 KB (3349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3d37b9bbcc43de1f8fe8118c41081cdcfd966be8958b1580a55f5bf7c28f2d`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 5.0 MB (5004097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286cf5fbaea9e4f37a8f90443318d2871d9713908a665e662dc92d60d3834920`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 350.5 KB (350540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e46401911bbcb91945b101aa870c0e07bb1375043745db2dbb7e7f5bb9606f`  
		Last Modified: Wed, 24 Apr 2024 16:33:39 GMT  
		Size: 77.8 KB (77805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccef9aef5aa61d73182fb3588b6057882ab40b9df4a38eaaa6b0b1e4bde19e6`  
		Last Modified: Wed, 24 Apr 2024 16:33:39 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1d39ab8449fcc390c58a6154c0ce1b84e3744cf58b9328561d547ec9f4f9cd`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 52.6 MB (52573310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e70f98e6ef6a3d89751ebb0a1ca161863df9ce35bbf9e3e5f67d0c008a2aa1`  
		Last Modified: Wed, 24 Apr 2024 16:33:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42909ec628ccda6f4c354819ff59a4e6694dea073705aba035e4881e2c98b7f`  
		Last Modified: Wed, 24 Apr 2024 16:33:40 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02019e9d3e69204668325fa500054957eaeff2ea662474a7fba7d35e2ec2d52d`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1852a167c7c17f616cfb8af6e64f66ce24e126c77bff92ddc5c24cb07f6db796`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ec658f3a337854cc192e391a55c35fa0845050edd7a7bc291b54046200bee5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed006c670980e9d3a71a17ba24813c4d71ba9e7c0529d8c9177e9f3fb9fef89e`

```dockerfile
```

-	Layers:
	-	`sha256:4ba15cba561d024911c651ed74ab31b845e759ecbc1ed4a3465f1c23ff71485f`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 4.0 MB (3965312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d0f5469c522b5bd39214ac5a04134c1472292202b433de6ad699d17ed2a545`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 31.7 KB (31740 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:58156bd24dfd7de4227f32f2dbde19f9acab236ab7d52ed51b15811b19f29814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95382853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107df9c0c0bbf7bc6c9bc7639943efd8d44aff0852963b413ef3559e84d1619a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf93d48de5264d046dc227a4328348a5ea98f8e5e17f3e44d45ea98e9c0e37`  
		Last Modified: Tue, 14 May 2024 07:25:07 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029e3d567de2a5542d5bfe4bd503ee45d6d696e74c26694e1c7bd08cb3cbbb2b`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 5.8 MB (5839119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89646478ea3afd92bdc34e494f0065b7e16ba2d0dcbc68e3873a4cd85ac0f6f6`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 446.6 KB (446638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5849ebb34c9f0408a08f2b9f9db21571eb050743cce644f69c7061041d499412`  
		Last Modified: Tue, 14 May 2024 07:25:09 GMT  
		Size: 77.8 KB (77836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1fd03b0ed7fa194ee23ef921f686c04a7faeb6f9ade2bd8ced8298341d56e7`  
		Last Modified: Tue, 14 May 2024 07:25:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa1e4d4072a4816c3de34f524ab4b2844328c1a6241e54fa07920f6aa2f1632`  
		Last Modified: Tue, 14 May 2024 07:25:11 GMT  
		Size: 53.7 MB (53700522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe786dabcaebd644d5eeb21594657da050a313f9292b3c065bcec9b2062af839`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35f04877d50ddb49947e9ec9fd1cd70955e2648c10ab1ee6a548efaa1ea865`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74919c23b96621fbba9071ef08f76ad12eff2d4a424b8b464fe71f3da76e544`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5094108149380d384cfc1787f1111c32697f41ac74ffc663eb77e88ecbcacc1d`  
		Last Modified: Tue, 14 May 2024 07:25:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:b4240c74cc620cb13c95219d0cd4ebddb3c152a9cc6c6f9c768b1d41ccb7e2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903c624fd72120f948fe122cc9954fe45c482b1e74e26b0eda2a40313d739dc9`

```dockerfile
```

-	Layers:
	-	`sha256:c997d4f66204e210e94dca5c7dd72af9d9c30c50fa2c23150c1f3f55abea3fe5`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 4.0 MB (3969610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:779824a851a2435907e1243f288941db96a8065847d330c4df65929055494b46`  
		Last Modified: Tue, 14 May 2024 07:25:07 GMT  
		Size: 31.8 KB (31780 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:8468aca9a5cbbaa6100efa87302661ce255feb45b6e50986a0d565e85345dfea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86397842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74463f0ad8a9e79556f2d92b80851de5a94d5547dda4183e65bff33d8f06dfec`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17949f5b9178ff1f3dce8917d65f6abb49fa54851e8a88b3e0aecc1743f9b47`  
		Last Modified: Tue, 14 May 2024 07:12:14 GMT  
		Size: 3.3 KB (3349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec78ff4e8cf95d46165b4d84b185bed3ac8ea331c246d1915ca1c70a76c2b6c`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 4.9 MB (4905536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b810001bf2a7e98cb5e0ba1e9b1997a57d1d5d4ff86cced5a78c4febb4f7eb01`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 357.4 KB (357436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b269993425a3098b5e0b499fe3db204c94a8be0ae19360b3da54256fa2003f`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 77.8 KB (77836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281891daf068f5795ee2a24ba747a80ec915f8229c131a925a2c5a29be72437d`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7989fc17c203a837193f1aa6faab79d4a0219c82ac4fec1ce3e099f1d8666b0f`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 51.4 MB (51375789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e8d59c4b116719043dacc2dcdc2a0d667eb73da2c3f03bf6a946bae551ca17`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b024bfc2555c5ff15c877ffa24d5893096351c23d861094be82172b21244505`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b058b59294f503329c5691063af2d32c36da46e2d0bf4af1c55275d7d42d6e0b`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48caa89c0ae55f706e44f768b7a231e55670970dbec0bb4b05c3404a6cfbfbe`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f111937931c3b100dfca90df9bea0d3df521194f4009489616638f863975e372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725927a02b9b4713f3245424fdd91c84333cb7aad4a15b0dea68b51261edc36a`

```dockerfile
```

-	Layers:
	-	`sha256:ede20e200e411cf8dda2d4a31cc6c72fbeb9accbe9310106eeeaf75f60ce103f`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 4.0 MB (3964648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16afbe0c3eff6c45da1676533800c7b55a674f0375bafe76ee8cb7f50124174b`  
		Last Modified: Tue, 14 May 2024 07:12:14 GMT  
		Size: 31.7 KB (31730 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:1c9b191b061a3b8f678b6084c2af0fa478ef1506fe910edcc5c2c9f1f8f35a73
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
$ docker pull couchdb@sha256:4331421a2e5dff323618e823c60efcc1ae8eacbe318319945e4855800d80fd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89655707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e531576bbaefd82bf65c1645920e94469b7e49ec5c3ad840d545fb9eeab148c9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d906fcb7e77b51c81aba3df31e682564bfc67c9ee478357ba93ccd921360a295`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bdf844da7575b7a40112dfc38f45b64fc0309377eb7cdb323e8094bf1330d6`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 5.0 MB (5019697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c432908a4bea2a28515a63bdf25cec4cd7d30946cc8345733a17f742b92f8a2`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 394.3 KB (394318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0901a2ab1c8cf3bcfdf8539468bd3aabf9d367f2b3db9f1a1dc4e05849b51bcd`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 77.9 KB (77891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49ef1bac64f318092a920be080d071cae96b005a5bda54778e86df20c1e38aa`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144b0b16749fe2b786daa57858eb3f1d70da0fb15365e5ad92122b065ce51e52`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 52.7 MB (52722303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832249bf8a9bb00720985cfed188497d1de365c9aaf52ea3b61ee1d59bdec669`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca46de6fcc9c3d401ed229e4613ebc74de01b085c9f11a6b0d370f85e0f8067`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc2999f6ec16d99fc4ead75fe603e73db9a37f9dca77aa0e40e9566e0407305`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6536369e9e5921aef5e7173fc3372a996702c23bb6b850a0799ae5c762baefc9`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:773db3b1f338a1cb34126e05583d59e8defefca80d4bb7a031887434aa5c117c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522035137d5c1936095a79d50124269c66969a0853f2551641cfbfa24f250cdd`

```dockerfile
```

-	Layers:
	-	`sha256:dc6b608370ebad9c972b3749519a5bfb9a6209849f052b64d9c2dfc18efc27c3`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 4.0 MB (3965078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79751d31bbe331aca7734b8c91c8d80b89d7369796647f7044b3073049aac7c1`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 31.7 KB (31730 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f0e9b2c649a6724a24d2fad16ef90e14854d2a30be1eac01136b37ef8ca75fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88100685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4158510fdd76185be535e81514159eeeb23941484eb43479a99b9bebde744489`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a159f04f5ba449e2ac588d65dac07b043f3869765baaa698f95493ff0b771f36`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 3.3 KB (3349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3d37b9bbcc43de1f8fe8118c41081cdcfd966be8958b1580a55f5bf7c28f2d`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 5.0 MB (5004097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286cf5fbaea9e4f37a8f90443318d2871d9713908a665e662dc92d60d3834920`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 350.5 KB (350540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e46401911bbcb91945b101aa870c0e07bb1375043745db2dbb7e7f5bb9606f`  
		Last Modified: Wed, 24 Apr 2024 16:33:39 GMT  
		Size: 77.8 KB (77805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccef9aef5aa61d73182fb3588b6057882ab40b9df4a38eaaa6b0b1e4bde19e6`  
		Last Modified: Wed, 24 Apr 2024 16:33:39 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1d39ab8449fcc390c58a6154c0ce1b84e3744cf58b9328561d547ec9f4f9cd`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 52.6 MB (52573310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e70f98e6ef6a3d89751ebb0a1ca161863df9ce35bbf9e3e5f67d0c008a2aa1`  
		Last Modified: Wed, 24 Apr 2024 16:33:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42909ec628ccda6f4c354819ff59a4e6694dea073705aba035e4881e2c98b7f`  
		Last Modified: Wed, 24 Apr 2024 16:33:40 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02019e9d3e69204668325fa500054957eaeff2ea662474a7fba7d35e2ec2d52d`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1852a167c7c17f616cfb8af6e64f66ce24e126c77bff92ddc5c24cb07f6db796`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:ec658f3a337854cc192e391a55c35fa0845050edd7a7bc291b54046200bee5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed006c670980e9d3a71a17ba24813c4d71ba9e7c0529d8c9177e9f3fb9fef89e`

```dockerfile
```

-	Layers:
	-	`sha256:4ba15cba561d024911c651ed74ab31b845e759ecbc1ed4a3465f1c23ff71485f`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 4.0 MB (3965312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d0f5469c522b5bd39214ac5a04134c1472292202b433de6ad699d17ed2a545`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 31.7 KB (31740 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:58156bd24dfd7de4227f32f2dbde19f9acab236ab7d52ed51b15811b19f29814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95382853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107df9c0c0bbf7bc6c9bc7639943efd8d44aff0852963b413ef3559e84d1619a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf93d48de5264d046dc227a4328348a5ea98f8e5e17f3e44d45ea98e9c0e37`  
		Last Modified: Tue, 14 May 2024 07:25:07 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029e3d567de2a5542d5bfe4bd503ee45d6d696e74c26694e1c7bd08cb3cbbb2b`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 5.8 MB (5839119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89646478ea3afd92bdc34e494f0065b7e16ba2d0dcbc68e3873a4cd85ac0f6f6`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 446.6 KB (446638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5849ebb34c9f0408a08f2b9f9db21571eb050743cce644f69c7061041d499412`  
		Last Modified: Tue, 14 May 2024 07:25:09 GMT  
		Size: 77.8 KB (77836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1fd03b0ed7fa194ee23ef921f686c04a7faeb6f9ade2bd8ced8298341d56e7`  
		Last Modified: Tue, 14 May 2024 07:25:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa1e4d4072a4816c3de34f524ab4b2844328c1a6241e54fa07920f6aa2f1632`  
		Last Modified: Tue, 14 May 2024 07:25:11 GMT  
		Size: 53.7 MB (53700522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe786dabcaebd644d5eeb21594657da050a313f9292b3c065bcec9b2062af839`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35f04877d50ddb49947e9ec9fd1cd70955e2648c10ab1ee6a548efaa1ea865`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74919c23b96621fbba9071ef08f76ad12eff2d4a424b8b464fe71f3da76e544`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5094108149380d384cfc1787f1111c32697f41ac74ffc663eb77e88ecbcacc1d`  
		Last Modified: Tue, 14 May 2024 07:25:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:b4240c74cc620cb13c95219d0cd4ebddb3c152a9cc6c6f9c768b1d41ccb7e2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903c624fd72120f948fe122cc9954fe45c482b1e74e26b0eda2a40313d739dc9`

```dockerfile
```

-	Layers:
	-	`sha256:c997d4f66204e210e94dca5c7dd72af9d9c30c50fa2c23150c1f3f55abea3fe5`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 4.0 MB (3969610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:779824a851a2435907e1243f288941db96a8065847d330c4df65929055494b46`  
		Last Modified: Tue, 14 May 2024 07:25:07 GMT  
		Size: 31.8 KB (31780 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:8468aca9a5cbbaa6100efa87302661ce255feb45b6e50986a0d565e85345dfea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86397842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74463f0ad8a9e79556f2d92b80851de5a94d5547dda4183e65bff33d8f06dfec`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
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
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17949f5b9178ff1f3dce8917d65f6abb49fa54851e8a88b3e0aecc1743f9b47`  
		Last Modified: Tue, 14 May 2024 07:12:14 GMT  
		Size: 3.3 KB (3349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec78ff4e8cf95d46165b4d84b185bed3ac8ea331c246d1915ca1c70a76c2b6c`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 4.9 MB (4905536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b810001bf2a7e98cb5e0ba1e9b1997a57d1d5d4ff86cced5a78c4febb4f7eb01`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 357.4 KB (357436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b269993425a3098b5e0b499fe3db204c94a8be0ae19360b3da54256fa2003f`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 77.8 KB (77836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281891daf068f5795ee2a24ba747a80ec915f8229c131a925a2c5a29be72437d`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7989fc17c203a837193f1aa6faab79d4a0219c82ac4fec1ce3e099f1d8666b0f`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 51.4 MB (51375789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e8d59c4b116719043dacc2dcdc2a0d667eb73da2c3f03bf6a946bae551ca17`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b024bfc2555c5ff15c877ffa24d5893096351c23d861094be82172b21244505`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b058b59294f503329c5691063af2d32c36da46e2d0bf4af1c55275d7d42d6e0b`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48caa89c0ae55f706e44f768b7a231e55670970dbec0bb4b05c3404a6cfbfbe`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:f111937931c3b100dfca90df9bea0d3df521194f4009489616638f863975e372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725927a02b9b4713f3245424fdd91c84333cb7aad4a15b0dea68b51261edc36a`

```dockerfile
```

-	Layers:
	-	`sha256:ede20e200e411cf8dda2d4a31cc6c72fbeb9accbe9310106eeeaf75f60ce103f`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 4.0 MB (3964648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16afbe0c3eff6c45da1676533800c7b55a674f0375bafe76ee8cb7f50124174b`  
		Last Modified: Tue, 14 May 2024 07:12:14 GMT  
		Size: 31.7 KB (31730 bytes)  
		MIME: application/vnd.in-toto+json
